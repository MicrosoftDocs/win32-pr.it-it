---
title: Metodo ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Chiama il callback di errore del sottooggetto sconosciuto di un oggetto che implementa questa interfaccia.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Metodo ErrorUnknownSubobject
- Metodo ErrorUnknownSubobject, interfaccia ID3DX12PipelineParserCallbacks
- Interfaccia ID3DX12PipelineParserCallbacks, metodo ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323109"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="76439-106">Metodo ID3DX12PipelineParserCallbacks:: ErrorUnknownSubobject</span><span class="sxs-lookup"><span data-stu-id="76439-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="76439-107">Chiama il callback di errore del sottooggetto sconosciuto di un oggetto che implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="76439-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="76439-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76439-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="76439-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="76439-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76439-110">*UnknownTypeValue*</span><span class="sxs-lookup"><span data-stu-id="76439-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="76439-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="76439-111">Type: **UINT**</span></span>

<span data-ttu-id="76439-112">Tipo di sottooggetto non riconosciuto del tentativo del sottooggetto.</span><span class="sxs-lookup"><span data-stu-id="76439-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76439-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76439-113">Return value</span></span>

<span data-ttu-id="76439-114">Non restituisce alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="76439-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="76439-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76439-115">Requirements</span></span>



| <span data-ttu-id="76439-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="76439-116">Requirement</span></span> | <span data-ttu-id="76439-117">Valore</span><span class="sxs-lookup"><span data-stu-id="76439-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76439-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76439-118">Header</span></span><br/>  | <dl> <span data-ttu-id="76439-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="76439-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="76439-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="76439-120">Library</span></span><br/> | <dl> <span data-ttu-id="76439-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76439-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="76439-122">DLL</span><span class="sxs-lookup"><span data-stu-id="76439-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="76439-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76439-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76439-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76439-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76439-125">Interfacce helper per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="76439-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="76439-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="76439-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





