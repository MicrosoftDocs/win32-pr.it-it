---
description: È possibile usare il buffer degli stencil per effetti più astratti, ad esempio struttura e silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Contorni e recinti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b5fcf26b3f3cbbe6e051e1a7d8517cc6d69044beb6eaed7f54baef3509a748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563411"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Contorni e recinti (Direct3D 9)

È possibile usare il buffer degli stencil per effetti più astratti, ad esempio struttura e silhouetting.

Se l'applicazione applica una maschera di stencil all'immagine di una primitiva con la stessa forma ma leggermente più piccola, l'immagine risultante contiene solo il contorno della primitiva. L'applicazione può quindi riempire l'area con maschera stencil dell'immagine con un colore a tinta unita, dando alla primitiva un aspetto in rilievo.

Se la maschera di stencil ha le stesse dimensioni e la stessa forma della primitiva di cui si esegue il rendering, l'immagine risultante contiene un foro in cui deve essere la primitiva. L'applicazione può quindi riempire il foro di nero per produrre una parte della primitiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer degli stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



