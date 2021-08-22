---
description: I poligoni coplanari nello spazio 3D possono essere fatti apparire come se non fossero coplanari aggiungendo una distorsione z a ognuno.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Distorsione della profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc99d606a561fd6f4eec412774ce53d9b5dd5e62c7f50b118a4e90a88664a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523812"
---
# <a name="depth-bias-direct3d-9"></a>Distorsione della profondità (Direct3D 9)

I poligoni coplanari nello spazio 3D possono essere fatti apparire come se non fossero coplanari aggiungendo una distorsione z a ognuno. Si tratta di una tecnica comunemente usata per garantire che le ombreggiature in una scena siano visualizzate correttamente. Ad esempio, un'ombreggiatura su una parete avrà probabilmente lo stesso valore di profondità della parete. Se si esegue prima il rendering del muro e quindi dell'ombreggiatura, l'ombreggiatura potrebbe non essere visibile o gli artefatti di profondità potrebbero essere visibili. È possibile invertire l'ordine in cui si esegue il rendering degli oggetti coplanari nella speranza di invertire l'effetto, ma è probabile che gli artefatti di profondità siano ancora presenti.

Un'applicazione consente di garantire che il rendering dei poligoni coplanari venga eseguito correttamente aggiungendo una distorsione ai valori z utilizzati dal sistema durante il rendering dei set di poligoni coplanari. Per aggiungere una distorsione z a un set di poligoni, chiamare il metodo [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) subito prima del rendering, impostando il parametro *State* su D3DRS DEPTHBIAS e il parametro Value su un valore float appropriato (ad esempio, un valore appropriato potrebbe essere compreso tra \_ -1.0 e 1.0); per passare questo valore a **SetRenderState,** è necessario anche eseguire il cast del valore a **un valore DWORD**.  Un valore di distorsione z più alto aumenta la probabilità che i poligoni di cui si esegue il rendering siano visibili quando vengono visualizzati con altri poligoni coplanari.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



dove m è l'inclinazione massima della profondità del triangolo sottoposto a rendering.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Le unità per gli stati di rendering \_ D3DRS DEPTHBIAS e D3DRS SLOPESCALEDEPTHBIAS variano a seconda che sia abilitato il buffering z o \_ w. L'applicazione deve fornire valori appropriati.

La distorsione non viene applicata ad alcuna primitiva linea e punto. Tuttavia, questa distorsione deve essere applicata ai triangoli tracciati in modalità wireframe.


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
