---
description: Direct3D consente di selezionare una modalità di ombreggiatura alla volta.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Impostazione della modalità di ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482084"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Impostazione della modalità di ombreggiatura (Direct3D 9)

Direct3D consente di selezionare una modalità di ombreggiatura alla volta. Per impostazione predefinita, è selezionata l'ombreggiatura Gouraud. In C++ è possibile modificare la modalità di ombreggiatura chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) . Impostare il parametro *state* su D3DRS \_ MODOOMBRA. Il parametro *state* deve essere impostato su un membro dell'enumerazione [**D3DSHADEMODE**](./d3dshademode.md) . Gli esempi di codice di esempio seguenti illustrano come è possibile impostare la modalità di ombreggiatura corrente di un'applicazione Direct3D sulla modalità di ombreggiatura flat o Gouraud.


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ombreggiatura](shading.md)
</dt> </dl>

 

 
