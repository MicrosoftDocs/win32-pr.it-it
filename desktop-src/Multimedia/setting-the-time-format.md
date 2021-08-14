---
title: Impostazione del formato dell'ora
description: Impostazione del formato dell'ora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eb5a9194f3f2598cd8f88fbefb3ea741f51eb9c25210deb6db69c54259e189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370889"
---
# <a name="setting-the-time-format"></a>Impostazione del formato dell'ora

Usare il [**messaggio di comando \_ MCI SET**](mci-set.md) insieme alla struttura [**MCI SET \_ \_ PARMS**](mci-set-parms.md) per impostare il formato dell'ora per un dispositivo aperto. Impostare il **membro dwTimeFormat** su una delle costanti seguenti.



| Costante                   | Formato ora                                          |
|----------------------------|------------------------------------------------------|
| BYTE IN FORMATO MCI \_ \_         | Byte (nei file di formato \[ PCM modulati nel codice \] di pulsazione) |
| MILLISECONDI \_ DI \_ FORMATO MCI  | Millisecondi                                         |
| FORMATO MCI \_ \_ MSF           | Minuto/secondo/fotogramma                                  |
| ESEMPI DI FORMATO MCI \_ \_       | Esempi                                              |
| MCI \_ FORMAT \_ SMPTE \_ 24     | SMPTE, 24 frame                                      |
| MCI \_ FORMAT \_ SMPTE \_ 25     | SMPTE, 25 frame                                      |
| MCI \_ FORMAT \_ SMPTE \_ 30     | SMPTE, 30 frame                                      |
| MCI \_ FORMAT \_ SMPTE \_ 30DROP | SMPTE, rilascio di 30 frame                                 |
| FORMATO MCI \_ \_ TMSF          | Track/minute/second/frame                            |
| MCI \_ SEQ \_ FORMAT \_ SONGPTR  | Puntatore del brano MIDI                                    |



 

L'esempio seguente imposta il formato dell'ora su millisecondi nel dispositivo specificato dalla variabile wDeviceID usando la [**funzione mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 