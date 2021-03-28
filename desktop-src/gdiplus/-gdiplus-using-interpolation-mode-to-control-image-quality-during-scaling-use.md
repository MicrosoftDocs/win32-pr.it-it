---
description: La modalità di interpolazione di un oggetto Graphics influisce sul modo in cui Windows GDI+ ridimensiona (estende e compatta) le immagini.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Uso della modalità di interpolazione per controllare la qualità dell'immagine durante il ridimensionamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977530"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="35df9-103">Uso della modalità di interpolazione per controllare la qualità dell'immagine durante il ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="35df9-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="35df9-104">La modalità di interpolazione di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influisce sul modo in cui Windows GDI+ ridimensiona (estende e compatta) le immagini.</span><span class="sxs-lookup"><span data-stu-id="35df9-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="35df9-105">L'enumerazione [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) in Gdiplusenums. h definisce diverse modalità di interpolazione, alcune delle quali sono mostrate nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="35df9-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="35df9-106">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="35df9-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="35df9-107">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="35df9-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="35df9-108">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="35df9-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="35df9-109">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="35df9-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="35df9-110">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="35df9-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="35df9-111">Per estendere un'immagine, è necessario eseguire il mapping di ogni pixel nell'immagine originale a un gruppo di pixel nell'immagine più grande.</span><span class="sxs-lookup"><span data-stu-id="35df9-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="35df9-112">Per compattare un'immagine, è necessario eseguire il mapping dei gruppi di pixel nell'immagine originale a singoli pixel nell'immagine più piccola.</span><span class="sxs-lookup"><span data-stu-id="35df9-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="35df9-113">L'efficacia degli algoritmi che eseguono questi mapping determina la qualità di un'immagine ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="35df9-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="35df9-114">Gli algoritmi che producono immagini con scalabilità di qualità superiore tendono a richiedere più tempo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="35df9-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="35df9-115">Nell'elenco precedente InterpolationModeNearestNeighbor è la modalità di qualità più bassa e InterpolationModeHighQualityBicubic è la modalità di qualità più elevata.</span><span class="sxs-lookup"><span data-stu-id="35df9-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="35df9-116">Per impostare la modalità di interpolazione, passare uno dei membri dell'enumerazione [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) al metodo **SetInterpolationMode** di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="35df9-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="35df9-117">Nell'esempio seguente viene disegnata un'immagine, quindi viene compattata l'immagine con tre diverse modalità di interpolazione:</span><span class="sxs-lookup"><span data-stu-id="35df9-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="35df9-118">La figura seguente illustra l'immagine originale e le tre immagini più piccole.</span><span class="sxs-lookup"><span data-stu-id="35df9-118">The following illustration shows the original image and the three smaller images.</span></span>

![illustrazione che mostra un'immagine originale di grandi dimensioni e le tre immagini più piccole di qualità variabile](images/grapes1.png)

 

 



