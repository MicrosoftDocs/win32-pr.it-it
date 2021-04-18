---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)
description: Chiama il callback del sottooggetto stato depth stencil di un oggetto che implementa questa interfaccia.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Metodo DepthStencilStateCb
- Metodo DepthStencilStateCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322160"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="23c80-106">Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="23c80-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="23c80-107">Chiama il callback del sottooggetto stato depth stencil di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="23c80-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c80-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23c80-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="23c80-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="23c80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c80-110">*DepthStencilState* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="23c80-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23c80-111">Tipo: **const [**D3D12 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span><span class="sxs-lookup"><span data-stu-id="23c80-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="23c80-112">Dettagli del sottooggetto depth stencil stato analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="23c80-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23c80-113">Return value</span></span>

<span data-ttu-id="23c80-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="23c80-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="23c80-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23c80-115">Requirements</span></span>



| <span data-ttu-id="23c80-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c80-116">Requirement</span></span> | <span data-ttu-id="23c80-117">Valore</span><span class="sxs-lookup"><span data-stu-id="23c80-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23c80-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23c80-118">Header</span></span><br/>  | <dl> <span data-ttu-id="23c80-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c80-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="23c80-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="23c80-120">Library</span></span><br/> | <dl> <span data-ttu-id="23c80-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23c80-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="23c80-122">DLL</span><span class="sxs-lookup"><span data-stu-id="23c80-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="23c80-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23c80-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c80-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23c80-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c80-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="23c80-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="23c80-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="23c80-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="23c80-127">**D3D12 \_ Depth \_ stencil \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="23c80-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





