---
title: Metodo ID3DX12PipelineParserCallbacks DSCb (D3DX12. h)
description: Chiama il callback del sottooggetto del Domain shader di un oggetto che implementa questa interfaccia.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Metodo DSCb
- Metodo DSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo DSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf5f68ca6e6e4891fa391a142d45a1496a42ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323115"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a><span data-ttu-id="b0fdf-106">ID3DX12PipelineParserCallbacks::D Metodo SCb</span><span class="sxs-lookup"><span data-stu-id="b0fdf-106">ID3DX12PipelineParserCallbacks::DSCb method</span></span>

<span data-ttu-id="b0fdf-107">Chiama il callback del sottooggetto del Domain shader di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b0fdf-107">Calls the domain shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0fdf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0fdf-108">Syntax</span></span>


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a><span data-ttu-id="b0fdf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0fdf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fdf-110">Servizi di *dominio Active Directory* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="b0fdf-110">*DS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b0fdf-111">Tipo: **const [**D3D12 \_ shader \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="b0fdf-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="b0fdf-112">Dettagli del sottooggetto Domain shader analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0fdf-112">Details of the domain shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fdf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0fdf-113">Return value</span></span>

<span data-ttu-id="b0fdf-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="b0fdf-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fdf-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0fdf-115">Requirements</span></span>



| <span data-ttu-id="b0fdf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0fdf-116">Requirement</span></span> | <span data-ttu-id="b0fdf-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b0fdf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fdf-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0fdf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b0fdf-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0fdf-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b0fdf-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0fdf-120">Library</span></span><br/> | <dl> <span data-ttu-id="b0fdf-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0fdf-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0fdf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b0fdf-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0fdf-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0fdf-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0fdf-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0fdf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fdf-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b0fdf-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b0fdf-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b0fdf-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b0fdf-127">**\_BYTECODE shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b0fdf-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





