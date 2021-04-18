---
description: Il buffering di profondità è un metodo per rimuovere le linee e le superfici nascoste. Per impostazione predefinita, Direct3D non usa la memorizzazione nel buffer di profondità.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Stato buffering profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481556"
---
# <a name="depth-buffering-state-direct3d-9"></a>Stato buffering profondità (Direct3D 9)

Il buffering di profondità è un metodo per rimuovere le linee e le superfici nascoste. Per impostazione predefinita, Direct3D non usa la memorizzazione nel buffer di profondità.

Per una panoramica concettuale dei buffer di profondità, vedere [buffer di profondità (Direct3D 9)](depth-buffers.md).

Le applicazioni C++ aggiornano lo stato di buffering di profondità con lo \_ stato di rendering ZENABLE di D3DRS, usando un membro dell'enumerazione [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) per specificare il nuovo valore di stato.

Se l'applicazione deve impedire a Direct3D di scrivere nel buffer di profondità, può usare il \_ valore enumerato D3DRS ZWRITEENABLE, specificando D3DZB \_ false come secondo parametro per la chiamata a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

Nell'esempio di codice seguente viene illustrato come impostare lo stato del buffer di profondità per abilitare il buffer z.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



L'applicazione può anche usare lo \_ stato di rendering ZFUNC di D3DRS per controllare la funzione di confronto utilizzata da Direct3D durante l'esecuzione del buffer di profondità.

La distorsione Z è un metodo di visualizzazione di una superficie davanti a un'altra, anche se i valori di profondità sono uguali. È possibile utilizzare questa tecnica per diversi effetti. Un esempio comune è il rendering di ombre sulle pareti. Sia l'ombreggiatura che la parete hanno lo stesso valore di profondità. Tuttavia, si desidera che l'applicazione mostri l'ombreggiatura sulla parete. Se si assegna una polarizzazione z all'ombreggiatura, Direct3D li visualizza correttamente (vedere D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
