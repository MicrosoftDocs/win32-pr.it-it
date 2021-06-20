---
title: Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 11)
description: Informazioni sul valore di riferimento di Stencil in Direct3D 11 Graphics. L'abilitazione dei pixel shader per l'uso del valore di riferimento dello stencil consente un controllo fine sulle operazioni degli stencil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408104"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="c3524-104">Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c3524-104">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="c3524-105">L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché usare quello specificato dall'API, consente un controllo granulare molto fine sulle operazioni di stencil.</span><span class="sxs-lookup"><span data-stu-id="c3524-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="c3524-106">Il valore specificato dello shader sostituisce il valore di riferimento *dello stencil* specificato dall'API per tale chiamata, il che significa che la modifica influisce sia sul test di stencil che quando lo stencil op D3D11 STENCIL OP REPLACE (un membro di \_ \_ \_ [**D3D11 \_ STENCIL \_ OP)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)viene usato per scrivere il valore di riferimento nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="c3524-106">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="c3524-107">Nelle versioni precedenti di D3D11, il valore di riferimento di Stencil può essere specificato solo dal metodo [**ID3D11DeviceContext::OMSetDepthStencilState.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate)</span><span class="sxs-lookup"><span data-stu-id="c3524-107">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="c3524-108">Questo significa che questo valore può essere definito solo in base a una granularità per disegno.</span><span class="sxs-lookup"><span data-stu-id="c3524-108">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="c3524-109">Questa funzionalità D3D11.3 consente agli sviluppatori di leggere e usare il valore di riferimento dello stencil ( ) restituito da un pixel shader, vale a dire che può essere specificato in base a una granularità per pixel o `SV_StencilRef` per campione.</span><span class="sxs-lookup"><span data-stu-id="c3524-109">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="c3524-110">Questa funzionalità è facoltativa in D3D11.3.</span><span class="sxs-lookup"><span data-stu-id="c3524-110">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="c3524-111">Per verificarne il supporto, controllare il campo `PSSpecifiedStencilRefSupported` booleano [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) usando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="c3524-111">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="c3524-112">Di seguito è riportato un esempio dell'uso `SV_StencilRef` di in un pixel shader:</span><span class="sxs-lookup"><span data-stu-id="c3524-112">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="c3524-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3524-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3524-114">Funzionalità di Direct3D 11.3</span><span class="sxs-lookup"><span data-stu-id="c3524-114">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="c3524-115">Modello shader 5.1</span><span class="sxs-lookup"><span data-stu-id="c3524-115">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
