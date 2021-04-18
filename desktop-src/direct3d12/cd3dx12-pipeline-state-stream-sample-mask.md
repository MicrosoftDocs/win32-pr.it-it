---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una maschera di esempio come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323572"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a><span data-ttu-id="6a94a-104">\_Struttura della \_ \_ maschera di esempio del flusso di stato della \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="6a94a-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK structure</span></span>

<span data-ttu-id="6a94a-105">Struttura di supporto utilizzata per descrivere una maschera di esempio come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="6a94a-105">A helper structure used to describe a sample mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a94a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a94a-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="6a94a-107">Members</span><span class="sxs-lookup"><span data-stu-id="6a94a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6a94a-108">**\_Maschera di \_ esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a94a-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="6a94a-109">Crea una nuova istanza non inizializzata di una \_ maschera di esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6a94a-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="6a94a-110">**\_Maschera di esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ (uint const &i)**</span><span class="sxs-lookup"><span data-stu-id="6a94a-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="6a94a-111">Crea una nuova istanza di una \_ maschera di esempio del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto del **tipo di \_ \_ \_ \_ \_ esempio \_ maschera di stato della pipeline D3D12** e dati di sottooggetti copiati da *i*, una maschera di esempio **uint** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_MASK** and subobject data copied from *i*, a **UINT** sample mask.</span></span>

</dd> <dt>

<span data-ttu-id="6a94a-112">**operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="6a94a-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="6a94a-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="6a94a-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="6a94a-114">**operatore UINT () const**</span><span class="sxs-lookup"><span data-stu-id="6a94a-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="6a94a-115">Conversione implicita in una maschera di esempio **uint** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-115">Implicit conversion to a **UINT** sample mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a94a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a94a-116">Remarks</span></span>

<span data-ttu-id="6a94a-117">\_ \_ \_ \_ La maschera di esempio del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6a94a-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="6a94a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a94a-118">Requirements</span></span>



| <span data-ttu-id="6a94a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a94a-119">Requirement</span></span> | <span data-ttu-id="6a94a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6a94a-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6a94a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a94a-121">Header</span></span><br/> | <dl> <span data-ttu-id="6a94a-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a94a-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a94a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a94a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a94a-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="6a94a-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6a94a-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a94a-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="6a94a-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="6a94a-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

