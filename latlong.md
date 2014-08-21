output_file = File.open("c:/users/067259/Desktop/output.txt", "w")

File.open("c:/users/067259/Desktop/editedapi8.txt", "r") do |input_file|
	input_file.each_line do |apinum|
		website = open("http://wwwgisp.rrc.state.tx.us/arcgis/rest/services/rrc_public/RRC_GIS_Viewer/MapServer/1/query?f=json&where=API%20like%20%27#{apinum.chomp}%27&returnGeometry=true&spatialRel=esriSpatialRelIntersects&outFields=*&outSR=102100")	
		data = JSON.parse(website.read)
		begin
		    latitude = data["features"][0]["attributes"]["GIS_LAT83"]
		    longitude = data["features"][0]["attributes"]["GIS_LONG83"]
		rescue
			latitude = 0
			longtidue = 0
			$stderr.puts "HEY #{apinum.chomp} doesn't return a proper JSON file"
		end
		output = [apinum.chomp, latitude, longitude].join("|")
		# puts(stubborn_open)
		#output_file.puts(output)
		puts(output)
		sleep 1
	end
end
