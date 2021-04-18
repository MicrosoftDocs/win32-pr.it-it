---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una maschera del nodo come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322238"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a><span data-ttu-id="4369c-104">\_Struttura della \_ \_ maschera del nodo del flusso di stato della \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4369c-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK structure</span></span>

<span data-ttu-id="4369c-105">Struttura di supporto utilizzata per descrivere una maschera del nodo come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="4369c-105">A helper structure used to describe a node mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4369c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4369c-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="4369c-107">Members</span><span class="sxs-lookup"><span data-stu-id="4369c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4369c-108">**\_Maschera del \_ nodo del flusso di stato della pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4369c-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="4369c-109">Crea una nuova istanza non inizializzata di una \_ maschera del nodo del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4369c-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="4369c-110">**\_Maschera del nodo del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ (uint const &i)**</span><span class="sxs-lookup"><span data-stu-id="4369c-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="4369c-111">Crea una nuova istanza di una \_ maschera del nodo del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto della maschera del nodo del tipo di sottooggetto  **stato della \_ pipeline \_ \_ \_ \_ \_ D3D12** e i dati di sottooggetti copiati da i, una maschera del nodo **uint** .</span><span class="sxs-lookup"><span data-stu-id="4369c-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_NODE\_MASK** and subobject data copied from *i*, a **UINT** node mask.</span></span>

</dd> <dt>

<span data-ttu-id="4369c-112">**operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="4369c-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="4369c-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="4369c-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="4369c-114">**operatore UINT () const**</span><span class="sxs-lookup"><span data-stu-id="4369c-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="4369c-115">Conversione implicita in una maschera del nodo **uint** .</span><span class="sxs-lookup"><span data-stu-id="4369c-115">Implicit conversion to a **UINT** node mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4369c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4369c-116">Remarks</span></span>

<span data-ttu-id="4369c-117">\_ \_ \_ \_ La maschera del nodo del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="4369c-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="4369c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4369c-118">Requirements</span></span>



| <span data-ttu-id="4369c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4369c-119">Requirement</span></span> | <span data-ttu-id="4369c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4369c-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4369c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4369c-121">Header</span></span><br/> | <dl> <span data-ttu-id="4369c-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4369c-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4369c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4369c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4369c-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="4369c-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4369c-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4369c-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="4369c-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4369c-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

