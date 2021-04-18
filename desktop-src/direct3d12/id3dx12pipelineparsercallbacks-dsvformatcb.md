---
title: Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) (DSV)
description: Chiama il callback del sottooggetto del formato del valore depth stencil di un oggetto che implementa questa interfaccia.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334359"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="6f856-106">Metodo ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) per depth stencil valore</span><span class="sxs-lookup"><span data-stu-id="6f856-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="6f856-107">Chiama il callback del sottooggetto del formato del valore depth stencil di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6f856-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f856-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f856-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="6f856-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f856-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f856-110">*DepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="6f856-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="6f856-111">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="6f856-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="6f856-112">Dettagli del depth stencil oggetto del formato del valore analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f856-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f856-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f856-113">Return value</span></span>

<span data-ttu-id="6f856-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="6f856-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f856-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f856-115">Requirements</span></span>



| <span data-ttu-id="6f856-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f856-116">Requirement</span></span> | <span data-ttu-id="6f856-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6f856-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f856-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f856-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6f856-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f856-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6f856-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f856-120">Library</span></span><br/> | <dl> <span data-ttu-id="6f856-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f856-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f856-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6f856-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6f856-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f856-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f856-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f856-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f856-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6f856-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6f856-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="6f856-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="6f856-127">**\_formato DXGI**</span><span class="sxs-lookup"><span data-stu-id="6f856-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

