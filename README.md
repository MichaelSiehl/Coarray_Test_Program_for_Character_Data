# Coarray Test Program for Character Data
# Overview
This Repository contains two test programs that may help to check for a coarray compiler bug with image-to-image transfer of charachter data.

# src_with_scalar_character_member source code folder
In our experiences such a bug may arise with coarrays of derived type containing a scalar character component. While the data transfer itself takes place, single letters of the coarray character component turn into something else after remote transfer. This failure may only occur with a slightly sophisticated code structure, as that of our example program.

# src_with_array_character_member source code folder
On the other hand, we did never experience such a compiler bug when using coarrays of derived type containing a (one-element) array character component. Thus, you should not experience a run-time error when executing the test program of this source code folder.

