---
description: È possibile utilizzare il buffer dello stencil per gli effetti più astratti, ad esempio la struttura e silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Strutture e sagome (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745535"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Strutture e sagome (Direct3D 9)

È possibile utilizzare il buffer dello stencil per gli effetti più astratti, ad esempio la struttura e silhouetting.

Se l'applicazione applica una maschera di stencil all'immagine di una primitiva che ha la stessa forma ma leggermente più piccola, l'immagine risultante contiene solo il contorno della primitiva. L'applicazione può quindi riempire l'area con maschera di stencil dell'immagine con un colore a tinta unita, assegnando alla primitiva un aspetto in rilievo.

Se la maschera dello stencil ha le stesse dimensioni e la stessa forma della primitiva di cui si sta eseguendo il rendering, l'immagine risultante contiene un foro in cui la primitiva deve essere. L'applicazione può quindi riempire il foro con il nero per produrre una silhouette della primitiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer dello stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



