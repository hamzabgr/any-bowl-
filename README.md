# any-bowl-
An automated Bash script to convert Dolby Vision Profile 7 (12-bit) to Profile 8 (10-bit) by injecting RPU metadata. Optimized for seamless playback on mid-range TV media players like Hisense/VIDAA with 0% error rate
chmod +x ./dovi_tool && mkvextract tracks movie.mkv 0:movie.hevc && ./dovi_tool -m 2 extract-rpu movie.hevc -o RPU.bin && ./dovi_tool inject-rpu --rpu-in RPU.bin --input movie.hevc -o final_movie.hevc && rm movie.hevc RPU.bin
