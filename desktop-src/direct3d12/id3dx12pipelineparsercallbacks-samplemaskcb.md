---
title: Metodo ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Chiama il callback del sottooggetto maschera di esempio di un oggetto che implementa questa interfaccia.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Metodo SampleMaskCb
- Metodo SampleMaskCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322150"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="4a9ab-106">Metodo ID3DX12PipelineParserCallbacks:: SampleMaskCb</span><span class="sxs-lookup"><span data-stu-id="4a9ab-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="4a9ab-107">Chiama il callback del sottooggetto maschera di esempio di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4a9ab-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a9ab-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="4a9ab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a9ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a9ab-110">*SampleMask*</span><span class="sxs-lookup"><span data-stu-id="4a9ab-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="4a9ab-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4a9ab-111">Type: **UINT**</span></span>

<span data-ttu-id="4a9ab-112">Dettagli del sottooggetto maschera di esempio analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a9ab-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a9ab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a9ab-113">Return value</span></span>

<span data-ttu-id="4a9ab-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="4a9ab-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a9ab-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a9ab-115">Requirements</span></span>



| <span data-ttu-id="4a9ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a9ab-116">Requirement</span></span> | <span data-ttu-id="4a9ab-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4a9ab-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9ab-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a9ab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4a9ab-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a9ab-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4a9ab-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a9ab-120">Library</span></span><br/> | <dl> <span data-ttu-id="4a9ab-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a9ab-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a9ab-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4a9ab-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a9ab-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a9ab-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a9ab-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a9ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9ab-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4a9ab-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4a9ab-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="4a9ab-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





