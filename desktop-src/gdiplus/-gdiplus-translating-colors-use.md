---
description: Una traduzione aggiunge un valore a uno o più dei quattro componenti del colore. Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano le traduzioni.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Conversione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569655"
---
# <a name="translating-colors"></a><span data-ttu-id="b4d8c-104">Conversione di colori</span><span class="sxs-lookup"><span data-stu-id="b4d8c-104">Translating Colors</span></span>

<span data-ttu-id="b4d8c-105">Una traduzione aggiunge un valore a uno o più dei quattro componenti del colore.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="b4d8c-106">Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano le traduzioni.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="b4d8c-107">Componente da tradurre</span><span class="sxs-lookup"><span data-stu-id="b4d8c-107">Component to be translated</span></span> | <span data-ttu-id="b4d8c-108">Voce matrice</span><span class="sxs-lookup"><span data-stu-id="b4d8c-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="b4d8c-109">Red</span><span class="sxs-lookup"><span data-stu-id="b4d8c-109">Red</span></span>                        | <span data-ttu-id="b4d8c-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="b4d8c-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="b4d8c-111">Green</span><span class="sxs-lookup"><span data-stu-id="b4d8c-111">Green</span></span>                      | <span data-ttu-id="b4d8c-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="b4d8c-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="b4d8c-113">Blu</span><span class="sxs-lookup"><span data-stu-id="b4d8c-113">Blue</span></span>                       | <span data-ttu-id="b4d8c-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="b4d8c-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="b4d8c-115">Alfa</span><span class="sxs-lookup"><span data-stu-id="b4d8c-115">Alpha</span></span>                      | <span data-ttu-id="b4d8c-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="b4d8c-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="b4d8c-117">Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars.bmp.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="b4d8c-118">Il codice aggiunge quindi 0,75 al componente rosso di ogni pixel nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="b4d8c-119">L'immagine originale viene disegnata insieme all'immagine trasformata.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="b4d8c-120">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine trasformata a destra.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![illustrazione che mostra quattro barre colorate, quindi le stesse barre con colori diversi](images/colortrans2.png)

<span data-ttu-id="b4d8c-122">Nella tabella seguente sono elencati i vettori di colore per le quattro barre prima e dopo la traduzione rossa.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="b4d8c-123">Si noti che poiché il valore massimo per un componente colore è 1, il componente rosso nella seconda riga non cambia.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="b4d8c-124">Analogamente, il valore minimo per un componente colore è 0.</span><span class="sxs-lookup"><span data-stu-id="b4d8c-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="b4d8c-125">Originale</span><span class="sxs-lookup"><span data-stu-id="b4d8c-125">Original</span></span>           | <span data-ttu-id="b4d8c-126">Convertito</span><span class="sxs-lookup"><span data-stu-id="b4d8c-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="b4d8c-127">Nero (0, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="b4d8c-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="b4d8c-129">Rosso (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="b4d8c-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="b4d8c-131">Verde (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="b4d8c-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="b4d8c-133">Blu (0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="b4d8c-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="b4d8c-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



