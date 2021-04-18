---
title: Metodo ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Chiama il callback del sottooggetto della matrice del formato della destinazione di rendering di un oggetto che implementa questa interfaccia.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Metodo RTVFormatsCb
- Metodo RTVFormatsCb, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323094"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="2135a-106">Metodo ID3DX12PipelineParserCallbacks:: RTVFormatsCb</span><span class="sxs-lookup"><span data-stu-id="2135a-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="2135a-107">Chiama il callback del sottooggetto della matrice del formato della destinazione di rendering di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2135a-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2135a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2135a-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="2135a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2135a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2135a-110">*RTVFormats* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="2135a-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2135a-111">Tipo: **const [**D3D12 \_ RT \_ Format \_ Array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="2135a-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="2135a-112">Dettagli del sottooggetto di matrice del formato della destinazione di rendering analizzato da un flusso di stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="2135a-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2135a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2135a-113">Return value</span></span>

<span data-ttu-id="2135a-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="2135a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2135a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2135a-115">Requirements</span></span>



| <span data-ttu-id="2135a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2135a-116">Requirement</span></span> | <span data-ttu-id="2135a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2135a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2135a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2135a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2135a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2135a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2135a-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="2135a-120">Library</span></span><br/> | <dl> <span data-ttu-id="2135a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2135a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2135a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2135a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2135a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2135a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2135a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2135a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2135a-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2135a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2135a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="2135a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="2135a-127">**\_Matrice di \_ formato D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="2135a-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





