---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Struttura helper utilizzata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322262"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a><span data-ttu-id="986f4-104">\_ \_ \_ \_ Struttura PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="986f4-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO structure</span></span>

<span data-ttu-id="986f4-105">Struttura helper utilizzata per descrivere un oggetto PSO memorizzato nella cache come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="986f4-105">A helper structure used to describe a cached PSO as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="986f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="986f4-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a><span data-ttu-id="986f4-107">Members</span><span class="sxs-lookup"><span data-stu-id="986f4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="986f4-108">**\_ \_ \_ \_ PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="986f4-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>
</dt> <dd>

<span data-ttu-id="986f4-109">Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ memorizzato nella cache di un oggetto \_ PSO.</span><span class="sxs-lookup"><span data-stu-id="986f4-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO.</span></span>

</dd> <dt>

<span data-ttu-id="986f4-110">**CD3DX12 della \_ pipeline del flusso di stato della pipeline \_ \_ \_ \_ (D3D12 della \_ pipeline memorizzato nella cache \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="986f4-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO(D3D12\_CACHED\_PIPELINE\_STATE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="986f4-111">Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ memorizzato nella cache di un oggetto \_ \_ \_ PSO, inizializzato con un tipo di SOTTOoggetto del **tipo di \_ \_ oggetto sottooggetto stato della pipeline D3D12 \_ \_ \_ memorizzato nella cache \_ PSO** e dati di oggetti suboggetto copiati da *i*, una struttura di [**\_ \_ \_ stato della pipeline D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)</span><span class="sxs-lookup"><span data-stu-id="986f4-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CACHED\_PSO** and subobject data copied from *i*, a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> <dt>

<span data-ttu-id="986f4-112">**operator = ( \_ stato della pipeline D3D12 memorizzato nella cache \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="986f4-112">**operator=(D3D12\_CACHED\_PIPELINE\_STATE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="986f4-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="986f4-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="986f4-114">**operatore D3D12 \_ memorizzato nella cache- \_ stato della pipeline \_ () const**</span><span class="sxs-lookup"><span data-stu-id="986f4-114">**operator D3D12\_CACHED\_PIPELINE\_STATE() const**</span></span>
</dt> <dd>

<span data-ttu-id="986f4-115">Conversione implicita in una struttura di [**\_ stato della \_ pipeline \_ D3D12 memorizzata nella cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="986f4-115">Implicit conversion to a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="986f4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="986f4-116">Remarks</span></span>

<span data-ttu-id="986f4-117">\_ \_ \_ \_ L'oggetto PSO memorizzato nella cache del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="986f4-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a><span data-ttu-id="986f4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="986f4-118">Requirements</span></span>



| <span data-ttu-id="986f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="986f4-119">Requirement</span></span> | <span data-ttu-id="986f4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="986f4-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="986f4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="986f4-121">Header</span></span><br/> | <dl> <span data-ttu-id="986f4-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="986f4-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="986f4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="986f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986f4-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="986f4-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="986f4-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="986f4-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="986f4-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="986f4-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

