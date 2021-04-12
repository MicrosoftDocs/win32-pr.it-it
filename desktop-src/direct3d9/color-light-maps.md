---
description: In genere, l'applicazione eseguirà il rendering di scene 3D in maniera più realistica se usa mappe chiare colorate. Una mappa chiara colorata usa i dati RGB nella mappa chiara per le relative informazioni di illuminazione.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Mappe per la luce del colore (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483173"
---
# <a name="color-light-maps-direct3d-9"></a>Mappe per la luce del colore (Direct3D 9)

In genere, l'applicazione eseguirà il rendering di scene 3D in maniera più realistica se usa mappe chiare colorate. Una mappa chiara colorata usa i dati RGB nella mappa chiara per le relative informazioni di illuminazione.

Nell'esempio di codice C++ riportato di seguito viene illustrato il mapping leggero con i dati cromatici RGB.


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



Questo esempio imposta la mappa chiara come prima trama. Imposta quindi lo stato della prima fase di fusione per modulare i dati della trama in ingresso. Usa la prima trama e il colore corrente della primitiva come argomenti dell'operazione di modulazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping chiaro con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



