---
title: Riepilogo dei Mappe e MIDI
description: Riepilogo dei Mappe e MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Instrument Digital Interface (MIDI), MIDI Mapper
- MIDI (Instrument Digital Interface), MIDI Mapper
- MIDI Mapper, mappa dei canali
- MIDI Mapper, mappe patch
- MIDI Mapper, mappe delle chiavi
- channel map
- Mappe patch
- mappe delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89c23d6326e19cb5680906155d5ee2e8dbcc32735fabd8625658410ef4ddfa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781851"
---
# <a name="summary-of-maps-and-midi-messages"></a>Riepilogo dei Mappe e MIDI

Di seguito sono riportati i byte di stato per i messaggi MIDI e i tipi di mappa che interessano ogni messaggio.



| Stato MIDI | Descrizione               | Tipi di mappa                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Nota disattivata                  | Mappe dei canali, mappe delle chiavi   |
| 0x90-0x9F   | Nota su                    | Mappe dei canali, mappe delle chiavi   |
| 0xA0-0xAF   | Chiave polifonico aftertouch | Mappe dei canali, mappe delle chiavi   |
| 0xB0-0xBF   | Modifica del controllo            | Mappe dei canali, mappe patch |
| 0xC0-0xCF   | Modifica del programma            | Mappe dei canali, mappe patch |
| 0xD0-0xDF   | Canale aftertouch        | Mappe dei canali             |
| 0xE0-0xEF   | Cambio di passo-passo         | Mappe dei canali             |
| 0xF0-0xFF   | Sistema                    | Non mappata               |



 

-   I quattro bit più alti rappresentano il valore di stato. I quattro bit meno importanti rappresentano le informazioni sul canale.
-   Le mappe patch influiscono solo sul controller 7 (volume principale).
-   I messaggi di sistema vengono inviati a tutti i dispositivi elencati in una mappa dei canali.

 

 




