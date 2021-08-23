---
description: Il buffering della profondità è un metodo per rimuovere le linee e le superfici nascoste. Per impostazione predefinita, Direct3D non usa il buffering di profondità.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Stato buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d6d0494511c7fc0434d97988152426eb888d6c3044de4e2359ac2cb41110ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988312"
---
# <a name="depth-buffering-state-direct3d-9"></a>Stato buffer di profondità (Direct3D 9)

Il buffering della profondità è un metodo per rimuovere le linee e le superfici nascoste. Per impostazione predefinita, Direct3D non usa il buffering di profondità.

Per una panoramica concettuale dei buffer di profondità, vedere [Buffer di profondità (Direct3D 9).](depth-buffers.md)

Le applicazioni C++ aggiornano lo stato di buffering di profondità con lo stato di rendering ZENABLE D3DRS, usando un membro dell'enumerazione \_ [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) per specificare il nuovo valore dello stato.

Se l'applicazione deve impedire a Direct3D di scrivere nel buffer di profondità, può usare il valore enumerato D3DRS ZWRITEENABLE, specificando D3DZB FALSE come secondo parametro per la chiamata a \_ \_ [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

Nell'esempio di codice seguente viene illustrato come lo stato del buffer di profondità è impostato per abilitare il buffer z.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



L'applicazione può anche usare lo stato di rendering ZFUNC D3DRS per controllare la funzione di confronto utilizzata da \_ Direct3D durante l'esecuzione del buffering di profondità.

La distorsione Z è un metodo per visualizzare una superficie davanti a un'altra, anche se i relativi valori di profondità sono gli stessi. È possibile usare questa tecnica per un'ampia gamma di effetti. Un esempio comune è il rendering delle ombreggiature sulle pareti. Sia l'ombreggiatura che la parete hanno lo stesso valore di profondità. Tuttavia, si vuole che l'applicazione mostri l'ombreggiatura sulla parete. Se si specifica una distorsione z per l'ombreggiatura, Direct3D le visualizza correttamente (vedere D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
