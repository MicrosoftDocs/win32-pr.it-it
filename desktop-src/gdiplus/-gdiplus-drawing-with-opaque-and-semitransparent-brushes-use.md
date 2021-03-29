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
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Disegno con pennelli opachi e semitrasparenti

Quando si riempie una forma, è necessario passare l'indirizzo di un oggetto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) a uno dei metodi Fill della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L'unico parametro del costruttore [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) è un oggetto [**color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) . Per riempire una forma opaca, impostare il componente alfa del colore su 255. Per riempire una forma semitrasparente, impostare il componente alfa su un valore qualsiasi compreso tra 1 e 254.

Quando si riempie una forma semitrasparente, il colore della forma viene sfumato con i colori dello sfondo. Il componente alfa specifica il modo in cui vengono combinati la forma e i colori di sfondo. i valori alfa vicini a 0 inseriscono un peso maggiore sui colori di sfondo e i valori alfa vicini a 255 prevalgono più il colore della forma.

Nell'esempio seguente viene disegnata un'immagine, quindi vengono riempiti tre ellissi che si sovrappongono all'immagine. Per la prima ellisse si usa un componente alfa con un valore pari a 255, quindi l'ellisse risulta opaca. Per la seconda e la terza ellisse si usa un componente alfa con un valore pari a 128, quindi le ellissi risultano semitrasparenti. L'immagine di sfondo è visibile attraverso le ellissi. La chiamata a [**Graphics:: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fa sì che la fusione per la terza ellisse venga eseguita in combinazione con la correzione gamma.


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



Nella figura seguente viene illustrato l'output del codice precedente.

![illustrazione che mostra un'immagine sovrapposta da tre ellissi: una opaca, una leggermente trasparente, una molto trasparente](images/compqualellipse.png)

 

 



