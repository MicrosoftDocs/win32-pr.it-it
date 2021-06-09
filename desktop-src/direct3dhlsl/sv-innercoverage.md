---
title: SV_InnerCoverage
description: SV InputCoverage rappresenta informazioni di rasterizzazione conservative sottostimate,ad esempio se un pixel è garantito per essere \_ completamente coperto.
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 168f90c17c9e6837d696ebb6dac8f39dc6dfb366
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826625"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="a9c30-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="a9c30-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="a9c30-105">SV InputCoverage rappresenta informazioni di rasterizzazione conservative sottostimate,ad esempio se un pixel è garantito per essere \_ completamente coperto.</span><span class="sxs-lookup"><span data-stu-id="a9c30-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="a9c30-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9c30-106">Type</span></span>



| <span data-ttu-id="a9c30-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9c30-107">Type</span></span>     |
|------|
| <span data-ttu-id="a9c30-108">uint</span><span class="sxs-lookup"><span data-stu-id="a9c30-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a9c30-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9c30-109">Remarks</span></span>

<span data-ttu-id="a9c30-110">Questo valore generato dal sistema è necessario per il supporto di livello 3 ed è disponibile solo in tale livello.</span><span class="sxs-lookup"><span data-stu-id="a9c30-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="a9c30-111">Questo input si escludono a vicenda con la copertura SV. Non \_ è possibile usare entrambi.</span><span class="sxs-lookup"><span data-stu-id="a9c30-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="a9c30-112">Per accedere a SV InnerCoverage, deve essere dichiarato come singolo componente di uno dei registri pixel shader \_ input.</span><span class="sxs-lookup"><span data-stu-id="a9c30-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="a9c30-113">La modalità di interpolazione nella dichiarazione deve essere costante (l'interpolazione non è applicabile).</span><span class="sxs-lookup"><span data-stu-id="a9c30-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="a9c30-114">La rasterizzazione conservativa è disponibile sia in D3D11.3 che in D3D12.</span><span class="sxs-lookup"><span data-stu-id="a9c30-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="a9c30-115">Fare riferimento a:</span><span class="sxs-lookup"><span data-stu-id="a9c30-115">Refer to:</span></span>

-   [<span data-ttu-id="a9c30-116">D3D11.3 Rasterizzazione conservativa</span><span class="sxs-lookup"><span data-stu-id="a9c30-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="a9c30-117">Rasterizzazione conservativa D3D12</span><span class="sxs-lookup"><span data-stu-id="a9c30-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="a9c30-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9c30-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c30-119">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="a9c30-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="a9c30-120">Valori di sistema del modello shader 5.1</span><span class="sxs-lookup"><span data-stu-id="a9c30-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
