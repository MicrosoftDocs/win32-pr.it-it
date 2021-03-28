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
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="e7165-103">Valore di riferimento stencil specificato dello shader (grafica Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e7165-103">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="e7165-104">L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.</span><span class="sxs-lookup"><span data-stu-id="e7165-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="e7165-105">Il valore specificato dello shader sostituisce il *valore di riferimento dello stencil* specificato dall'API per la chiamata, il che significa che la modifica ha effetto sia sul test dello stencil, sia quando lo stencil op d3d11 stencil op \_ \_ \_ Replace (un membro di [**d3d11 \_ stencil \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) viene usato per scrivere il valore di riferimento nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="e7165-105">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="e7165-106">Nelle versioni precedenti di D3D11, il valore di riferimento dello stencil può essere specificato solo dal metodo [**sul ID3D11DeviceContext:: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) .</span><span class="sxs-lookup"><span data-stu-id="e7165-106">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="e7165-107">Questo significa che questo valore può essere definito solo in una granularità per singolo progetto.</span><span class="sxs-lookup"><span data-stu-id="e7165-107">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="e7165-108">Questa funzionalità D3D 11.3 consente agli sviluppatori di leggere e usare il valore di riferimento dello stencil ( `SV_StencilRef` ) restituito da un pixel shader, ovvero può essere specificato in base a una granularità per pixel o per campione.</span><span class="sxs-lookup"><span data-stu-id="e7165-108">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="e7165-109">Questa funzionalità è facoltativa in D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="e7165-109">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="e7165-110">Per verificare il supporto, controllare il `PSSpecifiedStencilRefSupported` campo booleano dei [**\_ dati della funzionalità d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) usando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="e7165-110">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="e7165-111">Di seguito è riportato un esempio di utilizzo di `SV_StencilRef` in un pixel shader:</span><span class="sxs-lookup"><span data-stu-id="e7165-111">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="e7165-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7165-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7165-113">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="e7165-113">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="e7165-114">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="e7165-114">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
