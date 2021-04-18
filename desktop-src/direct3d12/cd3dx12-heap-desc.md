---
title: Struttura CD3DX12_HEAP_DESC (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura desc dell'heap D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Struttura CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322263"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="261b8-104">\_Struttura desc dell'heap CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="261b8-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="261b8-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ desc dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="261b8-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="261b8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="261b8-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="261b8-107">Members</span><span class="sxs-lookup"><span data-stu-id="261b8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="261b8-108">**CD3DX12 \_ heap \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="261b8-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-109">Crea una nuova istanza non inizializzata di una \_ Descrizione dell'heap CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="261b8-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="261b8-110">**heap CD3DX12 esplicito \_ \_ DESC (const D3D12 \_ heap \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="261b8-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-111">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ desc dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="261b8-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="261b8-112">**CD3DX12 \_ heap \_ DESC (dimensione UInt64, proprietà \_ heap D3D12 \_ proprietà, allineamento UInt64 = 0, flag \_ flag heap D3D12 \_ = D3D12 \_ \_ flag heap \_ nessuno)**</span><span class="sxs-lookup"><span data-stu-id="261b8-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-113">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="261b8-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="261b8-114">Dimensioni UINT64</span><span class="sxs-lookup"><span data-stu-id="261b8-114">UINT64 size</span></span>

<span data-ttu-id="261b8-115">[**D3D12 \_ Proprietà \_ heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) proprietà</span><span class="sxs-lookup"><span data-stu-id="261b8-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="261b8-116">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="261b8-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="261b8-117">consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="261b8-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="261b8-118">**CD3DX12 \_ heap \_ DESC (dimensione UInt64, \_ \_ tipo di tipo heap D3D12, allineamento UInt64 = 0, \_ flag \_ flag heap D3D12 = \_ D3D12 \_ flag heap \_ nessuno)**</span><span class="sxs-lookup"><span data-stu-id="261b8-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-119">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="261b8-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="261b8-120">Dimensioni UINT64</span><span class="sxs-lookup"><span data-stu-id="261b8-120">UINT64 size</span></span>

<span data-ttu-id="261b8-121">[**D3D12 \_ Tipo \_ di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="261b8-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="261b8-122">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="261b8-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="261b8-123">consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="261b8-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="261b8-124">**CD3DX12 \_ heap \_ DESC (dimensione UInt64, \_ \_ Proprietà pagina CPU D3D12 \_ cpuPageProperty, D3D12 \_ \_ pool di memoria MEMORYPOOLPREFERENCE, allineamento UInt64 = 0, D3D12 \_ flag heap flag \_ = D3D12 \_ heap flag \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="261b8-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-125">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="261b8-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="261b8-126">Dimensioni UINT64</span><span class="sxs-lookup"><span data-stu-id="261b8-126">UINT64 size</span></span>

<span data-ttu-id="261b8-127">[**D3D12 \_ \_ \_ Proprietà della pagina CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="261b8-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="261b8-128">[**D3D12 \_ MemoryPoolPreference \_ pool di memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="261b8-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="261b8-129">consenso esplicito Allineamento UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="261b8-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="261b8-130">consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="261b8-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="261b8-131">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 \_ heap \_ Properties Properties, D3D12 \_ heap Flags Flags \_ = D3D12 \_ Heap heap \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="261b8-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-132">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="261b8-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="261b8-133">[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="261b8-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="261b8-134">[**D3D12 \_ Proprietà \_ heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) proprietà</span><span class="sxs-lookup"><span data-stu-id="261b8-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="261b8-135">consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="261b8-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="261b8-136">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 tipo \_ \_ di heap, D3D12 heap flag Flags \_ \_ = D3D12 \_ Heap heap \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="261b8-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-137">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="261b8-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="261b8-138">[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="261b8-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="261b8-139">[**D3D12 \_ Tipo \_ di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="261b8-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="261b8-140">consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="261b8-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="261b8-141">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ Resource \_ allocation \_ info& ResAllocInfo, D3D12 \_ \_ pagina CPU \_ CPUPAGEPROPERTY, D3D12 \_ pool di memoria memoryPoolPreference \_ , D3D12 \_ heap flag Flags \_ = D3D12 \_ heap \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="261b8-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-142">Crea una nuova istanza di una \_ Descrizione dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="261b8-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="261b8-143">[**D3D12 \_ \_ \_ Informazioni sull'allocazione delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="261b8-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="261b8-144">[**D3D12 \_ \_ \_ Proprietà della pagina CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="261b8-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="261b8-145">[**D3D12 \_ MemoryPoolPreference \_ pool di memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="261b8-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="261b8-146">consenso esplicito [**D3D12 \_ Flag \_ heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = D3D12 \_ heap \_ flag \_ None</span><span class="sxs-lookup"><span data-stu-id="261b8-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="261b8-147">**operator const D3D12 \_ heap \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="261b8-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="261b8-148">Definisce il & operatore pass-by-reference per il \_ tipo di \_ struttura desc dell'heap CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="261b8-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="261b8-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="261b8-149">Requirements</span></span>



| <span data-ttu-id="261b8-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="261b8-150">Requirement</span></span> | <span data-ttu-id="261b8-151">Valore</span><span class="sxs-lookup"><span data-stu-id="261b8-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="261b8-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="261b8-152">Header</span></span><br/> | <dl> <span data-ttu-id="261b8-153"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="261b8-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="261b8-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="261b8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261b8-155">**D3D12 \_ heap \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="261b8-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="261b8-156">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="261b8-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





