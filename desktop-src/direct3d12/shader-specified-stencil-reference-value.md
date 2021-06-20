---
title: Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 12)
description: Informazioni sul valore di riferimento degli stencil nella grafica Direct3D 12. L'abilitazione dei pixel shader per l'uso del valore di riferimento degli stencil consente un controllo fine sulle operazioni degli stencil.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408314"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 12)

L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché usare quello specificato dall'API, consente un controllo granulare molto fine sulle operazioni degli stencil.

Il valore di riferimento dello stencil viene in genere specificato dal [**metodo ID3D12GraphicsCommandList::OMSetStencilRef.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) Questo metodo imposta il valore di riferimento dello stencil in base a una granularità per disegno. Tuttavia, questo valore può essere sovrascritto dal pixel shader.

Questa funzionalità D3D12 (e D3D11.3) consente agli sviluppatori di leggere e usare il valore di riferimento stencil *(SV \_ StencilRef)* restituito da un pixel shader, abilitando una granularità per pixel o per campione.

Il valore specificato dello shader sostituisce il valore di riferimento specificato dall'API per tale chiamata, il che significa che la modifica influisce sia sul test degli stencil che quando viene usata l'operazione stencil D3D12 STENCIL OP REPLACE (un membro di \_ \_ \_ [**D3D12 \_ STENCIL \_ OP)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)per scrivere il valore di riferimento nel buffer degli stencil.

Questa funzionalità è facoltativa sia in D3D12 che in D3D11.3. Per verificare il supporto, controllare il campo booleano *PSSpecifiedStencilRefSupported* di [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Di seguito è riportato un esempio dell'uso di *SV \_ StencilRef* in un pixel shader:

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

[Modello shader 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
