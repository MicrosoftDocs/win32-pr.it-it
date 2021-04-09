---
description: Quando illuminato da una sorgente di luce, oggetti lucidi, quelli che usano materiali altamente riflettenti, ricevono evidenziazioni speculari.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Mappe chiare speculari (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876506"
---
# <a name="specular-light-maps-direct3d-9"></a>Mappe chiare speculari (Direct3D 9)

Quando illuminato da una sorgente di luce, oggetti lucidi, quelli che usano materiali altamente riflettenti, ricevono evidenziazioni speculari. In alcuni casi, le evidenziazioni speculari prodotte dal modulo illuminazione non sono accurate. Per produrre un'evidenziazione più accattivante, molte applicazioni Direct3D applicano mappe chiare speculari alle primitive.

Per eseguire il mapping della luce speculare, aggiungere la mappa a luce speculare alla trama della primitiva, quindi modulare (moltiplicare il risultato per) la mappa chiara RGB.

Nell'esempio di codice seguente viene illustrato questo processo in C++.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping chiaro con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



