---
description: Direct3D consente di selezionare una modalità di ombreggiatura alla volta.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Impostazione della modalità ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068961"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Impostazione della modalità ombreggiatura (Direct3D 9)

Direct3D consente di selezionare una modalità di ombreggiatura alla volta. Per impostazione predefinita, è selezionata l'ombreggiatura Gouraud. In C++ è possibile modificare la modalità ombreggiatura chiamando il metodo [**IDirect3DDevice9::SetRenderState.**](/windows/desktop/api) Impostare il *parametro State* su D3DRS \_ SHADEMODE. Il *parametro State* deve essere impostato su un membro [**dell'enumerazione D3DSHADEMODE.**](./d3dshademode.md) Gli esempi di codice di esempio seguenti illustrano come la modalità di ombreggiatura corrente di un'applicazione Direct3D può essere impostata sulla modalità di ombreggiatura flat o Gouraud.


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

 

 
