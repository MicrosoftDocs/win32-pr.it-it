---
description: GDI+ fornisce la funzione GetImageEncoders in modo che sia possibile determinare i codificatori di immagini disponibili nel computer.
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: Elenco di codificatori installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310e9d366cdacde019373724f2b9feb3b94aef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978991"
---
# <a name="listing-installed-encoders"></a><span data-ttu-id="fa5c6-103">Elenco di codificatori installati</span><span class="sxs-lookup"><span data-stu-id="fa5c6-103">Listing Installed Encoders</span></span>

<span data-ttu-id="fa5c6-104">GDI+ fornisce la funzione [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) in modo che sia possibile determinare i codificatori di immagini disponibili nel computer.</span><span class="sxs-lookup"><span data-stu-id="fa5c6-104">GDI+ provides the [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) function so that you can determine which image encoders are available on your computer.</span></span> <span data-ttu-id="fa5c6-105">**GetImageEncoders** restituisce una matrice di oggetti [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="fa5c6-105">**GetImageEncoders** returns an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="fa5c6-106">Prima di chiamare **GetImageEncoders**, è necessario allocare un buffer sufficientemente grande da ricevere tale matrice.</span><span class="sxs-lookup"><span data-stu-id="fa5c6-106">Before you call **GetImageEncoders**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="fa5c6-107">È possibile chiamare [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) per determinare le dimensioni del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="fa5c6-107">You can call [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="fa5c6-108">Nell'applicazione console seguente sono elencati i codificatori di immagini disponibili:</span><span class="sxs-lookup"><span data-stu-id="fa5c6-108">The following console application lists the available image encoders:</span></span>


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

   UINT  num;        // number of image encoders
   UINT  size;       // size, in bytes, of the image encoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);

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



<span data-ttu-id="fa5c6-109">Quando si esegue l'applicazione console precedente, l'output sarà simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="fa5c6-109">When you run the preceding console application, the output will be similar to the following:</span></span>


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
