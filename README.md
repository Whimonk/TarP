<h1>TarP</h1>
<pre>    This is a miRNA target prediction tool based on polymorphic structured base alignment algorithm. The tool can realize target prediction of specific or non-specific species, conservative or non-conservative sequences based on user-defined parameter combinations. Using it can help users get the candidate targets of miRNA accurately, and lay the foundation for further research.</pre>


<h2>Data Frame:</h2>
<h3>Input Files</h3>
<h4>1. miRNA Sequence Input File:(eg:miR-Input.fa)</h4>
<pre>>miR-example1
GUUUGUGACCGUCACUAACGGGCAGU
>miR-example2
UCGUUUUGGCGAUCGCAAAAUG</pre>
<h4>2. mRNA Sequence Input File:(eg:Tar-Input.fa)</h4>
<pre>>Tar_example1
AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC
>Tar_example2
AGTAGCACTAGGCTACTGACACTCCCGGCGCCCTTCCGCATCCCTCGCTCACCCTCTCTCCCTCCTCGTTCCCATTCAAGCTATCGACTCATAAGCGACACGTCCTATATTCATTGTGAAGCCCTTAGACTTACTTGCCATCTAAGGATATTTATTCATATAATATATGTGTGGTATTTAATCAATTAATTAATTAAAATTATACAGATTCACAAATTCACTAATTGATCTTTAGACCTGCTCCATCTCATCTAACAATAAAAACAAATTCAAATACCTGAAATAAAATAAATTGCAAGTCACATCTGCCAATCTTAAATGTACCCATTTGCAAGGTGTGGCATCAAAATGTTCAACTTACATCCAGTTTAATTTTTCAGAGAAATGTAATTCCATTGCAATATATTGGTTGGTTGGGGTTGCATTGGTAGCGAGTCGCACGAACCTGCATTCTGCACTTTCGAAAACTCAAATCGAATCCTCAACATACCCAAAACCTTGATCTCCATAATATATTATGATAAAGTTGTACAGTAGTTTTTGTAGCCTTGTTGTATGCAAACAACTAATTCTTACAATTTATCACCAATTACATTGTAGTGCATCAGTAATAATATAATACTGCGT</pre>

<h3>Output Files</h3>
<h4>1. miRNA-mRNA Target Result File:(eg:TarPPreResult_auto_tar.txt)</h4>
<pre>TarID	TarSeq	MiRID	MiRSeq	Tar_Part	MiR_Part	Match_State	St	En
Tar_example1	AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC	miR-example1	GUUUGUGACCGUCACUAACGGGCAGU	GCUGCAUOUUGAGGACACUCACAAGA	UGACGGGCAAUCACUGCCAGUGUUUG	[2,1,1,1,1,0,2,0,1,1,2,0,0,1,1,1,0,0,1,1,1,1,1,1,2,0]	69.13	57.69
tar_example2	AGTAGCACTAGGCTACTGACACTCCCGGCGCCCTTCCGCATCCCTCGCTCACCCTCTCTCCCTCCTCGTTCCCATTCAAGCTATCGACTCATAAGCGACACGTCCTATATTCATTGTGAAGCCCTTAGACTTACTTGCCATCTAAGGATATTTATTCATATAATATATGTGTGGTATTTAATCAATTAATTAATTAAAATTATACAGATTCACAAATTCACTAATTGATCTTTAGACCTGCTCCATCTCATCTAACAATAAAAACAAATTCAAATACCTGAAATAAAATAAATTGCAAGTCACATCTGCCAATCTTAAATGTACCCATTTGCAAGGTGTGGCATCAAAATGTTCAACTTACATCCAGTTTAATTTTTCAGAGAAATGTAATTCCATTGCAATATATTGGTTGGTTGGGGTTGCATTGGTAGCGAGTCGCACGAACCTGCATTCTGCACTTTCGAAAACTCAAATCGAATCCTCAACATACCCAAAACCTTGATCTCCATAATATATTATGATAAAGTTGTACAGTAGTTTTTGTAGCCTTGTTGTATGCAAACAACTAATTCTTACAATTTATCACCAATTACATTGTAGTGCATCAGTAATAATATAATACTGCGT	miR-example2	UCGUUUUGGCGAUCGCAAAAUG	UAUAUOOUGGUUGGUUGGGGUUG	GUAAAACGCUAGOCGGUUUUGCU	[2,1,1,0,1,0,0,2,1,2,1,2,0,1,2,2,2,2,2,2,2,0,2]	63.32	52.31</pre>

<h4>2. miRNA-mRNA Binding Site File:(eg:TarPPreResult_auto_pair.txt)</h4>
<pre>Tar ID: tar_example1
Tar Seq: AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC
MiR ID: miR-example1
MiR Seq: GUUUGUGACCGUCACUAACGGGCAGU
St: 69.13
En: 57.69

Target:            5'      G C U G C A U   U U G A G G A C A C U C A C A A G A      3'	
matchstate:                : | | | |   :   | | :     | | |     | | | | | | :	   			
MiRNA:             3'      U G A C G G G C A A U C A C U G C C A G U G U U U G      5'	

Tar ID: tar_example2
Tar Seq: AGTAGCACTAGGCTACTGACACTCCCGGCGCCCTTCCGCATCCCTCGCTCACCCTCTCTCCCTCCTCGTTCCCATTCAAGCTATCGACTCATAAGCGACACGTCCTATATTCATTGTGAAGCCCTTAGACTTACTTGCCATCTAAGGATATTTATTCATATAATATATGTGTGGTATTTAATCAATTAATTAATTAAAATTATACAGATTCACAAATTCACTAATTGATCTTTAGACCTGCTCCATCTCATCTAACAATAAAAACAAATTCAAATACCTGAAATAAAATAAATTGCAAGTCACATCTGCCAATCTTAAATGTACCCATTTGCAAGGTGTGGCATCAAAATGTTCAACTTACATCCAGTTTAATTTTTCAGAGAAATGTAATTCCATTGCAATATATTGGTTGGTTGGGGTTGCATTGGTAGCGAGTCGCACGAACCTGCATTCTGCACTTTCGAAAACTCAAATCGAATCCTCAACATACCCAAAACCTTGATCTCCATAATATATTATGATAAAGTTGTACAGTAGTTTTTGTAGCCTTGTTGTATGCAAACAACTAATTCTTACAATTTATCACCAATTACATTGTAGTGCATCAGTAATAATATAATACTGCGT
MiR ID: miR-example2
MiR Seq: UCGUUUUGGCGAUCGCAAAAUG
St: 63.32
En: 52.31

Target:             5'      U A U A U     U G G U U G G U U G G G G U U G      3'	
matchstate:                 : | |   |     : | : | :   | : : : : : : :   :	   		
MiRNA:              3'      G U A A A A C G C U A G   C G G U U U U G C U      5'	</pre>

<h2>USAGE:</h2>

<h3>1. Windows:</h3>
<pre>    $ /absolute/path/to/tarp.exe [-Options <value/string>]
    # eg:/absolute/path/to/tarp.exe -prefile /absolute/path/to/miR-Input.fa -tarfile /absolute/path/to/Tar-Input.fa -outfdir /absolute/path/to/outputdir -display on</pre>
<h3>2. Linux:</h3>
<pre>    $ /absolute/path/to/tarp [-Options <value/string>]
    # eg:/absolute/path/to/tarp -prefile /absolute/path/to/miR-Input.fa -tarfile /absolute/path/to/Tar-Input.fa -outfdir /absolute/path/to/outputdir -outfpre OutPut_Result -auto on -ug on -seed on -move 3 -jump 0 -mode s2s -st 75 -en 65 -tarnum 1 -weight 2,10,3,7,0.01 -thread 2 -display on</pre>

<h3>-Options:</h3>

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
    -v,--version                                          # You can enter the '/absolute/path/to/tarp.exe -v'(Windows) or '/absolute/path/to/tarp -v'(Linux), and gain the help version information.
    -h,--help                                             # You can enter the '/absolute/path/to/tarp.exe -h'(Windows) or '/absolute/path/to/tarp -v'(Linux), and gain the help manual.


<h2>Other:</h2>

<pre>    If you have any doubts and suggestions about TarP software, you are welcome to communicate with us by email (FanTing_0123@163.com).</pre>
