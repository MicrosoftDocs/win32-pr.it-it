---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere un layout di input come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322239"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="46348-104">\_Struttura di \_ \_ layout di input del flusso di stato della \_ pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="46348-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="46348-105">Struttura di supporto utilizzata per descrivere un layout di input come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="46348-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="46348-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46348-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="46348-107">Members</span><span class="sxs-lookup"><span data-stu-id="46348-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="46348-108">**\_Layout di \_ input del flusso di stato della pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46348-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="46348-109">Crea una nuova istanza non inizializzata di un \_ layout di input del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="46348-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="46348-110">**\_Layout di input del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ ( \_ layout input D3D12 \_ \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="46348-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="46348-111">Crea una nuova istanza di un \_ layout di input del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di oggetto suboggetto di un **\_ \_ \_ \_ \_ \_ layout di input del tipo** di sottooggetto D3D12 di stato della pipeline e i dati di sottooggetti copiati da *i*, una struttura di [**\_ \_ layout \_ di input D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="46348-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="46348-112">**operator = ( \_ layout input \_ D3D12 \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="46348-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="46348-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="46348-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="46348-114">**operatore D3D12 \_ input \_ layout \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="46348-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="46348-115">Conversione implicita in una struttura [**\_ \_ \_ desc di layout input D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="46348-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46348-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="46348-116">Remarks</span></span>

<span data-ttu-id="46348-117">\_ \_ \_ \_ \_ Il layout di input del flusso di stato della pipeline CD3DX12 è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="46348-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="46348-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46348-118">Requirements</span></span>



| <span data-ttu-id="46348-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="46348-119">Requirement</span></span> | <span data-ttu-id="46348-120">Valore</span><span class="sxs-lookup"><span data-stu-id="46348-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46348-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46348-121">Header</span></span><br/> | <dl> <span data-ttu-id="46348-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="46348-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46348-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46348-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46348-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="46348-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="46348-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46348-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="46348-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="46348-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

