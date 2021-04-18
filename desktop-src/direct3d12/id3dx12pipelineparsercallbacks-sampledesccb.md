---
title: Metodo ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Chiama il callback di esempio della descrizione del sottooggetto di un oggetto che implementa questa interfaccia.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Metodo SampleDescCb
- Metodo SampleDescCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322151"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="88f4f-106">Metodo ID3DX12PipelineParserCallbacks:: SampleDescCb</span><span class="sxs-lookup"><span data-stu-id="88f4f-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="88f4f-107">Chiama il callback di esempio della descrizione del sottooggetto di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="88f4f-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f4f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88f4f-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="88f4f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88f4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f4f-110">*SampleDesc* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="88f4f-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="88f4f-111">Tipo: **const [**DXGI \_ Sample \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span><span class="sxs-lookup"><span data-stu-id="88f4f-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="88f4f-112">Dettagli del sottooggetto Descrizione di esempio analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="88f4f-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88f4f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88f4f-113">Return value</span></span>

<span data-ttu-id="88f4f-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="88f4f-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="88f4f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88f4f-115">Requirements</span></span>



| <span data-ttu-id="88f4f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f4f-116">Requirement</span></span> | <span data-ttu-id="88f4f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="88f4f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="88f4f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88f4f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88f4f-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="88f4f-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="88f4f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="88f4f-120">Library</span></span><br/> | <dl> <span data-ttu-id="88f4f-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88f4f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="88f4f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="88f4f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="88f4f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f4f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f4f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88f4f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f4f-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="88f4f-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="88f4f-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="88f4f-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="88f4f-127">**DXGI di \_ esempio \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="88f4f-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

