---
description: '\_SDURATION DELLE IMPOSTAZIONI LOCALI'
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb7031c5e9ddc3173fe7f10117eaad8c72820b1d3b81a82da33f6541901a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147364"
---
# <a name="locale_sduration"></a>\_SDURATION DELLE IMPOSTAZIONI LOCALI

**Windows Vista e versioni successive:** Formato della durata dell'ora costituito da immagini di formato elencate nella tabella seguente. Il formato è simile al formato per [LOCALE \_ STIMEFORMAT](locale-stime-constants.md). Come per LOCALE \_ STIMEFORMAT, questo formato può includere anche qualsiasi stringa di caratteri racchiusa tra virgolette singole. I formati possono includere, ad esempio, "h:mm:ss" o "d'd 'h'h 'm'm 's.fff's'". Rispetto a LOCALE \_ STIMEFORMAT, sono disponibili immagini di formato aggiuntive per le frazioni di secondo. Poiché questo formato è per durata, non per ora, non specifica un sistema di clock a 12 o 24 ore o include un indicatore AM/PM. Questa costante può essere usata, ad esempio, per un'applicazione multi-media che visualizza l'ora del file o un'applicazione per eventi di sport che visualizza gli orari di fine.



| Valore | Significato                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h     | Ore senza zeri iniziali per le ore a cifra singola                                                                                                                                                                                  |
| hh    | Ore con zeri iniziali per le ore a cifra singola                                                                                                                                                                                     |
| m     | Minuti senza zeri iniziali per minuti a cifra singola                                                                                                                                                                              |
| MM    | Minuti con zeri iniziali per minuti a cifra singola                                                                                                                                                                                 |
| s     | Secondi senza zeri iniziali per secondi a cifra singola                                                                                                                                                                              |
| ss    | Secondi con zeri iniziali per secondi a cifra singola                                                                                                                                                                                 |
| f     | Decime di secondo                                                                                                                                                                                                                  |
| ff    | Centesimi di secondo                                                                                                                                                                                                              |
| fff   | Millesima di secondo; il carattere "f" può verificarsi fino a nove volte consecutive (fffffffff), anche se il supporto per i timer di frequenza è limitato a 100 nanosecondi; se sono presenti nove caratteri, le ultime due cifre sono sempre zero |



 

 

 



