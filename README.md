# Architecture:

coding/:
  countLSP.py - counts LSP types after EasyScan runs
  makeinifiles.py - makes the .ini files used to run EasyScan
  microextract.py - converts the micromegas output to machine readable table (Comma separated)
  pyslha.py (Version 3.2.0) - library used by countLSP.py; changed such that it can read softsusy decays properly
  input/:
    pMSSMscan - raw slha file changed by Easyscan
    pMSSMscan.backup - This file is important as EasyScan changes pMSSMscan and could potentially crash
    scanparam/:
      fullscan.in - Table of scan parameters used by makeinifiles.py to make .ini files
   output/easyscans/:
    %Easyscan writes the output folders here, including plots. microextract.py and countLSP.py are also designed such that they write their outputs here.
softsusy/softsusy-4.0.1/:
  softpoint.x
micromegas_4.3.5/MSSM/:
  main.c - changed the output format into more machine readable ("Parameter\tValue" instead of "Parameter=Value") and deactivated unnecessary parts
EasyScan_HEP_1.0.0/:
  %whole folder is provided as many changes and bugfixes were implemented
