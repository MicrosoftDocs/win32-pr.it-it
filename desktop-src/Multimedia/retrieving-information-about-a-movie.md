---
title: Recupero di informazioni su un film
description: Recupero di informazioni su un film
ms.assetid: 678272e0-67fe-4ec1-88a8-924a773445a7
keywords:
- MciSendCommand - funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebc7d30d8eaef21bfe869e6cebbae7708758c9c26100562981be5b587aa2834
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805491"
---
# <a name="retrieving-information-about-a-movie"></a>Recupero di informazioni su un film

L'esempio seguente imposta il formato dell'ora su frame e ottiene la posizione corrente se il dispositivo viene riprodotto usando la [**funzione mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
MCI_DGV_SET_PARMS mciSet; 
MCI_DGV_STATUS_PARMS mciStatus; 
 
// Put in frame mode. 
mciSet.dwTimeFormat = MCI_FORMAT_FRAMES; 
mciSendCommand(wDeviceID, MCI_SET, 
    MCI_SET_TIME_FORMAT, 
    (DWORD)(LPSTR)&mciSet); 
 
mciStatus.dwItem = MCI_STATUS_MODE; 
mciSendCommand(wDeviceID, MCI_STATUS, 
    MCI_STATUS_ITEM, 
    (DWORD)(LPSTR)&mciStatus); 
 
// If device is playing, get the position. 
if (mciStatus.dwReturn == MCI_MODE_PLAY)
{ 
    mciStatus.dwItem = MCI_STATUS_POSITION; 
    mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM, 
        (DWORD)(LPSTR)&mciStatus); 
 
    // Update the position from mciStatus.dwReturn. 
} 
```



 

 