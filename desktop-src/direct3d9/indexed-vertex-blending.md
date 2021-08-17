---
description: La fusione dei vertici indicizzata estende il supporto della fusione dei vertici in Direct3D per consentire l'uso di matrici per la fusione.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Blending vertici indicizzati (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3d45e3ff72a33cd21265d1e4aa25e237e2a73e473914898d5c1057316d4ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728721"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Blending vertici indicizzati (Direct3D 9)

La fusione dei vertici indicizzata estende il supporto della fusione dei vertici in Direct3D per consentire l'uso di matrici per la fusione. A queste matrici viene fatto riferimento tramite un indice di matrice. Questi indici vengono forniti per vertice e fanno riferimento a una tavolozza con un massimo di 256 matrici. Ogni indice è di 8 bit e ogni vertice può avere fino a quattro indici, che consentono la fusione di quattro matrici per vertice. Gli indici vengono suddivisi in un valore DWORD. Poiché gli indici vengono specificati per vertice, un massimo di 12 matrici può influire su un singolo triangolo e qualsiasi matrice nella tavolozza può influire sui vertici di una chiamata di disegno. Questo approccio presenta i vantaggi seguenti.

-   Consente a più matrici di influire su un singolo triangolo.
-   Consente di passare più triangoli misti nella stessa chiamata di disegno.
-   Rende la fusione dei vertici indipendente dall'indice del triangolo. In questo modo le mesh progressive possono funzionare in combinazione con la fusione dei vertici.

Uno svantaggio di questo approccio è che non funziona con primitive di superficie curva quando si verifica la sfasatura prima dell'elaborazione dei vertici.

Il diagramma seguente illustra come quattro matrici possono influire su un vertice. Ogni vertice ha fino a quattro indici, quindi è possibile unire quattro matrici per vertice. Il diagramma usa le matrici indicizzate in corrispondenza di 0, 2, 5 e 6.

![diagramma della fusione dei vertici indicizzati tramite 4 di 256 matrici disponibili](images/dword1.png)

Il diagramma seguente illustra in che modo fino a 12 matrici possono influire su un triangolo. L'uso di indici specificati per vertice può influire sul triangolo fino a 12 matrici.

![diagramma della fusione dei vertici indicizzati per un triangolo usando 12 delle 256 matrici disponibili](images/dword2.png)

L'equazione seguente determina il caso generale dell'effetto delle matrici su un vertice.

![equazione della fusione dei vertici indicizzati](images/indexedvblend.png)

Il modello V <sub>è</sub> la posizione del vertice dello spazio del modello di input. Index0.. Index3 sono gli indici della matrice per vertice, suddivisi in un valore DWORD. M \[ \] è la matrice di matrici di mondo in cui vengono indicizzate. b₀.. b è il peso della blend. V<sub>world è</sub> la posizione del vertice dello spazio del mondo di output.

Per altre informazioni sulla fusione dei vertici indicizzata, vedere [Using Indexed Vertex Blending (Direct3D 9) (Uso della fusione dei vertici indicizzata (Direct3D 9).](using-indexed-vertex-blending.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Blending geometrico](geometry-blending.md)
</dt> </dl>

 

 



