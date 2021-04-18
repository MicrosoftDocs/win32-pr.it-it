---
description: Alcune schede dei tasti di scelta rapida 3D meno recenti non supportano la combinazione di trame usando il valore alfa del pixel di destinazione.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Mappe chiare monocromatiche (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303801"
---
# <a name="monochrome-light-maps-direct3d-9"></a>Mappe chiare monocromatiche (Direct3D 9)

Alcune schede dei tasti di scelta rapida 3D meno recenti non supportano la combinazione di trame usando il valore alfa del pixel di destinazione. Per ulteriori informazioni, vedere [Alpha texture blending (Direct3D 9)](alpha-texture-blending.md) . Questi adapter, in genere, non supportano la combinazione di più trame. Se l'applicazione è in esecuzione in una scheda, ad esempio, può usare la combinazione di trame MultiPASS per eseguire il mapping chiaro monocromatico.

Per eseguire il mapping chiaro monocromatico, un'applicazione archivia le informazioni di illuminazione nei dati alfa delle trame della mappa chiara. L'applicazione usa le funzionalità di filtro della trama di Direct3D per eseguire un mapping da ogni pixel nell'immagine della primitiva a un Texel corrispondente nella mappa chiara. Imposta il fattore di fusione di origine sul valore alfa del Texel corrispondente.

Nell'esempio seguente viene illustrato il modo in cui un'applicazione può utilizzare una trama come mappa chiara monocromatica:


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



Poiché gli adattatori di visualizzazione che non supportano la fusione alfa di destinazione in genere non supportano la combinazione di più trame, in questo esempio viene impostata la mappa chiara come prima trama, disponibile in tutte le schede di accelerazione 3D. Il codice di esempio imposta l'operazione di colore per la fase di fusione della trama per combinare i dati della trama con il colore esistente della primitiva. Quindi seleziona la prima trama e il colore esistente della primitiva come dati di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping chiaro con trame](light-mapping-with-textures.md)
</dt> </dl>

 

 



