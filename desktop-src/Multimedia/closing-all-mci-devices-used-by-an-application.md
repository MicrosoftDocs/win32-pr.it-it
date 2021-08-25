---
title: Chiusura di tutti i dispositivi MCI usati da un'applicazione
description: Chiusura di tutti i dispositivi MCI usati da un'applicazione
ms.assetid: 1d7d3800-b38f-4187-ba57-9849fef4d707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf1f122c7fe2d70d3022497cf1e039c01b6c76516703e57261767253191e9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807951"
---
# <a name="closing-all-mci-devices-used-by-an-application"></a>Chiusura di tutti i dispositivi MCI usati da un'applicazione

L'esempio seguente chiude tutti i dispositivi MCI aperti da un'applicazione usando la [**funzione mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
UINT wDeviceID;
DWORD dwReturn;
 
// Closes all MCI devices opened by this application.
// Waits until devices are closed before returning.

if(dwReturn = mciSendCommand(MCI_ALL_DEVICE_ID, MCI_CLOSE, MCI_WAIT, 
    NULL))
    
    // Error, unable to close all devices.
    
```



 

 