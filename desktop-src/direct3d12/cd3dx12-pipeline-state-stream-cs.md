---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_CS (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere un compute shader come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: B76B0CB4-FC76-4C5B-84FC-DCFF907BE2F8
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_CS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5796e0f96ad4e2a87d2a45519321c363078a34b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322257"
---
# <a name="cd3dx12_pipeline_state_stream_cs-structure"></a><span data-ttu-id="9fd5f-104">\_ \_ \_ Struttura CS del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="9fd5f-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CS structure</span></span>

<span data-ttu-id="9fd5f-105">Struttura di supporto utilizzata per descrivere un compute shader come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="9fd5f-105">A helper structure used to describe a compute shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd5f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fd5f-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CS {
                                   CD3DX12_PIPELINE_STATE_STREAM_CS;
                                   CD3DX12_PIPELINE_STATE_STREAM_CS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="9fd5f-107">Members</span><span class="sxs-lookup"><span data-stu-id="9fd5f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9fd5f-108">**\_ \_ CS flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fd5f-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5f-109">Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9fd5f-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CS.</span></span>

</dd> <dt>

<span data-ttu-id="9fd5f-110">**CD3DX12 \_ pipeline \_ state \_ Stream \_ cs (D3D12 \_ shader \_ BYTECODE const &i)**</span><span class="sxs-lookup"><span data-stu-id="9fd5f-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5f-111">Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ , inizializzato con un tipo di sottooggetto del **tipo di oggetto di stato della pipeline D3D12 \_ \_ \_ \_ \_ CS** e i dati di sottooggetti copiati da *i*, una struttura [**\_ \_ BYTECODE dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="9fd5f-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9fd5f-112">**operator = ( \_ BYTECODE D3D12 shader \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="9fd5f-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5f-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="9fd5f-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="9fd5f-114">**operatore D3D12 \_ shader \_ byte () const**</span><span class="sxs-lookup"><span data-stu-id="9fd5f-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="9fd5f-115">Conversione implicita in una struttura [**\_ \_ BYTECODE dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="9fd5f-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fd5f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fd5f-116">Remarks</span></span>

<span data-ttu-id="9fd5f-117">\_ \_ \_ Il flusso di stato \_ della pipeline CD3DX12 CS è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="9fd5f-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS>
    CD3DX12_PIPELINE_STATE_STREAM_CS;
          
```



## <a name="requirements"></a><span data-ttu-id="9fd5f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fd5f-118">Requirements</span></span>



| <span data-ttu-id="9fd5f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd5f-119">Requirement</span></span> | <span data-ttu-id="9fd5f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9fd5f-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd5f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fd5f-121">Header</span></span><br/> | <dl> <span data-ttu-id="9fd5f-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd5f-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd5f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fd5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd5f-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="9fd5f-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9fd5f-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fd5f-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="9fd5f-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="9fd5f-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

