---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere i formati della destinazione di rendering come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322223"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="b52fd-104">\_Struttura del \_ \_ formato di \_ destinazione di rendering del flusso di \_ stato della pipeline \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="b52fd-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="b52fd-105">Struttura di supporto utilizzata per descrivere i formati della destinazione di rendering come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="b52fd-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52fd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b52fd-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="b52fd-107">Members</span><span class="sxs-lookup"><span data-stu-id="b52fd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b52fd-108">**\_Formati di \_ \_ destinazione di rendering del flusso di stato \_ della \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="b52fd-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="b52fd-109">Crea una nuova istanza non inizializzata di un \_ flusso di destinazione di rendering del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b52fd-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="b52fd-110">**\_Formati di destinazione per il rendering del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ (D3D12 \_ RT \_ Format \_ Array Const &i)**</span><span class="sxs-lookup"><span data-stu-id="b52fd-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="b52fd-111">Crea una nuova istanza di un \_ flusso di destinazione di rendering del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto di tipi di destinazione di rendering dei tipi di oggetto sottooggetto di **\_ stato della pipeline \_ \_ \_ \_ \_ \_ D3D12** e dati di sottooggetti copiati da i, una struttura di [**\_ \_ \_ matrice di formato D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)</span><span class="sxs-lookup"><span data-stu-id="b52fd-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b52fd-112">**operator = (D3D12 \_ RT \_ Format \_ ARRAY const& i)**</span><span class="sxs-lookup"><span data-stu-id="b52fd-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="b52fd-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="b52fd-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="b52fd-114">**operatore D3D12 \_ RT \_ Format \_ Array () const**</span><span class="sxs-lookup"><span data-stu-id="b52fd-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="b52fd-115">Conversione implicita in una struttura di [**\_ matrici di \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="b52fd-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b52fd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b52fd-116">Remarks</span></span>

<span data-ttu-id="b52fd-117">\_ \_ \_ \_ \_ I formati di destinazione per il rendering del flusso di stato della pipeline CD3DX12 \_ sono una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) ed è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="b52fd-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="b52fd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b52fd-118">Requirements</span></span>



| <span data-ttu-id="b52fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b52fd-119">Requirement</span></span> | <span data-ttu-id="b52fd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b52fd-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b52fd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b52fd-121">Header</span></span><br/> | <dl> <span data-ttu-id="b52fd-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52fd-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52fd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b52fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52fd-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="b52fd-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b52fd-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b52fd-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="b52fd-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b52fd-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

