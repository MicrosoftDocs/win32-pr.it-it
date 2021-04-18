---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione di Blend come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322258"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a><span data-ttu-id="6023f-104">\_ \_ \_ \_ Struttura Desc del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="6023f-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC structure</span></span>

<span data-ttu-id="6023f-105">Struttura di supporto utilizzata per descrivere una descrizione di Blend come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="6023f-105">A helper structure used to describe a blend description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6023f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6023f-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="6023f-107">Members</span><span class="sxs-lookup"><span data-stu-id="6023f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6023f-108">**CD3DX12 \_ di \_ \_ Blend del flusso di stato \_ della pipeline \_**</span><span class="sxs-lookup"><span data-stu-id="6023f-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="6023f-109">Crea una nuova istanza non inizializzata di una CD3DX12 della \_ pipeline di \_ flusso dello stato della pipeline \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6023f-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6023f-110">**CD3DX12 \_ pipeline \_ state \_ Stream \_ Blend \_ DESC (CD3DX12 \_ Blend \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="6023f-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC(CD3DX12\_BLEND\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="6023f-111">Crea una nuova istanza di una CD3DX12 \_ della pipeline di \_ flusso dello stato della pipeline \_ \_ \_ , inizializzata con un tipo di sottooggetto di Blend di tipo di **oggetto di stato della \_ pipeline \_ \_ \_ \_ D3D12** e i dati di sottooggetti copiati da *i*, una struttura di [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="6023f-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_BLEND** and subobject data copied from *i*, a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6023f-112">**operator = (CD3DX12 \_ Blend \_ desc deconst& i)**</span><span class="sxs-lookup"><span data-stu-id="6023f-112">**operator=(CD3DX12\_BLEND\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="6023f-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="6023f-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="6023f-114">**operatore CD3DX12 \_ Blend \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="6023f-114">**operator CD3DX12\_BLEND\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="6023f-115">Conversione implicita in una struttura [**\_ \_ desc di CD3DX12 Blend**](cd3dx12-blend-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="6023f-115">Implicit conversion to a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6023f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6023f-116">Remarks</span></span>

<span data-ttu-id="6023f-117">\_La funzione \_ di flusso di stato della pipeline CD3DX12 \_ \_ \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6023f-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="6023f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6023f-118">Requirements</span></span>



| <span data-ttu-id="6023f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6023f-119">Requirement</span></span> | <span data-ttu-id="6023f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6023f-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6023f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6023f-121">Header</span></span><br/> | <dl> <span data-ttu-id="6023f-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6023f-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6023f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6023f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6023f-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="6023f-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6023f-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6023f-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="6023f-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="6023f-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

