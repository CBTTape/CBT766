# CBT766
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 766 is from Stephen McColley and contains the Mellon      *   FILE 766
//*           Mods for z/OS 1.7 and 1.8.  These are not called      *   FILE 766
//*           the Mellon Mods anymore, because Mellon Bank has      *   FILE 766
//*           long since stopped supporting them.  But Stephen      *   FILE 766
//*           McColley and his colleagues at SunTrust Bank do the   *   FILE 766
//*           support now.  See their explanations below.           *   FILE 766
//*                                                                 *   FILE 766
//*           McColley Systems Group Inc.                           *   FILE 766
//*           sgmccolley@windstream.net                             *   FILE 766
//*           SGMcColley@MVSProgrammer.com                          *   FILE 766
//*           http://WWW.MVSProgrammer.com                          *   FILE 766
//*           770-335-0478                                          *   FILE 766
//*                                                                 *   FILE 766
//*     --------------------------------------------------------    *   FILE 766
//*                                                                 *   FILE 766
//*                SSSS H   H  AAA  RRRR  EEEEE DDDD                *   FILE 766
//*               S     H   H A   A R   R E     D   D               *   FILE 766
//*                SSS  HHHHH AAAAA RRRR  EEEE  D   D               *   FILE 766
//*                   S H   H A   A R  R  E     D   D               *   FILE 766
//*               SSSS  H   H A   A R   R EEEEE DDDD                *   FILE 766
//*                                                                 *   FILE 766
//*                   SSSS PPPP   OOO   OOO  L                      *   FILE 766
//*                  S     P   P O   O O   O L                      *   FILE 766
//*                   SSS  PPPP  O   O O   O L                      *   FILE 766
//*                      S P     O   O O   O L                      *   FILE 766
//*                  SSSS  P      OOO   OOO  LLLLL                  *   FILE 766
//*                                                                 *   FILE 766
//*                     M   M  OOO  DDDD   SSSS                     *   FILE 766
//*                     MM MM O   O D   D S                         *   FILE 766
//*                     M M M O   O D   D  SSS                      *   FILE 766
//*                     M   M O   O D   D     S                     *   FILE 766
//*                     M   M  OOO  DDDD  SSSS                      *   FILE 766
//*                                                                 *   FILE 766
//*                    for jes2 1.7 and jes2 1.8                    *   FILE 766
//*                                                                 *   FILE 766
//*     --------------------------------------------------------    *   FILE 766
//*                                                                 *   FILE 766
//*     DISCLAIMER -                                                *   FILE 766
//*                                                                 *   FILE 766
//*         THE MODS ON THIS TAPE HAVE BEEN USED SUCCESSFULLY       *   FILE 766
//*      AND TO THE BEST OF OUR KNOWLEDGE THEY ARE OPERATIONAL,     *   FILE 766
//*      HOWEVER NO WARRANTY IS MADE TO THE ACCURACY OF THE MODS    *   FILE 766
//*      AND NO RESPONSIBILITY IS ASSUMED FOR ANY MODIFICATION      *   FILE 766
//*      DIRECTLY OR INDIRECTLY CAUSED BY THE USE OF THE            *   FILE 766
//*      MODIFICATIONS.  IT IS THE USERS RESPONSIBILITY TO          *   FILE 766
//*      EVALUATE THE USEFULLNESS OF THE MATERIAL.                  *   FILE 766
//*                                                                 *   FILE 766
//*         WE DO NOT GUARANTEE TO KEEP ANY MATERIAL PROVIDED UP    *   FILE 766
//*      TO DATE, NOR DO WE GUARANTEE TO PROVIDE ANY CORRECTIONS    *   FILE 766
//*      OR EXTENSIONS MADE IN THE FUTURE.                          *   FILE 766
//*                                                                 *   FILE 766
//*     --------------------------------------------------------    *   FILE 766
//*                                                                 *   FILE 766
//*      This is the installation PDS for the Shared Spool Mods     *   FILE 766
//*      for jes2 1.7 and jes2 1.8.  The shared spool mods were     *   FILE 766
//*      formerly known as the Mellon shared spool mods.            *   FILE 766
//*                                                                 *   FILE 766
//*      All who use the shared spool mods owe a debt of gratitude  *   FILE 766
//*      to Mellon Bank for the original implementaion of the       *   FILE 766
//*      shared spool mods, but because it has been maintained      *   FILE 766
//*      outside of Mellon for a dozen years, and has been          *   FILE 766
//*      rewritten twice since then, we will refer to the mods as   *   FILE 766
//*      the SHARED SPOOL MODS from now on.  Once again -           *   FILE 766
//*                           THANK YOU MELLON BANK !               *   FILE 766
//*                                                                 *   FILE 766
//*     --------------------------------------------------------    *   FILE 766
//*                                                                 *   FILE 766
//*       In this PDS you should find the following members.        *   FILE 766
//*                                                                 *   FILE 766
//*     @@README -   That is this member, you are reading it.       *   FILE 766
//*                                                                 *   FILE 766
//*     DISCLAIM -   Our standard disclaimer - we guarantee /       *   FILE 766
//*                  warrant nothing!                               *   FILE 766
//*                                                                 *   FILE 766
//*     SSMINSTP -   Shared Spool Mods installation manual -        *   FILE 766
//*                  PDF format                                     *   FILE 766
//*                                                                 *   FILE 766
//*     SSMINSTW -   Shared Spool Mods installation manual -        *   FILE 766
//*                  Word Document                                  *   FILE 766
//*                                                                 *   FILE 766
//*     SSMUSERP -   Shared Spool Mods Users Guide - PDF format     *   FILE 766
//*                                                                 *   FILE 766
//*     SSMUSERW -   Shared Spool Mods Users Buide - Word           *   FILE 766
//*                  Document                                       *   FILE 766
//*                                                                 *   FILE 766
//*     SSMOPSGP -   Shared Spool Mods Operations Guide - PDF       *   FILE 766
//*                  format                                         *   FILE 766
//*                                                                 *   FILE 766
//*     SSMOPSGW -   Shared Spool Mods Operations Guide - Word      *   FILE 766
//*                  Document                                       *   FILE 766
//*                                                                 *   FILE 766
//*     LSES500  -   THE Single usermod needed to install the       *   FILE 766
//*                  entire package.                                *   FILE 766
//*                                                                 *   FILE 766
//*     LSES501 and LSES502  -  Required fixes for LSES500.         *   FILE 766
//*                  Added later by Steve McColley.                 *   FILE 766
//*                                                                 *   FILE 766
//*     LSES500J -   Sample JCL to run the RECEIVE / APPLY          *   FILE 766
//*                  Check / APPLY                                  *   FILE 766
//*                                                                 *   FILE 766
//*     JES2PARM -   Sample JES2 parms needed to implement the      *   FILE 766
//*                  package.                                       *   FILE 766
//*                                                                 *   FILE 766
//*     *** Then we have the following three members - They are     *   FILE 766
//*     *** not really part of the shared spool mods - but we       *   FILE 766
//*     *** have been distributing them, and some folks still       *   FILE 766
//*     *** need them.  If you want to use these, you will have     *   FILE 766
//*     *** to apply them separately from the shared spool mods     *   FILE 766
//*     *** - we just have the source - they are not setup as       *   FILE 766
//*     *** usermods.                                               *   FILE 766
//*                                                                 *   FILE 766
//*     STSCX01A -   our version of the page seperator exit.        *   FILE 766
//*                  (not part of ssm's)                            *   FILE 766
//*                                                                 *   FILE 766
//*     STSCX05B -   Prevent purging by job range. (not part of     *   FILE 766
//*                  ssm's)                                         *   FILE 766
//*                                                                 *   FILE 766
//*     STSCX15A -   Causes FCBs to be reload with each job         *   FILE 766
//*                  unless std forms.                              *   FILE 766
//*                                                                 *   FILE 766
//*     STSCx36A -   SAF processing for jobs coming in from         *   FILE 766
//*                  RJE/NJE sources.                               *   FILE 766
//*                                                                 *   FILE 766
//*       The documentation members suffixed with a 'P' i.e.        *   FILE 766
//*     SSMINSTP are PDF format documents.  To use them you         *   FILE 766
//*     will need to transfer them to a PC using your favorite      *   FILE 766
//*     file transfer program using a BINARY option - ie.  no       *   FILE 766
//*     translation.  You will probably need to make sure they      *   FILE 766
//*     are transferred to a new file name that ends in ".PDF",     *   FILE 766
//*     or you may not be able to read them.                        *   FILE 766
//*                                                                 *   FILE 766
//*       If you can not read PDF docs the original "WORD"          *   FILE 766
//*     formatted docs are included in the members suffixed         *   FILE 766
//*     with a W i.e. SSMINSTW.  You will probably need to          *   FILE 766
//*     offload them to a PC file with a suffix of DOC to read      *   FILE 766
//*     them properly.                                              *   FILE 766
//*                                                                 *   FILE 766
//*       The three basic pieces of documentation are -             *   FILE 766
//*                                                                 *   FILE 766
//*     1 The installation guide - gives background,                *   FILE 766
//*       installation instructions, and other information          *   FILE 766
//*       needed to setup the package.                              *   FILE 766
//*                                                                 *   FILE 766
//*     2 The Users Guide - gives detailed info on JECL             *   FILE 766
//*       statements and is aimed at the end users - whoever        *   FILE 766
//*       codes and uses JCL.                                       *   FILE 766
//*                                                                 *   FILE 766
//*     3 The Operations Guide - gives detailed informatin          *   FILE 766
//*       about all of the   , new JES2 display and modify          *   FILE 766
//*       commands avaialable with the package.                     *   FILE 766
//*                                                                 *   FILE 766
//*       Once you have the package set up - please drop me a       *   FILE 766
//*        line at:                                                 *   FILE 766
//*                                                                 *   FILE 766
//*                SGMCCOLLEY@ALLTEL.NET  or                        *   FILE 766
//*        STEPHEN.MCCOLLEY@SUNTRUST.BANK so that                   *   FILE 766
//*                                                                 *   FILE 766
//*       I can add you to the mailing list.  That way I can        *   FILE 766
//*       let you know about bugs, fixes, and new releases as I     *   FILE 766
//*       make the avaialable.                                      *   FILE 766
//*                                                                 *   FILE 766
//*       If you drop me your real mailing address, I will send     *   FILE 766
//*       you a "Shared Spool Mods" coffee cup.                     *   FILE 766
//*                                                                 *   FILE 766
```
