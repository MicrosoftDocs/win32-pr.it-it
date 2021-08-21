---
description: Anziché disegnare una linea o una curva con un colore a tinta unita, è possibile disegnare con una trama.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Disegno di una linea riempita con una trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467037"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Disegno di una linea riempita con una trama

Anziché disegnare una linea o una curva con un colore a tinta unita, è possibile disegnare con una trama. Per disegnare linee e curve con una trama, creare un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e passare l'indirizzo di tale oggetto **TextureBrush** a un [**costruttore Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) L'immagine associata al pennello trama viene usata per affiancare il piano (in modo invisibile) e quando la penna disegna una linea o una curva, il tratto della penna individua alcuni pixel della trama affiancata.

Nell'esempio seguente viene creato un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Texture1.jpg. Tale immagine viene usata per costruire un [**oggetto TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) e l'oggetto **TextureBrush** viene usato per costruire un [**oggetto**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Pen. La chiamata a [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) disegna l'immagine con l'angolo superiore sinistro in corrispondenza di (0, 0). La chiamata a [**Graphics::D rawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa **l'oggetto Pen** per disegnare un'ellisse con trama.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



La figura seguente mostra l'immagine e l'ellisse con trama.

![figura che mostra una piccola immagine rettangolare, quindi un segmento di linea ellittica riempito con l'immagine originale](images/pens7.png)

 

 
