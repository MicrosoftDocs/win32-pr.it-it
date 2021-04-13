---
description: Quando illuminato da una sorgente di luce, le superfici opache visualizzano la reflection chiara diffusa.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Mappe chiare diffuse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481541"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Mappe chiare diffuse (Direct3D 9)

Quando illuminato da una sorgente di luce, le superfici opache visualizzano la reflection chiara diffusa. La luminosità della luce diffusa dipende dalla distanza dalla sorgente di luce e dall'angolo tra la normale della superficie e il vettore di direzione della sorgente di luce. Gli effetti di illuminazione diffusi simulati dai calcoli di illuminazione producono solo effetti generali.

L'applicazione è in grado di simulare un'illuminazione diffusa più complessa con texture Light maps. A tale scopo, aggiungere il mapping della luce diffusa alla trama di base, come illustrato nell'esempio di codice C++ riportato di seguito.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping chiaro con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



