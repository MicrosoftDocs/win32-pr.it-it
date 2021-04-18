---
title: Metodo ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12. h)
description: Chiama il callback del sottooggetto node mask di un oggetto che implementa questa interfaccia.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Metodo NodemaskCb
- Metodo NodemaskCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322158"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="45bf4-106">Metodo ID3DX12PipelineParserCallbacks:: NodemaskCb</span><span class="sxs-lookup"><span data-stu-id="45bf4-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="45bf4-107">Chiama il callback del sottooggetto node mask di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="45bf4-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="45bf4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45bf4-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="45bf4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="45bf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45bf4-110">*Node mask*</span><span class="sxs-lookup"><span data-stu-id="45bf4-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="45bf4-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="45bf4-111">Type: **UINT**</span></span>

<span data-ttu-id="45bf4-112">Dettagli del sottooggetto node mask analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="45bf4-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45bf4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45bf4-113">Return value</span></span>

<span data-ttu-id="45bf4-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="45bf4-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="45bf4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45bf4-115">Requirements</span></span>



| <span data-ttu-id="45bf4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="45bf4-116">Requirement</span></span> | <span data-ttu-id="45bf4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="45bf4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45bf4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45bf4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="45bf4-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="45bf4-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="45bf4-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="45bf4-120">Library</span></span><br/> | <dl> <span data-ttu-id="45bf4-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45bf4-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="45bf4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="45bf4-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="45bf4-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45bf4-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45bf4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45bf4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45bf4-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="45bf4-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="45bf4-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="45bf4-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





