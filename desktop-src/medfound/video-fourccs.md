---
description: Video FourCC
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Video FourCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344851"
---
# <a name="video-fourccs"></a><span data-ttu-id="eeda2-103">Video FourCC</span><span class="sxs-lookup"><span data-stu-id="eeda2-103">Video FOURCCs</span></span>

<span data-ttu-id="eeda2-104">A molti formati video sono assegnati codici FOURCC.</span><span class="sxs-lookup"><span data-stu-id="eeda2-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="eeda2-105">Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="eeda2-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="eeda2-106">Ad esempio, il codice FOURCC per YUY2 video è' YUY2'.</span><span class="sxs-lookup"><span data-stu-id="eeda2-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="eeda2-107">Diverse macro C/C++ sono definite per la dichiarazione di valori FOURCC nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="eeda2-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="eeda2-108">La macro **MAKEFOURCC** è definita in mmsystem. h e la macro **FCC** è definita in Aviriff. h e in diversi altri file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="eeda2-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="eeda2-109">È anche possibile dichiarare direttamente un codice FOURCC come valore letterale stringa semplicemente invertendo l'ordine dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="eeda2-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="eeda2-110">Pertanto, le istruzioni seguenti sono equivalenti:</span><span class="sxs-lookup"><span data-stu-id="eeda2-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="eeda2-111">Nell'ultimo esempio è necessario invertire l'ordine dei byte perché Windows utilizza un'architettura little-endian.</span><span class="sxs-lookup"><span data-stu-id="eeda2-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="eeda2-112">' Y ' = 0x59,' U ' = 0x55 è 2' = 0x32, quindi ' 2YUY ' è 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="eeda2-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="eeda2-113">Alcune delle API [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md) usano un valore **D3DFORMAT** per descrivere un formato video.</span><span class="sxs-lookup"><span data-stu-id="eeda2-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="eeda2-114">Un codice FOURCC può essere usato anche in questo contesto:</span><span class="sxs-lookup"><span data-stu-id="eeda2-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="eeda2-115">Costanti FOURCC</span><span class="sxs-lookup"><span data-stu-id="eeda2-115">FOURCC Constants</span></span>

<span data-ttu-id="eeda2-116">Nella tabella seguente sono elencati alcuni codici FOURCC comuni.</span><span class="sxs-lookup"><span data-stu-id="eeda2-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="eeda2-117">Valore FOURCC</span><span class="sxs-lookup"><span data-stu-id="eeda2-117">FOURCC value</span></span> | <span data-ttu-id="eeda2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeda2-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeda2-119">H264</span><span class="sxs-lookup"><span data-stu-id="eeda2-119">'H264'</span></span>       | <span data-ttu-id="eeda2-120">Video H. 264.</span><span class="sxs-lookup"><span data-stu-id="eeda2-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="eeda2-121">I420</span><span class="sxs-lookup"><span data-stu-id="eeda2-121">'I420'</span></span>       | <span data-ttu-id="eeda2-122">Video YUV archiviato in formato Planar 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="eeda2-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="eeda2-123">'IYUV'</span><span class="sxs-lookup"><span data-stu-id="eeda2-123">'IYUV'</span></span>       | <span data-ttu-id="eeda2-124">Video YUV archiviato in formato Planar 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="eeda2-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="eeda2-125">' 4S2'</span><span class="sxs-lookup"><span data-stu-id="eeda2-125">'M4S2'</span></span>       | <span data-ttu-id="eeda2-126">Video MPEG-4 Part 2.</span><span class="sxs-lookup"><span data-stu-id="eeda2-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="eeda2-127">Mp4s</span><span class="sxs-lookup"><span data-stu-id="eeda2-127">'MP4S'</span></span>       | <span data-ttu-id="eeda2-128">Microsoft MPEG 4 codec versione 3.</span><span class="sxs-lookup"><span data-stu-id="eeda2-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="eeda2-129">Questo codec non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="eeda2-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="eeda2-130">MP4V</span><span class="sxs-lookup"><span data-stu-id="eeda2-130">'MP4V'</span></span>       | <span data-ttu-id="eeda2-131">Video MPEG-4 Part 2.</span><span class="sxs-lookup"><span data-stu-id="eeda2-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="eeda2-132">MPG1</span><span class="sxs-lookup"><span data-stu-id="eeda2-132">'MPG1'</span></span>       | <span data-ttu-id="eeda2-133">Video MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="eeda2-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="eeda2-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="eeda2-134">'MSS1'</span></span>       | <span data-ttu-id="eeda2-135">Contenuto codificato con il codec Windows Media Video 7 dello schermo.</span><span class="sxs-lookup"><span data-stu-id="eeda2-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="eeda2-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="eeda2-136">'MSS2'</span></span>       | <span data-ttu-id="eeda2-137">Contenuto codificato con il codec della schermata Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="eeda2-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="eeda2-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="eeda2-138">'UYVY'</span></span>       | <span data-ttu-id="eeda2-139">Video YUV archiviato in formato 4:2:2 compresso.</span><span class="sxs-lookup"><span data-stu-id="eeda2-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="eeda2-140">Simile a YUY2 ma con un ordine di dati diverso.</span><span class="sxs-lookup"><span data-stu-id="eeda2-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="eeda2-141">WMV1</span><span class="sxs-lookup"><span data-stu-id="eeda2-141">'WMV1'</span></span>       | <span data-ttu-id="eeda2-142">Contenuto codificato con il codec Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="eeda2-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="eeda2-143">WMV2</span><span class="sxs-lookup"><span data-stu-id="eeda2-143">'WMV2'</span></span>       | <span data-ttu-id="eeda2-144">Contenuto codificato con il codec Windows Media Video 8.</span><span class="sxs-lookup"><span data-stu-id="eeda2-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="eeda2-145">WMV3</span><span class="sxs-lookup"><span data-stu-id="eeda2-145">'WMV3'</span></span>       | <span data-ttu-id="eeda2-146">Contenuto codificato con il codec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="eeda2-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="eeda2-147">'WMVA'</span><span class="sxs-lookup"><span data-stu-id="eeda2-147">'WMVA'</span></span>       | <span data-ttu-id="eeda2-148">Contenuto codificato con la versione precedente e obsoleta del codec del profilo avanzato Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="eeda2-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="eeda2-149">'WMVP'</span><span class="sxs-lookup"><span data-stu-id="eeda2-149">'WMVP'</span></span>       | <span data-ttu-id="eeda2-150">Contenuto codificato con il codec di immagine Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="eeda2-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="eeda2-151">WVC1</span><span class="sxs-lookup"><span data-stu-id="eeda2-151">'WVC1'</span></span>       | <span data-ttu-id="eeda2-152">SMPTE 421M ("VC-1").</span><span class="sxs-lookup"><span data-stu-id="eeda2-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="eeda2-153">Contenuto codificato con Windows Media Video 9 profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="eeda2-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="eeda2-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="eeda2-154">'WVP2'</span></span>       | <span data-ttu-id="eeda2-155">Contenuto codificato con il codec Windows Media Video 9,1 image V2.</span><span class="sxs-lookup"><span data-stu-id="eeda2-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="eeda2-156">YUY2</span><span class="sxs-lookup"><span data-stu-id="eeda2-156">'YUY2'</span></span>       | <span data-ttu-id="eeda2-157">Video YUV archiviato in formato 4:2:2 compresso.</span><span class="sxs-lookup"><span data-stu-id="eeda2-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="eeda2-158">YV12</span><span class="sxs-lookup"><span data-stu-id="eeda2-158">'YV12'</span></span>       | <span data-ttu-id="eeda2-159">Video YUV archiviato in formato Planar 4:2:0 o 4:1:1.</span><span class="sxs-lookup"><span data-stu-id="eeda2-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="eeda2-160">Identico a I420/IYUV, tranne per il fatto che i piani utente e V sono stati scambiati.</span><span class="sxs-lookup"><span data-stu-id="eeda2-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="eeda2-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="eeda2-161">'YVU9'</span></span>       | <span data-ttu-id="eeda2-162">Video YUV archiviato in formato Planar 16:1:1.</span><span class="sxs-lookup"><span data-stu-id="eeda2-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="eeda2-163">YVYU</span><span class="sxs-lookup"><span data-stu-id="eeda2-163">'YVYU'</span></span>       | <span data-ttu-id="eeda2-164">Video YUV archiviato in formato 4:2:2 compresso.</span><span class="sxs-lookup"><span data-stu-id="eeda2-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="eeda2-165">Simile a YUY2 ma con un ordine di dati diverso.</span><span class="sxs-lookup"><span data-stu-id="eeda2-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="eeda2-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eeda2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeda2-167">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="eeda2-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="eeda2-168">GUID del sottotipo video</span><span class="sxs-lookup"><span data-stu-id="eeda2-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



