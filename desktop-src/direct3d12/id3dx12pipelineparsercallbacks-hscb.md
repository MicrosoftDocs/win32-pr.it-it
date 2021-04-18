---
title: Metodo ID3DX12PipelineParserCallbacks HSCb (D3DX12. h)
description: Chiama il callback del sottooggetto Hull shader di un oggetto che implementa questa interfaccia.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Metodo HSCb
- Metodo HSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo HSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7d351e0b3827087cb51c38af173badd28d698c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323104"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a><span data-ttu-id="35eb3-106">Metodo ID3DX12PipelineParserCallbacks:: HSCb</span><span class="sxs-lookup"><span data-stu-id="35eb3-106">ID3DX12PipelineParserCallbacks::HSCb method</span></span>

<span data-ttu-id="35eb3-107">Chiama il callback del sottooggetto Hull shader di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="35eb3-107">Calls the hull shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eb3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35eb3-108">Syntax</span></span>


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a><span data-ttu-id="35eb3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35eb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35eb3-110">*HS* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="35eb3-110">*HS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="35eb3-111">Tipo: **const [**D3D12 \_ shader \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="35eb3-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="35eb3-112">Dettagli del sottooggetto Hull shader analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="35eb3-112">Details of the hull shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35eb3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35eb3-113">Return value</span></span>

<span data-ttu-id="35eb3-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="35eb3-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="35eb3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35eb3-115">Requirements</span></span>



| <span data-ttu-id="35eb3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="35eb3-116">Requirement</span></span> | <span data-ttu-id="35eb3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="35eb3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35eb3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35eb3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="35eb3-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="35eb3-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="35eb3-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="35eb3-120">Library</span></span><br/> | <dl> <span data-ttu-id="35eb3-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35eb3-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="35eb3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="35eb3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="35eb3-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35eb3-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35eb3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35eb3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eb3-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="35eb3-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="35eb3-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="35eb3-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="35eb3-127">**\_BYTECODE shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="35eb3-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





