
# QRes - Windows screen mode changer

## Introduction

The QRes core library and ```qres.exe``` are written in ANSI C, using Win32 API calls. 
QRes property pages (```qresprop.dll```) and the QRes Configuration Wizard (```QResCfg.exe```)
are written in C++, also using Microsoft Foundation Classes (MFC) libraries for Windows.


The original 1997 QRes project was set up in Microsoft Visual Studio 97 (version 
5.0). Currently project files are provided so that the binary can easily be 
compiled using Microsoft Visual C++ 6.0, Visual C++.NET 2003 and Borland C++
Builder versions 5.0 / 6.0.
 
 
## Project Dependencies (Compiler independent)

- All projects depend on ```qreslib```, build this library first.
- ```qres.exe``` also depends on ```qres32.lib```, i.e., ```qres32``` must be built before ```qres```

## Deploying binaries

- All ```*.DLL``` files should be copied to the Windows System directory
  (```%WINDIR%\System32``` on Windows NT, 2000, XP or Server 2003+ newer)
- ```qres.exe``` should be copied to the Windows directory
- Import ```qresprop``` \ ```qresprop.reg``` in the Windows Registry to enable Windows shell 
  integration of the QRes property page.
- Copy ```qres.hlp``` to ```%WINDIR%\help```


 
## Compiling with Microsoft Visual Studio 6.0

- Open the project ```qres``` \ ```qres.dsw``` in the Microsoft Visual C++ 6.0 IDE.
  This is the master project workspace that includes all QRes projects.
- Select menu option "Build" | "Batch Build ..."
- Press the button [Rebuild All]. This builds all debug and release binaries.
  All projects should compile error- and warning-free.

## Compiling with Microsoft Visual Studio .NET 2003

- Open the project ```qres``` \ ```qres.sln``` in the Microsoft Visual Studio .NET 2003 IDE.
  This is the master project workspace that includes all QRes projects.
- Select menu option "Build" | "Batch Build ..."
- Press the button [Select All], then [Rebuild]. This builds all debug and release
  binaries. All projects should compile error- and warning-free.

## Compiling with Borland C++ Builder 5.0

- Make sure Borland C++ MFC support is installed (use custom setup, not typical)
- Open the project group ```qres``` \ ```qres.bpg``` in the Borland C++ Builder 5 IDE.
  This is the master project group that includes all QRes projects.
- Select menu option "Project" | "Build All Projects". This builds all release
  binaries. All projects should compile error and warning-free.
- If you get this linker error: "```Fatal: Unable to open file 'ODBCCP32.LIB'```",
  copy the full contents of ```RUNIMAGE\Cbuilder5\LIB``` from your C++ Builder
  installation CD to ```C:\Program Files\Borland\CBuilder5\Lib```

## Compiling with Borland C++ Builder 6.0

- Open the project group ```qres``` \ ```qres.bpg``` in the Borland C++ Builder 6 IDE.
  This is the master project group that includes all QRes projects. The first 
  time that you do this, a message will be displayed for each project in the 
  group, informing you that the project has been updated to version 6.0.
- Select menu option "Project" | "Build All Projects". This builds all release
  binaries. All projects should compile error and warning-free.
