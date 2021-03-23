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
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="e94cb-103">Valore di riferimento stencil specificato dello shader (grafica Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="e94cb-103">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="e94cb-104">L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.</span><span class="sxs-lookup"><span data-stu-id="e94cb-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="e94cb-105">Il valore di riferimento dello stencil viene in genere specificato dal metodo [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) .</span><span class="sxs-lookup"><span data-stu-id="e94cb-105">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="e94cb-106">Questo metodo imposta il valore di riferimento dello stencil in base a una granularità per estrazione.</span><span class="sxs-lookup"><span data-stu-id="e94cb-106">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="e94cb-107">Tuttavia, questo valore può essere sovrascritto dal pixel shader.</span><span class="sxs-lookup"><span data-stu-id="e94cb-107">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="e94cb-108">Questa funzionalità D3D12 (e D3D 11.3) consente agli sviluppatori di leggere e usare il valore di riferimento dello stencil (*SV \_ StencilRef*) che viene restituito da un pixel shader, abilitando una granularità per pixel o per campione.</span><span class="sxs-lookup"><span data-stu-id="e94cb-108">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="e94cb-109">Il valore specificato dello shader sostituisce il valore di riferimento specificato dall'API per la chiamata, il che significa che la modifica ha effetto sia sul test dello stencil, sia quando viene usata l'operazione stencil D3D12 \_ stencil \_ op \_ Replace (un membro di [**D3D12 \_ stencil \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) per scrivere il valore di riferimento nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="e94cb-109">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="e94cb-110">Questa funzionalità è facoltativa sia per D3D12 che per D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="e94cb-110">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="e94cb-111">Per eseguire il test del supporto, controllare il campo booleano *PSSpecifiedStencilRefSupported* delle [**\_ \_ \_ \_ Opzioni D3D12 dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="e94cb-111">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="e94cb-112">Di seguito è riportato un esempio di utilizzo di *SV \_ StencilRef* in un pixel shader:</span><span class="sxs-lookup"><span data-stu-id="e94cb-112">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="e94cb-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e94cb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e94cb-114">Rendering</span><span class="sxs-lookup"><span data-stu-id="e94cb-114">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="e94cb-115">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="e94cb-115">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="e94cb-116">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="e94cb-116">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="e94cb-117">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="e94cb-117">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
