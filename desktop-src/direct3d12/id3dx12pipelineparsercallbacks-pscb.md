---
title: Metodo ID3DX12PipelineParserCallbacks PSCb (D3DX12. h)
description: Chiama il callback pixel shader sottooggetto di un oggetto che implementa questa interfaccia.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Metodo PSCb
- Metodo PSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo PSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c972702c215556b953797a6e332f8e86c480b094
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322157"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a><span data-ttu-id="78bf1-106">ID3DX12PipelineParserCallbacks::P metodo SCb</span><span class="sxs-lookup"><span data-stu-id="78bf1-106">ID3DX12PipelineParserCallbacks::PSCb method</span></span>

<span data-ttu-id="78bf1-107">Chiama il callback pixel shader sottooggetto di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="78bf1-107">Calls the pixel shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="78bf1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78bf1-108">Syntax</span></span>


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a><span data-ttu-id="78bf1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="78bf1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78bf1-110">*PS* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="78bf1-110">*PS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="78bf1-111">Tipo: **const [**D3D12 \_ shader \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="78bf1-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="78bf1-112">Dettagli del pixel shader sottooggetto analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="78bf1-112">Details of the pixel shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78bf1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78bf1-113">Return value</span></span>

<span data-ttu-id="78bf1-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="78bf1-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="78bf1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78bf1-115">Requirements</span></span>



| <span data-ttu-id="78bf1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="78bf1-116">Requirement</span></span> | <span data-ttu-id="78bf1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="78bf1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="78bf1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78bf1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="78bf1-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="78bf1-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="78bf1-120">Library</span></span><br/> | <dl> <span data-ttu-id="78bf1-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="78bf1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="78bf1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="78bf1-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78bf1-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78bf1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78bf1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78bf1-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="78bf1-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="78bf1-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="78bf1-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="78bf1-127">**\_BYTECODE shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="78bf1-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





