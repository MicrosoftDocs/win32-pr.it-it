---
title: Accesso a un buffer di I/O di file
description: Accesso a un buffer di I/O di file
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- I/O dei file multimediali, accesso ai buffer
- I/O di file, accesso ai buffer
- input e output (I/O), accesso ai buffer
- I/O (input e output), accesso ai buffer
- accesso ai buffer di I/O
- I/O memorizzato nel buffer
- mmioSetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299733"
---
# <a name="accessing-a-file-io-buffer"></a><span data-ttu-id="8d008-110">Accesso a un buffer di I/O di file</span><span class="sxs-lookup"><span data-stu-id="8d008-110">Accessing a File I/O Buffer</span></span>

<span data-ttu-id="8d008-111">Nell'esempio seguente viene accedere direttamente a un buffer di I/O per leggere i dati da un file Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8d008-111">The following example accesses an I/O buffer directly to read data from a waveform-audio file.</span></span>


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



<span data-ttu-id="8d008-112">Al termine dell'accesso a un buffer di I/O dei file, chiamare la funzione [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , passando un indirizzo della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) compilata dalla funzione [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) .</span><span class="sxs-lookup"><span data-stu-id="8d008-112">When you finish accessing a file I/O buffer, call the [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) function, passing an address of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure filled by the [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) function.</span></span> <span data-ttu-id="8d008-113">Se è stato scritto nel buffer, impostare il \_ flag MMIO Dirty nel membro **dwFlags** della struttura **MMIOINFO** prima di chiamare **mmioSetInfo**.</span><span class="sxs-lookup"><span data-stu-id="8d008-113">If you wrote to the buffer, set the MMIO\_DIRTY flag in the **dwFlags** member of the **MMIOINFO** structure before calling **mmioSetInfo**.</span></span> <span data-ttu-id="8d008-114">In caso contrario, il buffer non verrà scaricato su disco.</span><span class="sxs-lookup"><span data-stu-id="8d008-114">Otherwise, the buffer will not be flushed to disk.</span></span>

 

 