# any-bowl-
An automated script to convert Dolby Vision Profile 7 to Profile 8.

### 🛠 Prerequisites
Download these tools first:
- [dovi_tool](https://github.com/quietvoid/dovi_tool/releases)
- [MKVToolNix](https://mkvtoolnix.download/)

### 🚀 Commands
```bash
chmod +x ./dovi_tool && mkvextract tracks movie.mkv 0:movie.hevc && ./dovi_tool -m 2 extract-rpu movie.hevc -o RPU.bin && ./dovi_tool inject-rpu --rpu-in RPU.bin --input movie.hevc -o final_movie.hevc && rm movie.hevc RPU.bin
