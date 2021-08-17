---
description: Alcune schede di acceleratore 3D precedenti non supportano la fusione delle trame usando il valore alfa del pixel di destinazione.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Monochrome Light Mappe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac6f62aaba08ac6c8e1116a0bc5059fed3dea19da51d83b034bfae79653ed5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728238"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Monochrome Light Mappe (Direct3D 9)

Alcune schede di acceleratore 3D precedenti non supportano la fusione delle trame usando il valore alfa del pixel di destinazione. Per [altre informazioni, vedere Alpha Texture Blending (Direct3D 9) (Fusione](alpha-texture-blending.md) di trame alfa - Direct3D 9). Questi adattatori in genere non supportano anche la fusione di più trame. Se l'applicazione è in esecuzione su un adattatore come questo, può usare la fusione di trame multipass per eseguire il mapping di luce monocromatica.

Per eseguire il mapping di luce monocromatica, un'applicazione archivia le informazioni di illuminazione nei dati alfa delle trame della mappa di luce. L'applicazione usa le funzionalità di filtro della trama di Direct3D per eseguire un mapping da ogni pixel nell'immagine della primitiva a un texel corrispondente nella mappa di luce. Imposta il fattore di fusione di origine sul valore alfa del texel corrispondente.

L'esempio seguente illustra come un'applicazione può usare una trama come mappa di luce monocromatica:


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



Poiché gli adattatori di visualizzazione che non supportano la fusione alfa di destinazione in genere non supportano la fusione di più trame, questo esempio imposta la mappa di luce come prima trama, disponibile in tutte le schede di acceleratore 3D. Il codice di esempio imposta l'operazione di colore per la fase di fusione della trama per unire i dati della trama con il colore esistente della primitiva. Seleziona quindi la prima trama e il colore esistente della primitiva come dati di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping di luce con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



