---
title: Compressione dei dati
description: Compressione dei dati
ms.assetid: b231316b-0c81-410a-b2fe-b58ab7aca02b
keywords:
- gestione compressione video,compressione dei dati
- VCM (Gestione compressione video),compressione dei dati
- Macro ICCompressBegin
- Funzione ICCompress
- Macro ICCompressEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f45c7b592b4b55e77b71390d7ffd79b23714242ea678d641d4a3f5b8118bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145004"
---
# <a name="compressing-data"></a>Compressione dei dati

L'esempio seguente comprime i dati di immagine da usare in un file AVI. Presuppone che l'utente non supporti i flag TEMPORAL VIDCF \_ e VIDCF, ma \_ supporta VIDCF \_ QUALITY. L'esempio usa la macro [**ICCompressBegin,**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) [**la funzione ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) e la macro [**ICCompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-iccompressend)


```C++
DWORD dwCkID; 
DWORD dwCompFlags; 
DWORD dwQuality; 
LONG  lNumFrames, lFrameNum; 
// Assume dwNumFrames is initialized to the total number of frames. 
// Assume dwQuality holds the proper quality value (0-10000). 
// Assume lpbiOut, lpOut, lpbiIn, and lpIn are initialized properly. 
 
// If OK to start, compress each frame. 
if (ICCompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for ( lFrameNum = 0; lFrameNum < lNumFrames; lFrameNum++)
    { 
        if (ICCompress(hIC, 0, lpbiOut, lpOut, lpbiIn, lpIn, 
            &dwCkID, &dwCompFlags, lFrameNum, 
            0, dwQuality, NULL, NULL) == ICERR_OK)
        { 
            // Write compressed data to the AVI file. 
             
            // Set lpIn to the next frame in the sequence. 
             
        } 
        else 
        { 
            // Handle compressor error. 
        } 
    } 
    ICCompressEnd(hIC);    // terminate compression 
} 
else 
{ 
    // Handle the error identifying the unsupported format. 
} 
 
```



 

 




