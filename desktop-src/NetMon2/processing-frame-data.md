---
description: Nell'esempio di codice seguente il monitoraggio imposta un filtro di acquisizione che specifica solo IP e i dati del protocollo richiesti.
ms.assetid: 0945bceb-b5fe-4f07-866b-4e0468227610
title: Elaborazione dei dati del frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41c49de62d630033aa7d3ed3e8e115fd1a02f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967241"
---
# <a name="processing-frame-data"></a>Elaborazione dei dati del frame

Nell'esempio di codice seguente il monitoraggio imposta un filtro di acquisizione che specifica **solo IP** e i dati del protocollo richiesti.


```C++
STDMETHODIMP CTestMon::OnFrames(UPDATE_EVENT Event)
{
    DWORD i;
    LPFRAMETABLE lpFrameTable = Event.lpFrameTable;

    // The frame table can wrap the indexes.
    for (
      i = lpFrameTable->StartIndex; 
      i != lpFrameTable->EndIndex; 
     (i == lpFrameTable->FrameTableLength ) ? i=0: i ++ )
    {
        LPFRAME_DESCRIPTOR lpFrameDesc = &lpFrameTable->Frames[i];
        
        // Cast the frame data to an unaligned pointer to an IP  
        // structure. A try/catch block could be a workaround, but
        // if the capture filter is set correctly, this is the
        // verifiable IP.
        ULPIP ulpIP = (ULPIP)(&lpFrameDesc->FramePointer[lpFrameDesc->LowProtocolOffset]);
        // Now examine the IP frame.
    }
    return NOERROR;
}
```



 

 



