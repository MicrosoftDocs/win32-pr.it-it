---
title: Verifica del dispositivo di output
description: Verifica del dispositivo di output
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- Comando MCI_ stato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955586"
---
# <a name="verifying-the-output-device"></a>Verifica del dispositivo di output

Dopo l'apertura di Sequencer, è necessario verificare se il mapper del MIDI è stato disponibile e selezionato come dispositivo di output. Nell'esempio seguente viene usato il comando di [**\_ stato MCI**](mci-status.md) per verificare che il mapper MIDI sia il dispositivo di output per il sequencer MCI.


```C++
UINT wDeviceID;      // valid MCI sequencer ID
DWORD dwReturn;
MCI_STATUS_PARMS mciStatusParms;

// Make sure the opened device is the MIDI mapper.

mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;

if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM,
    (DWORD)(LPVOID) &mciStatusParms))
{
    
    // Error sending MCI_STATUS command. 
    
    return;
}
if (LOWORD(mciStatusParms.dwReturn) == MIDI_MAPPER)
{
    
    // The MIDI mapper is the output device. 
    
}
Else
{
    
    // The MIDI mapper is not the output device. 
    
} 
```



 

 




