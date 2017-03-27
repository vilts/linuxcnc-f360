# Fusion360 postprocessor for LinuxCNC lathe

Based on Tormach Slant-PRO PP.


## Development notes

1. Create 'intermediate CNC file' with Fusion 360 by post processing an operation or setup. `dump.cps` postprocessor can be used to get all possible variables.
   Intermediate file with export log is somewhere like this `C:\Users\<username>\AppData\Local\Temp\Fusion360CAM\1` with .cnc extension.
2. Locate `post.exe`, probably somewhere like `C:\Users\<username>\AppData\Local\Autodesk\webdeploy\production\f9042f554b0a0c3d14c46a7d9f3679baf42fdd2d\Applications\CAM360>`
3. Test by executing:
  `<post.exe> <processor.cps> <intermediate_file.cnc> --property unit MM --verbose`

>`C:\Users\vilts\AppData\Local\Autodesk\webdeploy\production\110e62f27b395d1e77f65827ad98f9392983e959\Applications\CAM360\post.exe "C:\Dropbox\Misc projects\linuxcnc-f360\linuxcnc_lathe.cps"  "C:\Users\vilts\AppData\Local\Temp\Fusion360CAM\1\post_devel.cnc" --property unit MM --verbose`

## Resources
1. AutoDesk CAM - [http://cam.autodesk.com/posts/reference/index.html](http://cam.autodesk.com/posts/reference/index.html)
2. AutoDesk CAM classes - [http://cam.autodesk.com/posts/reference/annotated.html](http://cam.autodesk.com/posts/reference/annotated.html)
3. [LinuxCNC G-code reference](http://linuxcnc.org/docs/html/gcode/g-code.html)
4. [LinuxCNC G76 threading cycle](http://linuxcnc.org/docs/html/gcode/g-code.html#gcode:g76)
5. [AutoDesk PostProcessor Manual (PDF)](http://fab.cba.mit.edu/content/tools/hurco_mill/hurco_post_processor_explanation_docs/Autodesk%20Post%20Processor%20manual-sm-130829.pdf)
6. [Forum: Help! My post processor needs to be edited; now what?](https://forums.autodesk.com/t5/hsm-post-processor-forum/help-my-post-processor-needs-to-be-edited-now-what/td-p/6095934?nobounce=) (Contains post.chm and Post manual)
7. [Forum: Getting started w post development](https://forums.autodesk.com/t5/hsm-post-processor-forum/getting-started-modify-posts/td-p/6371381)
