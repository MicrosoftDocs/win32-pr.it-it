---
title: Metodo ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12. h)
description: Chiama il callback del sottooggetto del tipo di topologia primitivo di un oggetto che implementa questa interfaccia.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Metodo PrimitiveTopologyTypeCb
- Metodo PrimitiveTopologyTypeCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323096"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a><span data-ttu-id="8fbdb-106">ID3DX12PipelineParserCallbacks::P metodo rimitiveTopologyTypeCb</span><span class="sxs-lookup"><span data-stu-id="8fbdb-106">ID3DX12PipelineParserCallbacks::PrimitiveTopologyTypeCb method</span></span>

<span data-ttu-id="8fbdb-107">Chiama il callback del sottooggetto del tipo di topologia primitivo di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8fbdb-107">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbdb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fbdb-108">Syntax</span></span>


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a><span data-ttu-id="8fbdb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fbdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbdb-110">*PrimitiveTopologyType*</span><span class="sxs-lookup"><span data-stu-id="8fbdb-110">*PrimitiveTopologyType*</span></span> 
</dt> <dd>

<span data-ttu-id="8fbdb-111">Tipo: **[ **\_ \_ \_ tipo di topologia primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span><span class="sxs-lookup"><span data-stu-id="8fbdb-111">Type: **[**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span></span>

<span data-ttu-id="8fbdb-112">Dettagli del sottooggetto del tipo di topologia primitivo analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8fbdb-112">Details of the primitive topology type subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbdb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fbdb-113">Return value</span></span>

<span data-ttu-id="8fbdb-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="8fbdb-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbdb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fbdb-115">Requirements</span></span>



| <span data-ttu-id="8fbdb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fbdb-116">Requirement</span></span> | <span data-ttu-id="8fbdb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8fbdb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbdb-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fbdb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8fbdb-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fbdb-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8fbdb-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fbdb-120">Library</span></span><br/> | <dl> <span data-ttu-id="8fbdb-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fbdb-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8fbdb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8fbdb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fbdb-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbdb-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbdb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fbdb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbdb-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8fbdb-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8fbdb-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8fbdb-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8fbdb-127">**\_Tipo di \_ topologia PRIMItiva D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8fbdb-127">**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





