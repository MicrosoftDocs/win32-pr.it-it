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
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="78a49-104">Valore di riferimento dello stencil specificato dello shader (grafica Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="78a49-104">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="78a49-105">L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché usare quello specificato dall'API, consente un controllo granulare molto fine sulle operazioni degli stencil.</span><span class="sxs-lookup"><span data-stu-id="78a49-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="78a49-106">Il valore di riferimento dello stencil viene in genere specificato dal [**metodo ID3D12GraphicsCommandList::OMSetStencilRef.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref)</span><span class="sxs-lookup"><span data-stu-id="78a49-106">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="78a49-107">Questo metodo imposta il valore di riferimento dello stencil in base a una granularità per disegno.</span><span class="sxs-lookup"><span data-stu-id="78a49-107">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="78a49-108">Tuttavia, questo valore può essere sovrascritto dal pixel shader.</span><span class="sxs-lookup"><span data-stu-id="78a49-108">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="78a49-109">Questa funzionalità D3D12 (e D3D11.3) consente agli sviluppatori di leggere e usare il valore di riferimento stencil *(SV \_ StencilRef)* restituito da un pixel shader, abilitando una granularità per pixel o per campione.</span><span class="sxs-lookup"><span data-stu-id="78a49-109">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="78a49-110">Il valore specificato dello shader sostituisce il valore di riferimento specificato dall'API per tale chiamata, il che significa che la modifica influisce sia sul test degli stencil che quando viene usata l'operazione stencil D3D12 STENCIL OP REPLACE (un membro di \_ \_ \_ [**D3D12 \_ STENCIL \_ OP)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)per scrivere il valore di riferimento nel buffer degli stencil.</span><span class="sxs-lookup"><span data-stu-id="78a49-110">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="78a49-111">Questa funzionalità è facoltativa sia in D3D12 che in D3D11.3.</span><span class="sxs-lookup"><span data-stu-id="78a49-111">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="78a49-112">Per verificare il supporto, controllare il campo booleano *PSSpecifiedStencilRefSupported* di [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="78a49-112">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="78a49-113">Di seguito è riportato un esempio dell'uso di *SV \_ StencilRef* in un pixel shader:</span><span class="sxs-lookup"><span data-stu-id="78a49-113">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="78a49-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78a49-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78a49-115">Rendering</span><span class="sxs-lookup"><span data-stu-id="78a49-115">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="78a49-116">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="78a49-116">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="78a49-117">Modello shader 5.1</span><span class="sxs-lookup"><span data-stu-id="78a49-117">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="78a49-118">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="78a49-118">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
