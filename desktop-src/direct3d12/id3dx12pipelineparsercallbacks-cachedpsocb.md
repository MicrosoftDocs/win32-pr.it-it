---
title: Metodo ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Chiama il callback del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) di un oggetto che implementa questa interfaccia.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Metodo CachedPSOCb
- Metodo CachedPSOCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323121"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="e6399-106">Metodo ID3DX12PipelineParserCallbacks:: CachedPSOCb</span><span class="sxs-lookup"><span data-stu-id="e6399-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="e6399-107">Chiama il callback del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e6399-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6399-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6399-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="e6399-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6399-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6399-110">*CachedPSO* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="e6399-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e6399-111">Tipo: **const [**D3D12- \_ \_ \_ stato della pipeline memorizzato nella cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="e6399-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="e6399-112">Dettagli del sottooggetto PSO memorizzato nella cache (oggetto stato della pipeline) analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6399-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6399-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6399-113">Return value</span></span>

<span data-ttu-id="e6399-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="e6399-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6399-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6399-115">Requirements</span></span>



| <span data-ttu-id="e6399-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6399-116">Requirement</span></span> | <span data-ttu-id="e6399-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e6399-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6399-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6399-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e6399-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6399-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e6399-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6399-120">Library</span></span><br/> | <dl> <span data-ttu-id="e6399-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6399-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6399-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e6399-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6399-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6399-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6399-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6399-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6399-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e6399-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e6399-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="e6399-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="e6399-127">**\_Stato della pipeline D3D12 memorizzato nella cache \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e6399-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





