---
description: La modalità di ombreggiatura usata per eseguire il rendering di un poligono ha un effetto sensibile sull'aspetto. Le modalità ombreggiatura determinano l'intensità del colore e dell'illuminazione in qualsiasi punto di un viso poligono. Direct3D supporta due modalità di ombreggiatura.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modalità ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714e9610e1cae344148bf78ef39bc5e8355cb2af6395e3f92a3bc01b87860605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092230"
---
# <a name="shading-modes-direct3d-9"></a>Modalità ombreggiatura (Direct3D 9)

La modalità di ombreggiatura usata per eseguire il rendering di un poligono ha un effetto sensibile sull'aspetto. Le modalità ombreggiatura determinano l'intensità del colore e dell'illuminazione in qualsiasi punto di un viso poligono. Direct3D supporta due modalità di ombreggiatura.

-   [Ombreggiatura piatta](#flat-shading)
-   [Ombreggiatura gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Ombreggiatura piatta

Nella modalità di ombreggiatura piana, la pipeline di rendering Direct3D esegue il rendering di un poligono, usando il colore del materiale poligono nel primo vertice come colore per l'intero poligono. Gli oggetti 3D di cui viene eseguito il rendering con ombreggiatura piatta hanno bordi visibilmente acuti tra i poligoni se non sono coplanari.

Nella figura seguente viene illustrato il rendering di una teiera con ombreggiatura piatta. Il contorno di ogni poligono è chiaramente visibile. L'ombreggiatura piatta è la forma più veloce di ombreggiatura.

![illustrazione di una teiera con ombreggiatura piatta](images/flattea.png)

## <a name="gouraud-shading"></a>Ombreggiatura gouraud

Quando Direct3D esegue il rendering di un poligono usando l'ombreggiatura Gouraud, calcola un colore per ogni vertice usando i parametri normali e di illuminazione dei vertici. Quindi, interpola il colore sul viso dei poligoni L'interpolazione viene eseguita in modo lineare. Ad esempio, se il componente rosso del colore del vertice 1 è 0,8 e il componente rosso del vertice 2 è 0,4, usando la modalità di ombreggiatura Gouraud e il modello di colore RGB, il modulo di illuminazione Direct3D assegna un componente rosso di 0,6 al pixel al punto medio della linea tra questi vertici.

La figura seguente illustra l'ombreggiatura di Gouraud. Questa teiera è costituita da molti poligoni piatte e triangolari. Tuttavia, l'ombreggiatura Gouraud rende la superficie dell'oggetto curva e uniforme.

![illustrazione della teiera usando l'ombreggiatura gouraud](images/gourtea.png)

L'ombreggiatura gouraud può essere usata anche per visualizzare oggetti con bordi acuti.

Per altre informazioni, vedere Vettori normali viso e [vertice (Direct3D 9).](face-and-vertex-normal-vectors.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ombreggiatura](shading.md)
</dt> </dl>

 

 



