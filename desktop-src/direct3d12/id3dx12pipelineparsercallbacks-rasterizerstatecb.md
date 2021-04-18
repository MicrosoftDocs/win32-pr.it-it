---
title: Metodo ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Chiama il callback del sottooggetto della descrizione dello stato di rasterizzazione di un oggetto che implementa questa interfaccia.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Metodo RasterizerStateCb
- Metodo RasterizerStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323095"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="22bea-106">Metodo ID3DX12PipelineParserCallbacks:: RasterizerStateCb</span><span class="sxs-lookup"><span data-stu-id="22bea-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="22bea-107">Chiama il callback del sottooggetto della descrizione dello stato di rasterizzazione di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="22bea-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="22bea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22bea-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="22bea-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="22bea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22bea-110">*RasterizerState* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="22bea-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="22bea-111">Tipo: **const [**D3D12 \_ rasterizzatore \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span><span class="sxs-lookup"><span data-stu-id="22bea-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="22bea-112">Dettagli del sottooggetto della descrizione dello stato di rasterizzazione analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22bea-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22bea-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22bea-113">Return value</span></span>

<span data-ttu-id="22bea-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="22bea-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="22bea-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22bea-115">Requirements</span></span>



| <span data-ttu-id="22bea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="22bea-116">Requirement</span></span> | <span data-ttu-id="22bea-117">Valore</span><span class="sxs-lookup"><span data-stu-id="22bea-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22bea-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22bea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="22bea-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="22bea-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="22bea-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="22bea-120">Library</span></span><br/> | <dl> <span data-ttu-id="22bea-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22bea-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="22bea-122">DLL</span><span class="sxs-lookup"><span data-stu-id="22bea-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="22bea-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22bea-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22bea-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22bea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22bea-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="22bea-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="22bea-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="22bea-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="22bea-127">**D3D12 \_ rasterizzatore \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="22bea-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





