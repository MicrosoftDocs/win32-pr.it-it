---
description: La modalità di ombreggiatura utilizzata per eseguire il rendering di un poligono ha un effetto profondo sull'aspetto. Le modalità di ombreggiatura determinano l'intensità del colore e dell'illuminazione in qualsiasi punto su una faccia poligonale. Direct3D supporta due modalità di ombreggiatura.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modalità di ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556414"
---
# <a name="shading-modes-direct3d-9"></a>Modalità di ombreggiatura (Direct3D 9)

La modalità di ombreggiatura utilizzata per eseguire il rendering di un poligono ha un effetto profondo sull'aspetto. Le modalità di ombreggiatura determinano l'intensità del colore e dell'illuminazione in qualsiasi punto su una faccia poligonale. Direct3D supporta due modalità di ombreggiatura.

-   [Ombreggiatura flat](#flat-shading)
-   [Ombreggiatura Gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Ombreggiatura flat

Nella modalità di ombreggiatura flat la pipeline di rendering Direct3D esegue il rendering di un poligono, utilizzando il colore del materiale del poligono al primo vertice come colore per l'intero poligono. gli oggetti 3D di cui viene eseguito il rendering con ombreggiatura piatta hanno bordi visibilmente nitidi tra i poligoni se non sono complanari.

Nell'illustrazione seguente viene mostrata una teiera con ombreggiatura piatta. Il contorno di ogni poligono è chiaramente visibile. L'ombreggiatura piatta è la forma più veloce di ombreggiatura.

![illustrazione di una teiera usando l'ombreggiatura piatta](images/flattea.png)

## <a name="gouraud-shading"></a>Ombreggiatura Gouraud

Quando Direct3D esegue il rendering di un poligono usando l'ombreggiatura Gouraud, calcola un colore per ogni vertice usando i parametri di illuminazione e normale del vertice. Esegue quindi l'interpolazione del colore sulla superficie dei poligoni. l'interpolazione viene eseguita in modo lineare. Se, ad esempio, il componente rosso del colore del vertice 1 è 0,8 e il componente rosso del vertice 2 è 0,4, usando la modalità di ombreggiatura Gouraud e il modello di colore RGB, il modulo di illuminazione Direct3D assegna un componente rosso di 0,6 al pixel al punto medio della linea tra questi vertici.

Nella figura seguente viene illustrata l'ombreggiatura Gouraud. Questa teiera è costituita da molti poligoni triangolari bidimensionali. Tuttavia, l'ombreggiatura Gouraud fa sì che la superficie dell'oggetto appaia curva e smussata.

![illustrazione della teiera usando l'ombreggiatura Gouraud](images/gourtea.png)

L'ombreggiatura Gouraud può essere usata anche per visualizzare oggetti con spigoli acuti.

Per altre informazioni, vedere [vettori normali per visi e vertici (Direct3D 9)](face-and-vertex-normal-vectors.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ombreggiatura](shading.md)
</dt> </dl>

 

 



