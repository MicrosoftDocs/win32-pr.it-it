---
title: Metodo ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Chiama il callback del sottooggetto layout di input di un oggetto che implementa questa interfaccia.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Metodo InputLayoutCb
- Metodo InputLayoutCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323098"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a><span data-ttu-id="c254c-106">Metodo ID3DX12PipelineParserCallbacks:: InputLayoutCb</span><span class="sxs-lookup"><span data-stu-id="c254c-106">ID3DX12PipelineParserCallbacks::InputLayoutCb method</span></span>

<span data-ttu-id="c254c-107">Chiama il callback del sottooggetto layout di input di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c254c-107">Calls the input layout subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c254c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c254c-108">Syntax</span></span>


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a><span data-ttu-id="c254c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c254c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c254c-110">*InputLayout* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="c254c-110">*InputLayout* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c254c-111">Tipo: **const [**D3D12 \_ input \_ layout \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span><span class="sxs-lookup"><span data-stu-id="c254c-111">Type: **const [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span></span>

<span data-ttu-id="c254c-112">Dettagli del sottooggetto layout di input analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="c254c-112">Details of the input layout subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c254c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c254c-113">Return value</span></span>

<span data-ttu-id="c254c-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="c254c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c254c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c254c-115">Requirements</span></span>



| <span data-ttu-id="c254c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c254c-116">Requirement</span></span> | <span data-ttu-id="c254c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c254c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c254c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c254c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c254c-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c254c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c254c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="c254c-120">Library</span></span><br/> | <dl> <span data-ttu-id="c254c-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c254c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c254c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c254c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c254c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c254c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c254c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c254c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c254c-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c254c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c254c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="c254c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="c254c-127">**\_ \_ Descrizione layout input \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="c254c-127">**D3D12\_INPUT\_LAYOUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





