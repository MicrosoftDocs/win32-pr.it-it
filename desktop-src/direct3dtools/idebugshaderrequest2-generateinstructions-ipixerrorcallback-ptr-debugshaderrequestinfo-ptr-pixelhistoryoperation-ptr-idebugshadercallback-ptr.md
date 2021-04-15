---
description: Richiede la generazione di istruzioni di traccia dello shader in una richiesta di debug. Il debug basato su traccia si verifica sulla CPU (Warp) invece che sulla GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderRequest2:: GenerateInstructions'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521858"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="f993f-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Metodo IDebugShaderRequest2:: GenerateInstructions</span><span class="sxs-lookup"><span data-stu-id="f993f-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="f993f-105">Richiede la generazione di istruzioni di traccia dello shader in una richiesta di debug.</span><span class="sxs-lookup"><span data-stu-id="f993f-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="f993f-106">Il debug basato su traccia si verifica sulla CPU (Warp) invece che sulla GPU.</span><span class="sxs-lookup"><span data-stu-id="f993f-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="f993f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f993f-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="f993f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f993f-108">Parameters</span></span>

<span data-ttu-id="f993f-109">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="f993f-109">*errorCallback* </span></span>  
<span data-ttu-id="f993f-110">Indirizzo di un callback per gli errori che potrebbero verificarsi durante la generazione di istruzioni di traccia dello shader.</span><span class="sxs-lookup"><span data-stu-id="f993f-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="f993f-111">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="f993f-111">*requestInfo* </span></span>  
<span data-ttu-id="f993f-112">Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.</span><span class="sxs-lookup"><span data-stu-id="f993f-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="f993f-113">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="f993f-113">*pPixelHistory* </span></span>  
<span data-ttu-id="f993f-114">Indirizzo dei risultati della Cronologia pixel utilizzati per trovare il pixel associato di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="f993f-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="f993f-115">Si applica solo quando si esegue il debug di un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f993f-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="f993f-116">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="f993f-116">*pCallback* </span></span>  
<span data-ttu-id="f993f-117">Indirizzo di un callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="f993f-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="f993f-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f993f-118">Return value</span></span>

<span data-ttu-id="f993f-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f993f-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f993f-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f993f-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f993f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f993f-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f993f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f993f-122">Header</span></span></p></td><td><span data-ttu-id="f993f-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f993f-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f993f-124"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f993f-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f993f-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="f993f-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
