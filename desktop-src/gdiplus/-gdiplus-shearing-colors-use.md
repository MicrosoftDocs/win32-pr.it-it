---
description: Il taglio aumenta o diminuisce un componente colore di un importo proporzionale a un altro componente colore.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Colori di taglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131331"
---
# <a name="shearing-colors"></a><span data-ttu-id="bde6f-103">Colori di taglio</span><span class="sxs-lookup"><span data-stu-id="bde6f-103">Shearing Colors</span></span>

<span data-ttu-id="bde6f-104">Il taglio aumenta o diminuisce un componente colore di un importo proporzionale a un altro componente colore.</span><span class="sxs-lookup"><span data-stu-id="bde6f-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="bde6f-105">Si consideri, ad esempio, la trasformazione in cui il componente rosso viene aumentato di una metà del valore del componente blu.</span><span class="sxs-lookup"><span data-stu-id="bde6f-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="bde6f-106">In tale trasformazione, il colore (0,2, 0,5, 1) diventerà (0,7, 0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="bde6f-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="bde6f-107">Il nuovo componente rosso è 0,2 + (1/2) (1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="bde6f-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="bde6f-108">Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars4.bmp.</span><span class="sxs-lookup"><span data-stu-id="bde6f-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="bde6f-109">Il codice applica quindi la trasformazione di taglio descritta nel paragrafo precedente a ogni pixel nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="bde6f-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="bde6f-110">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine tranciata a destra.</span><span class="sxs-lookup"><span data-stu-id="bde6f-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![illustrazione che mostra quattro barre colorate, quindi le stesse barre con colori diversi](images/colortrans6.png)

<span data-ttu-id="bde6f-112">Nella tabella seguente vengono illustrati i vettori di colore per le quattro barre prima e dopo la trasformazione di taglio.</span><span class="sxs-lookup"><span data-stu-id="bde6f-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="bde6f-113">Originale</span><span class="sxs-lookup"><span data-stu-id="bde6f-113">Original</span></span>           | <span data-ttu-id="bde6f-114">Tranciati</span><span class="sxs-lookup"><span data-stu-id="bde6f-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="bde6f-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="bde6f-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="bde6f-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="bde6f-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="bde6f-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="bde6f-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="bde6f-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="bde6f-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="bde6f-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



