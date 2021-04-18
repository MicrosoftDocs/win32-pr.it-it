---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Chiama lo stato depth stencil (D3D12 \_ Depth \_ stencil \_ DESC1) callback di un oggetto che implementa questa interfaccia.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Metodo DepthStencilState1Cb
- Metodo DepthStencilState1Cb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322159"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a><span data-ttu-id="7732a-106">ID3DX12PipelineParserCallbacks::D Metodo epthStencilState1Cb</span><span class="sxs-lookup"><span data-stu-id="7732a-106">ID3DX12PipelineParserCallbacks::DepthStencilState1Cb method</span></span>

<span data-ttu-id="7732a-107">Chiama lo stato depth stencil ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) callback di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7732a-107">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7732a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7732a-108">Syntax</span></span>


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="7732a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7732a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7732a-110">*DepthStencilState* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="7732a-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7732a-111">Tipo: **const [**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span><span class="sxs-lookup"><span data-stu-id="7732a-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span></span>

<span data-ttu-id="7732a-112">Dettagli del sottooggetto depth stencil stato analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="7732a-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7732a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7732a-113">Return value</span></span>

<span data-ttu-id="7732a-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="7732a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7732a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7732a-115">Requirements</span></span>



| <span data-ttu-id="7732a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7732a-116">Requirement</span></span> | <span data-ttu-id="7732a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7732a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7732a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7732a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7732a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7732a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7732a-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="7732a-120">Library</span></span><br/> | <dl> <span data-ttu-id="7732a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7732a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7732a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7732a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7732a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7732a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7732a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7732a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7732a-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7732a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7732a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="7732a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="7732a-127">**\_Stencil profondità \_ D3D12 \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="7732a-127">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





