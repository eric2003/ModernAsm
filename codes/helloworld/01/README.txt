Run the x64 Native Tools Command Prompt VS 2022.
d:
cd d:\work\asm_work\ModernAsm\codes\helloworld\01\build\
set PATH=c:\Program Files\NASM;%PATH%
nasm.exe -f win64 ../hello.asm -o ./hello.obj
link /subsystem:console /out:hello.exe hello.obj kernel32.lib msvcrt.lib legacy_stdio_definitions.lib
hello.exe