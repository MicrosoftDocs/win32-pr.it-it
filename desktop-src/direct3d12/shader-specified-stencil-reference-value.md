---
title: Valore di riferimento stencil specificato dello shader (grafica Direct3D 12)
description: L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548843"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Valore di riferimento stencil specificato dello shader (grafica Direct3D 12)

L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.

Il valore di riferimento dello stencil viene in genere specificato dal metodo [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) . Questo metodo imposta il valore di riferimento dello stencil in base a una granularità per estrazione. Tuttavia, questo valore può essere sovrascritto dal pixel shader.

Questa funzionalità D3D12 (e D3D 11.3) consente agli sviluppatori di leggere e usare il valore di riferimento dello stencil (*SV \_ StencilRef*) che viene restituito da un pixel shader, abilitando una granularità per pixel o per campione.

Il valore specificato dello shader sostituisce il valore di riferimento specificato dall'API per la chiamata, il che significa che la modifica ha effetto sia sul test dello stencil, sia quando viene usata l'operazione stencil D3D12 \_ stencil \_ op \_ Replace (un membro di [**D3D12 \_ stencil \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) per scrivere il valore di riferimento nel buffer dello stencil.

Questa funzionalità è facoltativa sia per D3D12 che per D3D 11.3. Per eseguire il test del supporto, controllare il campo booleano *PSSpecifiedStencilRefSupported* delle [**\_ \_ \_ \_ Opzioni D3D12 dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Di seguito è riportato un esempio di utilizzo di *SV \_ StencilRef* in un pixel shader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering](rendering.md)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
