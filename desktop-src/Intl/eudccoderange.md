---
description: La chiave del Registro di sistema EUDCCodeRange definisce intervalli di codice di caratteri definiti dall'utente finale (EUDC) per diverse code pages (set di caratteri).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120676"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La chiave del Registro di sistema EUDCCodeRange definisce intervalli di codice di caratteri definiti dall'utente [finale (EUDC)](end-user-defined-characters.md) per diverse code pages (set di caratteri). Viene usato solo dagli strumenti che creano UDC e non è di interesse diretto per gli utenti di EUDC. Questa chiave del Registro di sistema ha il percorso del Registro di sistema seguente:

HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange

Il formato è:

EUDCCodeRange CodePage=FromTo \[ ,FromTo\]

dove:



| Valore         | Descrizione                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Una delle stringhe "932" (giapponese), "936" (cinese semplificato), "949" (coreano), "950" (cinese tradizionale) o "Unicode" (Unicode). Non sono supportati altri valori.                                     |
| FromTo   | Valore stringa costituito da una coppia di valori esadecimali a 4 cifre separati da un trattino (-). È possibile specificare fino a quattro valori FromTo, ognuno dei quali deve essere separato dal valore precedente da una virgola (,). |



 

Di seguito sono riportati i valori corretti per la voce del Registro di sistema.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci del Registro di sistema EUDC](eudc-registry-entries.md)
</dt> <dt>

[Eudc](eudc.md)
</dt> </dl>

 

 



