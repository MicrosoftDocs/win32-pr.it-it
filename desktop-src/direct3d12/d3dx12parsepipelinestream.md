---
title: Funzione D3DX12ParsePipelineStream (D3dx12. h)
description: Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di sottooggetto analizzata.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream (funzione)
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322172"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="dd171-104">D3DX12ParsePipelineStream (funzione)</span><span class="sxs-lookup"><span data-stu-id="dd171-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="dd171-105">Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di sottooggetto analizzata.</span><span class="sxs-lookup"><span data-stu-id="dd171-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd171-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd171-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="dd171-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd171-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd171-108">*Desc* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="dd171-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dd171-109">Tipo: **const [**D3D12 \_ pipeline \_ state \_ Stream \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="dd171-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="dd171-110">Descrizione del flusso di stato della pipeline da analizzare.</span><span class="sxs-lookup"><span data-stu-id="dd171-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="dd171-111">*pCallbacks*</span><span class="sxs-lookup"><span data-stu-id="dd171-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="dd171-112">Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="dd171-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="dd171-113">Struttura che specifica i callback da chiamare per ogni tipo di sottooggetto e callback aggiuntivi da chiamare in caso di errore di analisi.</span><span class="sxs-lookup"><span data-stu-id="dd171-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd171-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd171-114">Return value</span></span>

<span data-ttu-id="dd171-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd171-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd171-116">Questo metodo restituisce un errore HRESULT Success (**S \_ OK** o **E \_ INVALIDARG** se viene rilevato un tipo di sottooggetto sconosciuto, se la descrizione del flusso è vuota, null o contiene oggetti SubObject duplicati, inclusi oggetti SubObject derivati), oppure se *pCallbacks* è null.</span><span class="sxs-lookup"><span data-stu-id="dd171-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="dd171-117">In ogni caso in cui \_ viene restituito E INVALIDARG, viene prima chiamato un callback corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dd171-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd171-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd171-118">Requirements</span></span>



| <span data-ttu-id="dd171-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd171-119">Requirement</span></span> | <span data-ttu-id="dd171-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dd171-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd171-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd171-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dd171-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd171-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="dd171-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd171-123">Library</span></span><br/> | <dl> <span data-ttu-id="dd171-124"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd171-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd171-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd171-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd171-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd171-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd171-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd171-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd171-128">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="dd171-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





