---
description: L'applicazione esegue in genere il rendering delle scene 3D in modo più realistico se usa mappe di luce colorata. Una mappa di luce colorata usa i dati RGB nella mappa di luce per le informazioni sull'illuminazione.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Colore chiaro Mappe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbff9fe246131fc90bda8ac9b5f1c49cd2413c412a7b3da5c013b1e936aa6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989301"
---
# <a name="color-light-maps-direct3d-9"></a>Colore chiaro Mappe (Direct3D 9)

L'applicazione esegue in genere il rendering delle scene 3D in modo più realistico se usa mappe di luce colorata. Una mappa di luce colorata usa i dati RGB nella mappa di luce per le informazioni sull'illuminazione.

L'esempio di codice C++ seguente illustra il mapping della luce con i dati di colore RGB.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



Questo esempio imposta la mappa di luce come prima trama. Imposta quindi lo stato della prima fase di fusione per modulare i dati della trama in ingresso. Usa la prima trama e il colore corrente della primitiva come argomenti per l'operazione di modulazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping di luce con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



