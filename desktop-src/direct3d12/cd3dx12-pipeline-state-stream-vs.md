---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_VS (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere un vertex shader come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_VS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ea426c857893b98b25792ecc8e6c3d5803546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322222"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a><span data-ttu-id="d34ad-104">\_Struttura del \_ flusso di stato della pipeline CD3DX12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d34ad-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_VS structure</span></span>

<span data-ttu-id="d34ad-105">Struttura di supporto utilizzata per descrivere un vertex shader come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="d34ad-105">A helper structure used to describe a vertex shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34ad-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d34ad-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="d34ad-107">Members</span><span class="sxs-lookup"><span data-stu-id="d34ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d34ad-108">**\_Confronto tra \_ flusso di stato della pipeline CD3DX12 e \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d34ad-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>
</dt> <dd>

<span data-ttu-id="d34ad-109">Crea una nuova istanza non inizializzata di un \_ flusso di stato della pipeline CD3DX12 \_ \_ \_ rispetto a</span><span class="sxs-lookup"><span data-stu-id="d34ad-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_VS.</span></span>

</dd> <dt>

<span data-ttu-id="d34ad-110">**Flusso di stato della pipeline CD3DX12 e \_ \_ \_ \_ (BYTECODE di D3D12 \_ shader \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="d34ad-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="d34ad-111">Crea una nuova istanza di un \_ flusso di stato della pipeline CD3DX12 rispetto a \_ \_ \_ , inizializzato con un tipo di sottooggetto del tipo di sottooggetto stato della pipeline D3D12 e dati di sottooggetti copiati da *i*, una struttura [**\_ \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) **\_ \_ \_ \_ \_ dello** shader D3D12.</span><span class="sxs-lookup"><span data-stu-id="d34ad-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_VS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_VS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d34ad-112">**operator = ( \_ BYTECODE D3D12 shader \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="d34ad-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="d34ad-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="d34ad-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="d34ad-114">**operatore D3D12 \_ shader \_ byte () const**</span><span class="sxs-lookup"><span data-stu-id="d34ad-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="d34ad-115">Conversione implicita in una struttura [**\_ \_ BYTECODE dello shader D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="d34ad-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d34ad-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d34ad-116">Remarks</span></span>

<span data-ttu-id="d34ad-117">\_ \_ \_ Il flusso di stato \_ della pipeline CD3DX12 rispetto a una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="d34ad-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_VS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
```



## <a name="requirements"></a><span data-ttu-id="d34ad-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d34ad-118">Requirements</span></span>



| <span data-ttu-id="d34ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34ad-119">Requirement</span></span> | <span data-ttu-id="d34ad-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d34ad-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d34ad-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d34ad-121">Header</span></span><br/> | <dl> <span data-ttu-id="d34ad-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34ad-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34ad-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d34ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34ad-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="d34ad-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d34ad-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d34ad-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="d34ad-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d34ad-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

