---
description: La tabella seguente definisce gli identificatori delle tabelle codici disponibili.
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: Identificatori della tabella codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128934"
---
# <a name="code-page-identifiers"></a>Identificatori della tabella codici

La tabella seguente definisce gli identificatori delle tabelle codici disponibili.

> [!Note]  
> Le tabelle codici ANSI possono essere diverse in computer diversi oppure possono essere modificate per un singolo computer, causando il danneggiamento dei dati. Per i risultati più coerenti, le applicazioni devono utilizzare Unicode, ad esempio UTF-8 o UTF-16, anziché una tabella codici specifica.

 



| Identificatore | Nome .NET               | Informazioni aggiuntive                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | US-Canada IBM EBCDIC                                                                                |
| 437        | IBM437                  | Stati Uniti OEM                                                                                   |
| 500        | IBM500                  | IBM EBCDIC International                                                                            |
| 708        | ASMO-708                | Arabo (ASMO 708)                                                                                   |
| 709        |                         | Arabo (ASMO-449 +, BCON v4)                                                                         |
| 710        |                         | Arabo trasparente                                                                         |
| 720        | DOS-720                 | Arabo (ASMO trasparente); Arabo (DOS)                                                             |
| 737        | ibm737                  | OEM greco (in precedenza 437G); Greco (DOS)                                                              |
| 775        | ibm775                  | Baltico OEM; Baltico (DOS)                                                                            |
| 850        | ibm850                  | OEM Multilingue Latino 1; Europa occidentale (DOS)                                                    |
| 852        | ibm852                  | OEM Latino 2; Europa centrale (DOS)                                                                 |
| 855        | IBM855                  | OEM Cirillico (principalmente russo)                                                                    |
| 857        | ibm857                  | Turco OEM; Turco (DOS)                                                                          |
| 858        | IBM00858                | Simbolo OEM Multilingue Latino 1 + euro                                                              |
| 860        | IBM860                  | Portoghese OEM; Portoghese (DOS)                                                                    |
| 861        | ibm861                  | Islandese OEM; Islandese (DOS)                                                                      |
| 862        | DOS-862                 | Ebraico OEM; Ebraico (DOS)                                                                            |
| 863        | IBM863                  | Canadese OEM francese; Francese canadese (DOS)                                                          |
| 864        | IBM864                  | Arabo OEM; Arabo (864)                                                                            |
| 865        | IBM865                  | OEM Nordic; Nordico (DOS)                                                                            |
| 866        | CP866                   | OEM Russo; Cirillico (DOS)                                                                         |
| 869        | ibm869                  | Greco moderno OEM; Greco, moderno (DOS)                                                               |
| 870        | IBM870                  | IBM EBCDIC multilingue/ROECE (Latino 2); IBM EBCDIC multilingue Latino 2                            |
| 874        | Windows-874             | Thai (Windows)                                                         |
| 875        | cp875                   | IBM EBCDIC greco moderno                                                                             |
| 932        | MAIUSC \_ JIS              | ANSI/OEM giapponese; Giapponese (Shift-JIS)                                                             |
| 936        | GB2312                  | ANSI/OEM-cinese semplificato (PRC, Singapore); Cinese semplificato (GB2312)                           |
| 949        | KS \_ c \_ 5601-1987        | ANSI/OEM Coreano (codice Hangul unificato)                                                               |
| 950        | Big5                    | Cinese tradizionale ANSI/OEM (Taiwan; RAS di Hong Kong, PRC); Cinese tradizionale (Big5)               |
| 1026       | IBM1026                 | IBM EBCDIC turco (Latino 5)                                                                        |
| 1047       | IBM01047                | IBM EBCDIC Latin 1/Open System                                                                      |
| 1140       | IBM01140                | IBM EBCDIC US-Canada (simbolo 037 + euro); IBM EBCDIC (Stati Uniti-Canada-Europa)                               |
| 1141       | IBM01141                | IBM EBCDIC Germania (simbolo 20273 + euro); IBM EBCDIC (Germania-Europa)                                 |
| 1142       | IBM01142                | IBM EBCDIC Denmark-Norway (simbolo 20277 + euro); IBM EBCDIC (Danimarca-Norvegia-Europa)                   |
| 1143       | IBM01143                | IBM EBCDIC Finland-Sweden (simbolo 20278 + euro); IBM EBCDIC (Finlandia-Svezia-Europa)                   |
| 1144       | IBM01144                | IBM EBCDIC Italia (simbolo 20280 + euro); IBM EBCDIC (Italia-Europa)                                     |
| 1145       | IBM01145                | IBM EBCDIC Latin America-Spain (simbolo 20284 + euro); IBM EBCDIC (Spagna-Europa)                       |
| 1146       | IBM01146                | IBM EBCDIC United Kingdom (simbolo 20285 + euro); IBM EBCDIC (Regno Unito-Europa)                               |
| 1147       | IBM01147                | IBM EBCDIC Francia (simbolo 20297 + euro); IBM EBCDIC (Francia-Europa)                                   |
| 1148       | IBM01148                | IBM EBCDIC International (simbolo 500 + euro); IBM EBCDIC (internazionale-Europa)                       |
| 1149       | IBM01149                | IBM EBCDIC islandese (simbolo 20871 + euro); IBM EBCDIC (islandese-Europa)                             |
| 1200       | UTF-16                  | Unicode UTF-16, little endian byte order (BMP ISO 10646); disponibile solo per le applicazioni gestite |
| 1201       | unicodeFFFE             | Unicode UTF-16, big endian byte order; disponibile solo per le applicazioni gestite                       |
| 1250       | Windows-1250            | Europa centrale ANSI; Europa centrale (Windows)                                                   |
| 1251       | Windows-1251            | ANSI cirillico; Cirillico (Windows)                                                                   |
| 1252       | Windows-1252            | ANSI Latino 1; Europa occidentale (Windows)                                                            |
| 1253       | Windows-1253            | Greco ANSI; Greco (Windows)                                                                         |
| 1254       | Windows-1254            | Turco ANSI; Turco (Windows)                                                                     |
| 1255       | Windows-1255            | Ebraico ANSI; Ebraico (Windows)                                                                       |
| 1256       | Windows-1256            | Arabo ANSI; Arabo (Windows)                                                                       |
| 1257       | Windows-1257            | Baltico ANSI; Baltico (Windows)                                                                       |
| 1258       | Windows-1258            | ANSI/OEM vietnamita; Vietnamita (Windows)                                                           |
| 1361       | Johab                   | Coreano (Johab)                                                                                      |
| 10000      | Macintosh               | MAC romano; Europa occidentale (Mac)                                                                   |
| 10001      | x-Mac-giapponese          | Giapponese (Mac)                                                                                      |
| 10002      | x-Mac-chinesetrad       | MAC cinese tradizionale (Big5); Cinese tradizionale (Mac)                                           |
| 10003      | x-Mac-coreano            | Korean (Mac)                                                                                        |
| 10004      | x-Mac-arabo            | Arabo (Mac)                                                                                        |
| 10005      | x-Mac-ebraico            | Ebraico (Mac)                                                                                        |
| 10006      | x-Mac-greco             | Greco (Mac)                                                                                         |
| 10007      | x-Mac-cirillico          | Cirillico (Mac)                                                                                      |
| 10008      | x-Mac-chinesesimp       | MAC cinese semplificato (GB 2312); Cinese semplificato (Mac)                                          |
| 10010      | x-Mac-rumeno          | Rumeno (Mac)                                                                                      |
| 10017      | x-Mac-ucraino         | Ucraino (Mac)                                                                                     |
| 10021      | x-Mac-tailandese              | Tailandese (Mac)                                                                                          |
| 10029      | x-Mac-CE                | MAC Latino 2; Europa centrale (Mac)                                                                 |
| 10079      | x-Mac-islandese         | Islandese (Mac)                                                                                     |
| 10081      | x-Mac-turco           | Turco (Mac)                                                                                       |
| 10082      | x-Mac-croato          | Croato (Mac)                                                                                      |
| 12000      | UTF-32                  | Unicode UTF-32, little endian byte order; disponibile solo per le applicazioni gestite                    |
| 12001      | UTF-32BE                | Unicode UTF-32, big endian byte order; disponibile solo per le applicazioni gestite                       |
| 20000      | x- \_ SNC cinese          | CNS Taiwan; Cinese tradizionale (CNS)                                                               |
| 20001      | x-cp20001               | TCA Taiwan                                                                                          |
| 20002      | x \_ cinese-eten         | Eten Taiwan; Cinese tradizionale (eTEN)                                                             |
| 20003      | x-cp20003               | IBM5550 Taiwan                                                                                      |
| 20004      | x-cp20004               | Televideo Taiwan                                                                                     |
| 20005      | x-cp20005               | Wang Taiwan                                                                                         |
| 20105      | x-IA5                   | IA5 (IRV International Alphabet No. 5, 7 bit); Europa occidentale (IA5)                               |
| 20106      | x-IA5-tedesco            | IA5 tedesco (7 bit)                                                                                  |
| 20107      | x-IA5-svedese           | IA5 svedese (7 bit)                                                                                 |
| 20108      | x-IA5-norvegese         | IA5 norvegese (7 bit)                                                                               |
| 20127      | US-ASCII                | US-ASCII (7 bit)                                                                                    |
| 20261      | x-cp20261               | T. 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 Segni diacritici di combinazione                                                                         |
| 20273      | IBM273                  | IBM EBCDIC Germania                                                                                  |
| 20277      | IBM277                  | Denmark-Norway IBM EBCDIC                                                                           |
| 20278      | IBM278                  | Finland-Sweden IBM EBCDIC                                                                           |
| 20280      | IBM280                  | IBM EBCDIC Italia                                                                                    |
| 20284      | IBM284                  | America-Spain IBM EBCDIC Latin                                                                      |
| 20285      | IBM285                  | IBM EBCDIC (Regno Unito)                                                                           |
| 20290      | IBM290                  | IBM EBCDIC giapponese Katakana esteso                                                               |
| 20297      | IBM297                  | IBM EBCDIC Francia                                                                                   |
| 20420      | IBM420                  | IBM EBCDIC arabo                                                                                   |
| 20423      | IBM423                  | Greco EBCDIC IBM                                                                                    |
| 20424      | IBM424                  | Ebraico IBM EBCDIC                                                                                   |
| 20833      | x-EBCDIC-KoreanExtended | IBM EBCDIC Coreano esteso                                                                          |
| 20838      | IBM-Thai                | IBM EBCDIC Thai                                                                                     |
| 20866      | KOI8-r                  | Russo (KOI8-R); Cirillico (KOI8-R)                                                                 |
| 20871      | IBM871                  | IBM EBCDIC islandese                                                                                |
| 20880      | IBM880                  | IBM EBCDIC cirillico russo                                                                         |
| 20905      | IBM905                  | IBM EBCDIC turco                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC Latin 1/Open System (simbolo 1047 + euro)                                                 |
| 20932      | EUC-JP                  | Giapponese (JIS 0208-1990 e 0212-1990)                                                              |
| 20936      | x-cp20936               | Cinese semplificato (GB2312); Cinese semplificato (GB2312-80)                                         |
| 20949      | x-cp20949               | Wansung coreano                                                                                      |
| 21025      | cp1025                  | IBM EBCDIC cirillico Serbian-Bulgarian                                                               |
| 21027      |                         | deprecato                                                                                        |
| 21866      | koi8-u                  | Ucraino (KOI8-U); Cirillico (KOI8-U)                                                               |
| 28591      | ISO-8859-1              | ISO 8859-1 Latino 1; Europa occidentale (ISO)                                                          |
| 28592      | ISO-8859-2              | ISO 8859-2 Europa centrale; Europa centrale (ISO)                                                 |
| 28593      | ISO-8859-3              | ISO 8859-3 Latin 3                                                                                  |
| 28594      | ISO-8859-4              | ISO 8859-4 Baltico                                                                                   |
| 28595      | ISO-8859-5              | ISO 8859-5 Cirillico                                                                                 |
| 28596      | ISO-8859-6              | ISO 8859-6 Arabo                                                                                   |
| 28597      | ISO-8859-7              | ISO 8859-7 Greco                                                                                    |
| 28598      | ISO-8859-8              | ISO 8859-8 ebraico; Ebraico (ISO-Visual)                                                              |
| 28599      | ISO-8859-9              | ISO 8859-9 Turco                                                                                  |
| 28603      | ISO-8859-13             | ISO 8859-13 estone                                                                                |
| 28605      | ISO-8859-15             | ISO 8859-15 Latin 9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | ISO-8859-8-i            | ISO 8859-8 ebraico; Ebraico (ISO-Logical)                                                             |
| 50220      | ISO-2022-JP             | ISO 2022 giapponese senza carattere katakana; Giapponese (JIS)                                        |
| 50221      | csISO2022JP             | ISO 2022 giapponese con carattere katakana; Giapponese (JIS-Consenti Kana a 1 byte)                         |
| 50222      | ISO-2022-JP             | ISO 2022 giapponese JIS X 0201-1989; Giapponese (JIS-Consenti Kana a 1 byte-SO/SI)                         |
| 50225      | ISO-2022-KR             | ISO 2022 coreano                                                                                     |
| 50227      | x-cp50227               | ISO 2022 cinese semplificato; Cinese semplificato (ISO 2022)                                          |
| 50229      |                         | ISO 2022 cinese tradizionale                                                                        |
| 50930      |                         | EBCDIC giapponese (katakana) esteso                                                                 |
| 50931      |                         | US-Canada EBCDIC e giapponese                                                                       |
| 50933      |                         | EBCDIC Coreano esteso e coreano                                                                   |
| 50935      |                         | EBCDIC cinese semplificato esteso e cinese semplificato                                           |
| 50936      |                         | EBCDIC cinese semplificato                                                                           |
| 50937      |                         | US-Canada EBCDIC e cinese tradizionale                                                            |
| 50939      |                         | EBCDIC giapponese (alfabeto latino) esteso e giapponese                                                       |
| 51932      | EUC-JP                  | EUC giapponese                                                                                        |
| 51936      | EUC-CN                  | EUC cinese semplificato; Cinese semplificato (EUC)                                                    |
| 51949      | EUC-KR                  | EUC coreano                                                                                          |
| 51950      |                         | EUC cinese tradizionale                                                                             |
| 52936      | Hz-GB-2312              | HZ-GB2312 cinese semplificato; Cinese semplificato (HZ)                                               |
| 54936      | GB18030                 | **Windows XP e versioni successive:** GB18030 Cinese semplificato (4 byte); Cinese semplificato (GB18030)         |
| 57002      | x-ISCII-de              | ISCII devangato                                                                                    |
| 57003      | x-ISCII-be              | ISCII Bangla                                                                                        |
| 57004      | x-ISCII-ta              | ISCII Tamil                                                                                         |
| 57005      | x-ISCII-te              | ISCII Telugu                                                                                        |
| 57006      | x-ISCII-As              | Assamese ISCII                                                                                      |
| 57007      | x-ISCII-or              | Odia ISCII                                                                                          |
| 57008      | x-ISCII-ka              | ISCII Kannada                                                                                       |
| 57009      | x-ISCII-ma              | ISCII Malayalam                                                                                     |
| 57010      | x-ISCII-GU              | ISCII Gujarati                                                                                      |
| 57011      | x-ISCII-PA              | Punjabi ISCII                                                                                       |
| 65000      | UTF-7                   | Unicode (UTF-7)                                                                                     |
| 65001      | utf-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



