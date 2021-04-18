---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere la firma radice come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323578"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a><span data-ttu-id="96bbd-104">\_Struttura della \_ \_ \_ firma radice del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="96bbd-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE structure</span></span>

<span data-ttu-id="96bbd-105">Struttura di supporto utilizzata per descrivere la firma radice come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="96bbd-105">A helper structure used to describe the root signature as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="96bbd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96bbd-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a><span data-ttu-id="96bbd-107">Members</span><span class="sxs-lookup"><span data-stu-id="96bbd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="96bbd-108">**\_ \_ \_ Firma radice del flusso dello stato \_ della pipeline \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="96bbd-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="96bbd-109">Crea una nuova istanza non inizializzata di una \_ firma radice del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="96bbd-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE.</span></span>

</dd> <dt>

<span data-ttu-id="96bbd-110">**\_Firma radice del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ (ID3D12RootSignature \* const &i)**</span><span class="sxs-lookup"><span data-stu-id="96bbd-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE(ID3D12RootSignature\* const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="96bbd-111">Crea una nuova istanza di una \_ firma radice del flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzata con un tipo di sottooggetto della **\_ \_ \_ \_ \_ \_ firma radice del tipo** di sottooggetto di stato della pipeline D3D12 e i dati di sottooggetti copiati da *i*, una struttura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="96bbd-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_ROOT\_SIGNATURE** and subobject data copied from *i*, a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure.</span></span>

</dd> <dt>

<span data-ttu-id="96bbd-112">**operator = (ID3D12RootSignature \* const& i)**</span><span class="sxs-lookup"><span data-stu-id="96bbd-112">**operator=(ID3D12RootSignature\* const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="96bbd-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="96bbd-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="96bbd-114">**operatore ID3D12RootSignature \* () const**</span><span class="sxs-lookup"><span data-stu-id="96bbd-114">**operator ID3D12RootSignature\*() const**</span></span>
</dt> <dd>

<span data-ttu-id="96bbd-115">Conversione implicita in un puntatore alla struttura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="96bbd-115">Implicit conversion to a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96bbd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="96bbd-116">Remarks</span></span>

<span data-ttu-id="96bbd-117">\_ \_ \_ \_ La firma radice del flusso di stato della pipeline CD3DX12 \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definita come segue:</span><span class="sxs-lookup"><span data-stu-id="96bbd-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a><span data-ttu-id="96bbd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96bbd-118">Requirements</span></span>



| <span data-ttu-id="96bbd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96bbd-119">Requirement</span></span> | <span data-ttu-id="96bbd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="96bbd-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="96bbd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96bbd-121">Header</span></span><br/> | <dl> <span data-ttu-id="96bbd-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="96bbd-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96bbd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96bbd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96bbd-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="96bbd-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="96bbd-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="96bbd-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="96bbd-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="96bbd-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

