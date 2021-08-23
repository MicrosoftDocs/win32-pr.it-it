---
description: Se non si accende con un vertex shader o un pixel shader, è possibile scegliere di usare il motore di illuminazione nel runtime.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Stato di illuminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674271"
---
# <a name="lighting-state-direct3d-9"></a>Stato di illuminazione (Direct3D 9)

Se non si accende con un vertex shader o un pixel shader, è possibile scegliere di usare il motore di illuminazione nel runtime. Il motore di illuminazione richiede che i dati dei vertici contengano normali per vertice; I vertici senza dati normali genereranno un prodotto punto pari a zero in tutti i calcoli di illuminazione. I calcoli dell'illuminazione sono trattati in modo più dettagliato in [Matematica dell'illuminazione (Direct3D 9).](mathematics-of-lighting.md)

Per abilitare il motore di illuminazione, usare:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 



