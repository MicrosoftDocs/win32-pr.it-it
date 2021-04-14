---
description: Anziché disegnare una linea o una curva con un colore a tinta unita, è possibile disegnare con una trama.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Disegno di una linea riempita con una trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979050"
---
# <a name="drawing-a-line-filled-with-a-texture"></a><span data-ttu-id="2c90e-103">Disegno di una linea riempita con una trama</span><span class="sxs-lookup"><span data-stu-id="2c90e-103">Drawing a Line Filled with a Texture</span></span>

<span data-ttu-id="2c90e-104">Anziché disegnare una linea o una curva con un colore a tinta unita, è possibile disegnare con una trama.</span><span class="sxs-lookup"><span data-stu-id="2c90e-104">Instead of drawing a line or curve with a solid color, you can draw with a texture.</span></span> <span data-ttu-id="2c90e-105">Per creare linee e curve con una trama, creare un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e passare l'indirizzo dell'oggetto **TextureBrush** a un costruttore di [**penna**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="2c90e-105">To draw lines and curves with a texture, create a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and pass the address of that **TextureBrush** object to a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor.</span></span> <span data-ttu-id="2c90e-106">L'immagine associata al pennello trama viene utilizzata per affiancare il piano (invisibile) e quando la penna disegna una linea o una curva, il tratto della penna rileva determinati pixel della trama affiancata.</span><span class="sxs-lookup"><span data-stu-id="2c90e-106">The image associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>

<span data-ttu-id="2c90e-107">Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Texture1.jpg.</span><span class="sxs-lookup"><span data-stu-id="2c90e-107">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Texture1.jpg.</span></span> <span data-ttu-id="2c90e-108">Tale immagine viene utilizzata per costruire un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e l'oggetto **TextureBrush** viene utilizzato per costruire un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="2c90e-108">That image is used to construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and the **TextureBrush** object is used to construct a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="2c90e-109">La chiamata a [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) disegna l'immagine con l'angolo superiore sinistro in corrispondenza di (0, 0).</span><span class="sxs-lookup"><span data-stu-id="2c90e-109">The call to [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) draws the image with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="2c90e-110">La chiamata a [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa l'oggetto **Pen** per creare un'ellisse con trama.</span><span class="sxs-lookup"><span data-stu-id="2c90e-110">The call to [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) uses the **Pen** object to draw a textured ellipse.</span></span>


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



<span data-ttu-id="2c90e-111">La figura seguente illustra l'immagine e l'ellisse con trama.</span><span class="sxs-lookup"><span data-stu-id="2c90e-111">The following illustration shows the image and the textured ellipse.</span></span>

![illustrazione che mostra una piccola immagine rettangolare, quindi un segmento di linea ellittica riempito con l'immagine originale](images/pens7.png)

 

 
