---
description: È possibile riempire una forma chiusa con una trama usando la classe Image e la classe TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Riempimento di una forma con una trama dell'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131342"
---
# <a name="filling-a-shape-with-an-image-texture"></a>Riempimento di una forma con una trama dell'immagine

È possibile riempire una forma chiusa con una trama usando la classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e la classe [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .

Nell'esempio seguente viene riempita un'ellisse con un'immagine. Il codice costruisce un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , quindi passa l'indirizzo di tale oggetto **immagine** come argomento a un costruttore [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) . La terza istruzione di codice ridimensiona l'immagine e la quarta viene riempita dall'ellisse con copie ripetute dell'immagine ridimensionata:


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



Nell'esempio di codice precedente, il metodo [**TextureBrush:: setransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) imposta la trasformazione applicata all'immagine prima che venga disegnata. Si supponga che l'immagine originale abbia una larghezza di 640 pixel e un'altezza di 480 pixel. La trasformazione compatta l'immagine a 75 × 75, impostando i valori di ridimensionamento orizzontale e verticale.

> [!Note]  
> Nell'esempio precedente, la dimensione dell'immagine è 75 × 75 e la dimensione dell'ellisse è 150 × 250. Poiché l'immagine è più piccola dell'ellisse che sta riempiendo, l'ellisse viene affiancata all'immagine. L'affiancamento significa che l'immagine viene ripetuta orizzontalmente e verticalmente fino a quando non viene raggiunto il limite della forma. Per ulteriori informazioni sull'affiancamento, vedere [affiancare una forma con un'immagine](-gdiplus-tiling-a-shape-with-an-image-use.md).

 

 

 



