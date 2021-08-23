---
description: Per migliorare le prestazioni di rendering, è possibile eliminare (o rimuovere) una primitiva che si allontana dalla fotocamera.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Culling State (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bf9d8ed8ecea46dcfee146784dc97a38e42f0261b8f78bfc9d45ffaf99ddd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608031"
---
# <a name="culling-state-direct3d-9"></a>Culling State (Direct3D 9)

Per migliorare le prestazioni di rendering, è possibile eliminare (o rimuovere) una primitiva che si allontana dalla fotocamera. Per le primitive a lato singolo, ciò consente di risparmiare tempo di rendering perché un back-face non è visibile. Per abilitare l'culling, è necessario conoscere l'ordine di avvolgimento dei vertici (in genere in senso antiorario). Questo esempio rimuove tutte le primitive il cui viso posteriore è rivolto in avanti (in base a un ordine di avvolgimento in senso antiorario):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 



