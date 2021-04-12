---
description: L'interpolazione di vertici combina due posizioni fornite dall'utente (o normali).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolazione di vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225419"
---
# <a name="vertex-tweening-direct3d-9"></a>Interpolazione di vertici (Direct3D 9)

L'interpolazione di vertici combina due posizioni fornite dall'utente (o normali). L'interpolazione si escludono a vicenda dalla fusione dei vertici con pesi. L'interpolazione viene eseguita prima dell'illuminazione e del ritaglio ed è abilitata impostando D3DRS \_ VERTEXBLEND su D3DVBF \_ tweening. La posizione del vertice risultante viene calcolata in base a quanto segue:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Lo stesso approccio viene usato per il calcolo delle normali. Per altre informazioni, vedere [using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Blending Geometry](geometry-blending.md)
</dt> </dl>

 

 



