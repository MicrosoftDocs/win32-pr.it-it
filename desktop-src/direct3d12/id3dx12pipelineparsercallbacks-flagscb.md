---
title: Metodo ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Chiama il callback del sottooggetto Flags di un oggetto che implementa questa interfaccia.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Metodo FlagsCb
- Metodo FlagsCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323107"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="83dfb-106">Metodo ID3DX12PipelineParserCallbacks:: FlagsCb</span><span class="sxs-lookup"><span data-stu-id="83dfb-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="83dfb-107">Chiama il callback del sottooggetto Flags di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="83dfb-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="83dfb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83dfb-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="83dfb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="83dfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83dfb-110">*Flag*</span><span class="sxs-lookup"><span data-stu-id="83dfb-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="83dfb-111">Tipo: **[ **\_ flag di \_ stato \_ della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="83dfb-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="83dfb-112">Dettagli del sottooggetto flag analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="83dfb-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83dfb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83dfb-113">Return value</span></span>

<span data-ttu-id="83dfb-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="83dfb-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="83dfb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83dfb-115">Requirements</span></span>



| <span data-ttu-id="83dfb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83dfb-116">Requirement</span></span> | <span data-ttu-id="83dfb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="83dfb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="83dfb-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83dfb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="83dfb-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="83dfb-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="83dfb-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="83dfb-120">Library</span></span><br/> | <dl> <span data-ttu-id="83dfb-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83dfb-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="83dfb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="83dfb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="83dfb-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83dfb-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83dfb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83dfb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83dfb-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="83dfb-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="83dfb-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="83dfb-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="83dfb-127">**\_Flag di \_ stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="83dfb-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





