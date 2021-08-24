---
description: Spesso i punti specificati per i vertici non corrispondono esattamente ai pixel sullo schermo. In questo caso, Direct3D applica le regole di rasterizzazione dei triangoli per decidere quali pixel applicare a un triangolo specificato.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Regole di rasterizzazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d241248f5a69262129f60fc005582dc5e03b2a6931cf024bc4613d81558cdb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746668"
---
# <a name="rasterization-rules-direct3d-9"></a>Regole di rasterizzazione (Direct3D 9)

Spesso i punti specificati per i vertici non corrispondono esattamente ai pixel sullo schermo. In questo caso, Direct3D applica le regole di rasterizzazione dei triangoli per decidere quali pixel applicare a un triangolo specificato.

-   [Regole di rasterizzazione dei triangoli](#triangle-rasterization-rules)
-   [Regole punto e linea](#point-and-line-rules)
-   [Regole di sprite dei punti](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Regole di rasterizzazione dei triangoli

Direct3D usa una convenzione di riempimento in alto a sinistra per il riempimento della geometria. Si tratta della stessa convenzione usata per i rettangoli in GDI e OpenGL. In Direct3D, il centro del pixel è il punto determinante. Se il centro si trova all'interno di un triangolo, il pixel fa parte del triangolo. I centri pixel sono in corrispondenza di coordinate intere.

Questa descrizione delle regole di rasterizzazione a triangolo usate da Direct3D non si applica necessariamente a tutto l'hardware disponibile. I test possono individuare variazioni secondarie nell'implementazione di queste regole.

La figura seguente mostra un rettangolo il cui angolo superiore sinistro è in corrispondenza di (0, 0) e il cui angolo inferiore destro è in corrispondenza di (5, 5). Questo rettangolo riempie 25 pixel, esattamente come ci si aspetterebbe. La larghezza del rettangolo è definita come destra meno sinistra. L'altezza è definita come inferiore meno la parte superiore.

![Illustrazione di un quadrato numerato diviso in sei righe e colonne](images/pixmap.png)

Nella convenzione di riempimento in alto a sinistra, *top* si riferisce alla posizione verticale degli intervalli orizzontali e *left* fa riferimento alla posizione orizzontale dei pixel all'interno di un intervallo. Un bordo non può essere un bordo superiore a meno che non sia orizzontale. In generale, la maggior parte dei triangoli ha solo bordi sinistro e destro. La figura seguente mostra un bordo superiore e un bordo destro.

![Illustrazione di un quadrato numerato che contiene due triangoli](images/triedge.png)

La convenzione di riempimento in alto a sinistra determina l'azione eseguita da Direct3D quando un triangolo passa attraverso il centro di un pixel. La figura seguente mostra due triangoli, uno in corrispondenza di (0, 0), (5, 0) e (5, 5) e l'altro in (0, 5), (0, 0) e (5, 5). Il primo triangolo in questo caso ottiene 15 pixel (visualizzati in nero), mentre il secondo ottiene solo 10 pixel (visualizzati in grigio) perché il bordo condiviso è il bordo sinistro del primo triangolo.

![Illustrazione di un quadrato numerato che mostra due triangoli](images/twotris.png)

Se si definisce un rettangolo con l'angolo superiore sinistro in corrispondenza di (0,5, 0,5) e l'angolo inferiore destro in corrispondenza di (2.5, 4.5), il punto centrale del rettangolo è in corrispondenza di (1,5, 2,5). Quando il rasterizzatore Direct3D tessella questo rettangolo, il centro di ogni pixel si trova in modo non ambiguo all'interno di ognuno dei quattro triangoli e la convenzione di riempimento in alto a sinistra non è necessaria. La figura seguente illustra questa operazione. I pixel nel rettangolo vengono etichettati in base al triangolo in cui Direct3D li include.

![Mostra un quadrato numerato contenente un rettangolo diviso in quattro triangoli.](images/noambig.png)

Se si sposta il rettangolo nell'illustrazione precedente in modo che l'angolo superiore sinistro sia a (1.0, 1.0), l'angolo inferiore destro in corrispondenza di (3.0, 5.0) e il relativo punto centrale in (2.0, 3.0), Direct3D applica la convenzione di riempimento in alto a sinistra. La maggior parte dei pixel di questo rettangolo si esercite sul bordo tra due o più triangoli, come illustrato nella figura seguente.

![Illustrazione di un quadrato numerato che contiene un rettangolo diviso in quattro triangoli](images/fillrule.png)

Per entrambi i rettangoli vengono interessati gli stessi pixel, come illustrato nella figura seguente.

![illustrazione dei pixel interessati dai due quadrati numerati precedenti](images/samepix.png)

## <a name="point-and-line-rules"></a>Regole punto e linea

Il rendering dei punti viene eseguito come gli sprite dei punti, entrambi sottoposti a rendering come quadrilaterali allineati allo schermo e quindi conformi alle stesse regole del rendering dei poligoni.

Le regole di rendering delle righe non antialias sono esattamente uguali a quelle per le [righe GDI.](../gdi/lines.md)

Per informazioni sul rendering della riga con antialias, vedere [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Regole di sprite dei punti

Gli sprite di punti e le primitive patch vengono rasterizzati come se le primitive fossero suddivise per la prima volta in triangoli e i triangoli risultanti fossero rasterizzati. Per altre informazioni, vedere [Point Sprites (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
