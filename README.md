# Coarray Test Program for Character Data
# Overview
This Repository contains two test programs that may help to check for a coarray compiler bug with image-to-image transfer of charachter data.

# src_with_scalar_character_member source code folder
In our experiences such a bug may arise with coarrays of derived type containing a scalar character component. While the data transfer itself takes place, single letters of the coarray character component turn into something else after remote transfer. This failure may only occur with a slightly sophisticated code structure, as that of our example program.

# src_with_array_character_member source code folder
On the other hand, we did never experience such a compiler bug when using coarrays of derived type containing a (one-element) array character component. Thus, you should not experience a run-time error when executing the test program of this source code folder.

# Test your Coarray Fortran Compiler
- Download the content of the 'src_with_scalar_character_member' source code folder.
- Compile the source code to execute on 3 coarray images. With ifort you may use this from a Linux (Ubuntu) terminal window:  ifort -coarray -coarray-num-images=3 OOOGglob_Globals.f90 OOOEerro_admError.f90 OOOPstpa_admStartPath.f90 OOOPimsc_admImageStatus_CA.f90 OOOPtmec_admTeamMember_CA.f90 OOOPtemc_admTeamManager_CA.f90 OOOPimmc_admImageManager_CA.f90 OOOPinmc_admInitialManager_CA.f90 OOOPtmem_admTeamMember.f90 OOOPtema_admTeamManager.f90 OOOPinma_admInitialManager.f90 OOOPimma_admImageManager.f90 Main_Sub.f90 Main.f90 -o a.out
- run the compiled program from the command line: a.out
