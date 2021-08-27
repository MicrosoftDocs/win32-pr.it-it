---
title: Riproduzione del file AVI
description: Riproduzione del file AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- MciSendCommand - funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038017"
---
# <a name="playing-the-avi-file"></a>Riproduzione del file AVI

Prima di usare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per inviare il comando [**MCI \_ PLAY,**](mci-play.md) l'applicazione alloca la memoria per la struttura, inizializza i membri che userà e imposta i flag corrispondenti ai membri usati nella struttura. Se l'applicazione non imposta un flag per un membro della struttura, i driver MCI ignorano il membro. Ad esempio, nell'esempio seguente viene riprodotto un film dalla posizione iniziale specificata da **dwFrom** alla posizione finale specificata da **dwTo**. Se una delle due posizioni è zero, l'esempio viene scritto in modo che la posizione non sia utilizzata.


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 