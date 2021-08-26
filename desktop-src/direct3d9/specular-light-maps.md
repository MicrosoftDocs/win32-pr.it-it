---
description: Quando sono illuminati da una sorgente di luce, gli oggetti luminosi, quelli che usano materiali altamente riflettenti, ricevono evidenziazioni speculari.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Luce speculare Mappe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05362eb4c0b79ebb980a6c0acb1607713765a446c0ef27823ae0e648cef88d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026101"
---
# <a name="specular-light-maps-direct3d-9"></a>Luce speculare Mappe (Direct3D 9)

Quando sono illuminati da una sorgente di luce, gli oggetti luminosi, quelli che usano materiali altamente riflettenti, ricevono evidenziazioni speculari. In alcuni casi, le evidenziazioni speculari prodotte dal modulo di illuminazione non sono accurate. Per produrre un'evidenziazione più accattivante, molte applicazioni Direct3D applicano mappe di luce speculare alle primitive.

Per eseguire il mapping della luce speculare, aggiungere la mappa di luce speculare alla trama della primitiva, quindi modulare (moltiplicare il risultato per) la mappa di luce RGB.

L'esempio di codice seguente illustra questo processo in C++.


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

[Mapping di luce con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



