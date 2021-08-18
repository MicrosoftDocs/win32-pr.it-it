---
description: Quando sono illuminate da una sorgente di luce, le superfici opace visualizzano una riflessione diffusa della luce.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Luce diffusa Mappe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fc2b5054a30bf8df703941b3cedf0810c378a5fb459d8c5783bb295ff9abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044449"
---
# <a name="diffuse-light-maps-direct3d-9"></a>Luce diffusa Mappe (Direct3D 9)

Quando sono illuminate da una sorgente di luce, le superfici opace visualizzano una riflessione diffusa della luce. La luminosità della luce diffusa dipende dalla distanza dalla sorgente di luce e dall'angolo tra la normale della superficie e il vettore di direzione della sorgente di luce. Gli effetti di illuminazione diffusa simulati dai calcoli di illuminazione producono solo effetti generali.

L'applicazione può simulare un'illuminazione diffusa più complessa con mappe di luce trama. A tale scopo, aggiungere la mappa di luce diffusa alla trama di base, come illustrato nell'esempio di codice C++seguente.


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

[Mapping di luce con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



