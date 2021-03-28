---
title: Valore di riferimento stencil specificato dello shader (grafica Direct3D 11)
description: L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340003"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Valore di riferimento stencil specificato dello shader (grafica Direct3D 11)

L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.

Il valore specificato dello shader sostituisce il *valore di riferimento dello stencil* specificato dall'API per la chiamata, il che significa che la modifica ha effetto sia sul test dello stencil, sia quando lo stencil op d3d11 stencil op \_ \_ \_ Replace (un membro di [**d3d11 \_ stencil \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) viene usato per scrivere il valore di riferimento nel buffer dello stencil.

Nelle versioni precedenti di D3D11, il valore di riferimento dello stencil può essere specificato solo dal metodo [**sul ID3D11DeviceContext:: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) . Questo significa che questo valore può essere definito solo in una granularità per singolo progetto. Questa funzionalità D3D 11.3 consente agli sviluppatori di leggere e usare il valore di riferimento dello stencil ( `SV_StencilRef` ) restituito da un pixel shader, ovvero può essere specificato in base a una granularità per pixel o per campione.

Questa funzionalità è facoltativa in D3D 11.3. Per verificare il supporto, controllare il `PSSpecifiedStencilRefSupported` campo booleano dei [**\_ dati della funzionalità d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) usando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Di seguito è riportato un esempio di utilizzo di `SV_StencilRef` in un pixel shader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
