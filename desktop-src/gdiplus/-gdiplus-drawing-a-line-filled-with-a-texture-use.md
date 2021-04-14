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
# <a name="drawing-a-line-filled-with-a-texture"></a>Disegno di una linea riempita con una trama

Anziché disegnare una linea o una curva con un colore a tinta unita, è possibile disegnare con una trama. Per creare linee e curve con una trama, creare un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e passare l'indirizzo dell'oggetto **TextureBrush** a un costruttore di [**penna**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . L'immagine associata al pennello trama viene utilizzata per affiancare il piano (invisibile) e quando la penna disegna una linea o una curva, il tratto della penna rileva determinati pixel della trama affiancata.

Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Texture1.jpg. Tale immagine viene utilizzata per costruire un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e l'oggetto **TextureBrush** viene utilizzato per costruire un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . La chiamata a [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) disegna l'immagine con l'angolo superiore sinistro in corrispondenza di (0, 0). La chiamata a [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa l'oggetto **Pen** per creare un'ellisse con trama.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



La figura seguente illustra l'immagine e l'ellisse con trama.

![illustrazione che mostra una piccola immagine rettangolare, quindi un segmento di linea ellittica riempito con l'immagine originale](images/pens7.png)

 

 
