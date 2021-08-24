---
title: Istruzione BLOCK VarFileInfo
description: Descrive il formato del blocco di informazioni sulle variabili.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Istruzione VARFileInfo BLOCK Menu e altre risorse
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15b4bf57a14d6bae6dd5b83c8ea86e38830113fbcfbbaa27b143bf02bb130e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846971"
---
# <a name="varfileinfo-block-statement"></a>Istruzione BLOCK VarFileInfo

Definisce un blocco di informazioni sulle variabili.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Uno degli identificatori di lingua specificati nella sezione Osservazioni.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Uno degli identificatori del set di caratteri specificati nella sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile specificare più di una coppia di identificatori, ma ogni coppia deve essere separata dalla coppia precedente con una virgola.

Il *parametro langID* specifica uno dei codici lingua seguenti.



| Codice   | Linguaggio            | Codice   | Linguaggio                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabo              | 0x0415 | Polacco                    |
| 0x0402 | Bulgaro           | 0x0416 | Portoghese (Brasile)       |
| 0x0403 | Catalano             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Cinese tradizionale | 0x0418 | Romeno                  |
| 0x0405 | Ceco               | 0x0419 | Russo                   |
| 0x0406 | Danese              | 0x041A | Croato-Serbian (alfabeto latino)    |
| 0x0407 | Tedesco              | 0x041B | Slovacco                    |
| 0x0408 | Greco               | 0x041C | Albanese                  |
| 0x0409 | Inglese Stati Uniti        | 0x041D | Svedese                   |
| 0x040A | Castiliano spagnolo   | 0x041E | Thai                      |
| 0x040B | Finlandese             | 0x041F | Turco                   |
| 0x040C | Francese              | 0x0420 | Urdu                      |
| 0x040D | Ebraico              | 0x0421 | Bahasa                    |
| 0x040E | Ungherese           | 0x0804 | Cinese semplificato        |
| 0x040F | Islandese           | 0x0807 | Tedesco svizzero              |
| 0x0410 | Italiano             | 0x0809 | Regno unito. Inglese              |
| 0x0411 | Giapponese            | 0x080A | Spagnolo (Messico)          |
| 0x0412 | Coreano              | 0x080C | Francese spagnolo            |
| 0x0413 | Olandese               | 0x0C0C | Francese (Canada)           |
| 0x0414 | Norvegese - Bokmal  | 0x100C | Francese svizzero              |
| 0x0810 | Italiano svizzero       | 0x0816 | Portoghese (Portogallo)     |
| 0x0813 | Olandese olandese       | 0x081A | Serbo-Croatian (alfabeto cirillico) |
| 0x0814 | Norvegese - Nynorsk | ?      | ?                         |



 

Il *parametro charsetID* specifica uno degli identificatori di set di caratteri seguenti:



| Identificatore | Set di caratteri              |
|------------|----------------------------|
| 0          | ASCII a 7 bit                |
| 932        | Giappone (MAIUSC - JIS X-0208) |
| 949        | Corea (MAIUSC - KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Europa orientale) |
| 1251       | Cirillico                   |
| 1252       | Multilingue               |
| 1253       | Greco                      |
| 1254       | Turco                    |
| 1255       | Ebraico                     |
| 1256       | Arabo                     |



 

 

 




