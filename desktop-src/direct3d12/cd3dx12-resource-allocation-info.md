---
title: Struttura CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di informazioni sull'allocazione delle risorse D3D12 \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Struttura CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322216"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="06302-104">\_Struttura delle \_ informazioni di allocazione delle risorse CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="06302-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="06302-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ informazioni sull'allocazione delle risorse D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="06302-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="06302-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06302-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="06302-107">Members</span><span class="sxs-lookup"><span data-stu-id="06302-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="06302-108">**\_Informazioni sull' \_ allocazione delle risorse CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="06302-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="06302-109">Crea una nuova istanza non inizializzata di una \_ risorsa di allocazione delle risorse CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="06302-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="06302-110">**informazioni sull' \_ allocazione delle risorse CD3DX12 esplicite \_ \_ (const D3D12 \_ Resource \_ allocation \_& o)**</span><span class="sxs-lookup"><span data-stu-id="06302-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="06302-111">Crea una nuova istanza di un' \_ informazione di \_ allocazione delle risorse CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ \_ informazioni sull'allocazione delle risorse D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="06302-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="06302-112">**\_Informazioni sull' \_ allocazione delle risorse CD3DX12 \_ (dimensione UINT64, allineamento UInt64)**</span><span class="sxs-lookup"><span data-stu-id="06302-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="06302-113">Crea una nuova istanza di una \_ risorsa di \_ allocazione delle risorse CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="06302-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="06302-114">Dimensioni UINT64</span><span class="sxs-lookup"><span data-stu-id="06302-114">UINT64 size</span></span>

<span data-ttu-id="06302-115">Allineamento UINT64</span><span class="sxs-lookup"><span data-stu-id="06302-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="06302-116">**operatore const D3D12 \_ Resource \_ allocation \_& () const**</span><span class="sxs-lookup"><span data-stu-id="06302-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="06302-117">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="06302-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06302-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06302-118">Requirements</span></span>



| <span data-ttu-id="06302-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06302-119">Requirement</span></span> | <span data-ttu-id="06302-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06302-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06302-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06302-121">Header</span></span><br/> | <dl> <span data-ttu-id="06302-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="06302-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06302-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06302-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06302-124">**\_Informazioni sull' \_ allocazione delle risorse D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="06302-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="06302-125">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="06302-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





