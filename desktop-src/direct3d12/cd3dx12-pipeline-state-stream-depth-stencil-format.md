---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere il formato depth stencil come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322256"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="86887-104">\_ \_ \_ \_ \_ Struttura formato stencil profondità flusso dello stato della pipeline \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="86887-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="86887-105">Struttura di supporto utilizzata per descrivere il formato depth stencil come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="86887-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="86887-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86887-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="86887-107">Members</span><span class="sxs-lookup"><span data-stu-id="86887-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="86887-108">**\_ \_ \_ \_ \_ Formato stencil profondità flusso dello stato della pipeline \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="86887-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="86887-109">Crea una nuova istanza non inizializzata di un \_ \_ formato dello stencil di profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="86887-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="86887-110">**\_ \_ Formato stencil profondità flusso dello stato della pipeline CD3DX12 \_ \_ \_ \_ ( \_ formato DXGI const &i)**</span><span class="sxs-lookup"><span data-stu-id="86887-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="86887-111">Crea una nuova istanza di un \_ \_ formato dello stencil di profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ \_ , inizializzato con un tipo di sottooggetto del formato dello stencil di profondità del tipo di sottooggetto **stato della \_ pipeline \_ \_ \_ \_ \_ \_ D3D12** e dati di sottooggetti copiati da i, un'enumerazione di [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="86887-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="86887-112">**operator = ( \_ formato DXGI const& i)**</span><span class="sxs-lookup"><span data-stu-id="86887-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="86887-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="86887-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="86887-114">**operatore DXGI \_ Format () const**</span><span class="sxs-lookup"><span data-stu-id="86887-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="86887-115">Conversione implicita in un'enumerazione del [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="86887-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86887-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="86887-116">Remarks</span></span>

<span data-ttu-id="86887-117">\_ \_ \_ Il formato dello stencil di profondità del flusso dello stato della pipeline CD3DX12 \_ \_ \_ è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="86887-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="86887-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86887-118">Requirements</span></span>



| <span data-ttu-id="86887-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86887-119">Requirement</span></span> | <span data-ttu-id="86887-120">Valore</span><span class="sxs-lookup"><span data-stu-id="86887-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86887-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86887-121">Header</span></span><br/> | <dl> <span data-ttu-id="86887-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="86887-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86887-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86887-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86887-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="86887-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="86887-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="86887-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="86887-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="86887-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

