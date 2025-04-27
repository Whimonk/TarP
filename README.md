=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
   +            TarP v1.0     Target Gene Prediction software            +   
=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
(c) 2023 State Key Laboratory of Resource Insects, Southwest University, Chongqing 400715, China

Authors: Fan Ting, MicroRNA research group

Software written by: Fan Ting
Distributed for anyone to use under the GNU Public License (GPL),See the files 'COPYING' and 'LICENSE' for details

If you use this software please cite:
The literature of TarP

TarP comes with ABSOLUTELY NO WARRANTY;
This is free software, and you are welcome to redistribute it under certain conditions;

TarP is an effective target prediction software which aims to predict target gene and acquire a target site binding map.


USAGE:	('#' is a command indicator, and some systems use '$'.)
    Windows:
        # /absolute/path/to/tarp.exe [-Options <value/string>]
    Linux:
        # /absolute/path/to/tarp [-Options <value/string>]


-Options:

    -prefile <file path>:                                 # Input unpredicted file, please enter the absolute path. (eg: miRNA)
    -tarfile <file path>:                                 # Input target file, please enter the absolute path. (eg: 3'UTR, 5'UTR, mRNA, lncRNA, etc.)
    -outfdir <directory path>:                            # Output directory,please enter the absolute path. (string: output directory)
    -outfpre <file name prefix>:(default:TarPPreResult)   # Output file prefix. (string: file name prefix)
    
    -weight  <string>:(default:1,10,2,5,0.05)             # The weight of miRNA sequence four areas and the weight between match and mismatch.
    -jump    <value>:(default:3)                          # The maximum of bases allowed to be skipped in alignment, and the (maximum-1) of mismatched bases allowed to be output in a single strand. (int:>=0, The smaller the value, the stricter the alignment.)
    -move    <value>:(default:1)                          # The number of bases moved by miRNA on the target sequence after each round of alignment.
    -ug      <string:on|off>:(default:on)                 # Determine whether allow the match of U:G.
    -seed    <string:on|off|none>:(default:off)           # Whether the target miRNA sequence is completely matched with the seed sequence (bases 2-8 of miRNA 5'-> 3').
    
    -auto    <string:on|off>:(default:on)                 # Automatic adaptation of parameter combination is an operation mode that can automatically optimize the target prediction results. Because this operation mode takes a long time, it is recommended to use it when the input data is small.
    -test    <string:on|off>:(default:off)                # Used for negative test (-test on) and positive test (-test off), it is generally used with "-auto on -st 0 -en 0". Note that the results will be different under different weights (-weight)
    -thread  <value>:(default:1)                          # Set the thread of the software executing. (int:1~, the higer value and the better)
    -mode    <string:s2s|m2m>:(default:m2m)               # The mode parameter is used to set the mode of sequence comparison, where "s2s" is "single to single" mode, which means that the sequences are compared in one-to-one correspondence. In this mode, the number of rows of the input miRNA sequence file should be the same as that of the mRNA sequence file. "m2m" is "multiplicity to multiplicity" mode, which means that the sequence is one-to-many, many-to-one or many-to-many cross-alignment. In this mode, the number of lines of the input miRNA sequence file should be the same as that of the mRNA sequence file.
    
    -st      <value|string>:(default:55)                  # Classification threshold of St coefficient. (int:-100~100, the higer value and the better;string:none,indicating whether the st coefficient is used as the filter condition.)
    -en      <value|string>:(default:48)                  # Classification threshold of En coefficient. The bigger, the better.(int:1~100, the higer value and the better;string:none,indicating whether the en coefficient is used as the filter condition.)
    -tarnum  <value>:(default:3)                          # Number of output predicted per target gene.
   
    -display <string:on|off>:(default:off)                # Output the running process on the terminal.
    -v,--version                                          # You can enter the 'python3 tarp.py -v' and gain the help version information.
    -h,--help                                             # You can enter the 'python3 tarp.py -h' and gain the help manual.


-Other:

    If you have any doubts and suggestions about TarP software, you are welcome to communicate with us by email (FanTing_0123@163.com).
