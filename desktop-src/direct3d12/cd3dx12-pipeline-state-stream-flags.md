---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere i flag di stato della pipeline come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323580"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a><span data-ttu-id="41c73-104">\_ \_ \_ Struttura flag del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="41c73-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS structure</span></span>

<span data-ttu-id="41c73-105">Struttura di supporto utilizzata per descrivere i flag di stato della pipeline come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="41c73-105">A helper structure used to describe pipeline state flags as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c73-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41c73-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a><span data-ttu-id="41c73-107">Members</span><span class="sxs-lookup"><span data-stu-id="41c73-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="41c73-108">**\_Flag di \_ flusso dello stato della pipeline \_ CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="41c73-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="41c73-109">Crea una nuova istanza non inizializzata di un \_ flag del flusso di stato della pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41c73-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="41c73-110">**\_Flag di \_ flusso dello stato della pipeline CD3DX12 \_ \_ (flag di \_ stato della pipeline D3D12 \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="41c73-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS(D3D12\_PIPELINE\_STATE\_FLAGS const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="41c73-111">Crea una nuova istanza di un \_ flag di flusso di stato della pipeline CD3DX12 \_ \_ \_ , inizializzato con un tipo di sottooggetto dei flag del **\_ \_ \_ \_ tipo \_** di sottooggetto stato della pipeline D3D12 e i dati di sottooggetti copiati da *i*, una struttura di flag di [**\_ \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="41c73-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_FLAGS** and subobject data copied from *i*, a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> <dt>

<span data-ttu-id="41c73-112">**operator = (D3D12 \_ pipeline \_ state \_ flags const& i)**</span><span class="sxs-lookup"><span data-stu-id="41c73-112">**operator=(D3D12\_PIPELINE\_STATE\_FLAGS const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="41c73-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="41c73-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="41c73-114">**operator D3D12 \_ pipeline \_ flag di stato \_ () const**</span><span class="sxs-lookup"><span data-stu-id="41c73-114">**operator D3D12\_PIPELINE\_STATE\_FLAGS() const**</span></span>
</dt> <dd>

<span data-ttu-id="41c73-115">Conversione implicita in una struttura di [**\_ flag di \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="41c73-115">Implicit conversion to a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c73-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="41c73-116">Remarks</span></span>

<span data-ttu-id="41c73-117">\_ \_ \_ I flag di flusso dello stato della pipeline CD3DX12 \_ sono una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) ed è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="41c73-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a><span data-ttu-id="41c73-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41c73-118">Requirements</span></span>



| <span data-ttu-id="41c73-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c73-119">Requirement</span></span> | <span data-ttu-id="41c73-120">Valore</span><span class="sxs-lookup"><span data-stu-id="41c73-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41c73-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41c73-121">Header</span></span><br/> | <dl> <span data-ttu-id="41c73-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c73-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c73-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41c73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c73-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="41c73-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="41c73-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c73-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="41c73-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="41c73-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

