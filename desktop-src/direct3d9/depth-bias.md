---
description: È possibile fare in modo che i poligoni complanari nello spazio 3D appaiano come se non fossero complanari aggiungendo una distorsione z a ciascuna di esse.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Distorsione profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481564"
---
# <a name="depth-bias-direct3d-9"></a>Distorsione profondità (Direct3D 9)

È possibile fare in modo che i poligoni complanari nello spazio 3D appaiano come se non fossero complanari aggiungendo una distorsione z a ciascuna di esse. Si tratta di una tecnica comunemente utilizzata per garantire che le ombre in una scena vengano visualizzate correttamente. Ad esempio, un'ombreggiatura su una parete avrà probabilmente lo stesso valore di profondità del muro. Se si esegue il rendering del muro per primo e poi l'ombreggiatura, l'ombreggiatura potrebbe non essere visibile oppure gli artefatti di profondità potrebbero essere visibili. È possibile invertire l'ordine in cui si esegue il rendering degli oggetti complanari nella speranza di inversare l'effetto, ma è probabile che gli artefatti di profondità siano ancora disponibili.

Un'applicazione può garantire che i poligoni compostivi vengano sottoposti a rendering correttamente aggiungendo una distorsione ai valori z usati dal sistema durante il rendering dei set di poligoni complanari. Per aggiungere una polarizzazione z a un set di poligoni, chiamare il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) immediatamente prima di eseguirne il rendering, impostando il parametro *state* su D3DRS \_ DEPTHBIAS e il parametro *value* su un valore float adatto (ad esempio, un valore appropriato può essere compreso tra-1,0 e 1,0). per passare questo valore a **SetRenderState**, è necessario eseguire il cast del valore a **DWORD**. Un valore di distorsione z superiore aumenta la probabilità che i poligoni di cui viene eseguito il rendering siano visibili quando vengono visualizzati con altri poligoni complanari.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



dove m è la pendenza massima della profondità del triangolo sottoposto a rendering.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Le unità per gli \_ Stati di rendering D3DRS DEPTHBIAS e D3DRS \_ SLOPESCALEDEPTHBIAS variano a seconda che sia abilitata la funzionalità di buffering z o w. L'applicazione deve fornire valori appropriati.

La distorsione non viene applicata a nessuna primitiva di linea e punto. Questa distorsione deve tuttavia essere applicata a triangoli disegnati in modalità wireframe.


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

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 
