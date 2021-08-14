---
description: L'interpolazione dei vertici unisce due posizioni fornite dall'utente (o normali).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Tweening vertice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8486f53e4eb1a3a003b15255baeb50d30f0ed205f4259625d7d66ba33e8274c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519222"
---
# <a name="vertex-tweening-direct3d-9"></a>Tweening vertice (Direct3D 9)

L'interpolazione dei vertici unisce due posizioni fornite dall'utente (o normali). L'interpolazione si escludono a vicenda dalla fusione dei vertici con i pesi. L'interpolazione viene eseguita prima dell'illuminazione e del ritaglio e viene abilitata impostando VERTEXBLEND D3DRS \_ su D3DVBF \_ TWEENING. La posizione del vertice risultante viene calcolata da:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Lo stesso approccio viene usato per calcolare le normali. Per altre informazioni, vedere [Uso dell'interpolazione dei vertici (Direct3D 9).](using-vertex-tweening.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione di geometrie](geometry-blending.md)
</dt> </dl>

 

 



