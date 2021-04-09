---
description: Richiesta asincrona per ottenere informazioni specificate su un singolo frame specificato.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameEventsRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123993"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span data-ttu-id="3b381-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Metodo IFrameEventsRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="3b381-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync method</span></span>

<span data-ttu-id="3b381-104">Richiesta asincrona per ottenere informazioni specificate su un singolo frame specificato.</span><span class="sxs-lookup"><span data-stu-id="3b381-104">An asynchronous request to get specified information about a single specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b381-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b381-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="3b381-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b381-106">Parameters</span></span>

<span data-ttu-id="3b381-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="3b381-107">*frameNumber* </span></span>  
<span data-ttu-id="3b381-108">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="3b381-108">The specified frame.</span></span>

<span data-ttu-id="3b381-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="3b381-109">*numColumns* </span></span>  
<span data-ttu-id="3b381-110">Colonne specificate (campi).</span><span class="sxs-lookup"><span data-stu-id="3b381-110">The specified columns (fields).</span></span>

<span data-ttu-id="3b381-111">*\_colonne count1* </span><span class="sxs-lookup"><span data-stu-id="3b381-111">*count1\_columns* </span></span>  
<span data-ttu-id="3b381-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="3b381-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="3b381-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="3b381-113">*requestCallback* </span></span>  
<span data-ttu-id="3b381-114">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="3b381-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="3b381-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="3b381-115">*requestCookie* </span></span>  
<span data-ttu-id="3b381-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="3b381-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="3b381-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="3b381-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="3b381-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3b381-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b381-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b381-119">Return value</span></span>

<span data-ttu-id="3b381-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b381-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b381-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b381-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b381-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b381-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3b381-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b381-123">Header</span></span></p></td><td><span data-ttu-id="3b381-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3b381-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3b381-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3b381-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3b381-126">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="3b381-126">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
