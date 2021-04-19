---
description: Direct3D supporta l'ombreggiatura sia flat che Gouraud. Il valore predefinito è Gouraud shading. Per controllare la modalità di ombreggiatura corrente, l'applicazione C++ specifica un membro del tipo enumerato D3DSHADEMODE per lo \_ stato di rendering D3DRS MODOOMBRA.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Stato ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304063"
---
# <a name="shading-state-direct3d-9"></a>Stato ombreggiatura (Direct3D 9)

Direct3D supporta l'ombreggiatura sia flat che Gouraud. Il valore predefinito è Gouraud shading. Per controllare la modalità di ombreggiatura corrente, l'applicazione C++ specifica un membro del tipo enumerato [**D3DSHADEMODE**](./d3dshademode.md) per lo \_ stato di rendering D3DRS MODOOMBRA.

Nell'esempio di codice C++ riportato di seguito viene illustrato il processo di impostazione dello stato di ombreggiatura sulla modalità ombreggiatura piatta.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
