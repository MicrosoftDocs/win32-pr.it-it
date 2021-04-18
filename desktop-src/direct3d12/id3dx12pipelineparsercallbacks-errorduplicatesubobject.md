---
title: Metodo ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12. h)
description: Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Metodo ErrorDuplicateSubobject
- Metodo ErrorDuplicateSubobject, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo ErrorDuplicateSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323111"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a><span data-ttu-id="b74ff-106">Metodo ID3DX12PipelineParserCallbacks:: ErrorDuplicateSubobject</span><span class="sxs-lookup"><span data-stu-id="b74ff-106">ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject method</span></span>

<span data-ttu-id="b74ff-107">Chiama il callback di errore del sottooggetto duplicato di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b74ff-107">Calls the duplicate subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b74ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b74ff-108">Syntax</span></span>


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a><span data-ttu-id="b74ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b74ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b74ff-110">*DuplicateType*</span><span class="sxs-lookup"><span data-stu-id="b74ff-110">*DuplicateType*</span></span> 
</dt> <dd>

<span data-ttu-id="b74ff-111">Tipo: **[ **\_ \_ \_ \_ tipo di sottooggetto stato della pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span><span class="sxs-lookup"><span data-stu-id="b74ff-111">Type: **[**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span></span>

<span data-ttu-id="b74ff-112">Tipo di sottooggetto duplicato.</span><span class="sxs-lookup"><span data-stu-id="b74ff-112">The subobject type that was duplicated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b74ff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b74ff-113">Return value</span></span>

<span data-ttu-id="b74ff-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="b74ff-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74ff-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b74ff-115">Requirements</span></span>



| <span data-ttu-id="b74ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b74ff-116">Requirement</span></span> | <span data-ttu-id="b74ff-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b74ff-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b74ff-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b74ff-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b74ff-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74ff-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b74ff-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b74ff-120">Library</span></span><br/> | <dl> <span data-ttu-id="b74ff-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b74ff-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b74ff-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b74ff-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b74ff-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b74ff-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b74ff-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b74ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74ff-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b74ff-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b74ff-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b74ff-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b74ff-127">**\_Tipo di \_ \_ sottooggetto stato della pipeline D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b74ff-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

