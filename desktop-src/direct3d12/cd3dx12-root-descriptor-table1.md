---
title: Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura Tabella1 del descrittore radice D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Struttura CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323564"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="4ce7e-104">\_ \_ Struttura Tabella1 del descrittore radice CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4ce7e-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="4ce7e-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ \_ Tabella1 del descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="4ce7e-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce7e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ce7e-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="4ce7e-107">Members</span><span class="sxs-lookup"><span data-stu-id="4ce7e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ce7e-108">**\_Descrittore radice CD3DX12 \_ \_ Tabella1 ()**</span><span class="sxs-lookup"><span data-stu-id="4ce7e-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="4ce7e-109">Crea una nuova istanza non inizializzata di un \_ \_ descrittore radice CD3DX12 \_ Tabella1.</span><span class="sxs-lookup"><span data-stu-id="4ce7e-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="4ce7e-110">**descrittore radice CD3DX12 esplicito \_ \_ \_ Tabella1 (const D3D12 \_ radice \_ descrittore \_ Tabella1 &o)**</span><span class="sxs-lookup"><span data-stu-id="4ce7e-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4ce7e-111">Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12 \_ Tabella1, inizializzato con il contenuto di un'altra struttura [**\_ \_ \_ Tabella1 del descrittore radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="4ce7e-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4ce7e-112">**\_Descrittore radice CD3DX12 \_ \_ Tabella1 (uint numDescriptorRanges, const D3D12 \_ descrittore \_ nell'intervallo 1 pDescriptorRanges \* \_ )**</span><span class="sxs-lookup"><span data-stu-id="4ce7e-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="4ce7e-113">Crea una nuova istanza di un \_ \_ descrittore radice CD3DX12 \_ Tabella1, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ce7e-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="4ce7e-114">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="4ce7e-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4ce7e-115">[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4ce7e-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="4ce7e-116">**inline init (UINT numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="4ce7e-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="4ce7e-117">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ce7e-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4ce7e-118">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="4ce7e-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4ce7e-119">[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4ce7e-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="4ce7e-120">**static inline init (D3D12 \_ root \_ descriptor \_ Tabella1 &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ Descriptor \_ nell'intervallo 1 pDescriptorRanges \* \_ )**</span><span class="sxs-lookup"><span data-stu-id="4ce7e-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="4ce7e-121">Specifica una funzione che Inizializza i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ce7e-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4ce7e-122">[**D3D12 \_ \_Descrittore radice \_ Tabella1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="4ce7e-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="4ce7e-123">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="4ce7e-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4ce7e-124">[**\_ descrittore \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) const nell'intervallo 1 \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="4ce7e-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ce7e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ce7e-125">Requirements</span></span>



| <span data-ttu-id="4ce7e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ce7e-126">Requirement</span></span> | <span data-ttu-id="4ce7e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4ce7e-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce7e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ce7e-128">Header</span></span><br/> | <dl> <span data-ttu-id="4ce7e-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ce7e-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce7e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ce7e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce7e-131">**\_Descrittore radice D3D12 \_ \_ Tabella1**</span><span class="sxs-lookup"><span data-stu-id="4ce7e-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="4ce7e-132">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="4ce7e-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





