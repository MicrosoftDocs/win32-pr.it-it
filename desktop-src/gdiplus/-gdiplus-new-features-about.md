---
description: Le sezioni seguenti descrivono alcune delle nuove funzionalità di Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Nuove funzioni e caratteristiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab303cd00f494e06d7567d93c9698878e02d178a7b4f31d230a4b47cafe279b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014861"
---
# <a name="new-features"></a>Nuove funzioni e caratteristiche

Le sezioni seguenti descrivono alcune delle nuove funzionalità di Windows GDI+.

-   [Pennelli sfumatura](#gradient-brushes)
-   [Spline di tipo Cardinal](#cardinal-splines)
-   [Oggetti percorso indipendente](#independent-path-objects)
-   [Trasformazioni e oggetto Matrix](#transformations-and-the-matrix-object)
-   [Aree scalabili](#scalable-regions)
-   [Fusione alfa](#alpha-blending)
-   [Supporto per più formati di immagine](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pennelli sfumatura

GDI+ si espande su Windows Graphics Device Interface (GDI) fornendo pennelli sfumatura lineare e sfumatura tracciato per il riempimento di forme, tracciati e aree. I pennelli sfumatura possono essere usati anche per disegnare linee, curve e tracciati. Quando si riempie una forma con un pennello sfumato lineare, il colore cambia gradualmente man mano che ci si sposta all'interno della forma. Si supponga, ad esempio, di creare un pennello sfumato orizzontale specificando blu al bordo sinistro di una forma e verde sul bordo destro. Quando si riempie la forma con il pennello sfumato orizzontale, questa cambia gradualmente da blu a verde quando si passa dal bordo sinistro al bordo destro. Analogamente, una forma riempita con un pennello sfumato verticale cambierà colore quando si passa dall'alto verso il basso. La figura seguente mostra un'ellisse riempita con un pennello sfumato orizzontale e un'area riempita con un pennello sfumatura diagonale.

![illustrazione di una forma riempita da una sfumatura orizzontale e una da una sfumatura diagonale](images/aboutgdip01-art01.png)

Quando si riempie una forma con un pennello sfumato tracciato, sono disponibili diverse opzioni per specificare come cambiano i colori quando si passa da una parte della forma a un'altra. Un'opzione è quella di avere un colore centrale e un colore limite in modo che i pixel cambino gradualmente da un colore all'altro man mano che ci si sposta dal centro della forma verso i bordi esterni. La figura seguente mostra un tracciato (creato da una coppia di spline di Bézier) riempito con un pennello sfumatura del tracciato.

![illustrazione di una forma simile a un segno infinito, riempita dal blu dove le metà si incontrano nell'acqua ai bordi](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Spline di tipo Cardinal

GDI+ supporta spline cardinali, che non sono supportate in GDI. Una spline cardinale è una sequenza di singole curve unite per formare una curva più grande. La spline viene specificata da una matrice di punti e passa attraverso ogni punto in tale matrice. Una spline cardinale passa senza problemi (senza angoli acuti) attraverso ogni punto della matrice e quindi è più perfezionata rispetto a un tracciato creato collegando linee rette. La figura seguente mostra due percorsi, uno creato connettendo linee rette e uno creato come spline di tipo cardinale.

![illustrazione che mostra gli stessi cinque punti due volte: una volta connessi da una spline cardinale, l'altro per segmenti di linea](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Oggetti percorso indipendente

In GDI, un percorso appartiene a un contesto di dispositivo e il percorso viene eliminato durante la disegnato. Con GDI+, il disegno viene eseguito da un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ed è possibile creare e gestire diversi oggetti [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) separati dall'oggetto **Graphics.** Un **oggetto GraphicsPath** non viene eliminato in modo eliminato dall'azione di disegno, pertanto è possibile usare lo stesso **oggetto GraphicsPath** per disegnare un tracciato più volte.

## <a name="transformations-and-the-matrix-object"></a>Trasformazioni e oggetto Matrix

GDI+ fornisce [**l'oggetto Matrix,**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) un potente strumento che rende le trasformazioni (rotazioni, traslazioni e così via) semplici e flessibili. Un oggetto matrice funziona in combinazione con gli oggetti trasformati. Ad esempio, un [**oggetto GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) ha un [**metodo GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) che riceve l'indirizzo di un **oggetto Matrix** come argomento. Una singola matrice ×3 può archiviare una trasformazione o una sequenza di trasformazioni. La figura seguente mostra un percorso prima e dopo una sequenza di due trasformazioni (prima scala e quindi rotazione).

![illustrazione che mostra il contorno di una forma, quindi lo stesso contorno, ma più stretto e ruotato](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Aree scalabili

GDI+ si espande notevolmente su GDI con il supporto per le aree. In GDI le aree vengono archiviate in coordinate del dispositivo e l'unica trasformazione che può essere applicata a un'area è una traduzione. GDI+ archivia le aree in coordinate globali e consente a un'area di sottoporsi a qualsiasi trasformazione (ad esempio il ridimensionamento) che può essere archiviata in una matrice di trasformazione. La figura seguente mostra un'area prima e dopo una sequenza di tre trasformazioni: ridimensionamento, rotazione e traslazione.

![illustrazione che mostra una forma centrata sugli assi delle coordinate, quindi la stessa forma ma più grande, ruotata e convertita a destra](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Fusione alfa

Si noti che nella figura precedente è possibile visualizzare l'area non trasformata (riempita di rosso) attraverso l'area trasformata (riempita con un pennello tratteggiato). Ciò è reso possibile dalla fusione alfa, supportata da GDI+. Con la fusione alfa è possibile specificare la trasparenza di un colore di riempimento. Un colore trasparente viene sfumato con il colore di sfondo: più trasparente è il colore di riempimento, più viene visualizzato lo sfondo. La figura seguente mostra quattro puntini di sospensione riempiti con lo stesso colore (rosso) a livelli di trasparenza diversi.

![illustrazione che mostra quattro ellissi di trasparenza variabile sovrapposte a un rettangolo semitrasparente](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Supporto per più formati di immagine

GDI+ fornisce le classi [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**Metafile,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) che consentono di caricare, salvare e modificare le immagini in diversi formati. Sono supportati i formati seguenti:

-   BMP
-   Graphics Interchange Format (GIF)
-   JPEG
-   Exif
-   PNG
-   TIFF
-   Icona
-   WMF
-   EMF

 

 



