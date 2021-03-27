---
description: Nelle sezioni seguenti vengono descritte alcune delle nuove funzionalità di Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Nuove funzioni e caratteristiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751338"
---
# <a name="new-features"></a>Nuove funzioni e caratteristiche

Nelle sezioni seguenti vengono descritte alcune delle nuove funzionalità di Windows GDI+.

-   [Pennelli sfumatura](#gradient-brushes)
-   [Spline cardinali](#cardinal-splines)
-   [Oggetti Path indipendenti](#independent-path-objects)
-   [Trasformazioni e oggetto Matrix](#transformations-and-the-matrix-object)
-   [Aree scalabili](#scalable-regions)
-   [Fusione alfa](#alpha-blending)
-   [Supporto per più formati di immagine](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pennelli sfumatura

GDI+ si espande in Windows Graphics Device Interface (GDI) fornendo pennelli sfumatura lineare e sfumatura tracciato per riempire forme, percorsi e aree. I pennelli sfumatura possono essere usati anche per tracciare linee, curve e percorsi. Quando si riempie una forma con un pennello sfumato lineare, il colore cambia gradualmente man mano che ci si sposta attraverso la forma. Si supponga, ad esempio, di creare un pennello a sfumatura orizzontale specificando il blu sul bordo sinistro di una forma e il verde sul bordo destro. Quando si riempie la forma con il pennello sfumato orizzontale, il passaggio passa dal blu al verde mentre si passa dal bordo sinistro al bordo destro. Analogamente, una forma riempita con un pennello a sfumatura verticale cambierà il colore durante lo spostamento dall'alto verso il basso. Nella figura seguente è illustrata un'ellisse riempita con un pennello sfumato orizzontale e un'area riempita con un pennello sfumato diagonale.

![illustrazione di una forma riempita da una sfumatura orizzontale e di una forma archiviata da una sfumatura diagonale](images/aboutgdip01-art01.png)

Quando si riempie una forma con un pennello sfumatura percorso, sono disponibili diverse opzioni per specificare il modo in cui i colori cambiano quando si passa da una parte della forma a un'altra. Un'opzione consiste nel disporre di un colore centrale e di un colore limite in modo che i pixel cambino gradualmente da un colore all'altro mentre si passa dal centro della forma verso i bordi esterni. La figura seguente mostra un percorso (creato da una coppia di spline di Bézier) riempito con un pennello sfumatura tracciato.

![illustrazione di una forma simile a un segno di infinito, riempita da blu dove le metà si incontrano per Aqua sui bordi](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Spline di tipo Cardinal

GDI+ supporta le spline cardinalhe, che non sono supportate in GDI. Una spline di tipo Cardinal è una sequenza di curve singole Unite per formare una curva più grande. La spline viene specificata da una matrice di punti e passa attraverso ogni punto della matrice. Una spline cardinale passa senza intoppi (nessun angolo acuto) attraverso ogni punto della matrice e pertanto è più raffinato rispetto a un tracciato creato connettendo linee rette. Nella figura seguente vengono illustrati due percorsi, uno creato connettendo linee rette e uno creato come spline di cardinalità.

![illustrazione che Mostra gli stessi cinque punti due volte: una volta connessi tramite una spline Cardinal, l'altra per segmenti di linea](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Oggetti Path indipendenti

In GDI un percorso appartiene a un contesto di dispositivo e il percorso viene eliminato mentre viene disegnato. Con GDI+, il disegno viene eseguito da un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ed è possibile creare e gestire diversi oggetti [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) distinti dall'oggetto **Graphics** . Un oggetto **GraphicsPath** non viene eliminato definitivamente dall'azione di disegno, pertanto è possibile utilizzare lo stesso oggetto **GraphicsPath** per tracciare più volte un percorso.

## <a name="transformations-and-the-matrix-object"></a>Trasformazioni e oggetto Matrix

GDI+ fornisce l'oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , uno strumento potente che rende semplice e flessibile le trasformazioni (rotazioni, traduzioni e così via). Un oggetto Matrix funziona insieme agli oggetti che vengono trasformati. Un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , ad esempio, dispone di un metodo [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) che riceve l'indirizzo di un oggetto **Matrix** come argomento. Una singola matrice da 3 × 3 può archiviare una trasformazione o una sequenza di trasformazioni. Nella figura seguente viene illustrato un percorso prima e dopo una sequenza di due trasformazioni (prima scala, quindi ruota).

![illustrazione che mostra il contorno di una forma, quindi lo stesso contorno, ma più ristretto e ruotato](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Aree scalabili

GDI+ si espande molto in GDI con il supporto per le aree. In GDI le aree vengono archiviate in coordinate del dispositivo e l'unica trasformazione che può essere applicata a un'area è una traduzione. GDI+ archivia le aree in coordinate internazionali e consente a un'area di subire qualsiasi trasformazione (ad esempio, ridimensionamento) che può essere archiviata in una matrice di trasformazione. Nella figura seguente viene illustrata un'area prima e dopo una sequenza di tre trasformazioni: scala, ruota e Traduci.

![illustrazione che mostra una forma centrata sugli assi della coordinata, quindi la stessa forma ma più grande, ruotata e convertita a destra](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Fusione alfa

Si noti che nella figura precedente è possibile visualizzare l'area non trasformata (piena di rosso) tramite l'area trasformata (riempita con un pennello di tratteggio). Questa operazione è resa possibile dalla fusione alfa, supportata da GDI+. Con la fusione alfa è possibile specificare la trasparenza di un colore di riempimento. Un colore trasparente viene mescolato con il colore di sfondo, più trasparente si crea un colore di riempimento, più lo sfondo viene visualizzato. Nella figura seguente sono illustrati quattro ellissi riempiti con lo stesso colore (rosso) a diversi livelli di trasparenza.

![illustrazione che mostra quattro puntini di sospensione di una trasparenza variabile sovrapposta a un rettangolo semi-trasparente](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Supporto per più formati di immagine

GDI+ fornisce le classi [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , che consentono di caricare, salvare e modificare le immagini in diversi formati. Sono supportati i formati seguenti:

-   BMP
-   Graphics Interchange Format (GIF)
-   JPEG
-   Exif
-   PNG
-   TIFF
-   ICONA
-   WMF
-   EMF

 

 



