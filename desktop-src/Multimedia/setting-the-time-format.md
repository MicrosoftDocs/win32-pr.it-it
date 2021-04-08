---
title: Impostazione del formato dell'ora
description: Impostazione del formato dell'ora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872414"
---
# <a name="setting-the-time-format"></a>Impostazione del formato dell'ora

Usare il messaggio del comando [**\_ set di MCI**](mci-set.md) insieme alla struttura [**\_ set \_ parametri di MCI**](mci-set-parms.md) per impostare il formato dell'ora per un dispositivo aperto. Impostare il membro **dwTimeFormat** su una delle seguenti costanti.



| Costante                   | Formato ora                                          |
|----------------------------|------------------------------------------------------|
| \_byte in formato MCI \_         | Byte (nei file in formato PCM con modulazione del codice Pulse \[ \] ) |
| \_ \_ millisecondi formato MCI  | Millisecondi                                         |
| \_MSF formato \_ MCI           | Minuto/secondo/frame                                  |
| \_esempi di formato MCI \_       | Esempi                                              |
| \_Formato MCI \_ \_ 24     | SMPTE, 24 frame                                      |
| \_Formato MCI \_ \_ 25     | SMPTE, 25 frame                                      |
| \_Formato MCI \_ \_ 30     | SMPTE, 30 frame                                      |
| \_Formato MCI \_ \_ 30DROP | SMPTE, 30 frame drop                                 |
| \_formato MCI \_ TMSF          | Traccia/minuto/secondo/frame                            |
| \_ \_ formato SONGPTR MCI \_ Seq  | Puntatore al brano MIDI                                    |



 

Nell'esempio seguente il formato dell'ora viene impostato su millisecondi sul dispositivo specificato dalla variabile wDeviceID usando la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .


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



 

 