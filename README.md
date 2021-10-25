# hse21_hw1
login as: aeshagaeva
Authenticating with public key "rsa-key-20211023"
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-87-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

 * Super-optimized for small spaces - read how we shrank the memory
   footprint of MicroK8s to make it the smallest full K8s around.

   https://ubuntu.com/blog/microk8s-memory-optimisation

 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

101 packages can be updated.
1 update is a security update.

New release '20.04.3 LTS' available.
Run 'do-release-upgrade' to upgrade to it.

Your Hardware Enablement Stack (HWE) is supported until April 2023.
*** System restart required ***
Last login: Mon Oct 25 23:05:28 2021 from 79.111.42.91
$ mkdir hw1
$ cd hw1
$ mkdir 1
$ cd 1
$ ls -1 /usr/share/data-minor-bionf/assembly/* | xargs -tI{} ln -s{}
ls: cannot access '/usr/share/data-minor-bionf/assembly/*': No such file or dire                                                                             ctory
$ ls -1 /usr/share/data-minor-bioinf/assembly/* | xargs -tI{} ln -s {}
ln -s /usr/share/data-minor-bioinf/assembly/oilMP_S4_L001_R1_001.fastq
ln -s /usr/share/data-minor-bioinf/assembly/oilMP_S4_L001_R2_001.fastq
ln -s /usr/share/data-minor-bioinf/assembly/oil_R1.fastq
ln -s /usr/share/data-minor-bioinf/assembly/oil_R2.fastq
$ seqtk sample -s1607 oil_R1.fastq 5000000 > pe_R1.fastq
$ seqtk sample -s1607 oil_R2.fastq 5000000 > pe_R2.fastq
$ seqtk sample -s1607 oilMP_S4_L001_R1_001.fastq 1500000 > mp_R1.fastq
$ seqtk sample -s1607 oilMP_S4_L001_R2_001.fastq 1500000 > mp_R2.fastq
$ mkdir fastqc
$ ls *.fastq | xargs -P 4 -tI{} fastqc -o fastqc {}
fastqc -o fastqc mp_R1.fastq
fastqc -o fastqc mp_R2.fastq
fastqc -o fastqc oilMP_S4_L001_R1_001.fastq
fastqc -o fastqc oilMP_S4_L001_R2_001.fastq
Started analysis of oilMP_S4_L001_R2_001.fastq
Started analysis of mp_R2.fastqStarted analysis of oilMP_S4_L001_R1_001.fastq

Started analysis of mp_R1.fastq
Approx 5% complete for mp_R2.fastq
Approx 5% complete for oilMP_S4_L001_R2_001.fastq
Approx 5% complete for oilMP_S4_L001_R1_001.fastq
Approx 5% complete for mp_R1.fastq
Approx 10% complete for mp_R2.fastq
Approx 10% complete for oilMP_S4_L001_R2_001.fastq
Approx 10% complete for oilMP_S4_L001_R1_001.fastq
Approx 10% complete for mp_R1.fastq
Approx 15% complete for mp_R2.fastq
Approx 15% complete for mp_R1.fastq
Approx 15% complete for oilMP_S4_L001_R2_001.fastq
Approx 15% complete for oilMP_S4_L001_R1_001.fastq
Approx 20% complete for mp_R2.fastq
Approx 20% complete for mp_R1.fastq
Approx 25% complete for mp_R2.fastq
Approx 20% complete for oilMP_S4_L001_R2_001.fastq
Approx 20% complete for oilMP_S4_L001_R1_001.fastq
Approx 25% complete for mp_R1.fastq
Approx 30% complete for mp_R2.fastq
Approx 25% complete for oilMP_S4_L001_R2_001.fastq
Approx 30% complete for mp_R1.fastq
Approx 25% complete for oilMP_S4_L001_R1_001.fastq
Approx 35% complete for mp_R2.fastq
Approx 35% complete for mp_R1.fastq
Approx 40% complete for mp_R2.fastq
Approx 30% complete for oilMP_S4_L001_R2_001.fastq
Approx 30% complete for oilMP_S4_L001_R1_001.fastq
Approx 40% complete for mp_R1.fastq
Approx 45% complete for mp_R2.fastq
Approx 35% complete for oilMP_S4_L001_R2_001.fastq
Approx 35% complete for oilMP_S4_L001_R1_001.fastq
Approx 45% complete for mp_R1.fastq
Approx 50% complete for mp_R2.fastq
Approx 50% complete for mp_R1.fastq
Approx 40% complete for oilMP_S4_L001_R2_001.fastq
Approx 40% complete for oilMP_S4_L001_R1_001.fastq
Approx 55% complete for mp_R2.fastq
Approx 55% complete for mp_R1.fastq
Approx 60% complete for mp_R2.fastq
Approx 45% complete for oilMP_S4_L001_R2_001.fastq
Approx 45% complete for oilMP_S4_L001_R1_001.fastq
Approx 60% complete for mp_R1.fastq
Approx 65% complete for mp_R2.fastq
Approx 50% complete for oilMP_S4_L001_R2_001.fastq
Approx 50% complete for oilMP_S4_L001_R1_001.fastq
Approx 65% complete for mp_R1.fastq
Approx 70% complete for mp_R2.fastq
Approx 70% complete for mp_R1.fastq
Approx 55% complete for oilMP_S4_L001_R2_001.fastq
Approx 55% complete for oilMP_S4_L001_R1_001.fastq
Approx 75% complete for mp_R2.fastq
Approx 75% complete for mp_R1.fastq
Approx 80% complete for mp_R2.fastq
Approx 60% complete for oilMP_S4_L001_R2_001.fastq
Approx 60% complete for oilMP_S4_L001_R1_001.fastq
Approx 80% complete for mp_R1.fastq
Approx 85% complete for mp_R2.fastq
Approx 65% complete for oilMP_S4_L001_R2_001.fastq
Approx 85% complete for mp_R1.fastq
Approx 65% complete for oilMP_S4_L001_R1_001.fastq
Approx 90% complete for mp_R2.fastq
Approx 90% complete for mp_R1.fastq
Approx 70% complete for oilMP_S4_L001_R2_001.fastq
Approx 70% complete for oilMP_S4_L001_R1_001.fastq
Approx 95% complete for mp_R2.fastq
Approx 95% complete for mp_R1.fastq
Approx 100% complete for mp_R2.fastq
Analysis complete for mp_R2.fastq
Approx 75% complete for oilMP_S4_L001_R2_001.fastq
Approx 75% complete for oilMP_S4_L001_R1_001.fastq
Approx 100% complete for mp_R1.fastq
Analysis complete for mp_R1.fastq
Approx 80% complete for oilMP_S4_L001_R2_001.fastq
Approx 80% complete for oilMP_S4_L001_R1_001.fastq
Approx 85% complete for oilMP_S4_L001_R2_001.fastq
Approx 85% complete for oilMP_S4_L001_R1_001.fastq
Approx 90% complete for oilMP_S4_L001_R2_001.fastq
Approx 90% complete for oilMP_S4_L001_R1_001.fastq
Approx 95% complete for oilMP_S4_L001_R2_001.fastq
Approx 95% complete for oilMP_S4_L001_R1_001.fastq
Analysis complete for oilMP_S4_L001_R2_001.fastq
Analysis complete for oilMP_S4_L001_R1_001.fastq
fastqc -o fastqc oil_R1.fastq
fastqc -o fastqc oil_R2.fastq
Started analysis of oil_R2.fastq
Started analysis of oil_R1.fastq
Approx 5% complete for oil_R1.fastq
Approx 5% complete for oil_R2.fastq
Approx 10% complete for oil_R1.fastq
Approx 10% complete for oil_R2.fastq
Approx 15% complete for oil_R1.fastq
Approx 15% complete for oil_R2.fastq
fastqc -o fastqc pe_R1.fastq
fastqc -o fastqc pe_R2.fastq
Started analysis of pe_R2.fastq
Approx 20% complete for oil_R1.fastq
Started analysis of pe_R1.fastq
Approx 20% complete for oil_R2.fastq
Approx 5% complete for pe_R2.fastq
Approx 25% complete for oil_R1.fastq
Approx 5% complete for pe_R1.fastq
Approx 25% complete for oil_R2.fastq
Approx 10% complete for pe_R2.fastq
Approx 10% complete for pe_R1.fastq
Approx 30% complete for oil_R1.fastq
Approx 30% complete for oil_R2.fastq
Approx 15% complete for pe_R2.fastq
Approx 15% complete for pe_R1.fastq
Approx 35% complete for oil_R1.fastq
Approx 20% complete for pe_R2.fastq
Approx 35% complete for oil_R2.fastq
Approx 20% complete for pe_R1.fastq
Approx 25% complete for pe_R2.fastq
Approx 40% complete for oil_R1.fastq
Approx 40% complete for oil_R2.fastq
Approx 25% complete for pe_R1.fastq
Approx 30% complete for pe_R2.fastq
Approx 45% complete for oil_R1.fastq
Approx 45% complete for oil_R2.fastq
Approx 30% complete for pe_R1.fastq
Approx 35% complete for pe_R2.fastq
Approx 50% complete for oil_R1.fastq
Approx 35% complete for pe_R1.fastq
Approx 50% complete for oil_R2.fastq
Approx 40% complete for pe_R2.fastq
Approx 40% complete for pe_R1.fastq
Approx 55% complete for oil_R1.fastq
Approx 45% complete for pe_R2.fastq
Approx 55% complete for oil_R2.fastq
Approx 45% complete for pe_R1.fastq
Approx 50% complete for pe_R2.fastq
Approx 60% complete for oil_R1.fastq
Approx 60% complete for oil_R2.fastq
Approx 50% complete for pe_R1.fastq
Approx 55% complete for pe_R2.fastq
Approx 65% complete for oil_R1.fastq
Approx 65% complete for oil_R2.fastq
Approx 55% complete for pe_R1.fastq
Approx 60% complete for pe_R2.fastq
Approx 70% complete for oil_R1.fastq
Approx 60% complete for pe_R1.fastq
Approx 70% complete for oil_R2.fastq
Approx 65% complete for pe_R2.fastq
Approx 75% complete for oil_R1.fastq
Approx 65% complete for pe_R1.fastq
Approx 70% complete for pe_R2.fastq
Approx 75% complete for oil_R2.fastq
Approx 70% complete for pe_R1.fastq
Approx 80% complete for oil_R1.fastq
Approx 75% complete for pe_R2.fastq
Approx 80% complete for oil_R2.fastq
Approx 75% complete for pe_R1.fastq
Approx 80% complete for pe_R2.fastq
Approx 85% complete for oil_R1.fastq
Approx 85% complete for oil_R2.fastq
Approx 80% complete for pe_R1.fastq
Approx 85% complete for pe_R2.fastq
Approx 90% complete for oil_R1.fastq
Approx 85% complete for pe_R1.fastq
Approx 90% complete for oil_R2.fastq
Approx 90% complete for pe_R2.fastq
Approx 95% complete for oil_R1.fastq
Approx 90% complete for pe_R1.fastq
Approx 95% complete for pe_R2.fastq
Approx 95% complete for oil_R2.fastq
Analysis complete for oil_R1.fastq
Approx 95% complete for pe_R1.fastq
Approx 100% complete for pe_R2.fastq
Analysis complete for pe_R2.fastq
Analysis complete for oil_R2.fastq
Approx 100% complete for pe_R1.fastq
Analysis complete for pe_R1.fastq
$ mkdir multiqc
$ multiqc -o multiqc fastqc
[WARNING]         multiqc : MultiQC Version v1.11 now available!
[INFO   ]         multiqc : This is MultiQC v1.10.dev0
[INFO   ]         multiqc : Template    : default
[INFO   ]         multiqc : Searching   : /home/aeshagaeva/hw1/1/fastqc
[INFO   ]          fastqc : Found 8 reports
[INFO   ]         multiqc : Compressing plot data
[INFO   ]         multiqc : Report      : multiqc/multiqc_report.html
[INFO   ]         multiqc : Data        : multiqc/multiqc_data
[INFO   ]         multiqc : MultiQC complete
$ platanus_trim pe_R1.fastq pe_R2.fastq
Running with trim adapter mode
Checking files:
  pe_R1.fastq pe_R2.fastq  (100%)

Number of trimmed read with adapter:
NUM_OF_TRIMMED_READ(FORWARD) = 209373
NUM_OF_TRIMMED_BASE(FORWARD) = 206099
NUM_OF_TRIMMED_READ(REVERSE) = 209431
NUM_OF_TRIMMED_BASE(REVERSE) = 353215
NUM_OF_TRIMMED_PAIR(OR) = 209451
NUM_OF_TRIMMED_PAIR(AND) = 209353


Number of trimmed read because of low quality or too short (< 11bp):
NUM_OF_TRIMMED_READ(FORWARD) = 907693
NUM_OF_TRIMMED_BASE(FORWARD) = 18130235
NUM_OF_TRIMMED_READ(REVERSE) = 1179756
NUM_OF_TRIMMED_BASE(REVERSE) = 35913734
NUM_OF_TRIMMED_PAIR(OR) = 1630958
NUM_OF_TRIMMED_PAIR(AND) = 456491


#### PROCESS INFORMATION ####
User Time:           1.09 min
System Time:         0.03 min
VmPeak:           0.130 GByte
VmHWM:            0.109 GByte
Execution time:      1.12 min

$ platunus_internal_trim mp_R1.fastq mp_R2.fastq
-sh: 16: platunus_internal_trim: not found
$ platanus_internal_trim mp_R1.fastq mp_R2.fastq
Running with trim internal adapter mode
Checking files:
  mp_R1.fastq mp_R2.fastq  (100%)

Number of trimmed read with internal adapter:
NUM_OF_TRIMMED_READ(FORWARD) = 972230
NUM_OF_TRIMMED_BASE(FORWARD) = 169638210
NUM_OF_TRIMMED_READ(REVERSE) = 955282
NUM_OF_TRIMMED_BASE(REVERSE) = 171209427
NUM_OF_TRIMMED_PAIR(OR) = 1187853
NUM_OF_TRIMMED_PAIR(AND) = 739659


Number of trimmed read with adapter:
NUM_OF_TRIMMED_READ(FORWARD) = 11124
NUM_OF_TRIMMED_BASE(FORWARD) = 363304
NUM_OF_TRIMMED_READ(REVERSE) = 11146
NUM_OF_TRIMMED_BASE(REVERSE) = 383820
NUM_OF_TRIMMED_PAIR(OR) = 11151
NUM_OF_TRIMMED_PAIR(AND) = 11119


Number of trimmed read because of low quality or too short (< 11bp):
NUM_OF_TRIMMED_READ(FORWARD) = 360442
NUM_OF_TRIMMED_BASE(FORWARD) = 11665685
NUM_OF_TRIMMED_READ(REVERSE) = 469214
NUM_OF_TRIMMED_BASE(REVERSE) = 23950461
NUM_OF_TRIMMED_PAIR(OR) = 724567
NUM_OF_TRIMMED_PAIR(AND) = 105089


#### PROCESS INFORMATION ####
User Time:           1.12 min
System Time:         0.01 min
VmPeak:           0.181 GByte
VmHWM:            0.161 GByte
Execution time:      1.13 min

$ mkdir trimmed_fastq
$ mv -v *trimmed_fastq/
mv: missing destination file operand after 'trimmed_fastq/'
Try 'mv --help' for more information.
$ ls trimmed_fastq/* | xargs -P 4 -tI{} fastqc -o trimmed_fastqc {}
ls: cannot access 'trimmed_fastq/*': No such file or directory
$ mkdir trimmed_fastq
mkdir: cannot create directory ‘trimmed_fastq’: File exists
$ mkdir trimmed_fastq1
$ mv -v *trimmed trimmed_fastq1/
renamed 'mp_R1.fastq.int_trimmed' -> 'trimmed_fastq1/mp_R1.fastq.int_trimmed'
renamed 'mp_R2.fastq.int_trimmed' -> 'trimmed_fastq1/mp_R2.fastq.int_trimmed'
renamed 'pe_R1.fastq.trimmed' -> 'trimmed_fastq1/pe_R1.fastq.trimmed'
renamed 'pe_R2.fastq.trimmed' -> 'trimmed_fastq1/pe_R2.fastq.trimmed'
$ mkdir trimmed_fastqc
$ ls trimmed_fastq1/* | xargs -P 4 -tI{} fastqc -o trimmed_fastqc {}
fastqc -o trimmed_fastqc trimmed_fastq1/mp_R1.fastq.int_trimmed
fastqc -o trimmed_fastqc trimmed_fastq1/mp_R2.fastq.int_trimmed
fastqc -o trimmed_fastqc trimmed_fastq1/pe_R1.fastq.trimmed
fastqc -o trimmed_fastqc trimmed_fastq1/pe_R2.fastq.trimmed
Started analysis of mp_R1.fastq.int_trimmed
Started analysis of pe_R2.fastq.trimmed
Approx 5% complete for mp_R1.fastq.int_trimmed
Started analysis of mp_R2.fastq.int_trimmed
Started analysis of pe_R1.fastq.trimmed
Approx 10% complete for mp_R1.fastq.int_trimmed
Approx 15% complete for mp_R1.fastq.int_trimmed
Approx 5% complete for mp_R2.fastq.int_trimmed
Approx 20% complete for mp_R1.fastq.int_trimmed
Approx 5% complete for pe_R2.fastq.trimmed
Approx 10% complete for mp_R2.fastq.int_trimmed
Approx 25% complete for mp_R1.fastq.int_trimmed
Approx 15% complete for mp_R2.fastq.int_trimmed
Approx 30% complete for mp_R1.fastq.int_trimmed
Approx 20% complete for mp_R2.fastq.int_trimmed
Approx 5% complete for pe_R1.fastq.trimmed
Approx 35% complete for mp_R1.fastq.int_trimmed
Approx 25% complete for mp_R2.fastq.int_trimmed
Approx 40% complete for mp_R1.fastq.int_trimmed
Approx 30% complete for mp_R2.fastq.int_trimmed
Approx 10% complete for pe_R2.fastq.trimmed
Approx 45% complete for mp_R1.fastq.int_trimmed
Approx 35% complete for mp_R2.fastq.int_trimmed
Approx 50% complete for mp_R1.fastq.int_trimmed
Approx 40% complete for mp_R2.fastq.int_trimmed
Approx 55% complete for mp_R1.fastq.int_trimmed
Approx 45% complete for mp_R2.fastq.int_trimmed
Approx 10% complete for pe_R1.fastq.trimmed
Approx 60% complete for mp_R1.fastq.int_trimmed
Approx 50% complete for mp_R2.fastq.int_trimmed
Approx 65% complete for mp_R1.fastq.int_trimmed
Approx 15% complete for pe_R2.fastq.trimmed
Approx 55% complete for mp_R2.fastq.int_trimmed
Approx 70% complete for mp_R1.fastq.int_trimmed
Approx 60% complete for mp_R2.fastq.int_trimmed
Approx 75% complete for mp_R1.fastq.int_trimmed
Approx 65% complete for mp_R2.fastq.int_trimmed
Approx 80% complete for mp_R1.fastq.int_trimmed
Approx 70% complete for mp_R2.fastq.int_trimmed
Approx 15% complete for pe_R1.fastq.trimmed
Approx 85% complete for mp_R1.fastq.int_trimmed
Approx 75% complete for mp_R2.fastq.int_trimmed
Approx 20% complete for pe_R2.fastq.trimmed
Approx 90% complete for mp_R1.fastq.int_trimmed
Approx 80% complete for mp_R2.fastq.int_trimmed
Approx 95% complete for mp_R1.fastq.int_trimmed
Approx 85% complete for mp_R2.fastq.int_trimmed
Analysis complete for mp_R1.fastq.int_trimmed
Approx 90% complete for mp_R2.fastq.int_trimmed
Approx 20% complete for pe_R1.fastq.trimmed
Approx 95% complete for mp_R2.fastq.int_trimmed
Analysis complete for mp_R2.fastq.int_trimmed
Approx 25% complete for pe_R2.fastq.trimmed
Approx 25% complete for pe_R1.fastq.trimmed
Approx 30% complete for pe_R2.fastq.trimmed
Approx 30% complete for pe_R1.fastq.trimmed
Approx 35% complete for pe_R2.fastq.trimmed
Approx 35% complete for pe_R1.fastq.trimmed
Approx 40% complete for pe_R2.fastq.trimmed
Approx 40% complete for pe_R1.fastq.trimmed
Approx 45% complete for pe_R2.fastq.trimmed
Approx 45% complete for pe_R1.fastq.trimmed
Approx 50% complete for pe_R2.fastq.trimmed
Approx 50% complete for pe_R1.fastq.trimmed
Approx 55% complete for pe_R2.fastq.trimmed
Approx 55% complete for pe_R1.fastq.trimmed
Approx 60% complete for pe_R2.fastq.trimmed
Approx 60% complete for pe_R1.fastq.trimmed
Approx 65% complete for pe_R2.fastq.trimmed
Approx 70% complete for pe_R2.fastq.trimmed
Approx 65% complete for pe_R1.fastq.trimmed
Approx 75% complete for pe_R2.fastq.trimmed
Approx 70% complete for pe_R1.fastq.trimmed
Approx 80% complete for pe_R2.fastq.trimmed
Approx 75% complete for pe_R1.fastq.trimmed
Approx 85% complete for pe_R2.fastq.trimmed
Approx 80% complete for pe_R1.fastq.trimmed
Approx 90% complete for pe_R2.fastq.trimmed
Approx 85% complete for pe_R1.fastq.trimmed
Approx 95% complete for pe_R2.fastq.trimmed
Approx 90% complete for pe_R1.fastq.trimmed
Analysis complete for pe_R2.fastq.trimmed
Approx 95% complete for pe_R1.fastq.trimmed
Analysis complete for pe_R1.fastq.trimmed
mk$ mkdir trimmed_multiqc
-sh: 26: $: not found
$ mkdir trimmed_multiqc
$ multiqc -o trimmed_multiqc trimmed fastqc
Usage: multiqc [OPTIONS] <analysis directory>

Error: Invalid value for '<analysis directory>': Path 'trimmed' does not exist.

This is MultiQC v1.10.dev0

For more help, run 'multiqc --help' or visit http://multiqc.info

$ mkdir trimmed_multiqc1
$ multiqc -o trimmed_multiqc1 trimmed_fastqc
[WARNING]         multiqc : MultiQC Version v1.11 now available!
[INFO   ]         multiqc : This is MultiQC v1.10.dev0
[INFO   ]         multiqc : Template    : default
[INFO   ]         multiqc : Searching   : /home/aeshagaeva/hw1/1/trimmed_fastqc
[INFO   ]          fastqc : Found 4 reports
[INFO   ]         multiqc : Compressing plot data
[INFO   ]         multiqc : Report      : trimmed_multiqc1/multiqc_report.html
[INFO   ]         multiqc : Data        : trimmed_multiqc1/multiqc_data
[INFO   ]         multiqc : MultiQC complete
$ mkdir otchet
$ mv multiqc otchet
$ mv trimmed_multiqc1 otchet
$ mv fastqc otchet
$ mv trimmed_fastqc otchet
$ tar -cvzf shagaeva.tar.gz otchet
otchet/
otchet/trimmed_multiqc1/
otchet/trimmed_multiqc1/multiqc_data/
otchet/trimmed_multiqc1/multiqc_data/multiqc_fastqc.txt
otchet/trimmed_multiqc1/multiqc_data/multiqc_general_stats.txt
otchet/trimmed_multiqc1/multiqc_data/multiqc_data.json
otchet/trimmed_multiqc1/multiqc_data/multiqc_sources.txt
otchet/trimmed_multiqc1/multiqc_data/multiqc.log
otchet/trimmed_multiqc1/multiqc_report.html
otchet/trimmed_fastqc/
otchet/trimmed_fastqc/pe_R2.fastq.trimmed_fastqc.zip
otchet/trimmed_fastqc/mp_R1.fastq.int_trimmed_fastqc.zip
otchet/trimmed_fastqc/pe_R1.fastq.trimmed_fastqc.zip
otchet/trimmed_fastqc/mp_R2.fastq.int_trimmed_fastqc.zip
otchet/trimmed_fastqc/mp_R2.fastq.int_trimmed_fastqc.html
otchet/trimmed_fastqc/mp_R1.fastq.int_trimmed_fastqc.html
otchet/trimmed_fastqc/pe_R1.fastq.trimmed_fastqc.html
otchet/trimmed_fastqc/pe_R2.fastq.trimmed_fastqc.html
otchet/fastqc/
otchet/fastqc/mp_R2_fastqc.zip
otchet/fastqc/mp_R1_fastqc.zip
otchet/fastqc/pe_R1_fastqc.html
otchet/fastqc/oilMP_S4_L001_R1_001_fastqc.zip
otchet/fastqc/mp_R1_fastqc.html
otchet/fastqc/oil_R1_fastqc.html
otchet/fastqc/pe_R2_fastqc.html
otchet/fastqc/oilMP_S4_L001_R2_001_fastqc.html
otchet/fastqc/oilMP_S4_L001_R2_001_fastqc.zip
otchet/fastqc/oil_R2_fastqc.zip
otchet/fastqc/oil_R2_fastqc.html
otchet/fastqc/mp_R2_fastqc.html
otchet/fastqc/oilMP_S4_L001_R1_001_fastqc.html
otchet/fastqc/pe_R2_fastqc.zip
otchet/fastqc/oil_R1_fastqc.zip
otchet/fastqc/pe_R1_fastqc.zip
otchet/multiqc/
otchet/multiqc/multiqc_data/
otchet/multiqc/multiqc_data/multiqc_fastqc.txt
otchet/multiqc/multiqc_data/multiqc_general_stats.txt
otchet/multiqc/multiqc_data/multiqc_data.json
otchet/multiqc/multiqc_data/multiqc_sources.txt
otchet/multiqc/multiqc_data/multiqc.log
otchet/multiqc/multiqc_report.html
$
