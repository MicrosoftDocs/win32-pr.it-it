---
description: impostazioni locali \_ SDURATION
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00740d2f041794b36e8f0e0d8ad2d25723bc12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319978"
---
# <a name="locale_sduration"></a>impostazioni locali \_ SDURATION

**Windows Vista e versioni successive:** Formato della durata dell'ora composto dalle immagini di formato elencate nella tabella seguente. Il formato è simile al formato per le [impostazioni locali \_ STIMEFORMAT](locale-stime-constants.md). Come per le impostazioni locali \_ STIMEFORMAT, questo formato può includere anche qualsiasi stringa di caratteri racchiusa tra virgolette singole. I formati possono includere, ad esempio, "h:mm: SS" o "d" h ' m'' s. fff ''. Rispetto alle impostazioni locali \_ STIMEFORMAT, sono disponibili immagini di formato aggiuntive per frazioni di secondo. Poiché questo formato è per la durata, non per il tempo, non specifica un sistema di clock a 12 o 24 ore o include un indicatore AM/PM. Questa costante può essere usata, ad esempio, per un'applicazione Multimedia che Visualizza l'ora di file o un'applicazione di eventi sportivi che visualizza le ore di fine.



| Valore | Significato                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h     | Ore senza zeri iniziali per le ore a una sola cifra                                                                                                                                                                                  |
| hh    | Ore con zeri iniziali per le ore a una sola cifra                                                                                                                                                                                     |
| m     | Minuti senza zeri iniziali per minuti a una sola cifra                                                                                                                                                                              |
| MM    | Minuti con zeri iniziali per minuti a una sola cifra                                                                                                                                                                                 |
| s     | Secondi senza zeri iniziali per i secondi a una sola cifra                                                                                                                                                                              |
| ss    | Secondi con zeri iniziali per i secondi a una sola cifra                                                                                                                                                                                 |
| f     | Decimi di secondo                                                                                                                                                                                                                  |
| ff    | Centesimi di secondo                                                                                                                                                                                                              |
| fff   | Millesimi di secondo; il carattere "f" può essere composto da un massimo di nove volte consecutive (fffffffff), sebbene il supporto per i timer di frequenza sia limitato a 100 nanosecondi. Se sono presenti nove caratteri, le ultime due cifre sono sempre zero |



 

 

 



