---
title: Struttura CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura delle proprietà dell'heap D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Struttura CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322261"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="e02c4-104">Struttura delle proprietà dell' \_ heap CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="e02c4-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="e02c4-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura delle [**\_ \_ proprietà dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="e02c4-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e02c4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e02c4-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="e02c4-107">Members</span><span class="sxs-lookup"><span data-stu-id="e02c4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e02c4-108">**\_Proprietà heap CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="e02c4-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-109">Crea una nuova istanza non inizializzata di una \_ proprietà dell'heap CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e02c4-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="e02c4-110">**Proprietà heap CD3DX12 esplicite \_ \_ (proprietà dell'heap const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="e02c4-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-111">Crea una nuova istanza di una \_ proprietà dell'heap CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ proprietà dell'heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="e02c4-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e02c4-112">**\_Proprietà heap CD3DX12 \_ ( \_ Proprietà pagina CPU D3D12 \_ \_ CPUPAGEPROPERTY, \_ pool di memoria D3D12 \_ MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint node mask = 1)**</span><span class="sxs-lookup"><span data-stu-id="e02c4-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-113">Crea una nuova istanza di una \_ proprietà dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e02c4-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="e02c4-114">[**D3D12 \_ \_ \_ Proprietà della pagina CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="e02c4-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="e02c4-115">[**D3D12 \_ MemoryPoolPreference \_ pool di memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="e02c4-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="e02c4-116">consenso esplicito UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="e02c4-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="e02c4-117">consenso esplicito UINT node mask = 1</span><span class="sxs-lookup"><span data-stu-id="e02c4-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="e02c4-118">**Proprietà heap CD3DX12 esplicite \_ \_ ( \_ \_ tipo di heap D3D12, uint CREATIONNODEMASK = 1, uint node mask = 1)**</span><span class="sxs-lookup"><span data-stu-id="e02c4-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-119">Crea una nuova istanza di una \_ proprietà dell'heap CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e02c4-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="e02c4-120">[**D3D12 \_ Tipo \_ di heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="e02c4-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="e02c4-121">consenso esplicito UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="e02c4-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="e02c4-122">consenso esplicito UINT node mask = 1</span><span class="sxs-lookup"><span data-stu-id="e02c4-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="e02c4-123">**operator const \_ D3D12 \_ proprietà heap& () const**</span><span class="sxs-lookup"><span data-stu-id="e02c4-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-124">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="e02c4-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="e02c4-125">**operatore inline = = (proprietà dell'heap const D3D12 \_ \_& l, proprietà dell'heap const D3D12 \_ \_& r)**</span><span class="sxs-lookup"><span data-stu-id="e02c4-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-126">Verifica l'uguaglianza tra le \_ istanze delle proprietà dell'heap D3D12 specificate \_ , in base all'uguaglianza dei campi di tutti i membri.</span><span class="sxs-lookup"><span data-stu-id="e02c4-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="e02c4-127">**operatore inline! = (const D3D12 \_ heap \_ Properties& l, const D3D12 \_ heap \_ Properties& r)**</span><span class="sxs-lookup"><span data-stu-id="e02c4-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="e02c4-128">Verifica la disuguaglianza tra le istanze delle proprietà dell'heap D3D12 specificate \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e02c4-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="e02c4-129">Implementato utilizzando l'inverso del valore **operator = =** .</span><span class="sxs-lookup"><span data-stu-id="e02c4-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e02c4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e02c4-130">Requirements</span></span>



| <span data-ttu-id="e02c4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e02c4-131">Requirement</span></span> | <span data-ttu-id="e02c4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e02c4-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e02c4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e02c4-133">Header</span></span><br/> | <dl> <span data-ttu-id="e02c4-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e02c4-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e02c4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e02c4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e02c4-136">**\_Proprietà heap \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="e02c4-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="e02c4-137">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="e02c4-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





