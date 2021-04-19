---
title: Struttura CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di barriera delle risorse D3D12 \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Struttura CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323568"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="2acad-104">\_Struttura della barriera delle risorse CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="2acad-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="2acad-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ barriera delle risorse D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .</span><span class="sxs-lookup"><span data-stu-id="2acad-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2acad-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2acad-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="2acad-107">Members</span><span class="sxs-lookup"><span data-stu-id="2acad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2acad-108">**\_Barriera risorse CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="2acad-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="2acad-109">Crea una nuova istanza non inizializzata di una \_ barriera della risorsa CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="2acad-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="2acad-110">**barriera della risorsa CD3DX12 esplicita \_ \_ (const D3D12 \_ Resource \_ Barrier &o)**</span><span class="sxs-lookup"><span data-stu-id="2acad-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2acad-111">Crea una nuova istanza di una \_ barriera della risorsa CD3DX12 \_ , inizializzata con il contenuto di un'altra [**\_ \_ barriera di risorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span><span class="sxs-lookup"><span data-stu-id="2acad-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="2acad-112">**transizione inline statica ( \* preorigine ID3D12Resource, \_ Stati risorsa D3D12 \_ stateBefore, D3D12 \_ \_ stati risorse stateAfter, uint subresource = D3D12 \_ Resource \_ Barrier \_ All \_ Resources, D3D12 Resource Barrier flag Flags \_ \_ \_ = D3D12 \_ Resource \_ Barrier \_ flag \_ None)**</span><span class="sxs-lookup"><span data-stu-id="2acad-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="2acad-113">Transizioni tra gli Stati delle risorse, usando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="2acad-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="2acad-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource</span><span class="sxs-lookup"><span data-stu-id="2acad-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="2acad-115">[**D3D12 \_ \_Stati delle risorse**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span><span class="sxs-lookup"><span data-stu-id="2acad-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="2acad-116">[**D3D12 \_ \_Stati delle risorse**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span><span class="sxs-lookup"><span data-stu-id="2acad-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="2acad-117">consenso esplicito UINT subresource = [ **D3D12 \_ Resource \_ Barrier \_ tutte le \_ sottorisorse**](constants.md)</span><span class="sxs-lookup"><span data-stu-id="2acad-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="2acad-118">consenso esplicito [**D3D12 \_ Flag \_ di \_ barriera delle risorse**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flag = D3D12 \_ flag di barriera delle risorse \_ \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2acad-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="2acad-119">**Aliasing inline statico (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**</span><span class="sxs-lookup"><span data-stu-id="2acad-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="2acad-120">Crea gli alias per la risorsa prima e dopo la transizione della barriera.</span><span class="sxs-lookup"><span data-stu-id="2acad-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="2acad-121">Parametri</span><span class="sxs-lookup"><span data-stu-id="2acad-121">Parameters:</span></span>

<span data-ttu-id="2acad-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore</span><span class="sxs-lookup"><span data-stu-id="2acad-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="2acad-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter</span><span class="sxs-lookup"><span data-stu-id="2acad-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="2acad-124">**inline UAV statico ( \* preorigine ID3D12Resource)**</span><span class="sxs-lookup"><span data-stu-id="2acad-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="2acad-125">Crea una visualizzazione non ordinata (UAV) per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2acad-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="2acad-126">Parametri</span><span class="sxs-lookup"><span data-stu-id="2acad-126">Parameters:</span></span>

<span data-ttu-id="2acad-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource</span><span class="sxs-lookup"><span data-stu-id="2acad-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="2acad-128">**operatore const D3D12 \_ Resource \_ Barrier& () const**</span><span class="sxs-lookup"><span data-stu-id="2acad-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="2acad-129">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="2acad-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2acad-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2acad-130">Requirements</span></span>



| <span data-ttu-id="2acad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2acad-131">Requirement</span></span> | <span data-ttu-id="2acad-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2acad-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2acad-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2acad-133">Header</span></span><br/> | <dl> <span data-ttu-id="2acad-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2acad-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2acad-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2acad-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2acad-136">**\_Barriera delle risorse D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="2acad-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="2acad-137">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="2acad-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





