---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere la topologia primitiva come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322236"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="e90d8-104">\_Struttura della \_ \_ \_ \_ topologia del flusso di stato della pipeline CD3DX12</span><span class="sxs-lookup"><span data-stu-id="e90d8-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="e90d8-105">Struttura di supporto utilizzata per descrivere la topologia primitiva come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="e90d8-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e90d8-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="e90d8-107">Members</span><span class="sxs-lookup"><span data-stu-id="e90d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e90d8-108">**\_ \_ \_ Topologia del flusso \_ di stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="e90d8-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="e90d8-109">Crea una nuova istanza non inizializzata di una \_ \_ \_ \_ topologia primitiva del flusso di stato della pipeline CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e90d8-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="e90d8-110">**\_Topologia del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ ( \_ tipo di topologia primitiva D3D12 \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="e90d8-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="e90d8-111">Crea una nuova istanza di una \_ \_ topologia primitiva del flusso di stato della pipeline CD3DX12 \_ \_ \_ , inizializzata con un tipo di sottooggetto della **\_ \_ \_ \_ \_ \_ topologia primitiva del tipo della pipeline D3D12** e dei dati di sottooggetti copiati da *i*, una struttura del [**\_ \_ \_ tipo di topologia primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="e90d8-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e90d8-112">**operator = ( \_ tipo di \_ topologia primitiva D3D12 \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="e90d8-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="e90d8-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="e90d8-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="e90d8-114">**operatore D3D12 \_ primitive \_ tipo di topologia \_ () const**</span><span class="sxs-lookup"><span data-stu-id="e90d8-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="e90d8-115">Conversione implicita in una struttura di [**\_ \_ \_ tipo topologia primitiva di D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="e90d8-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e90d8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e90d8-116">Remarks</span></span>

<span data-ttu-id="e90d8-117">\_ \_ \_ \_ \_ La topologia primitiva del flusso di stato della pipeline CD3DX12 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) ed è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="e90d8-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="e90d8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e90d8-118">Requirements</span></span>



| <span data-ttu-id="e90d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90d8-119">Requirement</span></span> | <span data-ttu-id="e90d8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e90d8-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e90d8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e90d8-121">Header</span></span><br/> | <dl> <span data-ttu-id="e90d8-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90d8-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90d8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e90d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90d8-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="e90d8-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e90d8-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e90d8-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="e90d8-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e90d8-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

