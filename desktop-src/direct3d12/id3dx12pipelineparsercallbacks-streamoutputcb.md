---
title: Metodo ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Chiama il callback del sottooggetto della descrizione di output del flusso di un oggetto che implementa questa interfaccia.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Metodo StreamOutputCb
- Metodo StreamOutputCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322149"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="ac1b2-106">Metodo ID3DX12PipelineParserCallbacks:: StreamOutputCb</span><span class="sxs-lookup"><span data-stu-id="ac1b2-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="ac1b2-107">Chiama il callback del sottooggetto della descrizione di output del flusso di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1b2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac1b2-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="ac1b2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac1b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1b2-110">*StreamOutput* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="ac1b2-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1b2-111">Tipo: **const [**D3D12 \_ Stream \_ output \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span><span class="sxs-lookup"><span data-stu-id="ac1b2-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="ac1b2-112">Dettagli del sottooggetto della descrizione di output del flusso analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac1b2-113">Return value</span></span>

<span data-ttu-id="ac1b2-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="ac1b2-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1b2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac1b2-115">Requirements</span></span>



| <span data-ttu-id="ac1b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac1b2-116">Requirement</span></span> | <span data-ttu-id="ac1b2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ac1b2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1b2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac1b2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ac1b2-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b2-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ac1b2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac1b2-120">Library</span></span><br/> | <dl> <span data-ttu-id="ac1b2-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b2-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac1b2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1b2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac1b2-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac1b2-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac1b2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac1b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1b2-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ac1b2-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ac1b2-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ac1b2-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="ac1b2-127">**\_Desc di \_ output \_ flusso D3D12**</span><span class="sxs-lookup"><span data-stu-id="ac1b2-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





