---
description: Quando si disegna una linea, devi passare l'indirizzo di un oggetto Pen al metodo DrawLine della classe Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Disegno di linee opache e semitrasparenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14cdf31a80be9ac2a0cf61a2a8eb82f530dc3558c876cba9190a79f42ac35baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036759"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Disegno di linee opache e semitrasparenti

Quando si disegna una linea, devi passare l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) al [metodo DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) della [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Uno dei parametri del costruttore **Pen** è un [**oggetto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Per disegnare una linea opaca, impostare il componente alfa del colore su 255. Per disegnare una linea semitrasparente, impostare il componente alfa su un valore qualsiasi compreso tra 1 e 254.

Quando si disegna una linea semitrasparente su uno sfondo, il colore della linea viene sfumato con i colori dello sfondo. Il componente alfa specifica come vengono misti i colori della linea e dello sfondo. I valori alfa vicini a 0 posizionano un peso maggiore sui colori di sfondo e i valori alfa vicini a 255 posizionano più peso sul colore della linea.

Nell'esempio seguente viene disegnata un'immagine e quindi vengono disegnate tre linee che usano l'immagine come sfondo. Per la prima linea si usa un componente alfa con un valore pari a 255, quindi la linea risulta opaca. Per la seconda e la terza linea si usa un componente alfa con un valore pari a 128, quindi le linee risultano semitrasparenti. L'immagine di sfondo è visibile attraverso le linee. La chiamata a [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causa la fusione per la terza riga in combinazione con la correzione gamma.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



La figura seguente mostra l'output del codice precedente.

![illustrazione che mostra un'immagine sovrapposta da tre linee ampie: una opaca, una leggermente trasparente e una molto trasparente](images/compqualline.png)

 

 



