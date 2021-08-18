---
description: Un'ellisse viene specificata dal rettangolo di delimitazione. La figura seguente mostra un'ellisse insieme al rettangolo di delimitazione.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellissi e archi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadd0a34107681d2d155ead5d4f80b7208b8926603f21fa4541d502886edaf73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036749"
---
# <a name="ellipses-and-arcs"></a>Ellissi e archi

Un'ellisse viene specificata dal rettangolo di delimitazione. La figura seguente mostra un'ellisse insieme al rettangolo di delimitazione.

![illustrazione di un'ellisse racchiusa all'interno di un rettangolo di delimitazione](images/aboutgdip02-art05.png)

Per disegnare un'ellisse, sono necessari [**un oggetto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) **L'oggetto Graphics** fornisce il [metodo DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) e l'oggetto **Pen** archivia gli attributi dell'ellisse, ad esempio lo spessore della linea e il colore. L'indirizzo **dell'oggetto Pen** viene passato come uno degli argomenti al metodo DrawEllipse. Gli argomenti rimanenti passati al metodo DrawEllipse specificano il rettangolo di delimitazione per l'ellisse. Nell'esempio seguente viene disegnata un'ellisse. il rettangolo di delimitazione ha una larghezza di 160, un'altezza di 80 e un angolo superiore sinistro di (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) è un metodo di overload della [**classe Graphics,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) quindi è possibile specificarlo in diversi modi con argomenti. Ad esempio, è possibile costruire un [**oggetto Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) e passare un riferimento all'oggetto **Rect** come argomento al metodo DrawEllipse.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Un arco è una parte di un'ellisse. Per disegnare un arco, chiamare il [metodo DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) della [**classe**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. I parametri del metodo DrawArc sono gli stessi dei parametri del metodo [DrawEllipse,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) ad eccezione del fatto che DrawArc richiede un angolo iniziale e un angolo di sweep. Nell'esempio seguente viene disegnato un arco con un angolo iniziale di 30 gradi e un angolo di sweep di 180 gradi.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



La figura seguente mostra l'arco, l'ellisse e il rettangolo di delimitazione.

![illustrazione di un'ellisse all'interno di un rettangolo di delimitazione; la metà inferiore sinistra dell'ellisse viene disegnata in rosso](images/aboutgdip02-art06.png)

 

 



