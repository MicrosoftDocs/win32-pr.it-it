---
description: Il colore di nebbia per la nebbia dei pixel e dei vertici viene impostato tramite lo \_ stato di rendering FogColor di D3DRS. I valori dello stato di rendering possono essere qualsiasi colore RGB, specificato come colore RGBA. Il componente alfa viene ignorato.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Colore nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048869"
---
# <a name="fog-color-direct3d-9"></a>Colore nebbia (Direct3D 9)

Il colore di nebbia per la nebbia dei pixel e dei vertici viene impostato tramite lo \_ stato di rendering FogColor di D3DRS. I valori dello stato di rendering possono essere qualsiasi colore RGB, specificato come colore RGBA. Il componente alfa viene ignorato.

Nell'esempio C++ riportato di seguito il colore della nebbia viene impostato su bianco.


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



La nebbia viene applicata in modo diverso dalla pipeline della funzione fissa e dalla pipeline programmabile.

1.  Se il driver supporta D3DPMISCCAPS \_ FOGANDSPECULARALPHA:
    -   Se viene usata la pipeline della funzione fissa e D3DRS \_ FogColor è impostato, V1. w (nella pixel shader) è uguale al valore impostato in fog RenderState.
    -   Se viene usata la pipeline programmabile, V1. w (nella pixel shader) è uguale a 0, anche se oD1. w è scritto in modo esplicito in un vertex shader.
2.  Se il driver non supporta il \_ FOGANDSPECULARALPHA D3DPMISCCAPS:
    -   Se viene usata la pipeline della funzione fissa e \_ viene impostato D3DRS FogColor, V1. w (nel pixel shader) è uguale al valore impostato in fog RenderState.
    -   Se oFog viene scritto in modo esplicito in un vertex shader, V1. w (nella pixel shader) è uguale a oFog, con un valore compreso tra 0 e 1.
    -   Se nessuno dei due casi precedenti si applica, V1. w (nella pixel shader) è uguale a 0, anche se oD1. w è scritto in modo esplicito in un vertex shader.

Per ulteriori informazioni, vedere [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 



