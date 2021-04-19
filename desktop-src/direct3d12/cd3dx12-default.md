---
title: Struttura CD3DX12_DEFAULT (D3dx12. h)
description: Passa \_ il valore predefinito di D3D12 in un costruttore per ogni struttura helper. Questa struttura viene semplicemente utilizzata come meccanismo per impostare i parametri predefiniti sulle altre strutture di supporto.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Struttura CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322279"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="6e2cc-105">\_Struttura predefinita CD3DX12</span><span class="sxs-lookup"><span data-stu-id="6e2cc-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="6e2cc-106">Passa \_ il valore predefinito di D3D12 in un costruttore per ogni struttura helper.</span><span class="sxs-lookup"><span data-stu-id="6e2cc-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="6e2cc-107">Questa struttura viene semplicemente utilizzata come meccanismo per impostare i parametri predefiniti sulle altre strutture di supporto.</span><span class="sxs-lookup"><span data-stu-id="6e2cc-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e2cc-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e2cc-108">Remarks</span></span>

<span data-ttu-id="6e2cc-109">Questa struct viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="6e2cc-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="6e2cc-110">Passa \_ il valore predefinito di D3D12 in un costruttore per ogni struct helper.</span><span class="sxs-lookup"><span data-stu-id="6e2cc-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="6e2cc-111">Ad esempio, il costruttore seguente viene dichiarato in d3dx12. h:</span><span class="sxs-lookup"><span data-stu-id="6e2cc-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="6e2cc-112">\_ \_ Handle descrittore CPU CD3DX12 \_ ( \_ valore predefinito CD3DX12) {ptr = 0;}</span><span class="sxs-lookup"><span data-stu-id="6e2cc-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="6e2cc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e2cc-113">Requirements</span></span>



| <span data-ttu-id="6e2cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e2cc-114">Requirement</span></span> | <span data-ttu-id="6e2cc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6e2cc-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2cc-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e2cc-116">Header</span></span><br/> | <dl> <span data-ttu-id="6e2cc-117"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e2cc-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e2cc-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e2cc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e2cc-119">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="6e2cc-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





