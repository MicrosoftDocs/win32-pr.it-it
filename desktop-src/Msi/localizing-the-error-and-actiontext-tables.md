---
description: Il Software Development Kit (SDK) di Microsoft Windows include le stringhe di risorsa localizzate, le tabelle degli errori localizzati e le tabelle ActionText localizzate per le lingue elencate nella tabella seguente.
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: Localizzazione delle tabelle Error e ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45428d9f0d3c4b8dcafbf489f7316225a83f032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346316"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>Localizzazione delle tabelle Error e ActionText

Il Software Development Kit (SDK) di Microsoft Windows include le stringhe di risorsa localizzate, le [tabelle degli errori](error-table.md)localizzati e le [tabelle ActionText](actiontext-table.md) localizzate per le lingue elencate nella tabella seguente. Il LANGIDs contrassegnato con asterischi indica che le stringhe delle risorse sono archiviate come lingua di base e possono quindi essere usate con tutti i dialetti di tale lingua.

È possibile importare le tabelle Error e ActionText localizzate nel database usando Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).



| LANGID (decimale) | LANGID (esadecimale) | Tabella codici ASCII | Abbreviazione | Linguaggio                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | ARA          | Arabo (Arabia Saudita)         | ar-SA            |
| 1027             | 0x403                | 1252            | GATTO          | Catalano                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | Cinese (Taiwan)              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | Cinese (Cina)               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | Ceco (Repubblica Ceca)        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | Danese (Danimarca)               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | Tedesco - Germania              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | Greco (Grecia)                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | Italian - Italy       | en-US            |
| 3082\*           | 0xC0A                | 1252            | ESN          | Spagnolo (ordinamento moderno)-Spagna | es-ES            |
| 1061             | 0x425                | 1257            | ETI          | Estone                      | et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | Finlandese-Finlandia             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | Francese - Francia               | fr-FR            |
| 1037             | 0x40D                | 1255            | HEB          | Ebraico-Israele               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | Ungherese (Ungheria)           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | Italiano - Italia               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | Giapponese - Giappone              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | Coreano - Corea del Sud                | Ko Ko            |
| 1063             | 0x427                | 1257            | LTH          | Lituano                    | lt-LT            |
| 1062             | 0x426                | 1257            | LVI          | Lettone                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | Olandese (Paesi Bassi)           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | Norvegese (Bokmål)-Norvegia    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | Polacco-Polonia               | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | Portoghese (Brasile)           | pt-BR            |
| 2070             | 0x816                | 1252            | PTG          | Portoghese (Portogallo)         | pt-PT            |
| 1048             | 0x418                | 1250            | ROM          | Rumeno (Romania)            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | Russo - Russia              | ru-RU            |
| 1050             | 0x41A                | 1250            | HRV          | Croato (Croazia)            | hr-HR            |
| 1051             | 0x41B                | 1250            | SKY          | Slovacco (Slovacchia)             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | Svedese (Svezia)              | sv-SE            |
| 1054             | 0x41E                | 874             | THA          | Thai-Thailandia               | th-TH            |
| 1055             | 0x41F                | 1254            | TRK          | Turco (Turchia)              | tr-TR            |
| 1060             | 0x424                | 1250            | SLV          | Sloveno (Slovenia)          | sl-SI            |
| 1066             | 0x42A                | 1258            | VIT          | Vietnamita-Vietnam         | vi-VN            |
| 1069             | 0x42D                | 1252            | EUQ          | Basco (Basco)               | eu-ES            |



 

**Windows Vista:** Oltre alle lingue elencate nella tabella precedente, le lingue nella tabella seguente sono disponibili a partire da Windows Vista.



| LANGID (decimale) | LANGID (esadecimale) | Tabella codici ASCII | Abbreviazione | Linguaggio        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BGR          | Bulgaro       | bg-BG            |
| 1058             | 0x422                | 1251            | UKR          | Ucraino       | uk-UA            |
| 2074             | 0x81A                | 1250            | SRL          | Serbo (alfabeto latino) | Sr-Latn-CS       |



 

 

 



