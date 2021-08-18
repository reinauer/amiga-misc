# amiga-misc: Miscellaneous Amiga scripts and tidbits

## scripts

* splitadf
  Split large file into more than one ADF and add a script to join
  them again easily

  Example 1:
```
$ splitadf
Splitter: Split large (LHA) files and create ADF files for Gotek drives

Usage: splitadf file.lha

$
```

  Example 2:
```
$ splitadf ~/Downloads/Roadshow.lha
Archive: Roadshow.lha
Name:Roadshow.XX
Full Archive: 3395383
Per disk: 860000
Number of disks: 4
Roadshow1                                        VOLUME  --------  17.08.2021 19:56:14.00  DOS1:ffs #512
  Roadshow.01                                    860000  ----rwed  17.08.2021 19:56:14.00
  RunMe                                             114  -sparwed  17.08.2021 19:56:14.00
sum:          1707  853Ki        873984
data:         1681  840Ki        860672  98.48%
fs:             26   13Ki         13312   1.52%
Roadshow2                                        VOLUME  --------  17.08.2021 19:56:14.00  DOS1:ffs #512
  Roadshow.02                                    860000  ----rwed  17.08.2021 19:56:14.00
sum:          1705  852Ki        872960
data:         1680  840Ki        860160  98.53%
fs:             25   12Ki         12800   1.47%
Roadshow3                                        VOLUME  --------  17.08.2021 19:56:14.00  DOS1:ffs #512
  Roadshow.03                                    860000  ----rwed  17.08.2021 19:56:14.00
sum:          1705  852Ki        872960
data:         1680  840Ki        860160  98.53%
fs:             25   12Ki         12800   1.47%
Roadshow4                                        VOLUME  --------  17.08.2021 19:56:14.00  DOS1:ffs #512
  Roadshow.04                                    815383  ----rwed  17.08.2021 19:56:14.00
sum:          1617  808Ki        827904
data:         1593  796Ki        815616  98.52%
fs:             24   12Ki         12288   1.48%
JOIN Roadshow1:Roadshow.01 Roadshow2:Roadshow.02 Roadshow3:Roadshow.03 Roadshow4:Roadshow.04 AS WORK:Roadshow.lha
$
```

On the Amiga you can then create the original file with:
```
1> df0:RunMe
```

