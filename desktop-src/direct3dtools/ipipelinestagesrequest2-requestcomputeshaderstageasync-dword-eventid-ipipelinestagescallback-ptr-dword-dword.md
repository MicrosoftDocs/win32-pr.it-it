---
description: Richiesta asincrona per ottenere se la fase compute shader è stata usata per il frame e l'evento specificati.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderStageAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest2:: RequestComputeShaderStageAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EC5695A6-70B5-4F7D-A235-974A0A59A44F
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderStageAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec7fe36a35e73ae2d047be11a2d5cf72f65825f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482021"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderstageasync-method"></a><span data-ttu-id="ac6c6-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest2:: RequestComputeShaderStageAsync</span><span class="sxs-lookup"><span data-stu-id="ac6c6-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderStageAsync method</span></span>

<span data-ttu-id="ac6c6-104">Richiesta asincrona per ottenere se la fase compute shader è stata usata per il frame e l'evento specificati.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-104">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac6c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac6c6-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderStageAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ac6c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac6c6-106">Parameters</span></span>

<span data-ttu-id="ac6c6-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="ac6c6-107">*frameNumber* </span></span>  
<span data-ttu-id="ac6c6-108">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-108">The specified frame.</span></span>

<span data-ttu-id="ac6c6-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="ac6c6-109">*eventID* </span></span>  
<span data-ttu-id="ac6c6-110">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-110">The specified event.</span></span>

<span data-ttu-id="ac6c6-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ac6c6-111">*requestCallback* </span></span>  
<span data-ttu-id="ac6c6-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ac6c6-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ac6c6-113">*requestCookie* </span></span>  
<span data-ttu-id="ac6c6-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ac6c6-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ac6c6-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ac6c6-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac6c6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac6c6-117">Return value</span></span>

<span data-ttu-id="ac6c6-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac6c6-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac6c6-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac6c6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac6c6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac6c6-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ac6c6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac6c6-121">Header</span></span></p></td><td><span data-ttu-id="ac6c6-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ac6c6-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ac6c6-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ac6c6-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ac6c6-124">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="ac6c6-124">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
