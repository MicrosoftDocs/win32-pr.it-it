---
title: Struttura CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di intervallo descrittore D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Struttura CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322269"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="562b4-104">\_Struttura dell'intervallo descrittore CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="562b4-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="562b4-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ intervallo descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="562b4-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="562b4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="562b4-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="562b4-107">Members</span><span class="sxs-lookup"><span data-stu-id="562b4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="562b4-108">**\_Intervallo descrittore CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="562b4-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="562b4-109">Crea una nuova istanza non inizializzata di un \_ intervallo di descrittori D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="562b4-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="562b4-110">**\_intervallo descrittore CD3DX12 esplicito \_ ( \_ intervallo descrittore const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="562b4-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="562b4-111">Crea una nuova istanza di un \_ intervallo di descrittori D3DX12 \_ , inizializzato con il contenuto di un'altra struttura di [**\_ \_ intervallo descrittore D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="562b4-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="562b4-112">**\_Intervallo descrittore CD3DX12 (D3D12 descrittor \_ \_ \_ \_ Type RANGETYPE, uint descrittori numerici, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="562b4-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="562b4-113">Crea una nuova istanza di un \_ intervallo di descrittori D3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="562b4-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="562b4-114">[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="562b4-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="562b4-115">Descrittori numerici UINT</span><span class="sxs-lookup"><span data-stu-id="562b4-115">UINT numDescriptors</span></span>

<span data-ttu-id="562b4-116">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="562b4-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="562b4-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="562b4-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="562b4-118">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_</span><span class="sxs-lookup"><span data-stu-id="562b4-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="562b4-119">**inline init ( \_ tipo di intervallo descrittore D3D12 \_ \_ RangeType, UINT descrittori numerici, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="562b4-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="562b4-120">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="562b4-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="562b4-121">[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="562b4-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="562b4-122">Descrittori numerici UINT</span><span class="sxs-lookup"><span data-stu-id="562b4-122">UINT numDescriptors</span></span>

<span data-ttu-id="562b4-123">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="562b4-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="562b4-124">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="562b4-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="562b4-125">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_</span><span class="sxs-lookup"><span data-stu-id="562b4-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="562b4-126">**static inline init (D3D12 \_ descrittor range \_ &Range, D3D12 \_ Descriptor \_ Range \_ Type RANGETYPE, uint descrittori numerici, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descrittor \_ \_ offset range \_ Append)**</span><span class="sxs-lookup"><span data-stu-id="562b4-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="562b4-127">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="562b4-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="562b4-128">[**D3D12 \_ Intervallo \_ &di DEscrittori**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)</span><span class="sxs-lookup"><span data-stu-id="562b4-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="562b4-129">[**D3D12 \_ \_ \_ Tipo di intervallo descrittore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="562b4-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="562b4-130">Descrittori numerici UINT</span><span class="sxs-lookup"><span data-stu-id="562b4-130">UINT numDescriptors</span></span>

<span data-ttu-id="562b4-131">BaseShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="562b4-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="562b4-132">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="562b4-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="562b4-133">UINT offsetInDescriptorsFromTableStart = D3D12 \_ descrittore \_ \_ offset intervallo \_</span><span class="sxs-lookup"><span data-stu-id="562b4-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="562b4-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="562b4-134">Requirements</span></span>



| <span data-ttu-id="562b4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="562b4-135">Requirement</span></span> | <span data-ttu-id="562b4-136">Valore</span><span class="sxs-lookup"><span data-stu-id="562b4-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="562b4-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="562b4-137">Header</span></span><br/> | <dl> <span data-ttu-id="562b4-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="562b4-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562b4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="562b4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562b4-140">**\_Intervallo descrittore D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="562b4-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="562b4-141">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="562b4-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





