---
description: Una trasformazione di ridimensionamento moltiplica uno o più dei quattro componenti colore per numero. Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano il ridimensionamento.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Ridimensionamento di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234416"
---
# <a name="scaling-colors"></a><span data-ttu-id="4fbba-104">Ridimensionamento di colori</span><span class="sxs-lookup"><span data-stu-id="4fbba-104">Scaling Colors</span></span>

<span data-ttu-id="4fbba-105">Una trasformazione di ridimensionamento moltiplica uno o più dei quattro componenti colore per numero.</span><span class="sxs-lookup"><span data-stu-id="4fbba-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="4fbba-106">Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="4fbba-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="4fbba-107">Componente da ridimensionare</span><span class="sxs-lookup"><span data-stu-id="4fbba-107">Component to be scaled</span></span> | <span data-ttu-id="4fbba-108">Voce matrice</span><span class="sxs-lookup"><span data-stu-id="4fbba-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="4fbba-109">Red</span><span class="sxs-lookup"><span data-stu-id="4fbba-109">Red</span></span>                    | <span data-ttu-id="4fbba-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="4fbba-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="4fbba-111">Green</span><span class="sxs-lookup"><span data-stu-id="4fbba-111">Green</span></span>                  | <span data-ttu-id="4fbba-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="4fbba-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="4fbba-113">Blu</span><span class="sxs-lookup"><span data-stu-id="4fbba-113">Blue</span></span>                   | <span data-ttu-id="4fbba-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="4fbba-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="4fbba-115">Alfa</span><span class="sxs-lookup"><span data-stu-id="4fbba-115">Alpha</span></span>                  | <span data-ttu-id="4fbba-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="4fbba-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="4fbba-117">Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="4fbba-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="4fbba-118">Quindi il codice ridimensiona il componente blu di ogni pixel nell'immagine per un fattore di 2.</span><span class="sxs-lookup"><span data-stu-id="4fbba-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="4fbba-119">L'immagine originale viene disegnata insieme all'immagine trasformata.</span><span class="sxs-lookup"><span data-stu-id="4fbba-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="4fbba-120">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine ridimensionata a destra.</span><span class="sxs-lookup"><span data-stu-id="4fbba-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Mostra quattro barre colorate, quindi le stesse barre con colori diversi.](images/colortrans3.png)

<span data-ttu-id="4fbba-122">La tabella seguente mostra i vettori di colore per le quattro barre prima e dopo il ridimensionamento blu.</span><span class="sxs-lookup"><span data-stu-id="4fbba-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="4fbba-123">Si noti che il componente blu nella quarta barra dei colori è stato compreso tra 0,8 e 0,6.</span><span class="sxs-lookup"><span data-stu-id="4fbba-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="4fbba-124">Ciò è dovuto al fatto che GDI+ mantiene solo la parte frazionaria del risultato.</span><span class="sxs-lookup"><span data-stu-id="4fbba-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="4fbba-125">Ad esempio, (2) (0.8) = 1,6 e la parte frazionaria di 1,6 è 0,6.</span><span class="sxs-lookup"><span data-stu-id="4fbba-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="4fbba-126">La conservazione solo della parte frazionaria garantisce che il risultato sia sempre nell'intervallo \[ compreso tra 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="4fbba-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="4fbba-127">Originale</span><span class="sxs-lookup"><span data-stu-id="4fbba-127">Original</span></span>           | <span data-ttu-id="4fbba-128">Ridimensionato</span><span class="sxs-lookup"><span data-stu-id="4fbba-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="4fbba-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="4fbba-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="4fbba-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="4fbba-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="4fbba-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="4fbba-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="4fbba-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="4fbba-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="4fbba-137">Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="4fbba-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="4fbba-138">Il codice Ridimensiona quindi i componenti rosso, verde e blu di ogni pixel nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="4fbba-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="4fbba-139">I componenti rossi vengono ridimensionati fino al 25%, i componenti verdi vengono ridimensionati fino al 35% e i componenti blu vengono ridimensionati fino al 50%.</span><span class="sxs-lookup"><span data-stu-id="4fbba-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="4fbba-140">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine ridimensionata a destra.</span><span class="sxs-lookup"><span data-stu-id="4fbba-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![illustrazione che mostra quattro barre colorate, quindi le barre con colori diversi](images/colortrans4.png)

<span data-ttu-id="4fbba-142">La tabella seguente mostra i vettori di colore per le quattro barre prima e dopo il ridimensionamento rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="4fbba-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="4fbba-143">Originale</span><span class="sxs-lookup"><span data-stu-id="4fbba-143">Original</span></span>           | <span data-ttu-id="4fbba-144">Ridimensionato</span><span class="sxs-lookup"><span data-stu-id="4fbba-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="4fbba-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="4fbba-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="4fbba-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="4fbba-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="4fbba-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="4fbba-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="4fbba-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="4fbba-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="4fbba-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



