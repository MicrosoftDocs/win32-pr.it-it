---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322224"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a><span data-ttu-id="2d9b1-104">\_Struttura di \_ \_ output del \_ flusso di stato della pipeline \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="2d9b1-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT structure</span></span>

<span data-ttu-id="2d9b1-105">Struttura di supporto utilizzata per descrivere la descrizione dell'output del flusso come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="2d9b1-105">A helper structure used to describe the stream output description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9b1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d9b1-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="2d9b1-107">Members</span><span class="sxs-lookup"><span data-stu-id="2d9b1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d9b1-108">**\_ \_ \_ \_ \_ Output flusso flusso di stato della pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="2d9b1-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="2d9b1-109">Crea una nuova istanza non inizializzata di un output del flusso del flusso di \_ stato della pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2d9b1-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT.</span></span>

</dd> <dt>

<span data-ttu-id="2d9b1-110">**Output del flusso di \_ \_ flusso dello stato della pipeline CD3DX12 \_ (output del flusso \_ \_ D3D12 \_ \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="2d9b1-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT(D3D12\_STREAM\_OUTPUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="2d9b1-111">Crea una nuova istanza di un output del flusso di flusso di \_ stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzato con un tipo di sottooggetto di output del flusso di **\_ tipo di oggetto di \_ \_ \_ tipo \_ \_ pipeline D3D12** e dati di sottooggetti copiati da *i*, una struttura di [**\_ \_ output \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) del flusso di D3D12.</span><span class="sxs-lookup"><span data-stu-id="2d9b1-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_STREAM\_OUTPUT** and subobject data copied from *i*, a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2d9b1-112">**operator = ( \_ output flusso \_ D3D12 \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="2d9b1-112">**operator=(D3D12\_STREAM\_OUTPUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="2d9b1-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="2d9b1-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="2d9b1-114">**operatore D3D12 \_ Stream \_ output \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="2d9b1-114">**operator D3D12\_STREAM\_OUTPUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="2d9b1-115">Conversione implicita in una struttura [**\_ desc di \_ output \_ del flusso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="2d9b1-115">Implicit conversion to a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d9b1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d9b1-116">Remarks</span></span>

<span data-ttu-id="2d9b1-117">\_ \_ \_ \_ L'output del flusso di flusso dello stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="2d9b1-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
```



## <a name="requirements"></a><span data-ttu-id="2d9b1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d9b1-118">Requirements</span></span>



| <span data-ttu-id="2d9b1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d9b1-119">Requirement</span></span> | <span data-ttu-id="2d9b1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2d9b1-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9b1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d9b1-121">Header</span></span><br/> | <dl> <span data-ttu-id="2d9b1-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d9b1-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d9b1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d9b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9b1-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="2d9b1-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2d9b1-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d9b1-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="2d9b1-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="2d9b1-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

