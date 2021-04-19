---
title: Metodo ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Chiama il callback di errore del parametro di input errato di un oggetto che implementa questa interfaccia.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Metodo ErrorBadInputParameter
- Metodo ErrorBadInputParameter, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323112"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="df72a-106">Metodo ID3DX12PipelineParserCallbacks:: ErrorBadInputParameter</span><span class="sxs-lookup"><span data-stu-id="df72a-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="df72a-107">Chiama il callback di errore del parametro di input errato di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="df72a-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="df72a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df72a-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="df72a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="df72a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df72a-110">*ParameterIndex*</span><span class="sxs-lookup"><span data-stu-id="df72a-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="df72a-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="df72a-111">Type: **UINT**</span></span>

<span data-ttu-id="df72a-112">Posizione del parametro che contiene un input non valido.</span><span class="sxs-lookup"><span data-stu-id="df72a-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="df72a-113">Il parametro più a sinistra si trova nella posizione 1, non nella posizione 0.</span><span class="sxs-lookup"><span data-stu-id="df72a-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df72a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df72a-114">Return value</span></span>

<span data-ttu-id="df72a-115">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="df72a-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="df72a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df72a-116">Requirements</span></span>



| <span data-ttu-id="df72a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df72a-117">Requirement</span></span> | <span data-ttu-id="df72a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="df72a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df72a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df72a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="df72a-120"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="df72a-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="df72a-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="df72a-121">Library</span></span><br/> | <dl> <span data-ttu-id="df72a-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df72a-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="df72a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="df72a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="df72a-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df72a-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df72a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df72a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df72a-126">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="df72a-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="df72a-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="df72a-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





