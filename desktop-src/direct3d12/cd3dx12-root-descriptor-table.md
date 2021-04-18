---
title: Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di tabella del descrittore radice D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322206"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="8edfd-104">\_Struttura della \_ tabella descrittore radice CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="8edfd-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="8edfd-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ tabella del descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="8edfd-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8edfd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8edfd-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="8edfd-107">Members</span><span class="sxs-lookup"><span data-stu-id="8edfd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8edfd-108">**\_ \_ Tabella descrittore radice CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8edfd-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="8edfd-109">Crea una nuova istanza non inizializzata di una \_ \_ tabella del descrittore radice CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8edfd-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="8edfd-110">**\_ \_ tabella descrittore radice CD3DX12 esplicita \_ ( \_ \_ tabella descrittore radice D3D12 const \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8edfd-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8edfd-111">Crea una nuova istanza di una \_ tabella del \_ descrittore radice CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura della [**\_ \_ \_ tabella del descrittore radice di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="8edfd-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8edfd-112">**\_ \_ Tabella descrittore radice CD3DX12 \_ (uint numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="8edfd-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="8edfd-113">Crea una nuova istanza di una \_ tabella del \_ descrittore radice CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="8edfd-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="8edfd-114">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="8edfd-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8edfd-115">[**D3D12 \_ \_Intervallo descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8edfd-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="8edfd-116">**inline init (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="8edfd-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="8edfd-117">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="8edfd-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8edfd-118">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="8edfd-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8edfd-119">[**D3D12 \_ \_Intervallo descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8edfd-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="8edfd-120">**static inline init ( \_ \_ tabella descrittore radice D3D12 \_ &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ Descriptor \_ Range \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="8edfd-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="8edfd-121">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="8edfd-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8edfd-122">[**D3D12 \_ \_ \_ Tabella descrittore radice**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="8edfd-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="8edfd-123">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="8edfd-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8edfd-124">[**D3D12 \_ \_Intervallo descrittore**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8edfd-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8edfd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8edfd-125">Requirements</span></span>



| <span data-ttu-id="8edfd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8edfd-126">Requirement</span></span> | <span data-ttu-id="8edfd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8edfd-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8edfd-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8edfd-128">Header</span></span><br/> | <dl> <span data-ttu-id="8edfd-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8edfd-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8edfd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8edfd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edfd-131">**\_ \_ Tabella descrittore radice D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8edfd-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="8edfd-132">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="8edfd-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





