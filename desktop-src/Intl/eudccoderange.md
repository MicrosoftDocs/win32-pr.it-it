---
description: La chiave del registro di sistema EUDCCodeRange definisce gli intervalli di codice dei caratteri definiti dall'utente finale (EUDC) per varie tabelle codici (set di caratteri).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317151"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La chiave del registro di sistema EUDCCodeRange definisce gli intervalli di codice dei [caratteri definiti dall'utente finale (EUDC)](end-user-defined-characters.md) per varie tabelle codici (set di caratteri). Viene usato solo da strumenti che creano EUDCs e non è un problema diretto per gli utenti di EUDC. Questa chiave del registro di sistema presenta il seguente percorso del registro di sistema:

HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ controllo \\ NLS tabella \\ codici \\ EUDCCodeRange

Il formato è:

Tabella codici EUDCCodeRange = FromTo \[ , FromTo\]

dove:



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Una delle stringhe "932" (giapponese), "936" (cinese semplificato), "949" (coreano), "950" (cinese tradizionale) o "Unicode" (Unicode). Nessun altro valore supportato.                                     |
| FromTo   | Valore stringa costituito da una coppia di valori esadecimali a 4 cifre separati da un trattino (-). È possibile specificare fino a quattro valori FromTo, ognuno dei quali deve essere separato dal valore precedente mediante una virgola (,). |



 

Di seguito sono riportati i valori corretti per la voce del registro di sistema.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci del registro di sistema EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



