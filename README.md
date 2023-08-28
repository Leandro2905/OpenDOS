# The DR-DOS/OpenDOS Revival Project

OpenDOS had originally been released by Caldera under a commercial license, and it is still bound to this license. If you plan to use OpenDOS for commercial purposes, you need a commercial license on the company that now owns DR-DOS/OpenDOS.

The original Caldera license agreement is in the file license.txt, and it also applies for any modified versions that you can download here, as far as they are based on OpenDOS, except that you should not contact their tech support on matters specific to the modified versions. You should read license.txt before you start using any of them.

Note that the source code patches are not cumulative, meaning that you have to apply the earlier patches to the source code as well, with the exception of Work-In-Progress (WIP) and Release Candidate (RC) versions; these refer to the previous main release version.

For those who do not want to compile the source code themselves or lack the necessary development software, there are also pre-compiled binaries available.

# Components List

The Caldera OpenDOS MRS kit contains the following components:

* IBMBIO, IBMDOS and COMMAND

These components are accompanied with batch files (MAKE.BAT) that enable them to be built.  These batch files are to be found at the root of each component directory.

## IBMBIO

To build IBMBIO.COM run the MAKE.BAT found in the root of the IBMBIO\ directory.  The MAKE.BAT file sets environment variables that point to the local tools directory and to the Third Party tools required.  The Third party tools directory is set to C:\TOOLS but this can be changed by editing the MAKE.BAT file if required.

When this component has built all built files are placed in the BIN\ directory under the component.

## IBMDOS

To build IBMDOS.COM run the MAKE.BAT found in the root of the IBMDOS\ directory.  The MAKE.BAT file sets environment variables that point to the local tools directory and to the Third party tools required.  The Third party tools directory is set to C:\TOOLS but this can be changed by editing the MAKE.BAT file if required.

When this component has built all built files are placed in the BIN\ directory under the component.

## COMMAND

To build COMMAND.COM run the MAKE.BAT found in the root of the COMMAND\ directory.  The MAKE.BAT file sets environment variables that point to the local tools directory and to the Third party tools required.  The Third party tools directory is set to C:\TOOLS but this can be changed by editing the MAKE.BAT file if required.

When this component has built all built files are placed in the BIN\ directory under the component.

For this component we use the WATCOM optimising compiler, which greatly reduces the size of COMMAND.COM when built.  For this reason it is highly likely that the COMMAND.COM built on your local machine will differ from the shipped version of COMMAND.COM.

To gain better optimisation you will need a large TPA. This is best achieved by installing OpenDOS 7.01 setup to map Video memory into TPA.

In days past this component used to be built with the standard Borland compilers (v2.0) and if required can be modified to do so.

# Building from the Source Code

In order to build these components we have provided some of the "in house" tools that were developed to aid the process. The remainder of the tools have been omitted as you need to obtain the required licences for them.

The following third party tools were used to build the executables. Other versions of these tools may work but have not been tested.

* COMMAND only: Watcom C and Borland C
* Both IBMBIO and COMMAND: Microsoft MASM and Link
* IBMBIO only: Microsoft Lib
