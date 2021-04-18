---
title: Lettura da un flusso e scrittura in un'altra
description: Lettura da un flusso e scrittura in un'altra
ms.assetid: 035a8862-9a0f-49d2-a060-5131ff2b7887
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b217dbfd0b88962b037c2822dbc7095bc87a83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298639"
---
# <a name="reading-from-one-stream-and-writing-to-another"></a><span data-ttu-id="f2971-103">Lettura da un flusso e scrittura in un'altra</span><span class="sxs-lookup"><span data-stu-id="f2971-103">Reading from One Stream and Writing to Another</span></span>

<span data-ttu-id="f2971-104">Nell'esempio seguente vengono letti i dati da un flusso, viene eseguita un'operazione con i dati e i dati compressi vengono scritti in un flusso di un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f2971-104">The following example reads data from a stream, does something with the data, and writes the compressed data into a stream of a new file.</span></span>


```C++
// SaveSmall - copies a stream of data from one file, compresses 
// the stream, and writes the compressed stream to a new file. 
// 
// ps stream interface pointer 
// lpFilename - new AVI file to build 
// 
 
void SaveSmall(PAVISTREAM ps, LPSTR lpFilename) 
{ 
    PAVIFILE         pf; 
    PAVISTREAM       psSmall; 
    HRESULT          hr; 
    AVISTREAMINFO    strhdr; 
    BITMAPINFOHEADER bi; 
    BITMAPINFOHEADER biNew; 
    LONG             lStreamSize; 
    LPVOID           lpOld; 
    LPVOID           lpNew; 
 
    // Determine the size of the format data using 
    // AVIStreamFormatSize. 
    AVIStreamFormatSize(ps, 0, &lStreamSize); 
    if (lStreamSize > sizeof(bi)) // Format too large? 
        return; 
 
    lStreamSize = sizeof(bi); 
    hr = AVIStreamReadFormat(ps, 0, &bi, &lStreamSize); // Read format 
    if (bi.biCompression != BI_RGB) // Wrong compression format? 
        return; 
 
    hr = AVIStreamInfo(ps, &strhdr, sizeof(strhdr)); 
 
    // Create new AVI file using AVIFileOpen. 
    hr = AVIFileOpen(&pf, lpFilename, OF_WRITE | OF_CREATE, NULL); 
    if (hr != 0) 
        return; 
 
    // Set parameters for the new stream. 
    biNew = bi; 
    biNew.biWidth /= 2; 
    biNew.biHeight /= 2; 
    biNew.biSizeImage = ((((UINT)biNew.biBitCount * biNew.biWidth 
                        + 31)&~31) / 8) * biNew.biHeight; 
    SetRect(&strhdr.rcFrame, 0, 0, (int) biNew.biWidth, 
            (int) biNew.biHeight); 
 
    // Create a stream using AVIFileCreateStream. 
    hr = AVIFileCreateStream(pf, &psSmall, &strhdr); 
    if (hr != 0) {            //Stream created OK? If not, close file. 
        AVIFileRelease(pf); 
        return; 
    } 
 
    // Set format of new stream using AVIStreamSetFormat. 
    hr = AVIStreamSetFormat(psSmall, 0, &biNew, sizeof(biNew)); 
    if (hr != 0) { 
        AVIStreamRelease(psSmall); 
        AVIFileRelease(pf); 
        return; 
    } 
 
    // Allocate memory for the bitmaps. 
    lpOld = GlobalAllocPtr(GMEM_MOVEABLE, bi.biSizeImage); 
    lpNew = GlobalAllocPtr(GMEM_MOVEABLE, biNew.biSizeImage); 
 
    // Read the stream data using AVIStreamRead. 
    for (lStreamSize = AVIStreamStart(ps); lStreamSize <
        AVIStreamEnd(ps); lStreamSize++) { 
        hr = AVIStreamRead(ps, lStreamSize, 1, lpOld, bi.biSizeImage,
            NULL, NULL); 
        // 
        // Place error check here. 
        // 
 
        // Do something with the data and write it to lpNew buffer. 
 
        // Save the compressed data using AVIStreamWrite. 
        hr = AVIStreamWrite(psSmall, lStreamSize, 1, lpNew,
            biNew.biSizeImage, AVIIF_KEYFRAME, NULL, NULL); 
    } 
 
     // Close the stream and file. 
    AVIStreamRelease(psSmall); 
    AVIFileRelease(pf); 
} 
 
```



 

 




