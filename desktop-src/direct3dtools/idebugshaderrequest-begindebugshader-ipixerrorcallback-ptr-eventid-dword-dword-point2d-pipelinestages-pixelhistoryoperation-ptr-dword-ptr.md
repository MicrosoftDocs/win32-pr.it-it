---
description: Richiede l'avvio di una sessione di debug dello shader per la fase della pipeline specificata, il pixel/vertice, se applicabile, l'evento e il frame.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderRequest:: BeginDebugShader'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124632"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="49f73-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Metodo IDebugShaderRequest:: BeginDebugShader</span><span class="sxs-lookup"><span data-stu-id="49f73-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="49f73-104">Richiede l'avvio di una sessione di debug dello shader per la fase della pipeline specificata, il pixel/vertice, se applicabile, l'evento e il frame.</span><span class="sxs-lookup"><span data-stu-id="49f73-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f73-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49f73-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="49f73-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49f73-106">Parameters</span></span>

<span data-ttu-id="49f73-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="49f73-107">*errorCallback* </span></span>  
<span data-ttu-id="49f73-108">Indirizzo di un callback per gli errori che potrebbero verificarsi durante il debug.</span><span class="sxs-lookup"><span data-stu-id="49f73-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="49f73-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="49f73-109">*eventID* </span></span>  
<span data-ttu-id="49f73-110">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="49f73-110">The specified event.</span></span>

<span data-ttu-id="49f73-111">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="49f73-111">*frameNumber* </span></span>  
<span data-ttu-id="49f73-112">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="49f73-112">The specified frame.</span></span>

<span data-ttu-id="49f73-113">*vertice* </span><span class="sxs-lookup"><span data-stu-id="49f73-113">*vertex* </span></span>  
<span data-ttu-id="49f73-114">Vertice specificato.</span><span class="sxs-lookup"><span data-stu-id="49f73-114">The specified vertex.</span></span> <span data-ttu-id="49f73-115">Si applica solo quando si esegue il debug di un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="49f73-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="49f73-116">*pixel* </span><span class="sxs-lookup"><span data-stu-id="49f73-116">*pixel* </span></span>  
<span data-ttu-id="49f73-117">Pixel specificato.</span><span class="sxs-lookup"><span data-stu-id="49f73-117">The specified pixel.</span></span> <span data-ttu-id="49f73-118">Si applica solo quando si esegue il debug di un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="49f73-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="49f73-119">*fase* </span><span class="sxs-lookup"><span data-stu-id="49f73-119">*stage* </span></span>  
<span data-ttu-id="49f73-120">Fase della pipeline specificata.</span><span class="sxs-lookup"><span data-stu-id="49f73-120">The specified pipeline stage.</span></span>

<span data-ttu-id="49f73-121">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="49f73-121">*pPixelHistory* </span></span>  
<span data-ttu-id="49f73-122">Indirizzo dei risultati della Cronologia pixel utilizzati per trovare il pixel associato di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="49f73-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="49f73-123">Si applica solo quando si esegue il debug di un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="49f73-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="49f73-124">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="49f73-124">*pDevice* </span></span>  
<span data-ttu-id="49f73-125">Indirizzo da passare al motore di debug per la comunicazione con questa sessione di debug (motore di debug ReadProcessMemory su questo indirizzo).</span><span class="sxs-lookup"><span data-stu-id="49f73-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="49f73-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49f73-126">Return value</span></span>

<span data-ttu-id="49f73-127">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49f73-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49f73-128">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49f73-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f73-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49f73-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="49f73-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49f73-130">Header</span></span></p></td><td><span data-ttu-id="49f73-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="49f73-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="49f73-132"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="49f73-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="49f73-133">**IDebugShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="49f73-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
