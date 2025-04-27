<h1>TarP</h1>
<p>This is a miRNA target prediction tool based on polymorphic structured base alignment algorithm. The tool can realize target prediction of specific or non-specific species, conservative or non-conservative sequences based on user-defined parameter combinations. Using it can help users get the candidate targets of miRNA accurately, and lay the foundation for further research.</p>


<h2>Data Frame:</h2>
<h3>Input Files</h3>
<h4>1. miRNA Sequence Input File:(miR-Input.fa)</h4>
<p>>miR-example1</p>
<p>GUUUGUGACCGUCACUAACGGGCAGU</p>
<p>>miR-example2</p>
<p>UCGUUUUGGCGAUCGCAAAAUG</p>
<h4>2. mRNA Sequence Input File:(Tar-Input.fa)</h4>
<p>>Tar_example1</p>
<p>AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC</p>
<p>>Tar_example2</p>
<p>AGTAGCACTAGGCTACTGACACTCCCGGCGCCCTTCCGCATCCCTCGCTCACCCTCTCTCCCTCCTCGTTCCCATTCAAGCTATCGACTCATAAGCGACACGTCCTATATTCATTGTGAAGCCCTTAGACTTACTTGCCATCTAAGGATATTTATTCATATAATATATGTGTGGTATTTAATCAATTAATTAATTAAAATTATACAGATTCACAAATTCACTAATTGATCTTTAGACCTGCTCCATCTCATCTAACAATAAAAACAAATTCAAATACCTGAAATAAAATAAATTGCAAGTCACATCTGCCAATCTTAAATGTACCCATTTGCAAGGTGTGGCATCAAAATGTTCAACTTACATCCAGTTTAATTTTTCAGAGAAATGTAATTCCATTGCAATATATTGGTTGGTTGGGGTTGCATTGGTAGCGAGTCGCACGAACCTGCATTCTGCACTTTCGAAAACTCAAATCGAATCCTCAACATACCCAAAACCTTGATCTCCATAATATATTATGATAAAGTTGTACAGTAGTTTTTGTAGCCTTGTTGTATGCAAACAACTAATTCTTACAATTTATCACCAATTACATTGTAGTGCATCAGTAATAATATAATACTGCGT</p>

<h3>Output Files</h3>
<h4>1. miRNA-mRNA Target Result File:(TarPPreResult_auto_tar.txt)</h4>
TarID	TarSeq	MiRID	MiRSeq	Tar_Part	MiR_Part	Match_State	St	En
Tar_example1	AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC	miR-example1	GUUUGUGACCGUCACUAACGGGCAGU	GCUGCAUOUUGAGGACACUCACAAGA	UGACGGGCAAUCACUGCCAGUGUUUG	[2,1,1,1,1,0,2,0,1,1,2,0,0,1,1,1,0,0,1,1,1,1,1,1,2,0]	69.13	57.69
Tar_example1	AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC	miR-example1	GUUUGUGACCGUCACUAACGGGCAGU	GCUGCAUOUUGAGGACACUCACAAGO	UGACGGGCAAUCACUGCCAGUGUUUG	[2,1,1,1,1,0,2,0,1,1,2,0,0,1,1,1,0,0,1,1,1,1,1,1,2,0]	69.13	57.69

<h4>2. miRNA-mRNA Binding Site File:(TarPPreResult_auto_pair.txt)</h4>
<p>
Tar ID:  tar_example1
Tar Seq:  AGGGCCCGCCTCCGCCACCGTCGCCCTCACACTCGTTGATTGAACGATAGTAAATTTAACGTCAAAAAATGTATTGTTTGTTAGAGAATTCGCGCGACAGGCGCTCGGTGCCCTTGAACCCAAACATAGCTGCATTTGAGGACACTCACAAGAACGTCGCTAAGAACATCCTCGCCGTCTCTGGCGTGAAACATCAACTTGAATCCGCTCCTCGGCTTGTGTAGACACGGCCCCCAGTCCCCATCCATGACGTGTTGCCTCAACATCTCAGCGCAGACTACGAACTACCTTGCTTGACATCGTCATTGCGTAGTAAAGTTCTATATATAATAGAAAAAAACACTATATGGTTTAGTGCGATAAGTCTGGCAAGTTTGATAAGATAAGCCAAAGCTCAGCACTAAAGTCTGCAGACAACGCGCAC
MiR ID:	miR-example1
MiR Seq:   GUUUGUGACCGUCACUAACGGGCAGU
St:   69.13
En:   57.69

Target:			5'		G	C	U	G	C	A	U		U	U	G	A	G	G	A	C	A	C	U	C	A	C	A	A	G	A			3'	
matchstate:				:	|	|	|	|		:		|	|	:			|	|	|			|	|	|	|	|	|	:		   			
MiRNA:			3'		U	G	A	C	G	G	G	C	A	A	U	C	A	C	U	G	C	C	A	G	U	G	U	U	U	G			5'	

Tar ID:  tar_example2
Tar Seq:  AGTAGCACTAGGCTACTGACACTCCCGGCGCCCTTCCGCATCCCTCGCTCACCCTCTCTCCCTCCTCGTTCCCATTCAAGCTATCGACTCATAAGCGACACGTCCTATATTCATTGTGAAGCCCTTAGACTTACTTGCCATCTAAGGATATTTATTCATATAATATATGTGTGGTATTTAATCAATTAATTAATTAAAATTATACAGATTCACAAATTCACTAATTGATCTTTAGACCTGCTCCATCTCATCTAACAATAAAAACAAATTCAAATACCTGAAATAAAATAAATTGCAAGTCACATCTGCCAATCTTAAATGTACCCATTTGCAAGGTGTGGCATCAAAATGTTCAACTTACATCCAGTTTAATTTTTCAGAGAAATGTAATTCCATTGCAATATATTGGTTGGTTGGGGTTGCATTGGTAGCGAGTCGCACGAACCTGCATTCTGCACTTTCGAAAACTCAAATCGAATCCTCAACATACCCAAAACCTTGATCTCCATAATATATTATGATAAAGTTGTACAGTAGTTTTTGTAGCCTTGTTGTATGCAAACAACTAATTCTTACAATTTATCACCAATTACATTGTAGTGCATCAGTAATAATATAATACTGCGT
MiR ID:	miR-example2
MiR Seq:   UCGUUUUGGCGAUCGCAAAAUG
St:   63.32
En:   52.31

Target:			5'		U	A	U	A	U			U	G	G	U	U	G	G	U	U	G	G	G	G	U	U	G			3'	
matchstate:				:	|	|		|			:	|	:	|	:		|	:	:	:	:	:	:	:		:	   			
MiRNA:			3'		G	U	A	A	A	A	C	G	C	U	A	G		C	G	G	U	U	U	U	G	C	U			5'	
</p>

<h2>USAGE:</h2>

<h3>Windows:</h3>
    $ /absolute/path/to/tarp.exe [-Options <value/string>]
    # eg:
<h3>Linux:</h3>
    $ /absolute/path/to/tarp [-Options <value/string>]


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


<h2>Other:</h2>

    If you have any doubts and suggestions about TarP software, you are welcome to communicate with us by email (FanTing_0123@163.com).
