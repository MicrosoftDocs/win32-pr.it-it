---
description: La fusione di vertici indicizzati estende il supporto per la fusione dei vertici in Direct3D per consentire l'utilizzo di matrici per la fusione.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Fusione di vertici indicizzati (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480716"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Fusione di vertici indicizzati (Direct3D 9)

La fusione di vertici indicizzati estende il supporto per la fusione dei vertici in Direct3D per consentire l'utilizzo di matrici per la fusione. A queste matrici viene fatto riferimento tramite un indice della matrice. Questi indici vengono forniti in base ai singoli vertici e fanno riferimento a una tavolozza di un massimo di 256 matrici. Ogni indice è a 8 bit e ogni vertice può avere un massimo di quattro indici, che consente di unire quattro matrici per ogni vertice. Gli indici vengono compressi in un valore DWORD. Poiché gli indici vengono specificati per ogni vertice, fino a 12 matrici possono influire su un singolo triangolo e qualsiasi matrice nella tavolozza può influire sui vertici di una chiamata di progetto. Questo approccio offre i vantaggi seguenti.

-   Consente a più matrici di influenzare un singolo triangolo.
-   Consente di passare triangoli più Blend nella stessa chiamata di progetto.
-   Rende la fusione dei vertici indipendente dagli indici dei triangoli. In questo modo, le mesh progressive funzionano insieme alla fusione dei vertici.

Uno svantaggio di questo approccio è che non funziona con le primitive di superficie curva quando si verifica il mosaico prima dell'elaborazione del vertice.

Il diagramma seguente illustra il modo in cui quattro matrici possono influenzare un vertice. Ogni vertice è costituito da un massimo di quattro indici, pertanto quattro matrici possono essere combinate per ogni vertice. Il diagramma usa le matrici indicizzate a 0, 2, 5 e 6.

![diagramma della fusione dei vertici indicizzati con 4 di 256 matrici disponibili](images/dword1.png)

Il diagramma seguente illustra il modo in cui fino a 12 matrici possono influenzare un triangolo. Utilizzando gli indici specificati per ogni vertice, fino a 12 matrici possono influire sul triangolo.

![diagramma della fusione dei vertici indicizzati per un triangolo usando 12 di 256 matrici disponibili](images/dword2.png)

L'equazione seguente determina il caso generale per il modo in cui le matrici hanno effetto su un vertice.

![equazione della fusione dei vertici indicizzati](images/indexedvblend.png)

V <sub>Model</sub> è la posizione del vertice dello spazio del modello di input. Index0.. Index3 sono gli indici di matrice per vertice compressi in un valore DWORD. M \[ \] è la matrice di matrici globali che vengono indicizzate in. b ₀.. b ₂ sono i pesi di Blend. V<sub>World</sub> è la posizione del vertice dello spazio globale di output.

Per altre informazioni sulla combinazione di vertici indicizzati, vedere [uso della combinazione di vertici indicizzati (Direct3D 9)](using-indexed-vertex-blending.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Blending Geometry](geometry-blending.md)
</dt> </dl>

 

 



