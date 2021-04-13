---
description: 'A volte può essere necessario creare una bitmap fuori schermo con le caratteristiche seguenti:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Uso della modalità di composizione per controllare la fusione alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978911"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Uso della modalità di composizione per controllare la fusione alfa

A volte può essere necessario creare una bitmap fuori schermo con le caratteristiche seguenti:

-   I colori hanno valori alfa minori di 255.
-   Quando si crea la bitmap, i colori non vengono combinati con l'alfa.
-   Quando si visualizza la bitmap completata, i colori nella bitmap sono alpha blended con i colori di sfondo sul dispositivo di visualizzazione.

Per creare una bitmap di questo tipo, costruire un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) vuoto e quindi costruire un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su tale bitmap. Impostare la modalità di composizione dell'oggetto **Graphics** su CompositingModeSourceCopy.

Nell'esempio seguente viene creato un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Il codice usa l'oggetto **Graphics** insieme a due pennelli semitrasparenti (alpha = 160) per disegnare sulla bitmap. Il codice riempie un'ellisse rossa e un'ellisse verde usando i pennelli semitrasparenti. L'ellisse verde si sovrappone all'ellisse rossa, ma il verde non viene mescolato con il rosso perché la modalità di composizione dell'oggetto **Graphics** è impostata su CompositingModeSourceCopy.

Successivamente, il codice viene preparato per l'estrazione sullo schermo chiamando [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) e creando un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su un contesto di dispositivo. Il codice disegna la bitmap sullo schermo due volte: una volta su uno sfondo bianco e una volta su uno sfondo a più colori. I pixel nella bitmap che fanno parte dei due ellissi hanno un componente alfa di 160, quindi i puntini di sospensione vengono combinati con i colori di sfondo sullo schermo.


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



Nella figura seguente viene illustrato l'output del codice precedente. Si noti che i puntini di sospensione vengono combinati con lo sfondo, ma non sono combinati tra loro.

![illustrazione che mostra due ellissi colorate in modo diverso, ciascuna delle quali si fonde con lo sfondo multicolore](images/sourcecopy.png)

Nell'esempio di codice precedente è presente l'istruzione seguente:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Se si desidera che i puntini di sospensione vengano combinati tra loro e con lo sfondo, modificare l'istruzione seguente:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



Nella figura seguente viene illustrato l'output del codice modificato.

![uso della modalità di composizione per controllare l'illustrazione della fusione alfa](images/sourceover.png)

 

 



