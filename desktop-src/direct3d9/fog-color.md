---
description: Il colore della nebbia per pixel e vertex viene impostato tramite lo stato di rendering D3DRS \_ FOGCOLOR. I valori dello stato di rendering possono essere qualsiasi colore RGB, specificato come colore RGBA. Il componente alfa viene ignorato.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Colore osanna (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 395bb17c9d6495ade54bc7c761b8c8024c53fbd9a51f620a45ee3a807dc6e20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988001"
---
# <a name="fog-color-direct3d-9"></a>Colore osanna (Direct3D 9)

Il colore della nebbia per pixel e vertex viene impostato tramite lo stato di rendering D3DRS \_ FOGCOLOR. I valori dello stato di rendering possono essere qualsiasi colore RGB, specificato come colore RGBA. Il componente alfa viene ignorato.

Nell'esempio C++ seguente il colore della nebbia viene impostato sul bianco.


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



La nebbia viene applicata in modo diverso dalla pipeline di funzioni fisse e dalla pipeline programmabile.

1.  Se il driver supporta D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Se viene usata la pipeline di funzioni fisse ed è impostato D3DRS \_ FOGCOLOR, la versione 1.w (nel pixel shader) è uguale al valore impostato in osasto renderstate.
    -   Se viene usata la pipeline programmabile, la versione 1.w (nel pixel shader) è uguale a 0, anche se oD1.w viene scritto in modo esplicito in un vertex shader.
2.  Se il driver NON supporta D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Se viene usata la pipeline di funzioni fisse ed è impostato D3DRS \_ FOGCOLOR, v1.w (nel pixel shader) è uguale al valore impostato in stato di rendering osa.
    -   Se oFog viene scritto in modo esplicito in un vertex shader, v1.w (nel pixel shader) è uguale a oFog, con un intervallo compreso tra 0 e 1.
    -   Se nessuno dei due casi precedenti si applica, v1.w (nel pixel shader) è uguale a 0, anche se oD1.w viene scritto in modo esplicito in un vertex shader.

Per altre informazioni, vedere [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 



