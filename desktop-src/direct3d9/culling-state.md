---
description: Per migliorare le prestazioni di rendering, è possibile eliminare o rimuovere una primitiva che faccia parte della fotocamera.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Stato di eliminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127126"
---
# <a name="culling-state-direct3d-9"></a>Stato di eliminazione (Direct3D 9)

Per migliorare le prestazioni di rendering, è possibile eliminare o rimuovere una primitiva che faccia parte della fotocamera. Per le primitive unilaterali, questo consente di risparmiare tempo di rendering perché un back-face non è visibile. Per abilitare l'eliminazione, è necessario conoscerne l'ordine di avvolgimento (in genere in senso antiorario). In questo esempio vengono rimosse tutte le primitive il cui retro è rivolto verso l'esterno (dato un ordine di avvolgimento in senso antiorario):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 



