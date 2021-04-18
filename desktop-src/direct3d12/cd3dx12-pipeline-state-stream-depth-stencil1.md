---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso. | Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322245"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="ba01e-105">\_ \_ \_ \_ Struttura STENCIL1 della profondità del flusso dello stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="ba01e-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="ba01e-106">Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="ba01e-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba01e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba01e-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="ba01e-108">Members</span><span class="sxs-lookup"><span data-stu-id="ba01e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba01e-109">**\_Profondità flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="ba01e-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="ba01e-110">Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1.</span><span class="sxs-lookup"><span data-stu-id="ba01e-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="ba01e-111">**CD3DX12 \_ - \_ profondità flusso di stato della pipeline \_ \_ \_ STENCIL1 (CD3DX12 \_ Depth \_ stencil \_ DESC1 const &i)**</span><span class="sxs-lookup"><span data-stu-id="ba01e-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="ba01e-112">Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ STENCIL1, inizializzata con un tipo di oggetto suboggetto di **D3D12 la profondità del tipo di \_ \_ sottooggetto stato della pipeline \_ \_ \_ \_ STENCIL1** e dati di sottooggetti copiati da *i*, una struttura CD3DX12 [**\_ Depth \_ stencil \_ DESC1**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="ba01e-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ba01e-113">**operator = (CD3DX12 \_ Depth \_ stencil \_ DESC1 const& i)**</span><span class="sxs-lookup"><span data-stu-id="ba01e-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="ba01e-114">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="ba01e-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="ba01e-115">**operatore CD3DX12 \_ Depth \_ stencil \_ DESC1 () const**</span><span class="sxs-lookup"><span data-stu-id="ba01e-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="ba01e-116">Conversione implicita in una struttura [**DESC1 di CD3DX12 \_ Depth \_ stencil \_**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="ba01e-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba01e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba01e-117">Remarks</span></span>

<span data-ttu-id="ba01e-118">\_ \_ \_ \_ La profondità del flusso di stato della pipeline CD3DX12 \_ STENCIL1 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:</span><span class="sxs-lookup"><span data-stu-id="ba01e-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="ba01e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba01e-119">Requirements</span></span>



| <span data-ttu-id="ba01e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba01e-120">Requirement</span></span> | <span data-ttu-id="ba01e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ba01e-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba01e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba01e-122">Header</span></span><br/> | <dl> <span data-ttu-id="ba01e-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba01e-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba01e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba01e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba01e-125">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="ba01e-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ba01e-126">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba01e-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="ba01e-127">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="ba01e-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

