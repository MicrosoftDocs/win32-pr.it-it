---
title: Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 11)
description: Informazioni sul valore di riferimento di Stencil in Direct3D 11 Graphics. L'abilitazione dei pixel shader per l'uso del valore di riferimento dello stencil consente un controllo fine sulle operazioni di stencil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d780c7a800f4291b3cce01c6f974cdeedaa8f590fc76fdf8afa8b3fb3c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632311"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 11)

L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, invece di usare quello specificato dall'API, consente un controllo granulare molto fine sulle operazioni di stencil.

Il valore specificato dello shader sostituisce il valore di riferimento *dello stencil* specificato dall'API per tale chiamata, il che significa che la modifica influisce sia sul test di stencil che quando lo stencil op D3D11 STENCIL OP REPLACE (un membro di \_ \_ \_ [**D3D11 \_ STENCIL \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) viene usato per scrivere il valore di riferimento nel buffer dello stencil.

Nelle versioni precedenti di D3D11, il valore di riferimento di Stencil può essere specificato solo dal metodo [**ID3D11DeviceContext::OMSetDepthStencilState.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) Questo significa che questo valore può essere definito solo in base a una granularità per disegno. Questa funzionalità D3D11.3 consente agli sviluppatori di leggere e usare il valore di riferimento dello stencil ( ) restituito da un pixel shader, vale a dire che può essere specificato in base a una granularità per pixel o `SV_StencilRef` per campione.

Questa funzionalità è facoltativa in D3D11.3. Per verificarne il supporto, controllare il campo `PSSpecifiedStencilRefSupported` booleano [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) usando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Di seguito è riportato un esempio dell'uso `SV_StencilRef` di in un pixel shader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11.3](direct3d-11-3-features.md)
</dt> <dt>

[Modello shader 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
