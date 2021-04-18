---
title: Metodo ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Chiama il callback del sottooggetto del valore della riduzione del buffer di indice di un oggetto che implementa questa interfaccia.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Metodo IBStripCutValueCb
- Metodo IBStripCutValueCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323102"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="46942-106">Metodo ID3DX12PipelineParserCallbacks:: IBStripCutValueCb</span><span class="sxs-lookup"><span data-stu-id="46942-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="46942-107">Chiama il callback del sottooggetto del valore della riduzione del buffer di indice di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="46942-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="46942-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46942-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="46942-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="46942-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46942-110">*IBStripCutValue*</span><span class="sxs-lookup"><span data-stu-id="46942-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="46942-111">Tipo: **[ **D3D12 \_ index \_ buffer \_ \_ Cut Stripe \_ value**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="46942-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="46942-112">Dettagli del sottooggetto del valore di strip-cut buffer index analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="46942-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46942-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46942-113">Return value</span></span>

<span data-ttu-id="46942-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="46942-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="46942-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46942-115">Requirements</span></span>



| <span data-ttu-id="46942-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="46942-116">Requirement</span></span> | <span data-ttu-id="46942-117">Valore</span><span class="sxs-lookup"><span data-stu-id="46942-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="46942-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46942-118">Header</span></span><br/>  | <dl> <span data-ttu-id="46942-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="46942-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="46942-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="46942-120">Library</span></span><br/> | <dl> <span data-ttu-id="46942-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46942-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="46942-122">DLL</span><span class="sxs-lookup"><span data-stu-id="46942-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="46942-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46942-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46942-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46942-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46942-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="46942-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="46942-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="46942-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="46942-127">**\_ \_ \_ \_ Valore Cut Strip buffer index \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="46942-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





