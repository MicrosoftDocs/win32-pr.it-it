---
description: Spesso i punti specificati per i vertici non corrispondono esattamente ai pixel sullo schermo. Quando si verifica questa situazione, Direct3D applica le regole di rasterizzazione dei triangoli per decidere quali pixel applicare a un determinato triangolo.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Regole di rasterizzazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234414"
---
# <a name="rasterization-rules-direct3d-9"></a>Regole di rasterizzazione (Direct3D 9)

Spesso i punti specificati per i vertici non corrispondono esattamente ai pixel sullo schermo. Quando si verifica questa situazione, Direct3D applica le regole di rasterizzazione dei triangoli per decidere quali pixel applicare a un determinato triangolo.

-   [Regole di rasterizzazione triangolare](#triangle-rasterization-rules)
-   [Regole per punti e linee](#point-and-line-rules)
-   [Regole sprite punto](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Regole di rasterizzazione triangolare

Direct3D utilizza una convenzione di riempimento in alto a sinistra per riempire la geometria. Si tratta della stessa convenzione utilizzata per i rettangoli in GDI e OpenGL. In Direct3D, il centro del pixel è il punto decisivo. Se il centro si trova all'interno di un triangolo, il pixel fa parte del triangolo. I pixel Center sono coordinate di tipo Integer.

Questa descrizione delle regole di rasterizzazione dei triangolari utilizzate da Direct3D non si applica necessariamente a tutti i componenti hardware disponibili. I test possono individuare variazioni minime nell'implementazione di queste regole.

Nella figura seguente viene illustrato un rettangolo il cui angolo superiore sinistro è (0,0) e il cui angolo inferiore destro è (5, 5). Questo rettangolo riempie 25 pixel, esattamente come ci si aspetterebbe. La larghezza del rettangolo è definita come Right minu Left. L'altezza è definita come inferiore meno in alto.

![illustrazione di un quadrato numerato diviso in sei righe e colonne](images/pixmap.png)

Nella convenzione di riempimento in alto a sinistra, *Top* si riferisce alla posizione verticale degli intervalli orizzontali e a *sinistra* si riferisce alla posizione orizzontale dei pixel all'interno di un intervallo. Un bordo non può essere un bordo superiore a meno che non sia orizzontale. In generale, la maggior parte dei triangoli ha solo bordi sinistro e destro. La figura seguente mostra un bordo superiore e un bordo destro.

![illustrazione di un quadrato numerato che contiene due triangoli](images/triedge.png)

La convenzione di riempimento in alto a sinistra determina l'azione eseguita da Direct3D quando un triangolo passa attraverso il centro di un pixel. Nella figura seguente vengono mostrati due triangoli, uno a (0,0), (5, 0) e (5, 5) e l'altro in (0,5), (0, 0) e (5, 5). Il primo triangolo in questo caso ottiene 15 pixel (visualizzato in nero), mentre il secondo ottiene solo 10 pixel (visualizzati in grigio) perché il bordo condiviso è il bordo sinistro del primo triangolo.

![illustrazione di un quadrato numerato che mostra due triangoli](images/twotris.png)

Se si definisce un rettangolo con l'angolo superiore sinistro in (0,5, 0,5) e l'angolo inferiore destro in (2,5, 4,5), il punto centrale di questo rettangolo è (1,5, 2,5). Quando l'rasterizzatore Direct3D tessellates questo rettangolo, il centro di ogni pixel non è ambiguo all'interno di ognuno dei quattro triangoli e la convenzione di riempimento in alto a sinistra non è necessaria. La figura seguente illustra questa situazione. I pixel nel rettangolo sono contrassegnati in base al triangolo in cui vengono inclusi in Direct3D.

![Mostra un quadrato numerato contenente un rettangolo diviso in quattro triangoli.](images/noambig.png)

Se si sposta il rettangolo nell'illustrazione precedente in modo che l'angolo superiore sinistro si trovi in (1,0, 1,0), nell'angolo inferiore destro in (3,0, 5,0) e nel punto centrale in (2,0, 3,0), Direct3D applica la convenzione di riempimento superiore sinistro. La maggior parte dei pixel in questo rettangolo è a cavalcioni del bordo tra due o più triangoli, come illustrato nella figura seguente.

![illustrazione di un quadrato numerato contenente un rettangolo diviso in quattro triangoli](images/fillrule.png)

Per entrambi i rettangoli, sono interessati gli stessi pixel, come illustrato nella figura seguente.

![illustrazione dei pixel interessati dai due quadrati numerati precedenti](images/samepix.png)

## <a name="point-and-line-rules"></a>Regole per punti e linee

Il rendering dei punti viene eseguito come gli sprite di punti, che vengono entrambi sottoposti a rendering come quadrilateri allineati allo schermo e quindi rispettano le stesse regole del rendering poligono.

Le regole di rendering della linea non con alias sono identiche a quelle per le [righe GDI](../gdi/lines.md).

Per informazioni sul rendering di linee con anti-aliasing, vedere [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Regole sprite punto

Gli sprite di punti e le primitive patch vengono rasterizzati come se le primitive fossero prima tassellati in triangoli e i triangoli risultanti rasterizzati. Per altre informazioni, vedere [punti sprite (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
