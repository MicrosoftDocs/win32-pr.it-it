---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso. | Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322252"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a><span data-ttu-id="f23d1-105">\_ \_ \_ \_ Struttura stencil profondità flusso dello stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="f23d1-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL structure</span></span>

<span data-ttu-id="f23d1-106">Struttura di supporto utilizzata per descrivere una descrizione depth stencil come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="f23d1-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23d1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f23d1-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="f23d1-108">Members</span><span class="sxs-lookup"><span data-stu-id="f23d1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f23d1-109">**\_ \_ \_ \_ Stencil profondità flusso dello stato della pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="f23d1-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>
</dt> <dd>

<span data-ttu-id="f23d1-110">Crea una nuova istanza non inizializzata di uno \_ stencil di profondità del \_ flusso dello stato della pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f23d1-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL.</span></span>

</dd> <dt>

<span data-ttu-id="f23d1-111">**\_ \_ Stencil profondità flusso di stato della pipeline CD3DX12 \_ \_ \_ (CD3DX12 \_ Depth \_ stencil \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="f23d1-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL(CD3DX12\_DEPTH\_STENCIL\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f23d1-112">Crea una nuova istanza di uno \_ stencil di \_ profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ , inizializzato con un tipo di sottooggetto dello stencil di profondità del tipo di sottooggetto **\_ \_ dello stato \_ \_ \_ \_** della pipeline D3D12 e dati di sottooggetti copiati da i, una struttura di [**\_ \_ stencil \_ depth di CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="f23d1-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f23d1-113">**operator = (CD3DX12 \_ Depth \_ stencil \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="f23d1-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f23d1-114">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="f23d1-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f23d1-115">**operatore CD3DX12 \_ Depth \_ stencil \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="f23d1-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="f23d1-116">Conversione implicita in una struttura [**CD3DX12 \_ Depth \_ stencil \_ desc**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="f23d1-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f23d1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f23d1-117">Remarks</span></span>

<span data-ttu-id="f23d1-118">\_ \_ Lo \_ stencil profondità flusso dello stato della pipeline CD3DX12 \_ \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="f23d1-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
```



## <a name="requirements"></a><span data-ttu-id="f23d1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f23d1-119">Requirements</span></span>



| <span data-ttu-id="f23d1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23d1-120">Requirement</span></span> | <span data-ttu-id="f23d1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f23d1-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f23d1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f23d1-122">Header</span></span><br/> | <dl> <span data-ttu-id="f23d1-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23d1-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23d1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f23d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23d1-125">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="f23d1-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f23d1-126">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f23d1-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f23d1-127">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f23d1-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

