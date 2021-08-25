---
description: Così come le tessere possono essere posizionate una accanto all'altra per coprire un piano, le immagini rettangolari possono essere posizionate una accanto all'altra per riempire (affiancare) una forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Affiancare una forma con un'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fc04439db21191ddc110859ae628e975d50bf617db3da63189859070766b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943771"
---
# <a name="tiling-a-shape-with-an-image"></a>Affiancare una forma con un'immagine

Così come le tessere possono essere posizionate una accanto all'altra per coprire un piano, le immagini rettangolari possono essere posizionate una accanto all'altra per riempire (affiancare) una forma. Per affiancare l'interno di una forma, usare un pennello trama. Quando costruisci un [**oggetto TextureBrush,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) uno degli argomenti passati al costruttore è l'indirizzo di un [**oggetto**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Image. Quando si usa il pennello trama per disegnare l'interno di una forma, la forma viene riempita con copie ripetute di questa immagine.

La proprietà wrap mode [**dell'oggetto TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina come l'immagine viene orientata mentre viene ripetuta in una griglia rettangolare. È possibile fare in modo che tutti i riquadri nella griglia abbia lo stesso orientamento oppure fare in modo che l'immagine si capovolge da una posizione della griglia a quella successiva. Il capovolgimento può essere orizzontale, verticale o entrambi. Gli esempi seguenti illustrano la affiancamento con diversi tipi di capovolgimento.

## <a name="tiling-an-image"></a>Affiancamento di un'immagine

Questo esempio usa l'immagine 75 ×75 seguente per affiancare un rettangolo di 200 ×200:

![illustrazione usata come base di altre illustrazioni in questo argomento: una casa e un albero sullo sfondo e centrate in un rettangolo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



La figura seguente mostra come il rettangolo viene affiancato con l'immagine. Si noti che tutti i riquadri hanno lo stesso orientamento. non è presente alcuna capovolgimento.

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente e verticalmente in un rettangolo di grandi dimensioni](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling&quot;></a>Capovolgimento orizzontale di un'immagine durante la affiancamento

Questo esempio usa un'immagine di 75 ×75 per riempire un rettangolo di 200 ×200. La modalità a capo automatico è impostata per capovolgere orizzontalmente l'immagine.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



La figura seguente mostra come il rettangolo viene affiancato con l'immagine. Si noti che quando si passa da un riquadro a quello successivo in una determinata riga, l'immagine viene capovolta orizzontalmente.

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente, ma le istanze con numeri pari sono invertite orizzontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling&quot;></a>Capovolgimento verticale di un'immagine durante la affiancamento

Questo esempio usa un'immagine di 75 ×75 per riempire un rettangolo di 200 ×200. La modalità a capo automatico è impostata per capovolgere verticalmente l'immagine.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



La figura seguente mostra come il rettangolo viene affiancato con l'immagine. Si noti che quando si passa da un riquadro a quello successivo in una determinata colonna, l'immagine viene capovolta verticalmente.

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente e verticalmente, ma le righe con numeri pari vengono invertite verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling&quot;></a>Capovolgimento orizzontale e verticale di un'immagine durante la affiancamento

Questo esempio usa un'immagine di 75 ×75 per affiancare un rettangolo di 200 ×200. La modalità a capo automatico è impostata per capovolgere l'immagine sia orizzontalmente che verticalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



La figura seguente mostra come il rettangolo viene affiancato dall'immagine. Si noti che quando si passa da un riquadro a quello successivo in una determinata riga, l'immagine viene capovolta orizzontalmente e quando si passa da un riquadro a quello successivo in una determinata colonna, l'immagine viene capovolta verticalmente.

![illustrazione che mostra le istanze alterne dell'immagine di base in ogni riga capovolte orizzontalmente e le righe alterne capovolte verticalmente](images/tile5.png)

 

 



