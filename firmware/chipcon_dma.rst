                              1 ;--------------------------------------------------------
                              2 ; File Created by SDCC : free open source ANSI-C Compiler
                              3 ; Version 3.3.0 #8604 (Dec 30 2013) (Linux)
                              4 ; This file was generated Fri Dec 16 14:41:38 2016
                              5 ;--------------------------------------------------------
                              6 	.module chipcon_dma
                              7 	.optsdcc -mmcs51 --model-small
                              8 	
                              9 ;--------------------------------------------------------
                             10 ; Public variables in this module
                             11 ;--------------------------------------------------------
                             12 	.globl _memset
                             13 	.globl _USBIF
                             14 	.globl _MODE
                             15 	.globl _RE
                             16 	.globl _SLAVE
                             17 	.globl _FE
                             18 	.globl _ERR
                             19 	.globl _RX_BYTE
                             20 	.globl _TX_BYTE
                             21 	.globl _ACTIVE
                             22 	.globl _B_7
                             23 	.globl _B_6
                             24 	.globl _B_5
                             25 	.globl _B_4
                             26 	.globl _B_3
                             27 	.globl _B_2
                             28 	.globl _B_1
                             29 	.globl _B_0
                             30 	.globl _WDTIF
                             31 	.globl _P1IF
                             32 	.globl _UTX1IF
                             33 	.globl _UTX0IF
                             34 	.globl _P2IF
                             35 	.globl _ACC_7
                             36 	.globl _ACC_6
                             37 	.globl _ACC_5
                             38 	.globl _ACC_4
                             39 	.globl _ACC_3
                             40 	.globl _ACC_2
                             41 	.globl _ACC_1
                             42 	.globl _ACC_0
                             43 	.globl _OVFIM
                             44 	.globl _T4CH1IF
                             45 	.globl _T4CH0IF
                             46 	.globl _T4OVFIF
                             47 	.globl _T3CH1IF
                             48 	.globl _T3CH0IF
                             49 	.globl _T3OVFIF
                             50 	.globl _CY
                             51 	.globl _AC
                             52 	.globl _F0
                             53 	.globl _RS1
                             54 	.globl _RS0
                             55 	.globl _OV
                             56 	.globl _F1
                             57 	.globl _P
                             58 	.globl _STIF
                             59 	.globl _P0IF
                             60 	.globl _T4IF
                             61 	.globl _T3IF
                             62 	.globl _T2IF
                             63 	.globl _T1IF
                             64 	.globl _DMAIF
                             65 	.globl _P0IE
                             66 	.globl _T4IE
                             67 	.globl _T3IE
                             68 	.globl _T2IE
                             69 	.globl _T1IE
                             70 	.globl _DMAIE
                             71 	.globl _EA
                             72 	.globl _STIE
                             73 	.globl _ENCIE
                             74 	.globl _URX1IE
                             75 	.globl _URX0IE
                             76 	.globl _ADCIE
                             77 	.globl _RFTXRXIE
                             78 	.globl _P2_7
                             79 	.globl _P2_6
                             80 	.globl _P2_5
                             81 	.globl _P2_4
                             82 	.globl _P2_3
                             83 	.globl _P2_2
                             84 	.globl _P2_1
                             85 	.globl _P2_0
                             86 	.globl _ENCIF_1
                             87 	.globl _ENCIF_0
                             88 	.globl _P1_7
                             89 	.globl _P1_6
                             90 	.globl _P1_5
                             91 	.globl _P1_4
                             92 	.globl _P1_3
                             93 	.globl _P1_2
                             94 	.globl _P1_1
                             95 	.globl _P1_0
                             96 	.globl _URX1IF
                             97 	.globl _ADCIF
                             98 	.globl _URX0IF
                             99 	.globl _IT1
                            100 	.globl _RFTXRXIF
                            101 	.globl _IT0
                            102 	.globl _P0_7
                            103 	.globl _P0_6
                            104 	.globl _P0_5
                            105 	.globl _P0_4
                            106 	.globl _P0_3
                            107 	.globl _P0_2
                            108 	.globl _P0_1
                            109 	.globl _P0_0
                            110 	.globl _P2DIR
                            111 	.globl _P1DIR
                            112 	.globl _P0DIR
                            113 	.globl _U1GCR
                            114 	.globl _U1UCR
                            115 	.globl _U1BAUD
                            116 	.globl _U1DBUF
                            117 	.globl _U1CSR
                            118 	.globl _P2INP
                            119 	.globl _P1INP
                            120 	.globl _P2SEL
                            121 	.globl _P1SEL
                            122 	.globl _P0SEL
                            123 	.globl _ADCCFG
                            124 	.globl _PERCFG
                            125 	.globl _B
                            126 	.globl _T4CC1
                            127 	.globl _T4CCTL1
                            128 	.globl _T4CC0
                            129 	.globl _T4CCTL0
                            130 	.globl _T4CTL
                            131 	.globl _T4CNT
                            132 	.globl _RFIF
                            133 	.globl _IRCON2
                            134 	.globl _T1CCTL2
                            135 	.globl _T1CCTL1
                            136 	.globl _T1CCTL0
                            137 	.globl _T1CTL
                            138 	.globl _T1CNTH
                            139 	.globl _T1CNTL
                            140 	.globl _RFST
                            141 	.globl _ACC
                            142 	.globl _T1CC2H
                            143 	.globl _T1CC2L
                            144 	.globl _T1CC1H
                            145 	.globl _T1CC1L
                            146 	.globl _T1CC0H
                            147 	.globl _T1CC0L
                            148 	.globl _RFD
                            149 	.globl _TIMIF
                            150 	.globl _DMAREQ
                            151 	.globl _DMAARM
                            152 	.globl _DMA0CFGH
                            153 	.globl _DMA0CFGL
                            154 	.globl _DMA1CFGH
                            155 	.globl _DMA1CFGL
                            156 	.globl _DMAIRQ
                            157 	.globl _PSW
                            158 	.globl _T3CC1
                            159 	.globl _T3CCTL1
                            160 	.globl _T3CC0
                            161 	.globl _T3CCTL0
                            162 	.globl _T3CTL
                            163 	.globl _T3CNT
                            164 	.globl _WDCTL
                            165 	.globl __SFRC8
                            166 	.globl _MEMCTR
                            167 	.globl _CLKCON
                            168 	.globl _U0GCR
                            169 	.globl _U0UCR
                            170 	.globl __SFRC3
                            171 	.globl _U0BAUD
                            172 	.globl _U0DBUF
                            173 	.globl _IRCON
                            174 	.globl __SFRBF
                            175 	.globl _SLEEP
                            176 	.globl _RNDH
                            177 	.globl _RNDL
                            178 	.globl _ADCH
                            179 	.globl _ADCL
                            180 	.globl _IP1
                            181 	.globl _IEN1
                            182 	.globl __SFRB7
                            183 	.globl _ADCCON3
                            184 	.globl _ADCCON2
                            185 	.globl _ADCCON1
                            186 	.globl _ENCCS
                            187 	.globl _ENCDO
                            188 	.globl _ENCDI
                            189 	.globl __SFRB0
                            190 	.globl _FWDATA
                            191 	.globl _FCTL
                            192 	.globl _FADDRH
                            193 	.globl _FADDRL
                            194 	.globl _FWT
                            195 	.globl __SFRAA
                            196 	.globl _IP0
                            197 	.globl _IEN0
                            198 	.globl __SFRA7
                            199 	.globl _WORTIME1
                            200 	.globl _WORTIME0
                            201 	.globl _WOREVT1
                            202 	.globl _WOREVT0
                            203 	.globl _WORCTRL
                            204 	.globl _WORIRQ
                            205 	.globl _P2
                            206 	.globl __SFR9F
                            207 	.globl _T2CTL
                            208 	.globl _T2PR
                            209 	.globl _T2CT
                            210 	.globl _S1CON
                            211 	.globl _IEN2
                            212 	.globl __SFR99
                            213 	.globl _S0CON
                            214 	.globl __SFR97
                            215 	.globl __SFR96
                            216 	.globl __SFR95
                            217 	.globl __SFR94
                            218 	.globl __XPAGE
                            219 	.globl _MPAGE
                            220 	.globl _DPS
                            221 	.globl _RFIM
                            222 	.globl _P1
                            223 	.globl _P0INP
                            224 	.globl __SFR8E
                            225 	.globl _P1IEN
                            226 	.globl _PICTL
                            227 	.globl _P2IFG
                            228 	.globl _P1IFG
                            229 	.globl _P0IFG
                            230 	.globl _TCON
                            231 	.globl _PCON
                            232 	.globl _U0CSR
                            233 	.globl _DPH1
                            234 	.globl _DPL1
                            235 	.globl _DPH0
                            236 	.globl _DPL0
                            237 	.globl _SP
                            238 	.globl _P0
                            239 	.globl _dma_configs
                            240 	.globl _USBF5
                            241 	.globl _USBF4
                            242 	.globl _USBF3
                            243 	.globl _USBF2
                            244 	.globl _USBF1
                            245 	.globl _USBF0
                            246 	.globl _USBCNTH
                            247 	.globl _USBCNTL
                            248 	.globl _USBCNT0
                            249 	.globl _USBCSOH
                            250 	.globl _USBCSOL
                            251 	.globl _USBMAXO
                            252 	.globl _USBCSIH
                            253 	.globl _USBCSIL
                            254 	.globl _USBCS0
                            255 	.globl _USBMAXI
                            256 	.globl _USBINDEX
                            257 	.globl _USBFRMH
                            258 	.globl _USBFRML
                            259 	.globl _USBCIE
                            260 	.globl _USBOIE
                            261 	.globl _USBIIE
                            262 	.globl _USBCIF
                            263 	.globl _USBOIF
                            264 	.globl _USBIIF
                            265 	.globl _USBPOW
                            266 	.globl _USBADDR
                            267 	.globl _X_P2DIR
                            268 	.globl _X_P1DIR
                            269 	.globl _X_P0DIR
                            270 	.globl _X_U1GCR
                            271 	.globl _X_U1UCR
                            272 	.globl _X_U1BAUD
                            273 	.globl _X_U1DBUF
                            274 	.globl _X_U1CSR
                            275 	.globl _X_P2INP
                            276 	.globl _X_P1INP
                            277 	.globl _X_P2SEL
                            278 	.globl _X_P1SEL
                            279 	.globl _X_P0SEL
                            280 	.globl _X_ADCCFG
                            281 	.globl _X_PERCFG
                            282 	.globl __NA_B
                            283 	.globl _X_T4CC1
                            284 	.globl _X_T4CCTL1
                            285 	.globl _X_T4CC0
                            286 	.globl _X_T4CCTL0
                            287 	.globl _X_T4CTL
                            288 	.globl _X_T4CNT
                            289 	.globl _X_RFIF
                            290 	.globl __NA_IRCON2
                            291 	.globl _X_T1CCTL2
                            292 	.globl _X_T1CCTL1
                            293 	.globl _X_T1CCTL0
                            294 	.globl _X_T1CTL
                            295 	.globl _X_T1CNTH
                            296 	.globl _X_T1CNTL
                            297 	.globl _X_RFST
                            298 	.globl __NA_ACC
                            299 	.globl _X_T1CC2H
                            300 	.globl _X_T1CC2L
                            301 	.globl _X_T1CC1H
                            302 	.globl _X_T1CC1L
                            303 	.globl _X_T1CC0H
                            304 	.globl _X_T1CC0L
                            305 	.globl _X_RFD
                            306 	.globl _X_TIMIF
                            307 	.globl _X_DMAREQ
                            308 	.globl _X_DMAARM
                            309 	.globl _X_DMA0CFGH
                            310 	.globl _X_DMA0CFGL
                            311 	.globl _X_DMA1CFGH
                            312 	.globl _X_DMA1CFGL
                            313 	.globl _X_DMAIRQ
                            314 	.globl __NA_PSW
                            315 	.globl _X_T3CC1
                            316 	.globl _X_T3CCTL1
                            317 	.globl _X_T3CC0
                            318 	.globl _X_T3CCTL0
                            319 	.globl _X_T3CTL
                            320 	.globl _X_T3CNT
                            321 	.globl _X_WDCTL
                            322 	.globl __X_SFRC8
                            323 	.globl _X_MEMCTR
                            324 	.globl _X_CLKCON
                            325 	.globl _X_U0GCR
                            326 	.globl _X_U0UCR
                            327 	.globl __X_SFRC3
                            328 	.globl _X_U0BAUD
                            329 	.globl _X_U0DBUF
                            330 	.globl __NA_IRCON
                            331 	.globl __X_SFRBF
                            332 	.globl _X_SLEEP
                            333 	.globl _X_RNDH
                            334 	.globl _X_RNDL
                            335 	.globl _X_ADCH
                            336 	.globl _X_ADCL
                            337 	.globl __NA_IP1
                            338 	.globl __NA_IEN1
                            339 	.globl __X_SFRB7
                            340 	.globl _X_ADCCON3
                            341 	.globl _X_ADCCON2
                            342 	.globl _X_ADCCON1
                            343 	.globl _X_ENCCS
                            344 	.globl _X_ENCDO
                            345 	.globl _X_ENCDI
                            346 	.globl __X_SFRB0
                            347 	.globl _X_FWDATA
                            348 	.globl _X_FCTL
                            349 	.globl _X_FADDRH
                            350 	.globl _X_FADDRL
                            351 	.globl _X_FWT
                            352 	.globl __X_SFRAA
                            353 	.globl __NA_IP0
                            354 	.globl __NA_IEN0
                            355 	.globl __X_SFRA7
                            356 	.globl _X_WORTIME1
                            357 	.globl _X_WORTIME0
                            358 	.globl _X_WOREVT1
                            359 	.globl _X_WOREVT0
                            360 	.globl _X_WORCTRL
                            361 	.globl _X_WORIRQ
                            362 	.globl __NA_P2
                            363 	.globl __X_SFR9F
                            364 	.globl _X_T2CTL
                            365 	.globl _X_T2PR
                            366 	.globl _X_T2CT
                            367 	.globl __NA_S1CON
                            368 	.globl __NA_IEN2
                            369 	.globl __X_SFR99
                            370 	.globl __NA_S0CON
                            371 	.globl __X_SFR97
                            372 	.globl __X_SFR96
                            373 	.globl __X_SFR95
                            374 	.globl __X_SFR94
                            375 	.globl _X_MPAGE
                            376 	.globl __NA_DPS
                            377 	.globl _X_RFIM
                            378 	.globl __NA_P1
                            379 	.globl _X_P0INP
                            380 	.globl __X_SFR8E
                            381 	.globl _X_P1IEN
                            382 	.globl _X_PICTL
                            383 	.globl _X_P2IFG
                            384 	.globl _X_P1IFG
                            385 	.globl _X_P0IFG
                            386 	.globl __NA_TCON
                            387 	.globl __NA_PCON
                            388 	.globl _X_U0CSR
                            389 	.globl __NA_DPH1
                            390 	.globl __NA_DPL1
                            391 	.globl __NA_DPH0
                            392 	.globl __NA_DPL0
                            393 	.globl __NA_SP
                            394 	.globl __NA_P0
                            395 	.globl _I2SCLKF2
                            396 	.globl _I2SCLKF1
                            397 	.globl _I2SCLKF0
                            398 	.globl _I2SSTAT
                            399 	.globl _I2SWCNT
                            400 	.globl _I2SDATH
                            401 	.globl _I2SDATL
                            402 	.globl _I2SCFG1
                            403 	.globl _I2SCFG0
                            404 	.globl _VCO_VC_DAC
                            405 	.globl _PKTSTATUS
                            406 	.globl _MARCSTATE
                            407 	.globl _RSSI
                            408 	.globl _LQI
                            409 	.globl _FREQEST
                            410 	.globl _VERSION
                            411 	.globl _PARTNUM
                            412 	.globl __XREGDF35
                            413 	.globl __XREGDF34
                            414 	.globl __XREGDF33
                            415 	.globl __XREGDF32
                            416 	.globl _IOCFG0
                            417 	.globl _IOCFG1
                            418 	.globl _IOCFG2
                            419 	.globl _PA_TABLE0
                            420 	.globl _PA_TABLE1
                            421 	.globl _PA_TABLE2
                            422 	.globl _PA_TABLE3
                            423 	.globl _PA_TABLE4
                            424 	.globl _PA_TABLE5
                            425 	.globl _PA_TABLE6
                            426 	.globl _PA_TABLE7
                            427 	.globl __XREGDF26
                            428 	.globl _TEST0
                            429 	.globl _TEST1
                            430 	.globl _TEST2
                            431 	.globl __XREGDF22
                            432 	.globl __XREGDF21
                            433 	.globl __XREGDF20
                            434 	.globl _FSCAL0
                            435 	.globl _FSCAL1
                            436 	.globl _FSCAL2
                            437 	.globl _FSCAL3
                            438 	.globl _FREND0
                            439 	.globl _FREND1
                            440 	.globl _AGCCTRL0
                            441 	.globl _AGCCTRL1
                            442 	.globl _AGCCTRL2
                            443 	.globl _BSCFG
                            444 	.globl _FOCCFG
                            445 	.globl _MCSM0
                            446 	.globl _MCSM1
                            447 	.globl _MCSM2
                            448 	.globl _DEVIATN
                            449 	.globl _MDMCFG0
                            450 	.globl _MDMCFG1
                            451 	.globl _MDMCFG2
                            452 	.globl _MDMCFG3
                            453 	.globl _MDMCFG4
                            454 	.globl _FREQ0
                            455 	.globl _FREQ1
                            456 	.globl _FREQ2
                            457 	.globl _FSCTRL0
                            458 	.globl _FSCTRL1
                            459 	.globl _CHANNR
                            460 	.globl _ADDR
                            461 	.globl _PKTCTRL0
                            462 	.globl _PKTCTRL1
                            463 	.globl _PKTLEN
                            464 	.globl _SYNC0
                            465 	.globl _SYNC1
                            466 	.globl _MDMCTRL0H
                            467 	.globl _dma_channels
                            468 	.globl _initDMA
                            469 	.globl _getDMA
                            470 ;--------------------------------------------------------
                            471 ; special function registers
                            472 ;--------------------------------------------------------
                            473 	.area RSEG    (ABS,DATA)
   0000                     474 	.org 0x0000
                     0080   475 _P0	=	0x0080
                     0081   476 _SP	=	0x0081
                     0082   477 _DPL0	=	0x0082
                     0083   478 _DPH0	=	0x0083
                     0084   479 _DPL1	=	0x0084
                     0085   480 _DPH1	=	0x0085
                     0086   481 _U0CSR	=	0x0086
                     0087   482 _PCON	=	0x0087
                     0088   483 _TCON	=	0x0088
                     0089   484 _P0IFG	=	0x0089
                     008A   485 _P1IFG	=	0x008a
                     008B   486 _P2IFG	=	0x008b
                     008C   487 _PICTL	=	0x008c
                     008D   488 _P1IEN	=	0x008d
                     008E   489 __SFR8E	=	0x008e
                     008F   490 _P0INP	=	0x008f
                     0090   491 _P1	=	0x0090
                     0091   492 _RFIM	=	0x0091
                     0092   493 _DPS	=	0x0092
                     0093   494 _MPAGE	=	0x0093
                     0093   495 __XPAGE	=	0x0093
                     0094   496 __SFR94	=	0x0094
                     0095   497 __SFR95	=	0x0095
                     0096   498 __SFR96	=	0x0096
                     0097   499 __SFR97	=	0x0097
                     0098   500 _S0CON	=	0x0098
                     0099   501 __SFR99	=	0x0099
                     009A   502 _IEN2	=	0x009a
                     009B   503 _S1CON	=	0x009b
                     009C   504 _T2CT	=	0x009c
                     009D   505 _T2PR	=	0x009d
                     009E   506 _T2CTL	=	0x009e
                     009F   507 __SFR9F	=	0x009f
                     00A0   508 _P2	=	0x00a0
                     00A1   509 _WORIRQ	=	0x00a1
                     00A2   510 _WORCTRL	=	0x00a2
                     00A3   511 _WOREVT0	=	0x00a3
                     00A4   512 _WOREVT1	=	0x00a4
                     00A5   513 _WORTIME0	=	0x00a5
                     00A6   514 _WORTIME1	=	0x00a6
                     00A7   515 __SFRA7	=	0x00a7
                     00A8   516 _IEN0	=	0x00a8
                     00A9   517 _IP0	=	0x00a9
                     00AA   518 __SFRAA	=	0x00aa
                     00AB   519 _FWT	=	0x00ab
                     00AC   520 _FADDRL	=	0x00ac
                     00AD   521 _FADDRH	=	0x00ad
                     00AE   522 _FCTL	=	0x00ae
                     00AF   523 _FWDATA	=	0x00af
                     00B0   524 __SFRB0	=	0x00b0
                     00B1   525 _ENCDI	=	0x00b1
                     00B2   526 _ENCDO	=	0x00b2
                     00B3   527 _ENCCS	=	0x00b3
                     00B4   528 _ADCCON1	=	0x00b4
                     00B5   529 _ADCCON2	=	0x00b5
                     00B6   530 _ADCCON3	=	0x00b6
                     00B7   531 __SFRB7	=	0x00b7
                     00B8   532 _IEN1	=	0x00b8
                     00B9   533 _IP1	=	0x00b9
                     00BA   534 _ADCL	=	0x00ba
                     00BB   535 _ADCH	=	0x00bb
                     00BC   536 _RNDL	=	0x00bc
                     00BD   537 _RNDH	=	0x00bd
                     00BE   538 _SLEEP	=	0x00be
                     00BF   539 __SFRBF	=	0x00bf
                     00C0   540 _IRCON	=	0x00c0
                     00C1   541 _U0DBUF	=	0x00c1
                     00C2   542 _U0BAUD	=	0x00c2
                     00C3   543 __SFRC3	=	0x00c3
                     00C4   544 _U0UCR	=	0x00c4
                     00C5   545 _U0GCR	=	0x00c5
                     00C6   546 _CLKCON	=	0x00c6
                     00C7   547 _MEMCTR	=	0x00c7
                     00C8   548 __SFRC8	=	0x00c8
                     00C9   549 _WDCTL	=	0x00c9
                     00CA   550 _T3CNT	=	0x00ca
                     00CB   551 _T3CTL	=	0x00cb
                     00CC   552 _T3CCTL0	=	0x00cc
                     00CD   553 _T3CC0	=	0x00cd
                     00CE   554 _T3CCTL1	=	0x00ce
                     00CF   555 _T3CC1	=	0x00cf
                     00D0   556 _PSW	=	0x00d0
                     00D1   557 _DMAIRQ	=	0x00d1
                     00D2   558 _DMA1CFGL	=	0x00d2
                     00D3   559 _DMA1CFGH	=	0x00d3
                     00D4   560 _DMA0CFGL	=	0x00d4
                     00D5   561 _DMA0CFGH	=	0x00d5
                     00D6   562 _DMAARM	=	0x00d6
                     00D7   563 _DMAREQ	=	0x00d7
                     00D8   564 _TIMIF	=	0x00d8
                     00D9   565 _RFD	=	0x00d9
                     00DA   566 _T1CC0L	=	0x00da
                     00DB   567 _T1CC0H	=	0x00db
                     00DC   568 _T1CC1L	=	0x00dc
                     00DD   569 _T1CC1H	=	0x00dd
                     00DE   570 _T1CC2L	=	0x00de
                     00DF   571 _T1CC2H	=	0x00df
                     00E0   572 _ACC	=	0x00e0
                     00E1   573 _RFST	=	0x00e1
                     00E2   574 _T1CNTL	=	0x00e2
                     00E3   575 _T1CNTH	=	0x00e3
                     00E4   576 _T1CTL	=	0x00e4
                     00E5   577 _T1CCTL0	=	0x00e5
                     00E6   578 _T1CCTL1	=	0x00e6
                     00E7   579 _T1CCTL2	=	0x00e7
                     00E8   580 _IRCON2	=	0x00e8
                     00E9   581 _RFIF	=	0x00e9
                     00EA   582 _T4CNT	=	0x00ea
                     00EB   583 _T4CTL	=	0x00eb
                     00EC   584 _T4CCTL0	=	0x00ec
                     00ED   585 _T4CC0	=	0x00ed
                     00EE   586 _T4CCTL1	=	0x00ee
                     00EF   587 _T4CC1	=	0x00ef
                     00F0   588 _B	=	0x00f0
                     00F1   589 _PERCFG	=	0x00f1
                     00F2   590 _ADCCFG	=	0x00f2
                     00F3   591 _P0SEL	=	0x00f3
                     00F4   592 _P1SEL	=	0x00f4
                     00F5   593 _P2SEL	=	0x00f5
                     00F6   594 _P1INP	=	0x00f6
                     00F7   595 _P2INP	=	0x00f7
                     00F8   596 _U1CSR	=	0x00f8
                     00F9   597 _U1DBUF	=	0x00f9
                     00FA   598 _U1BAUD	=	0x00fa
                     00FB   599 _U1UCR	=	0x00fb
                     00FC   600 _U1GCR	=	0x00fc
                     00FD   601 _P0DIR	=	0x00fd
                     00FE   602 _P1DIR	=	0x00fe
                     00FF   603 _P2DIR	=	0x00ff
                            604 ;--------------------------------------------------------
                            605 ; special function bits
                            606 ;--------------------------------------------------------
                            607 	.area RSEG    (ABS,DATA)
   0000                     608 	.org 0x0000
                     0080   609 _P0_0	=	0x0080
                     0081   610 _P0_1	=	0x0081
                     0082   611 _P0_2	=	0x0082
                     0083   612 _P0_3	=	0x0083
                     0084   613 _P0_4	=	0x0084
                     0085   614 _P0_5	=	0x0085
                     0086   615 _P0_6	=	0x0086
                     0087   616 _P0_7	=	0x0087
                     0088   617 _IT0	=	0x0088
                     0089   618 _RFTXRXIF	=	0x0089
                     008A   619 _IT1	=	0x008a
                     008B   620 _URX0IF	=	0x008b
                     008D   621 _ADCIF	=	0x008d
                     008F   622 _URX1IF	=	0x008f
                     0090   623 _P1_0	=	0x0090
                     0091   624 _P1_1	=	0x0091
                     0092   625 _P1_2	=	0x0092
                     0093   626 _P1_3	=	0x0093
                     0094   627 _P1_4	=	0x0094
                     0095   628 _P1_5	=	0x0095
                     0096   629 _P1_6	=	0x0096
                     0097   630 _P1_7	=	0x0097
                     0098   631 _ENCIF_0	=	0x0098
                     0099   632 _ENCIF_1	=	0x0099
                     00A0   633 _P2_0	=	0x00a0
                     00A1   634 _P2_1	=	0x00a1
                     00A2   635 _P2_2	=	0x00a2
                     00A3   636 _P2_3	=	0x00a3
                     00A4   637 _P2_4	=	0x00a4
                     00A5   638 _P2_5	=	0x00a5
                     00A6   639 _P2_6	=	0x00a6
                     00A7   640 _P2_7	=	0x00a7
                     00A8   641 _RFTXRXIE	=	0x00a8
                     00A9   642 _ADCIE	=	0x00a9
                     00AA   643 _URX0IE	=	0x00aa
                     00AB   644 _URX1IE	=	0x00ab
                     00AC   645 _ENCIE	=	0x00ac
                     00AD   646 _STIE	=	0x00ad
                     00AF   647 _EA	=	0x00af
                     00B8   648 _DMAIE	=	0x00b8
                     00B9   649 _T1IE	=	0x00b9
                     00BA   650 _T2IE	=	0x00ba
                     00BB   651 _T3IE	=	0x00bb
                     00BC   652 _T4IE	=	0x00bc
                     00BD   653 _P0IE	=	0x00bd
                     00C0   654 _DMAIF	=	0x00c0
                     00C1   655 _T1IF	=	0x00c1
                     00C2   656 _T2IF	=	0x00c2
                     00C3   657 _T3IF	=	0x00c3
                     00C4   658 _T4IF	=	0x00c4
                     00C5   659 _P0IF	=	0x00c5
                     00C7   660 _STIF	=	0x00c7
                     00D0   661 _P	=	0x00d0
                     00D1   662 _F1	=	0x00d1
                     00D2   663 _OV	=	0x00d2
                     00D3   664 _RS0	=	0x00d3
                     00D4   665 _RS1	=	0x00d4
                     00D5   666 _F0	=	0x00d5
                     00D6   667 _AC	=	0x00d6
                     00D7   668 _CY	=	0x00d7
                     00D8   669 _T3OVFIF	=	0x00d8
                     00D9   670 _T3CH0IF	=	0x00d9
                     00DA   671 _T3CH1IF	=	0x00da
                     00DB   672 _T4OVFIF	=	0x00db
                     00DC   673 _T4CH0IF	=	0x00dc
                     00DD   674 _T4CH1IF	=	0x00dd
                     00DE   675 _OVFIM	=	0x00de
                     00E0   676 _ACC_0	=	0x00e0
                     00E1   677 _ACC_1	=	0x00e1
                     00E2   678 _ACC_2	=	0x00e2
                     00E3   679 _ACC_3	=	0x00e3
                     00E4   680 _ACC_4	=	0x00e4
                     00E5   681 _ACC_5	=	0x00e5
                     00E6   682 _ACC_6	=	0x00e6
                     00E7   683 _ACC_7	=	0x00e7
                     00E8   684 _P2IF	=	0x00e8
                     00E9   685 _UTX0IF	=	0x00e9
                     00EA   686 _UTX1IF	=	0x00ea
                     00EB   687 _P1IF	=	0x00eb
                     00EC   688 _WDTIF	=	0x00ec
                     00F0   689 _B_0	=	0x00f0
                     00F1   690 _B_1	=	0x00f1
                     00F2   691 _B_2	=	0x00f2
                     00F3   692 _B_3	=	0x00f3
                     00F4   693 _B_4	=	0x00f4
                     00F5   694 _B_5	=	0x00f5
                     00F6   695 _B_6	=	0x00f6
                     00F7   696 _B_7	=	0x00f7
                     00F8   697 _ACTIVE	=	0x00f8
                     00F9   698 _TX_BYTE	=	0x00f9
                     00FA   699 _RX_BYTE	=	0x00fa
                     00FB   700 _ERR	=	0x00fb
                     00FC   701 _FE	=	0x00fc
                     00FD   702 _SLAVE	=	0x00fd
                     00FE   703 _RE	=	0x00fe
                     00FF   704 _MODE	=	0x00ff
                     00E8   705 _USBIF	=	0x00e8
                            706 ;--------------------------------------------------------
                            707 ; overlayable register banks
                            708 ;--------------------------------------------------------
                            709 	.area REG_BANK_0	(REL,OVR,DATA)
   0000                     710 	.ds 8
                            711 ;--------------------------------------------------------
                            712 ; internal ram data
                            713 ;--------------------------------------------------------
                            714 	.area DSEG    (DATA)
   000D                     715 _dma_channels::
   000D                     716 	.ds 2
                            717 ;--------------------------------------------------------
                            718 ; overlayable items in internal ram 
                            719 ;--------------------------------------------------------
                            720 ;--------------------------------------------------------
                            721 ; indirectly addressable internal ram data
                            722 ;--------------------------------------------------------
                            723 	.area ISEG    (DATA)
                            724 ;--------------------------------------------------------
                            725 ; absolute internal ram data
                            726 ;--------------------------------------------------------
                            727 	.area IABS    (ABS,DATA)
                            728 	.area IABS    (ABS,DATA)
                            729 ;--------------------------------------------------------
                            730 ; bit data
                            731 ;--------------------------------------------------------
                            732 	.area BSEG    (BIT)
                            733 ;--------------------------------------------------------
                            734 ; paged external ram data
                            735 ;--------------------------------------------------------
                            736 	.area PSEG    (PAG,XDATA)
                            737 ;--------------------------------------------------------
                            738 ; external ram data
                            739 ;--------------------------------------------------------
                            740 	.area XSEG    (XDATA)
                     DF02   741 _MDMCTRL0H	=	0xdf02
                     DF00   742 _SYNC1	=	0xdf00
                     DF01   743 _SYNC0	=	0xdf01
                     DF02   744 _PKTLEN	=	0xdf02
                     DF03   745 _PKTCTRL1	=	0xdf03
                     DF04   746 _PKTCTRL0	=	0xdf04
                     DF05   747 _ADDR	=	0xdf05
                     DF06   748 _CHANNR	=	0xdf06
                     DF07   749 _FSCTRL1	=	0xdf07
                     DF08   750 _FSCTRL0	=	0xdf08
                     DF09   751 _FREQ2	=	0xdf09
                     DF0A   752 _FREQ1	=	0xdf0a
                     DF0B   753 _FREQ0	=	0xdf0b
                     DF0C   754 _MDMCFG4	=	0xdf0c
                     DF0D   755 _MDMCFG3	=	0xdf0d
                     DF0E   756 _MDMCFG2	=	0xdf0e
                     DF0F   757 _MDMCFG1	=	0xdf0f
                     DF10   758 _MDMCFG0	=	0xdf10
                     DF11   759 _DEVIATN	=	0xdf11
                     DF12   760 _MCSM2	=	0xdf12
                     DF13   761 _MCSM1	=	0xdf13
                     DF14   762 _MCSM0	=	0xdf14
                     DF15   763 _FOCCFG	=	0xdf15
                     DF16   764 _BSCFG	=	0xdf16
                     DF17   765 _AGCCTRL2	=	0xdf17
                     DF18   766 _AGCCTRL1	=	0xdf18
                     DF19   767 _AGCCTRL0	=	0xdf19
                     DF1A   768 _FREND1	=	0xdf1a
                     DF1B   769 _FREND0	=	0xdf1b
                     DF1C   770 _FSCAL3	=	0xdf1c
                     DF1D   771 _FSCAL2	=	0xdf1d
                     DF1E   772 _FSCAL1	=	0xdf1e
                     DF1F   773 _FSCAL0	=	0xdf1f
                     DF20   774 __XREGDF20	=	0xdf20
                     DF21   775 __XREGDF21	=	0xdf21
                     DF22   776 __XREGDF22	=	0xdf22
                     DF23   777 _TEST2	=	0xdf23
                     DF24   778 _TEST1	=	0xdf24
                     DF25   779 _TEST0	=	0xdf25
                     DF26   780 __XREGDF26	=	0xdf26
                     DF27   781 _PA_TABLE7	=	0xdf27
                     DF28   782 _PA_TABLE6	=	0xdf28
                     DF29   783 _PA_TABLE5	=	0xdf29
                     DF2A   784 _PA_TABLE4	=	0xdf2a
                     DF2B   785 _PA_TABLE3	=	0xdf2b
                     DF2C   786 _PA_TABLE2	=	0xdf2c
                     DF2D   787 _PA_TABLE1	=	0xdf2d
                     DF2E   788 _PA_TABLE0	=	0xdf2e
                     DF2F   789 _IOCFG2	=	0xdf2f
                     DF30   790 _IOCFG1	=	0xdf30
                     DF31   791 _IOCFG0	=	0xdf31
                     DF32   792 __XREGDF32	=	0xdf32
                     DF33   793 __XREGDF33	=	0xdf33
                     DF34   794 __XREGDF34	=	0xdf34
                     DF35   795 __XREGDF35	=	0xdf35
                     DF36   796 _PARTNUM	=	0xdf36
                     DF37   797 _VERSION	=	0xdf37
                     DF38   798 _FREQEST	=	0xdf38
                     DF39   799 _LQI	=	0xdf39
                     DF3A   800 _RSSI	=	0xdf3a
                     DF3B   801 _MARCSTATE	=	0xdf3b
                     DF3C   802 _PKTSTATUS	=	0xdf3c
                     DF3D   803 _VCO_VC_DAC	=	0xdf3d
                     DF40   804 _I2SCFG0	=	0xdf40
                     DF41   805 _I2SCFG1	=	0xdf41
                     DF42   806 _I2SDATL	=	0xdf42
                     DF43   807 _I2SDATH	=	0xdf43
                     DF44   808 _I2SWCNT	=	0xdf44
                     DF45   809 _I2SSTAT	=	0xdf45
                     DF46   810 _I2SCLKF0	=	0xdf46
                     DF47   811 _I2SCLKF1	=	0xdf47
                     DF48   812 _I2SCLKF2	=	0xdf48
                     DF80   813 __NA_P0	=	0xdf80
                     DF81   814 __NA_SP	=	0xdf81
                     DF82   815 __NA_DPL0	=	0xdf82
                     DF83   816 __NA_DPH0	=	0xdf83
                     DF84   817 __NA_DPL1	=	0xdf84
                     DF85   818 __NA_DPH1	=	0xdf85
                     DF86   819 _X_U0CSR	=	0xdf86
                     DF87   820 __NA_PCON	=	0xdf87
                     DF88   821 __NA_TCON	=	0xdf88
                     DF89   822 _X_P0IFG	=	0xdf89
                     DF8A   823 _X_P1IFG	=	0xdf8a
                     DF8B   824 _X_P2IFG	=	0xdf8b
                     DF8C   825 _X_PICTL	=	0xdf8c
                     DF8D   826 _X_P1IEN	=	0xdf8d
                     DF8E   827 __X_SFR8E	=	0xdf8e
                     DF8F   828 _X_P0INP	=	0xdf8f
                     DF90   829 __NA_P1	=	0xdf90
                     DF91   830 _X_RFIM	=	0xdf91
                     DF92   831 __NA_DPS	=	0xdf92
                     DF93   832 _X_MPAGE	=	0xdf93
                     DF94   833 __X_SFR94	=	0xdf94
                     DF95   834 __X_SFR95	=	0xdf95
                     DF96   835 __X_SFR96	=	0xdf96
                     DF97   836 __X_SFR97	=	0xdf97
                     DF98   837 __NA_S0CON	=	0xdf98
                     DF99   838 __X_SFR99	=	0xdf99
                     DF9A   839 __NA_IEN2	=	0xdf9a
                     DF9B   840 __NA_S1CON	=	0xdf9b
                     DF9C   841 _X_T2CT	=	0xdf9c
                     DF9D   842 _X_T2PR	=	0xdf9d
                     DF9E   843 _X_T2CTL	=	0xdf9e
                     DF9F   844 __X_SFR9F	=	0xdf9f
                     DFA0   845 __NA_P2	=	0xdfa0
                     DFA1   846 _X_WORIRQ	=	0xdfa1
                     DFA2   847 _X_WORCTRL	=	0xdfa2
                     DFA3   848 _X_WOREVT0	=	0xdfa3
                     DFA4   849 _X_WOREVT1	=	0xdfa4
                     DFA5   850 _X_WORTIME0	=	0xdfa5
                     DFA6   851 _X_WORTIME1	=	0xdfa6
                     DFA7   852 __X_SFRA7	=	0xdfa7
                     DFA8   853 __NA_IEN0	=	0xdfa8
                     DFA9   854 __NA_IP0	=	0xdfa9
                     DFAA   855 __X_SFRAA	=	0xdfaa
                     DFAB   856 _X_FWT	=	0xdfab
                     DFAC   857 _X_FADDRL	=	0xdfac
                     DFAD   858 _X_FADDRH	=	0xdfad
                     DFAE   859 _X_FCTL	=	0xdfae
                     DFAF   860 _X_FWDATA	=	0xdfaf
                     DFB0   861 __X_SFRB0	=	0xdfb0
                     DFB1   862 _X_ENCDI	=	0xdfb1
                     DFB2   863 _X_ENCDO	=	0xdfb2
                     DFB3   864 _X_ENCCS	=	0xdfb3
                     DFB4   865 _X_ADCCON1	=	0xdfb4
                     DFB5   866 _X_ADCCON2	=	0xdfb5
                     DFB6   867 _X_ADCCON3	=	0xdfb6
                     DFB7   868 __X_SFRB7	=	0xdfb7
                     DFB8   869 __NA_IEN1	=	0xdfb8
                     DFB9   870 __NA_IP1	=	0xdfb9
                     DFBA   871 _X_ADCL	=	0xdfba
                     DFBB   872 _X_ADCH	=	0xdfbb
                     DFBC   873 _X_RNDL	=	0xdfbc
                     DFBD   874 _X_RNDH	=	0xdfbd
                     DFBE   875 _X_SLEEP	=	0xdfbe
                     DFBF   876 __X_SFRBF	=	0xdfbf
                     DFC0   877 __NA_IRCON	=	0xdfc0
                     DFC1   878 _X_U0DBUF	=	0xdfc1
                     DFC2   879 _X_U0BAUD	=	0xdfc2
                     DFC3   880 __X_SFRC3	=	0xdfc3
                     DFC4   881 _X_U0UCR	=	0xdfc4
                     DFC5   882 _X_U0GCR	=	0xdfc5
                     DFC6   883 _X_CLKCON	=	0xdfc6
                     DFC7   884 _X_MEMCTR	=	0xdfc7
                     DFC8   885 __X_SFRC8	=	0xdfc8
                     DFC9   886 _X_WDCTL	=	0xdfc9
                     DFCA   887 _X_T3CNT	=	0xdfca
                     DFCB   888 _X_T3CTL	=	0xdfcb
                     DFCC   889 _X_T3CCTL0	=	0xdfcc
                     DFCD   890 _X_T3CC0	=	0xdfcd
                     DFCE   891 _X_T3CCTL1	=	0xdfce
                     DFCF   892 _X_T3CC1	=	0xdfcf
                     DFD0   893 __NA_PSW	=	0xdfd0
                     DFD1   894 _X_DMAIRQ	=	0xdfd1
                     DFD2   895 _X_DMA1CFGL	=	0xdfd2
                     DFD3   896 _X_DMA1CFGH	=	0xdfd3
                     DFD4   897 _X_DMA0CFGL	=	0xdfd4
                     DFD5   898 _X_DMA0CFGH	=	0xdfd5
                     DFD6   899 _X_DMAARM	=	0xdfd6
                     DFD7   900 _X_DMAREQ	=	0xdfd7
                     DFD8   901 _X_TIMIF	=	0xdfd8
                     DFD9   902 _X_RFD	=	0xdfd9
                     DFDA   903 _X_T1CC0L	=	0xdfda
                     DFDB   904 _X_T1CC0H	=	0xdfdb
                     DFDC   905 _X_T1CC1L	=	0xdfdc
                     DFDD   906 _X_T1CC1H	=	0xdfdd
                     DFDE   907 _X_T1CC2L	=	0xdfde
                     DFDF   908 _X_T1CC2H	=	0xdfdf
                     DFE0   909 __NA_ACC	=	0xdfe0
                     DFE1   910 _X_RFST	=	0xdfe1
                     DFE2   911 _X_T1CNTL	=	0xdfe2
                     DFE3   912 _X_T1CNTH	=	0xdfe3
                     DFE4   913 _X_T1CTL	=	0xdfe4
                     DFE5   914 _X_T1CCTL0	=	0xdfe5
                     DFE6   915 _X_T1CCTL1	=	0xdfe6
                     DFE7   916 _X_T1CCTL2	=	0xdfe7
                     DFE8   917 __NA_IRCON2	=	0xdfe8
                     DFE9   918 _X_RFIF	=	0xdfe9
                     DFEA   919 _X_T4CNT	=	0xdfea
                     DFEB   920 _X_T4CTL	=	0xdfeb
                     DFEC   921 _X_T4CCTL0	=	0xdfec
                     DFED   922 _X_T4CC0	=	0xdfed
                     DFEE   923 _X_T4CCTL1	=	0xdfee
                     DFEF   924 _X_T4CC1	=	0xdfef
                     DFF0   925 __NA_B	=	0xdff0
                     DFF1   926 _X_PERCFG	=	0xdff1
                     DFF2   927 _X_ADCCFG	=	0xdff2
                     DFF3   928 _X_P0SEL	=	0xdff3
                     DFF4   929 _X_P1SEL	=	0xdff4
                     DFF5   930 _X_P2SEL	=	0xdff5
                     DFF6   931 _X_P1INP	=	0xdff6
                     DFF7   932 _X_P2INP	=	0xdff7
                     DFF8   933 _X_U1CSR	=	0xdff8
                     DFF9   934 _X_U1DBUF	=	0xdff9
                     DFFA   935 _X_U1BAUD	=	0xdffa
                     DFFB   936 _X_U1UCR	=	0xdffb
                     DFFC   937 _X_U1GCR	=	0xdffc
                     DFFD   938 _X_P0DIR	=	0xdffd
                     DFFE   939 _X_P1DIR	=	0xdffe
                     DFFF   940 _X_P2DIR	=	0xdfff
                     DE00   941 _USBADDR	=	0xde00
                     DE01   942 _USBPOW	=	0xde01
                     DE02   943 _USBIIF	=	0xde02
                     DE04   944 _USBOIF	=	0xde04
                     DE06   945 _USBCIF	=	0xde06
                     DE07   946 _USBIIE	=	0xde07
                     DE09   947 _USBOIE	=	0xde09
                     DE0B   948 _USBCIE	=	0xde0b
                     DE0C   949 _USBFRML	=	0xde0c
                     DE0D   950 _USBFRMH	=	0xde0d
                     DE0E   951 _USBINDEX	=	0xde0e
                     DE10   952 _USBMAXI	=	0xde10
                     DE11   953 _USBCS0	=	0xde11
                     DE11   954 _USBCSIL	=	0xde11
                     DE12   955 _USBCSIH	=	0xde12
                     DE13   956 _USBMAXO	=	0xde13
                     DE14   957 _USBCSOL	=	0xde14
                     DE15   958 _USBCSOH	=	0xde15
                     DE16   959 _USBCNT0	=	0xde16
                     DE16   960 _USBCNTL	=	0xde16
                     DE17   961 _USBCNTH	=	0xde17
                     DE20   962 _USBF0	=	0xde20
                     DE22   963 _USBF1	=	0xde22
                     DE24   964 _USBF2	=	0xde24
                     DE26   965 _USBF3	=	0xde26
                     DE28   966 _USBF4	=	0xde28
                     DE2A   967 _USBF5	=	0xde2a
   F9B5                     968 _dma_configs::
   F9B5                     969 	.ds 24
                            970 ;--------------------------------------------------------
                            971 ; absolute external ram data
                            972 ;--------------------------------------------------------
                            973 	.area XABS    (ABS,XDATA)
                            974 ;--------------------------------------------------------
                            975 ; external initialized ram data
                            976 ;--------------------------------------------------------
                            977 	.area XISEG   (XDATA)
                            978 	.area HOME    (CODE)
                            979 	.area GSINIT0 (CODE)
                            980 	.area GSINIT1 (CODE)
                            981 	.area GSINIT2 (CODE)
                            982 	.area GSINIT3 (CODE)
                            983 	.area GSINIT4 (CODE)
                            984 	.area GSINIT5 (CODE)
                            985 	.area GSINIT  (CODE)
                            986 	.area GSFINAL (CODE)
                            987 	.area CSEG    (CODE)
                            988 ;--------------------------------------------------------
                            989 ; global & static initialisations
                            990 ;--------------------------------------------------------
                            991 	.area HOME    (CODE)
                            992 	.area GSINIT  (CODE)
                            993 	.area GSFINAL (CODE)
                            994 	.area GSINIT  (CODE)
                            995 ;	chipcon_dma.c:27: __data dma_channels= 0;
   010C E4            [12]  996 	clr	a
   010D F5 0D         [12]  997 	mov	_dma_channels,a
   010F F5 0E         [12]  998 	mov	(_dma_channels + 1),a
                            999 ;--------------------------------------------------------
                           1000 ; Home
                           1001 ;--------------------------------------------------------
                           1002 	.area HOME    (CODE)
                           1003 	.area HOME    (CODE)
                           1004 ;--------------------------------------------------------
                           1005 ; code
                           1006 ;--------------------------------------------------------
                           1007 	.area CSEG    (CODE)
                           1008 ;------------------------------------------------------------
                           1009 ;Allocation info for local variables in function 'initDMA'
                           1010 ;------------------------------------------------------------
                           1011 ;	chipcon_dma.c:29: void initDMA(void)
                           1012 ;	-----------------------------------------
                           1013 ;	 function initDMA
                           1014 ;	-----------------------------------------
   229F                    1015 _initDMA:
                     0007  1016 	ar7 = 0x07
                     0006  1017 	ar6 = 0x06
                     0005  1018 	ar5 = 0x05
                     0004  1019 	ar4 = 0x04
                     0003  1020 	ar3 = 0x03
                     0002  1021 	ar2 = 0x02
                     0001  1022 	ar1 = 0x01
                     0000  1023 	ar0 = 0x00
                           1024 ;	chipcon_dma.c:33: DMA0CFGH = ((u16)(&dma_configs[0]))>>8;
   229F 7E B5         [12] 1025 	mov	r6,#_dma_configs
   22A1 7F F9         [12] 1026 	mov	r7,#(_dma_configs >> 8)
   22A3 8F D5         [24] 1027 	mov	_DMA0CFGH,r7
                           1028 ;	chipcon_dma.c:34: DMA0CFGL = ((u16)(&dma_configs[0]))&0xff;
   22A5 7E B5         [12] 1029 	mov	r6,#_dma_configs
   22A7 7F F9         [12] 1030 	mov	r7,#(_dma_configs >> 8)
   22A9 8E D4         [24] 1031 	mov	_DMA0CFGL,r6
                           1032 ;	chipcon_dma.c:38: DMA1CFGH = ((u16)(&dma_configs[1]))>>8;
   22AB 7E BD         [12] 1033 	mov	r6,#(_dma_configs + 0x0008)
   22AD 7F F9         [12] 1034 	mov	r7,#((_dma_configs + 0x0008) >> 8)
   22AF 8F D3         [24] 1035 	mov	_DMA1CFGH,r7
                           1036 ;	chipcon_dma.c:39: DMA1CFGL = ((u16)(&dma_configs[1]))&0xff;
   22B1 7E BD         [12] 1037 	mov	r6,#(_dma_configs + 0x0008)
   22B3 7F F9         [12] 1038 	mov	r7,#((_dma_configs + 0x0008) >> 8)
   22B5 8E D2         [24] 1039 	mov	_DMA1CFGL,r6
                           1040 ;	chipcon_dma.c:42: memset(dma_configs,'\0',sizeof(DMA_DESC)*DMA_CHANNELS);
   22B7 75 14 00      [24] 1041 	mov	_memset_PARM_2,#0x00
   22BA 75 15 18      [24] 1042 	mov	_memset_PARM_3,#0x18
   22BD 75 16 00      [24] 1043 	mov	(_memset_PARM_3 + 1),#0x00
   22C0 90 F9 B5      [24] 1044 	mov	dptr,#_dma_configs
   22C3 75 F0 00      [24] 1045 	mov	b,#0x00
   22C6 02 33 9C      [24] 1046 	ljmp	_memset
                           1047 ;------------------------------------------------------------
                           1048 ;Allocation info for local variables in function 'getDMA'
                           1049 ;------------------------------------------------------------
                           1050 ;	chipcon_dma.c:46: u8 getDMA(void)
                           1051 ;	-----------------------------------------
                           1052 ;	 function getDMA
                           1053 ;	-----------------------------------------
   22C9                    1054 _getDMA:
                           1055 ;	chipcon_dma.c:48: if(dma_channels == DMA_CHANNELS)
   22C9 74 03         [12] 1056 	mov	a,#0x03
   22CB B5 0D 06      [24] 1057 	cjne	a,_dma_channels,00109$
   22CE E4            [12] 1058 	clr	a
   22CF B5 0E 02      [24] 1059 	cjne	a,(_dma_channels + 1),00109$
   22D2 80 02         [24] 1060 	sjmp	00110$
   22D4                    1061 00109$:
   22D4 80 04         [24] 1062 	sjmp	00102$
   22D6                    1063 00110$:
                           1064 ;	chipcon_dma.c:49: return 0xff;
   22D6 75 82 FF      [24] 1065 	mov	dpl,#0xFF
   22D9 22            [24] 1066 	ret
   22DA                    1067 00102$:
                           1068 ;	chipcon_dma.c:51: return dma_channels++;
   22DA AE 0D         [24] 1069 	mov	r6,_dma_channels
   22DC AF 0E         [24] 1070 	mov	r7,(_dma_channels + 1)
   22DE 05 0D         [12] 1071 	inc	_dma_channels
   22E0 E4            [12] 1072 	clr	a
   22E1 B5 0D 02      [24] 1073 	cjne	a,_dma_channels,00111$
   22E4 05 0E         [12] 1074 	inc	(_dma_channels + 1)
   22E6                    1075 00111$:
   22E6 8E 82         [24] 1076 	mov	dpl,r6
   22E8 22            [24] 1077 	ret
                           1078 	.area CSEG    (CODE)
                           1079 	.area CONST   (CODE)
                           1080 	.area XINIT   (CODE)
                           1081 	.area CABS    (ABS,CODE)
