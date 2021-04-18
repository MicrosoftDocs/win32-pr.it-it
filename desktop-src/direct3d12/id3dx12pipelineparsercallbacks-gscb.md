---
title: Metodo ID3DX12PipelineParserCallbacks GSCb (D3DX12. h)
description: Chiama il callback del sottooggetto geometry shader di un oggetto che implementa questa interfaccia.
ms.assetid: 0D8846C5-15E4-43EB-AA82-163BB514C5B7
keywords:
- Metodo GSCb
- Metodo GSCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo GSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.GSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768e64ccdf06eccce731cafd0d40a9862b695e1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323105"
---
# <a name="id3dx12pipelineparsercallbacksgscb-method"></a><span data-ttu-id="da0b2-106">Metodo ID3DX12PipelineParserCallbacks:: GSCb</span><span class="sxs-lookup"><span data-stu-id="da0b2-106">ID3DX12PipelineParserCallbacks::GSCb method</span></span>

<span data-ttu-id="da0b2-107">Chiama il callback del sottooggetto geometry shader di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="da0b2-107">Calls the geometry shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0b2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da0b2-108">Syntax</span></span>


```C++
void GSCb(
  [ref] const D3D12_SHADER_BYTECODE &GS
);
```



## <a name="parameters"></a><span data-ttu-id="da0b2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="da0b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0b2-110">*GS* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="da0b2-110">*GS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="da0b2-111">Tipo: **const [**D3D12 \_ shader \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="da0b2-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="da0b2-112">Dettagli del sottooggetto geometry shader analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="da0b2-112">Details of the geometry shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da0b2-113">Return value</span></span>

<span data-ttu-id="da0b2-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="da0b2-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0b2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da0b2-115">Requirements</span></span>



| <span data-ttu-id="da0b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="da0b2-116">Requirement</span></span> | <span data-ttu-id="da0b2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="da0b2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da0b2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da0b2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="da0b2-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0b2-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="da0b2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="da0b2-120">Library</span></span><br/> | <dl> <span data-ttu-id="da0b2-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da0b2-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="da0b2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="da0b2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="da0b2-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da0b2-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da0b2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da0b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0b2-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="da0b2-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="da0b2-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="da0b2-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="da0b2-127">**\_BYTECODE shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="da0b2-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





