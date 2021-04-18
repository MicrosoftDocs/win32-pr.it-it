---
title: Metodo ID3DX12PipelineParserCallbacks RootSignatureCb (D3DX12. h)
description: Chiama il callback del sottooggetto della firma radice di un oggetto che implementa questa interfaccia.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Metodo RootSignatureCb
- Metodo RootSignatureCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo RootSignatureCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322155"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a><span data-ttu-id="d34ff-106">Metodo ID3DX12PipelineParserCallbacks:: RootSignatureCb</span><span class="sxs-lookup"><span data-stu-id="d34ff-106">ID3DX12PipelineParserCallbacks::RootSignatureCb method</span></span>

<span data-ttu-id="d34ff-107">Chiama il callback del sottooggetto della firma radice di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d34ff-107">Calls the root signature subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d34ff-108">Syntax</span></span>


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a><span data-ttu-id="d34ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d34ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34ff-110">*RootSignature*</span><span class="sxs-lookup"><span data-stu-id="d34ff-110">*RootSignature*</span></span> 
</dt> <dd>

<span data-ttu-id="d34ff-111">Tipo: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span><span class="sxs-lookup"><span data-stu-id="d34ff-111">Type: **[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span></span>

<span data-ttu-id="d34ff-112">Dettagli del sottooggetto della firma radice analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d34ff-112">Details of the root signature subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34ff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d34ff-113">Return value</span></span>

<span data-ttu-id="d34ff-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="d34ff-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d34ff-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d34ff-115">Requirements</span></span>



| <span data-ttu-id="d34ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34ff-116">Requirement</span></span> | <span data-ttu-id="d34ff-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d34ff-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d34ff-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d34ff-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d34ff-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34ff-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d34ff-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="d34ff-120">Library</span></span><br/> | <dl> <span data-ttu-id="d34ff-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d34ff-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d34ff-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d34ff-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d34ff-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34ff-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34ff-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d34ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34ff-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d34ff-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d34ff-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d34ff-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d34ff-127">**ID3D12RootSignature**</span><span class="sxs-lookup"><span data-stu-id="d34ff-127">**ID3D12RootSignature**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

