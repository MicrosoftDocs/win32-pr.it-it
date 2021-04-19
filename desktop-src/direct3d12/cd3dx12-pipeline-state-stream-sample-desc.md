---
title: Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Struttura di supporto utilizzata per descrivere una descrizione di esempio come singolo oggetto adatto per la descrizione di un flusso.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Struttura CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323576"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="31736-104">\_ \_ \_ \_ Struttura desc di esempio del flusso di stato della pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="31736-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="31736-105">Struttura di supporto utilizzata per descrivere una descrizione di esempio come singolo oggetto adatto per la descrizione di un flusso.</span><span class="sxs-lookup"><span data-stu-id="31736-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="31736-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31736-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="31736-107">Members</span><span class="sxs-lookup"><span data-stu-id="31736-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31736-108">**\_Esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="31736-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="31736-109">Crea una nuova istanza non inizializzata di un \_ esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="31736-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="31736-110">**\_Esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC ( \_ esempio DXGI \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="31736-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="31736-111">Crea una nuova istanza di un \_ esempio di flusso di stato della pipeline CD3DX12 \_ \_ \_ \_ DESC, inizializzato con un tipo di sottooggetto di **esempio di tipo di \_ \_ \_ oggetto sottooggetto stato della pipeline D3D12 \_ \_ \_ desc** e dati di sottooggetti copiati da *i*, una struttura di [**\_ esempio \_ desc DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="31736-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="31736-112">**operator = ( \_ esempio DXGI \_ desc const& i)**</span><span class="sxs-lookup"><span data-stu-id="31736-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="31736-113">Operatore di assegnazione di copia.</span><span class="sxs-lookup"><span data-stu-id="31736-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="31736-114">**operatore DXGI \_ Sample \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="31736-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="31736-115">Conversione implicita in una struttura [**\_ \_ desc di esempio DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .</span><span class="sxs-lookup"><span data-stu-id="31736-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31736-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="31736-116">Remarks</span></span>

<span data-ttu-id="31736-117">\_ \_ \_ Esempio di flusso di stato della pipeline CD3DX12 \_ \_ DESC è una specializzazione typedef del modello di [**\_ \_ \_ \_ sottooggetto flusso di stato della pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="31736-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="31736-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31736-118">Requirements</span></span>



| <span data-ttu-id="31736-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="31736-119">Requirement</span></span> | <span data-ttu-id="31736-120">Valore</span><span class="sxs-lookup"><span data-stu-id="31736-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31736-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31736-121">Header</span></span><br/> | <dl> <span data-ttu-id="31736-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="31736-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31736-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31736-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31736-124">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="31736-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="31736-125">**\_Sottooggetto \_ flusso di stato della pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31736-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="31736-126">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="31736-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

