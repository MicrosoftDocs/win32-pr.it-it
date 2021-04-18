---
description: Richiede l'output del framebuffer della destinazione di rendering, dell'evento e del frame specificati.
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameBufferRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304032"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="5a506-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>Metodo IFrameBufferRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="5a506-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="5a506-104">Richiede l'output del framebuffer della destinazione di rendering, dell'evento e del frame specificati.</span><span class="sxs-lookup"><span data-stu-id="5a506-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a506-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a506-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5a506-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a506-106">Parameters</span></span>

<span data-ttu-id="5a506-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="5a506-107">*frameNumber* </span></span>  
<span data-ttu-id="5a506-108">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="5a506-108">The specified frame.</span></span>

<span data-ttu-id="5a506-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="5a506-109">*eventID* </span></span>  
<span data-ttu-id="5a506-110">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="5a506-110">The specified event.</span></span>

<span data-ttu-id="5a506-111">*renderTargetIndex* </span><span class="sxs-lookup"><span data-stu-id="5a506-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="5a506-112">Indice della destinazione di rendering specificata.</span><span class="sxs-lookup"><span data-stu-id="5a506-112">The index of the specified render target.</span></span>

<span data-ttu-id="5a506-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="5a506-113">*requestCallback* </span></span>  
<span data-ttu-id="5a506-114">Indirizzo di un callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="5a506-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="5a506-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="5a506-115">*requestCookie* </span></span>  
<span data-ttu-id="5a506-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="5a506-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5a506-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="5a506-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5a506-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5a506-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a506-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a506-119">Return value</span></span>

<span data-ttu-id="5a506-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a506-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a506-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a506-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a506-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a506-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5a506-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a506-123">Header</span></span></p></td><td><span data-ttu-id="5a506-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5a506-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5a506-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5a506-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5a506-126">**IFrameBufferRequest**</span><span class="sxs-lookup"><span data-stu-id="5a506-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
