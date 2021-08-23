---
title: Accesso a un buffer di I/O di file
description: Accesso a un buffer di I/O di file
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- I/O di file multimediali, accesso ai buffer
- I/O di file, accesso ai buffer
- input e output (I/O), accesso ai buffer
- I/O (input e output), accesso ai buffer
- accesso ai buffer di I/O
- I/O memorizzato nel buffer
- Funzione mmioSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4ab9533f0f121d42f859961b60d405477856faacee8d8cf36a0dfb975e2587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808641"
---
# <a name="accessing-a-file-io-buffer"></a>Accesso a un buffer di I/O di file

L'esempio seguente accede direttamente a un buffer di I/O per leggere i dati da un file waveform-audio.


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



Al termine dell'accesso a un buffer di I/O di file, chiamare la funzione [**mmioSetInfo,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) passando un indirizzo della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) riempita dalla funzione [**mmioGetInfo.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) Se è stato scritto nel buffer, impostare il flag MMIO DIRTY nel membro \_ **dwFlags** della struttura **MMIOINFO** prima di chiamare **mmioSetInfo**. In caso contrario, il buffer non verrà scaricato su disco.

 

 