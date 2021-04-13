---
description: Più destinazioni di rendering (MRT) si riferiscono alla possibilità di eseguire il rendering su più superfici (vedere IDirect3D9Surface) con una singola chiamata di disegnare.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Più destinazioni di rendering (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482045"
---
# <a name="multiple-render-targets-direct3d-9"></a>Più destinazioni di rendering (Direct3D 9)

Più destinazioni di rendering (MRT) si riferiscono alla possibilità di eseguire il rendering su più superfici (vedere [**IDirect3D9Surface**](/windows/desktop/api)) con una singola chiamata di disegnare. Queste superfici possono essere create indipendentemente l'una dall'altra. È possibile impostare le destinazioni di rendering usando [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).

Più destinazioni di rendering presentano le restrizioni seguenti:

-   Tutte le superfici di destinazione di rendering utilizzate insieme devono avere la stessa profondità del bit, ma possono avere formati diversi, a meno che non \_ sia impostato il limite di D3DPMISCCAPS MRTINDEPENDENTBITDEPTHS.
-   Tutte le superfici di una destinazione di rendering multipla devono avere la stessa larghezza e altezza.
-   Alcune implementazioni non possono eseguire operazioni post-pixel shader su più destinazioni di rendering, tra cui: nessun dithering, test alfa, nessuna nebbia, nessuna fusione o maschera, eccetto il test z-test e stencil. I dispositivi in grado di supportare operazioni post-pixel shader impostano il bit Cap su D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.

    Quando \_ viene impostato il limite di MRTPOSTPIXELSHADERBLENDING D3DPMISCCAPS, è necessario prima di tutto consultare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con la query sull'utilizzo \_ POSTPIXELSHADER il risultato della \_ \_ fusione per il formato di superficie specifico. Se false, non sarà disponibile alcuna operazione di fusione post-pixel shader per quel formato di superficie specifico. Se true, il dispositivo dovrebbe applicare lo stesso stato a tutte le destinazioni di rendering simultanee come segue:

    -   Alpha Blend: il valore del colore in oCi viene blended con la destinazione di rendering Ith.
    -   Test alfa: il confronto avverrà con oC0. Se il confronto ha esito negativo, il test pixel viene terminato per tutte le destinazioni di rendering.
    -   Fog: la destinazione di rendering 0 viene offuscata. Altre destinazioni di rendering non sono definite. Le implementazioni possono scegliere di offuscarle tutte usando lo stesso stato.
    -   Rethering: non definito.

-   Non è supportato l'anti-aliasing.
-   Alcune implementazioni non applicano la maschera di scrittura di output (D3DRS \_ COLORWRITEENABLE). Quelli che possono avere maschere di scrittura a colori indipendenti. Viene espresso usando un nuovo bit di funzionalità. Il numero di maschere di scrittura a colori indipendenti disponibili sarà uguale al numero massimo di elementi che il dispositivo è in grado di supportare.

Nuovi tappi hardware:


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 
