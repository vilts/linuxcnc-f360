# Fusion360 postprocessor for LinuxCNC lathe

Based on Tormach Slant-PRO PP.


## Development notes

1. Create 'intermediate CNC file' with Fusion 360 by post processing an operation or setup. `dump.cps` postprocessor can be used to get all possible variables.
   Intermediate file with export log is somewhere like this `C:\Users\<username>\AppData\Local\Temp\Fusion360CAM\1` with .cnc extension.
2. Locate `post.exe`, probably somewhere like `C:\Users\<username>\AppData\Local\Autodesk\webdeploy\production\f9042f554b0a0c3d14c46a7d9f3679baf42fdd2d\Applications\CAM360>`
3. Test by executing:
  `<post.exe> <processor.cps> <intermediate_file.cnc> --property unit MM --verbose` 



>`C:\Users\vilts\AppData\Local\Autodesk\webdeploy\production\f9042f554b0a0c3d14c46a7d9f3679baf42fdd2d\Applications\CAM360\post.exe "C
:\Dropbox\Misc projects\linuxcnc-f360\linuxcnc_lathe.cps"  "C:\Users\vilts\AppData\Local\Temp\Fusion360CAM\1\post_devel.cnc"`