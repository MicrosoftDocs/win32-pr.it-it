---
title: Ritaglio e ridimensionamento di immagini GDI+
description: La classe Graphics fornisce diversi metodi DrawImage, alcuni dei quali hanno parametri di origine e di destinazione rettangolari che è possibile usare per ritagliare e ridimensionare le immagini.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987880"
---
# <a name="cropping-and-scaling-gdi-images"></a><span data-ttu-id="9a22e-103">Ritaglio e ridimensionamento di immagini GDI+</span><span class="sxs-lookup"><span data-stu-id="9a22e-103">Cropping and scaling GDI+ images</span></span>

<span data-ttu-id="9a22e-104">La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce diversi metodi **DrawImage** , alcuni dei quali hanno parametri di origine e di destinazione rettangolari che è possibile usare per ritagliare e ridimensionare le immagini.</span><span class="sxs-lookup"><span data-stu-id="9a22e-104">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several **DrawImage** methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>

<span data-ttu-id="9a22e-105">Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Apple.gif.</span><span class="sxs-lookup"><span data-stu-id="9a22e-105">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Apple.gif.</span></span> <span data-ttu-id="9a22e-106">Il codice disegna l'intera immagine Apple nelle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="9a22e-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="9a22e-107">Il codice chiama quindi il metodo **DrawImage** di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare una parte dell'immagine Apple in un rettangolo di destinazione più grande dell'immagine Apple originale.</span><span class="sxs-lookup"><span data-stu-id="9a22e-107">The code then calls the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>

<span data-ttu-id="9a22e-108">Il metodo **DrawImage** determina la parte della mela da creare osservando il rettangolo di origine, specificato dal terzo, dal quarto, dal quinto e dal sesto argomento.</span><span class="sxs-lookup"><span data-stu-id="9a22e-108">The **DrawImage** method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="9a22e-109">In questo caso, la mela viene ritagliata al 75% della larghezza e il 75% dell'altezza.</span><span class="sxs-lookup"><span data-stu-id="9a22e-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>

<span data-ttu-id="9a22e-110">Il metodo **DrawImage** determina la posizione in cui creare la mela ritagliata e la dimensione della mela ritagliata esaminando il rettangolo di destinazione, specificato dal secondo argomento.</span><span class="sxs-lookup"><span data-stu-id="9a22e-110">The **DrawImage** method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="9a22e-111">In questo caso, il rettangolo di destinazione è più grande del 30% e il 30% più alto rispetto all'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="9a22e-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="9a22e-112">La figura seguente mostra l'Apple originale e l'Apple ritagliata e ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="9a22e-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>

![illustrazione che mostra una mela, quindi una parte ingrandita della mela originale](images/cropscale1.png)

 

 



