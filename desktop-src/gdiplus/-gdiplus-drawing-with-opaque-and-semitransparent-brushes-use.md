---
description: Quando si riempie una forma, è necessario passare l'indirizzo di un oggetto Brush a uno dei metodi Fill della classe Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Disegno con pennelli opachi e semitrasparenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131350"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="f5535-103">Disegno con pennelli opachi e semitrasparenti</span><span class="sxs-lookup"><span data-stu-id="f5535-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="f5535-104">Quando si riempie una forma, è necessario passare l'indirizzo di un oggetto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) a uno dei metodi Fill della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f5535-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="f5535-105">L'unico parametro del costruttore [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) è un oggetto [**color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="f5535-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="f5535-106">Per riempire una forma opaca, impostare il componente alfa del colore su 255.</span><span class="sxs-lookup"><span data-stu-id="f5535-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="f5535-107">Per riempire una forma semitrasparente, impostare il componente alfa su un valore qualsiasi compreso tra 1 e 254.</span><span class="sxs-lookup"><span data-stu-id="f5535-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="f5535-108">Quando si riempie una forma semitrasparente, il colore della forma viene sfumato con i colori dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="f5535-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="f5535-109">Il componente alfa specifica il modo in cui vengono combinati la forma e i colori di sfondo. i valori alfa vicini a 0 inseriscono un peso maggiore sui colori di sfondo e i valori alfa vicini a 255 prevalgono più il colore della forma.</span><span class="sxs-lookup"><span data-stu-id="f5535-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="f5535-110">Nell'esempio seguente viene disegnata un'immagine, quindi vengono riempiti tre ellissi che si sovrappongono all'immagine.</span><span class="sxs-lookup"><span data-stu-id="f5535-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="f5535-111">Per la prima ellisse si usa un componente alfa con un valore pari a 255, quindi l'ellisse risulta opaca.</span><span class="sxs-lookup"><span data-stu-id="f5535-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="f5535-112">Per la seconda e la terza ellisse si usa un componente alfa con un valore pari a 128, quindi le ellissi risultano semitrasparenti. L'immagine di sfondo è visibile attraverso le ellissi.</span><span class="sxs-lookup"><span data-stu-id="f5535-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="f5535-113">La chiamata a [**Graphics:: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fa sì che la fusione per la terza ellisse venga eseguita in combinazione con la correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="f5535-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



<span data-ttu-id="f5535-114">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="f5535-114">The following illustration shows the output of the preceding code.</span></span>

![illustrazione che mostra un'immagine sovrapposta da tre ellissi: una opaca, una leggermente trasparente, una molto trasparente](images/compqualellipse.png)

 

 



