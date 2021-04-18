---
description: Il motore di illuminazione combina il colore del materiale, il colore del vertice e le informazioni sull'illuminazione per generare un colore per ogni vertice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Fusione di trame alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304996"
---
# <a name="alpha-texture-blending-direct3d-9"></a>Fusione di trame alfa (Direct3D 9)

Il motore di illuminazione combina il colore del materiale, il colore del vertice e le informazioni sull'illuminazione per generare un colore per ogni vertice. Una volta interpolata, viene generato un colore per pixel che viene scritto nel buffer del frame. Se un'applicazione Abilita la fusione di trame, il colore del pixel diventerà una combinazione del pixel corrente nel buffer del frame e di un colore della trama.

Questa formula determina il colore finale del pixel Blend:


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



Dove:

-   Color è il colore del pixel di output.
-   TexelColor è il colore di input dopo il filtro della trama.
-   SourceBlend è la percentuale del colore finale del pixel che è costituita dal colore di Texel di origine.
-   CurrentPixelColor è il colore del pixel corrente.
-   DestBlend è la percentuale del colore finale del pixel che è costituita dal colore del pixel corrente.

L'equazione di Blend finale viene impostata chiamando [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) e specificando lo stato di rendering di Blend (D3DRS \_ BLENDXXX) con un fattore di fusione corrispondente ([**D3DBLEND**](./d3dblend.md)). I valori di SourceBlend e DestBlend variano da 0,0 (trasparente) a 1,0 (opaco) inclusi. Inoltre, un'applicazione può controllare la trasparenza di un pixel impostando il valore alfa in una trama. In questo caso, utilizzare quanto segue:


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



L'equazione di fusione provocherà la trasparenza del pixel sottoposto a rendering. I valori predefiniti sono:


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di trame](texture-blending.md)
</dt> <dt>

[Filtraggio delle trame (Direct3D 9)](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
