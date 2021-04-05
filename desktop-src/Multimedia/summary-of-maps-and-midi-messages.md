---
title: Riepilogo delle mappe e dei messaggi MIDI
description: Riepilogo delle mappe e dei messaggi MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappa canali
- Mapper MIDI, mappe patch
- Mapper MIDI, mappe chiave
- Mappa canali
- Mappe patch
- Mappe chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713303"
---
# <a name="summary-of-maps-and-midi-messages"></a>Riepilogo delle mappe e dei messaggi MIDI

Di seguito sono riportati i byte di stato per i messaggi MIDI e i tipi di mappa che interessano ogni messaggio.



| Stato MIDI | Descrizione               | Tipi di mappa                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Nota disattivato                  | Mappe canali, mappe chiave   |
| 0x90-0x9F   | Nota su                    | Mappe canali, mappe chiave   |
| Messaggi 0XA0-0xAF   | Aftertouch chiave polifonica | Mappe canali, mappe chiave   |
| 0xB0-0xBF   | Modifica controllo            | Mappe del canale, mappe delle patch |
| 0xC0-0xCF   | Modifica del programma            | Mappe del canale, mappe delle patch |
| 0xD0-0xDF   | Canale aftertouch        | Mappe del canale             |
| 0xE0-0xEF   | Modifica Pitch-Bend         | Mappe del canale             |
| 0xF0-0xFF   | Sistema                    | Non mappata               |



 

-   I quattro bit più significativi rappresentano il valore dello stato. I quattro bit di ordine inferiore rappresentano le informazioni sul canale.
-   Le mappe delle patch hanno effetto solo sul controller 7 (volume principale).
-   I messaggi di sistema vengono inviati a tutti i dispositivi elencati in una mappa canali.

 

 




