---
title: Individuazione e apertura di commediatori e decompressori
description: Individuazione e apertura di commediatori e decompressori
ms.assetid: ed931f01-dbfc-4fdc-b725-c062302b037b
keywords:
- Gestione compressione video (VCM), apertura di compressatori
- VCM (Gestione compressione video), apertura di comprimeri
- ICLocate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45b07c619095b4d50bdbdde5c3d2b1ca9209471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044432"
---
# <a name="locating-and-opening-compressors-and-decompressors"></a><span data-ttu-id="26856-106">Individuazione e apertura di commediatori e decompressori</span><span class="sxs-lookup"><span data-stu-id="26856-106">Locating and Opening Compressors and Decompressors</span></span>

<span data-ttu-id="26856-107">Nell'esempio seguente viene usata la funzione [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) per trovare un commutatore in grado di comprimere una bitmap a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="26856-107">The following example uses the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) function to find a compressor that can compress an 8-bits-per-pixel bitmap.</span></span>


```C++
BITMAPINFOHEADER bih; 
HIC              hIC 
 
// Initialize the bitmap structure. 
bih.biSize = sizeof(BITMAPINFOHEADER); 
bih.biWidth = bih.biHeight = 0; 
bih.biPlanes = 1; 
bih.biCompression = BI_RGB;      // standard RGB bitmap 
bih.biBitcount = 8;              // 8 bits-per-pixel format 
bih.biSizeImage = 0; 
bih.biXPelsPerMeter = bih.biYPelsPerMeter = 0; 
bih.biClrUsed = bih.biClrImportant = 256; 
 
hIC = ICLocate (ICTYPE_VIDEO, 0L, (LPBITMAPINFOHEADER) &bih, 
    NULL, ICMODE_COMPRESS); 
 
```



<span data-ttu-id="26856-108">Nell'esempio seguente vengono enumerati i decompressori del sistema per individuarne uno in grado di gestire il formato delle relative immagini.</span><span class="sxs-lookup"><span data-stu-id="26856-108">The following example enumerates the decompressors in the system to find one that can handle the format of its images.</span></span> <span data-ttu-id="26856-109">Questo esempio usa **ICTYPE \_ video** (equivalente al codice a quattro caratteri "vidc") e la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) per determinare se un compressore o un decompressore supporta il formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="26856-109">This example uses **ICTYPE\_VIDEO** (which is equivalent to the "VIDC" four-character code) and the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro to determine if a compressor or decompressor supports the image format.</span></span>


```C++
for (i=0; ICInfo(fccType, i, &icinfo); i++) 
{ 
    hic = ICOpen(icinfo.fccType, icinfo.fccHandler, ICMODE_QUERY); 
    if (hic) 
    { 
        // Skip this compressor if it can't handle the format. 
        if (fccType == ICTYPE_VIDEO && pvIn != NULL && 
            ICDecompressQuery(hic, pvIn, NULL) != ICERR_OK) 
        { 
            ICClose(hic); 
            continue; 
        } 
 
        // Find out the compressor name. 
        ICGetInfo(hic, &icinfo, sizeof(icinfo)); 
 
        // Add it to the combo box. 
        n = ComboBox_AddString(hwndC,icinfo.szDescription); 
        ComboBox_SetItemData(hwndC, n, hic); 
    } 
} 
 
```



<span data-ttu-id="26856-110">Nell'esempio seguente viene effettuato un tentativo di individuare un compressore specifico per comprimere il formato RGB a 8 bit in un formato RLE a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="26856-110">The following example attempts to locate a specific compressor to compress the 8-bit RGB format to an 8-bit RLE format.</span></span>


```C++
BITMAPINFOHEADER    bihIn, bihOut; 
HIC                 hIC 
 
// Initialize the bitmap structure. 

biSize = bihOut.biSize = sizeof(BITMAPINFOHEADER); 
bihIn.biWidth = bihIn.biHeight = bihOut.biWidth = bihOut.biHeight = 0; 
bihIn.biPlanes = bihOut.biPlanes= 1; 
bihIn.biCompression = BI_RGB;        // standard RGB bitmap for input 
bihOut.biCompression = BI_RLE8;      // 8-bit RLE for output format 
bihIn.biBitcount = bihOut.biBitCount = 8;  // 8 bits-per-pixel format 
bihIn.biSizeImage = bihOut.biSizeImage = 0; 
bihIn.biXPelsPerMeter = bih.biYPelsPerMeter = 
    bihOut.biXPelsPerMeter = bihOut.biYPelsPerMeter = 0; 
bihIn.biClrUsed = bih.biClrImportant = 
    bihOut.biClrUsed = bihOut.biClrImportant = 256; 

hIC = ICLocate (ICTYPE_VIDEO, 0L, 
    (LPBITMAPINFOHEADER)&bihIn, 
    (LPBITMAPINFOHEADER)&bihOut, ICMODE_COMPRESS); 
 
```



## <a name="related-topics"></a><span data-ttu-id="26856-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26856-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26856-112">Utilizzo di Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="26856-112">Using the Video Compression Manager</span></span>](using-the-video-compression-manager.md)
</dt> </dl>

 

 




