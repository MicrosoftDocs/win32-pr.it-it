---
title: Metodo ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12. h)
description: Chiama il callback del sottooggetto Descrizione dello stato di Blend di un oggetto che implementa questa interfaccia.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Metodo BlendStateCb
- Metodo BlendStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo BlendStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323122"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a><span data-ttu-id="8936d-106">Metodo ID3DX12PipelineParserCallbacks:: BlendStateCb</span><span class="sxs-lookup"><span data-stu-id="8936d-106">ID3DX12PipelineParserCallbacks::BlendStateCb method</span></span>

<span data-ttu-id="8936d-107">Chiama il callback del sottooggetto Descrizione dello stato di Blend di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8936d-107">Calls the blend state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8936d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8936d-108">Syntax</span></span>


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a><span data-ttu-id="8936d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8936d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8936d-110">*BlendState* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="8936d-110">*BlendState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8936d-111">Tipo: **const [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span><span class="sxs-lookup"><span data-stu-id="8936d-111">Type: **const [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span></span>

<span data-ttu-id="8936d-112">Dettagli del sottooggetto della descrizione dello stato di Blend analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8936d-112">Details of the blend state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8936d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8936d-113">Return value</span></span>

<span data-ttu-id="8936d-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="8936d-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8936d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8936d-115">Requirements</span></span>



| <span data-ttu-id="8936d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8936d-116">Requirement</span></span> | <span data-ttu-id="8936d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8936d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8936d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8936d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8936d-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8936d-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8936d-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="8936d-120">Library</span></span><br/> | <dl> <span data-ttu-id="8936d-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8936d-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8936d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8936d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8936d-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8936d-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8936d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8936d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8936d-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8936d-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8936d-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8936d-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8936d-127">**D3D12 \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8936d-127">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





