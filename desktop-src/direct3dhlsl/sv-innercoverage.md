---
title: SV_InnerCoverage
description: SV \_ InputCoverage rappresenta le informazioni di rasterizzazione conservative sottostimate, ad esempio se un pixel è garantito per essere completamente coperto.
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
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993549"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="d429b-104">\_INNERCOVERAGE SV</span><span class="sxs-lookup"><span data-stu-id="d429b-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="d429b-105">SV \_ InputCoverage rappresenta le informazioni di rasterizzazione conservative sottostimate, ad esempio se un pixel è garantito per essere completamente coperto.</span><span class="sxs-lookup"><span data-stu-id="d429b-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="d429b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d429b-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="d429b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d429b-107">Type</span></span> |
| <span data-ttu-id="d429b-108">uint</span><span class="sxs-lookup"><span data-stu-id="d429b-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d429b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d429b-109">Remarks</span></span>

<span data-ttu-id="d429b-110">Questo valore generato dal sistema è richiesto per il supporto di livello 3 ed è disponibile solo in tale livello.</span><span class="sxs-lookup"><span data-stu-id="d429b-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="d429b-111">Questo input si escludono a vicenda con SV \_ coverage. non è possibile usare entrambi.</span><span class="sxs-lookup"><span data-stu-id="d429b-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="d429b-112">Per accedere a SV \_ InnerCoverage, è necessario dichiararlo come componente singolo da uno dei registri di input pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d429b-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="d429b-113">La modalità di interpolazione nella dichiarazione deve essere costante (l'interpolazione non è applicabile).</span><span class="sxs-lookup"><span data-stu-id="d429b-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="d429b-114">La rasterizzazione conservativa è disponibile sia in D3D 11.3 che in D3D12.</span><span class="sxs-lookup"><span data-stu-id="d429b-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="d429b-115">Fare riferimento a:</span><span class="sxs-lookup"><span data-stu-id="d429b-115">Refer to:</span></span>

-   [<span data-ttu-id="d429b-116">Rasterizzazione conservativa D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="d429b-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="d429b-117">Rasterizzazione conservativa D3D12</span><span class="sxs-lookup"><span data-stu-id="d429b-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="d429b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d429b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d429b-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d429b-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="d429b-120">Valori di sistema del modello shader 5,1</span><span class="sxs-lookup"><span data-stu-id="d429b-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 