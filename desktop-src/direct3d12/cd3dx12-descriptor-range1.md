---
title: Struttura CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura nell'intervallo 1 del descrittore D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Struttura CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322266"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="1dedd-104">\_Struttura nell'intervallo 1 del descrittore CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="1dedd-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="1dedd-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**\_ \_ nell'intervallo 1 del descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="1dedd-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dedd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dedd-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="1dedd-107">Members</span><span class="sxs-lookup"><span data-stu-id="1dedd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1dedd-108">**\_Descrittore CD3DX12 \_ nell'intervallo 1 ()**</span><span class="sxs-lookup"><span data-stu-id="1dedd-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="1dedd-109">Crea una nuova istanza non inizializzata di un \_ descrittore CD3DX12 \_ nell'intervallo 1.</span><span class="sxs-lookup"><span data-stu-id="1dedd-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="1dedd-110">**descrittore CD3DX12 esplicito \_ \_ nell'intervallo 1 (CONSt D3D12 \_ descrittore \_ nell'intervallo 1 &o)**</span><span class="sxs-lookup"><span data-stu-id="1dedd-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="1dedd-111">Crea una nuova istanza di un \_ descrittore CD3DX12 \_ nell'intervallo 1, inizializzato con il contenuto di un'altra struttura di [**\_ descrittore D3D12 \_ nell'intervallo 1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="1dedd-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1dedd-112">**\_Descrittore CD3DX12 \_ nell'intervallo 1 ( \_ tipo di intervallo descrittore D3D12 \_ \_ RANGETYPE, uint descrittori numerici, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descrittor range Flags Flags \_ \_ = D3D12 \_ descrittor \_ Range flag \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="1dedd-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="1dedd-113">Crea una nuova istanza di un \_ descrittore CD3DX12 \_ nell'intervallo 1, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dedd-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="1dedd-114">[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="1dedd-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="1dedd-115">Descrittori numerici UINT</span><span class="sxs-lookup"><span data-stu-id="1dedd-115">UINT numDescriptors</span></span>

<span data-ttu-id="1dedd-116">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="1dedd-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="1dedd-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="1dedd-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="1dedd-118">[**D3D12 \_ Flag \_ intervallo \_ descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flag = D3D12 \_ flag intervallo descrittore \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1dedd-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="1dedd-119">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_</span><span class="sxs-lookup"><span data-stu-id="1dedd-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="1dedd-120">**inline init ( \_ tipo di intervallo descrittore D3D12 \_ \_ RangeType, UINT descrittori numerici, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ Descriptor \_ Range FLAGs Flags \_ = D3D12 \_ descrittor \_ Range flag \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset intervallo \_ )**</span><span class="sxs-lookup"><span data-stu-id="1dedd-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="1dedd-121">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dedd-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1dedd-122">[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="1dedd-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="1dedd-123">Descrittori numerici UINT</span><span class="sxs-lookup"><span data-stu-id="1dedd-123">UINT numDescriptors</span></span>

<span data-ttu-id="1dedd-124">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="1dedd-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="1dedd-125">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="1dedd-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="1dedd-126">[**D3D12 \_ Flag \_ intervallo \_ descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flag = D3D12 \_ flag intervallo descrittore \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1dedd-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="1dedd-127">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_</span><span class="sxs-lookup"><span data-stu-id="1dedd-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="1dedd-128">**static inline init (D3D12 \_ descrittor \_ nell'intervallo 1 &Range, D3D12 \_ descrittor \_ Range \_ Type RANGETYPE, uint descrittori numerici, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descrittor \_ Range \_ Flags Flags = D3D12 \_ descrittor \_ Range \_ flag \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="1dedd-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="1dedd-129">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="1dedd-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1dedd-130">[**D3D12 \_ Descrittore \_ nell'intervallo 1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &intervallo</span><span class="sxs-lookup"><span data-stu-id="1dedd-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="1dedd-131">[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="1dedd-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="1dedd-132">Descrittori numerici UINT</span><span class="sxs-lookup"><span data-stu-id="1dedd-132">UINT numDescriptors</span></span>

<span data-ttu-id="1dedd-133">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="1dedd-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="1dedd-134">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="1dedd-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="1dedd-135">[**D3D12 \_ Flag \_ intervallo \_ descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flag = D3D12 \_ flag intervallo descrittore \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1dedd-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="1dedd-136">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_</span><span class="sxs-lookup"><span data-stu-id="1dedd-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1dedd-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dedd-137">Requirements</span></span>



| <span data-ttu-id="1dedd-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dedd-138">Requirement</span></span> | <span data-ttu-id="1dedd-139">Valore</span><span class="sxs-lookup"><span data-stu-id="1dedd-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1dedd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dedd-140">Header</span></span><br/> | <dl> <span data-ttu-id="1dedd-141"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dedd-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dedd-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dedd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dedd-143">**\_Descrittore D3D12 \_ nell'intervallo 1**</span><span class="sxs-lookup"><span data-stu-id="1dedd-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="1dedd-144">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="1dedd-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





