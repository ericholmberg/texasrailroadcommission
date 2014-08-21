#!/usr/bin/env ruby

file01 = File.open("file01.txt", "w")
file02 = File.open("file02.txt", "w")
file03 = File.open("file03.txt", "w")
file04 = File.open("file04.txt", "w")
file05 = File.open("file05.txt", "w")
file06 = File.open("file06.txt", "w")
file07 = File.open("file07.txt", "w")
file08 = File.open("file08.txt", "w")
file09 = File.open("file09.txt", "w")
file10 = File.open("file10.txt", "w")
file11 = File.open("file11.txt", "w")
file12 = File.open("file12.txt", "w")
file13 = File.open("file13.txt", "w")
file14 = File.open("file14.txt", "w")

str01 = "A2A9A9A6A6A3A5A8A1A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A1A2A2A2A2A2A2A2A2A2A2A2A2A1A30A30A9A9A5A5A5A5A5A1A1A1A1A1A1A1A1A1A1A1A1A1A1A5A1A1A1A1A1A1A1A1A2A2A1A1A1A1A1A6A3A1A6A3A1A6A3A1A6A1A6A1A6A1A1A2A1A2A2A2A2A1A1A1A2A2A2A2A1A2A2A2A2A6A1A2A2A2A2A4A4A4A52A28A1A1A1A5A5A1A2A2A2A2A3A6A2A2A2A5A4A5A5A20A28A2A2A2A2A3A2A2A5A54"
str02 = "A2A3A2A2A60A3A4A2A2A10"
str03 = "A2A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A3A3A3A3A3A3A3A3A3A3A3A3A3A3A3A1A2A2A2A2A1A1A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A1A5A15A1A1A1A75A20A5A2A2A2A1A4A2A1A1A4A2A1A26"
str04 = "A2A2A2A2A3A3A5A5A3A3A2A4A4A4"
str05 = "A2A2A2A2A3A3A3A3A5A3A3A3A7"
str06 = "A2A2A60A3"
str07 = "A2A8A2A2A2A2A2A2A2A2A2A1A1A2A2A2A2A2A2A2A2A1A2A2A2A5A2A2A2A2A5A5A2A2A2A1A3A1A1A23A4A20A1A2A2A2A2A1A30A1A1A1A1A1A20A1A1A36A1A1A22A29A11"
str08 = "A2A2A60A3"
str09 = "A2A1A1A18"
str10 = "A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A1A1A8"
str11 = "A2A4A5A10A11"
str12 = "A2A2A60A3"
str13 = "A2A6A6A1A1A1A1A1A1A1A1A1A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A2A8A8A8A8A8A6A6A6A20A40A1A4A2A1A17"
str14 = "A2A4A2A4A2A2A8A4A2A2A4A2A2A1A8A2A2A4A2A2A1A40"

File.open("c:/file_name.txt", "r") do |input_file|
        root_segment = ""
	input_file.each_line do |row|
				if row.slice(0,2) == '01'
					rarray = row.unpack(str01)
					root_segment = rarray.join("|").chomp
					file01.puts root_segment
				elsif row.slice(0,2) == '02'
					rarray = row.unpack(str02)
					file02.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '03'
					rarray = row.unpack(str03)
					file03.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '04'
					rarray = row.unpack(str04)
					file04.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '05'
					rarray = row.unpack(str05)
					file05.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '06'
					rarray = row.unpack(str06)
					file06.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '07'
					rarray = row.unpack(str07)
					file07.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '08'
					rarray = row.unpack(str08)
					file08.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '09'
					rarray = row.unpack(str09)
					file09.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '10'
					rarray = row.unpack(str10)
					file10.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '11'
					rarray = row.unpack(str11)
					file11.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '12'
					rarray = row.unpack(str12)
					file12.puts(root_segment + "|" + rarray.join("|").chomp)
				elsif row.slice(0,2) == '13'
					rarray = row.unpack(str13)
					file13.puts(root_segment + "|" + rarray.join("|").chomp)
				else row.slice(0,2) == '14'
					rarray = row.unpack(str14)
					file14.puts(root_segment + "|" + rarray.join("|").chomp)
				end
	end
end
