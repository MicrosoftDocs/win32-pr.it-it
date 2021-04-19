---
title: Metodo ID3DX12PipelineParserCallbacks VSCb (D3DX12. h)
description: Chiama il callback del sottooggetto vertex shader di un oggetto che implementa questa interfaccia.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Metodo VSCb
- Metodo VSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo VSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323092"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a><span data-ttu-id="4914c-106">Metodo ID3DX12PipelineParserCallbacks:: VSCb</span><span class="sxs-lookup"><span data-stu-id="4914c-106">ID3DX12PipelineParserCallbacks::VSCb method</span></span>

<span data-ttu-id="4914c-107">Chiama il callback del sottooggetto vertex shader di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4914c-107">Calls the vertex shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4914c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4914c-108">Syntax</span></span>


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a><span data-ttu-id="4914c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4914c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4914c-110">*Visual* \[ Studio Ref\]</span><span class="sxs-lookup"><span data-stu-id="4914c-110">*VS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4914c-111">Tipo: **const [**D3D12 \_ shader \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="4914c-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="4914c-112">Dettagli del sottooggetto vertex shader analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="4914c-112">Details of the vertex shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4914c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4914c-113">Return value</span></span>

<span data-ttu-id="4914c-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="4914c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4914c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4914c-115">Requirements</span></span>



| <span data-ttu-id="4914c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4914c-116">Requirement</span></span> | <span data-ttu-id="4914c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4914c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4914c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4914c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4914c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4914c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="4914c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4914c-120">Library</span></span><br/> | <dl> <span data-ttu-id="4914c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4914c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="4914c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4914c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4914c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4914c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4914c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4914c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4914c-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4914c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4914c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="4914c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="4914c-127">**\_BYTECODE shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4914c-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





