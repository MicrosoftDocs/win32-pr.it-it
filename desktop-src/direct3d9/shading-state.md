---
description: Direct3D supporta sia l'ombreggiatura flat che l'ombreggiatura Gouraud. Il valore predefinito è Gouraud shading. Per controllare la modalità di ombreggiatura corrente, l'applicazione C++ specifica un membro del tipo enumerato D3DSHADEMODE per lo stato di rendering D3DRS \_ SHADEMODE.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Stato ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f28514fefbf39e75bd84a0ae56324fd859f0fd85fa4a25449e349ce592ab3b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727601"
---
# <a name="shading-state-direct3d-9"></a>Stato ombreggiatura (Direct3D 9)

Direct3D supporta sia l'ombreggiatura flat che l'ombreggiatura Gouraud. Il valore predefinito è Gouraud shading. Per controllare la modalità di ombreggiatura corrente, l'applicazione C++ specifica un membro del tipo enumerato [**D3DSHADEMODE**](./d3dshademode.md) per lo stato di rendering D3DRS \_ SHADEMODE.

Nell'esempio di codice C++ seguente viene illustrato il processo di impostazione dello stato dell'ombreggiatura sulla modalità di ombreggiatura flat.


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

 

 
