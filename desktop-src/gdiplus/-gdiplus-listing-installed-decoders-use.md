---
description: Windows GDI+ fornisce la funzione GetImageDecoders in modo che sia possibile determinare i decodificatori di immagini disponibili nel computer.
ms.assetid: 793e23de-d959-4feb-8bf6-647a455c85ae
title: Elenco di decodificatori installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a20a4e8ac88fa884483ebeaf6592b8085fde807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978994"
---
# <a name="listing-installed-decoders"></a><span data-ttu-id="7528e-103">Elenco di decodificatori installati</span><span class="sxs-lookup"><span data-stu-id="7528e-103">Listing Installed Decoders</span></span>

<span data-ttu-id="7528e-104">Windows GDI+ fornisce la funzione [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) in modo che sia possibile determinare i decodificatori di immagini disponibili nel computer.</span><span class="sxs-lookup"><span data-stu-id="7528e-104">Windows GDI+ provides the [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) function so that you can determine which image decoders are available on your computer.</span></span> <span data-ttu-id="7528e-105">**GetImageDecoders** restituisce una matrice di oggetti [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="7528e-105">**GetImageDecoders** returns an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="7528e-106">Prima di chiamare **GetImageDecoders**, è necessario allocare un buffer sufficientemente grande da ricevere tale matrice.</span><span class="sxs-lookup"><span data-stu-id="7528e-106">Before you call **GetImageDecoders**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="7528e-107">È possibile chiamare [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) per determinare le dimensioni del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="7528e-107">You can call [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="7528e-108">Nell'applicazione console seguente sono elencati i decodificatori di immagini disponibili:</span><span class="sxs-lookup"><span data-stu-id="7528e-108">The following console application lists the available image decoders:</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image decoders
   UINT  size;       // size, in bytes, of the image decoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many decoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageDecodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageDecoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageDecoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageDecoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="7528e-109">Quando si esegue l'applicazione console precedente, l'output sarà simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="7528e-109">When you run the preceding console application, the output will be similar to the following:</span></span>


```
image/bmp
image/jpeg
image/gif
image/x-emf
image/x-wmf
image/tiff
image/png
image/x-icon
```



 

 
