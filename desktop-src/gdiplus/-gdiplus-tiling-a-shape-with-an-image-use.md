---
description: Così come i riquadri possono essere posizionati uno accanto all'altro per coprire un pavimento, le immagini rettangolari possono essere posizionate l'una accanto all'altra per riempire (affiancare) una forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Affiancamento di una forma con un'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129062"
---
# <a name="tiling-a-shape-with-an-image"></a>Affiancamento di una forma con un'immagine

Così come i riquadri possono essere posizionati uno accanto all'altro per coprire un pavimento, le immagini rettangolari possono essere posizionate l'una accanto all'altra per riempire (affiancare) una forma. Per affiancare l'interno di una forma, utilizzare un pennello di trama. Quando si crea un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , uno degli argomenti passati al costruttore è l'indirizzo di un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) . Quando si usa il pennello trama per disegnare l'interno di una forma, la forma viene riempita con copie ripetute dell'immagine.

La proprietà modalità a capo dell'oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina il modo in cui l'immagine è orientata mentre viene ripetuta in una griglia rettangolare. È possibile fare in modo che tutti i riquadri nella griglia abbiano lo stesso orientamento oppure è possibile far passare l'immagine da una posizione della griglia a quella successiva. Il capovolgimento può essere orizzontale, verticale o entrambi. Gli esempi seguenti illustrano l'affiancamento con tipi diversi di capovolgimento.

## <a name="tiling-an-image"></a>Affiancamento di un'immagine

Questo esempio usa l'immagine 75 × 75 seguente per affiancare un rettangolo 200 × 200:

![illustrazione utilizzata come base di altre illustrazioni in questo argomento: una casa e un albero sullo sfondo e centrato in un rettangolo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato all'immagine. Si noti che tutti i riquadri hanno lo stesso orientamento; Nessun capovolgimento.

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente e verticalmente in un rettangolo di grandi dimensioni](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a>Capovolgimento orizzontale di un'immagine durante l'affiancamento

Questo esempio usa un'immagine 75 × 75 per riempire un rettangolo 200 × 200. La modalità a capo automatico è impostata per capovolgere orizzontalmente l'immagine.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato all'immagine. Si noti che quando si passa da un riquadro all'altro in una determinata riga, l'immagine viene capovolta orizzontalmente.

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente, ma le istanze con numerazione uniforme vengono invertite orizzontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a>Capovolgimento verticale di un'immagine durante l'affiancamento

Questo esempio usa un'immagine 75 × 75 per riempire un rettangolo 200 × 200. La modalità Wrap è impostata per capovolgere l'immagine verticalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato all'immagine. Si noti che quando si passa da un riquadro all'altro in una colonna specificata, l'immagine viene capovolta verticalmente.

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente e verticalmente, ma le righe con numerazione uniforme vengono invertite verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a>Capovolgimento orizzontale e verticale di un'immagine durante l'affiancamento

Questo esempio usa un'immagine 75 × 75 per affiancare un rettangolo 200 × 200. La modalità a capo è impostata per capovolgere l'immagine sia orizzontalmente che verticalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato dall'immagine. Si noti che quando si passa da un riquadro all'altro in una determinata riga, l'immagine viene capovolta orizzontalmente e quando si passa da un riquadro all'altro in una colonna specificata, l'immagine viene capovolta verticalmente.

![illustrazione che mostra le istanze alternate dell'immagine di base in ogni riga viene capovolta orizzontalmente e le righe alternate vengono capovolte verticalmente.](images/tile5.png)

 

 



