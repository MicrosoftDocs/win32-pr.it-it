---
description: Se non si fa luce con un vertex shader o una pixel shader, è possibile scegliere di usare il motore di illuminazione nel Runtime.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Stato illuminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303724"
---
# <a name="lighting-state-direct3d-9"></a>Stato illuminazione (Direct3D 9)

Se non si fa luce con un vertex shader o una pixel shader, è possibile scegliere di usare il motore di illuminazione nel Runtime. Il motore di illuminazione richiede che i dati dei vertici contengano normali per ogni vertice; i vertici senza dati normali genereranno un prodotto a virgola pari a zero in tutti i calcoli di illuminazione. I calcoli di illuminazione sono trattati in modo più dettagliato in [matematica di illuminazione (Direct3D 9)](mathematics-of-lighting.md).

Per abilitare il motore di illuminazione, usare:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 



