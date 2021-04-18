---
description: Richiesta asincrona per ottenere un elenco di fasi usate per il frame e l'evento specificati.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest:: RequestSupportedStagesAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304309"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="150e5-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest:: RequestSupportedStagesAsync</span><span class="sxs-lookup"><span data-stu-id="150e5-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="150e5-104">Richiesta asincrona per ottenere un elenco di fasi usate per il frame e l'evento specificati.</span><span class="sxs-lookup"><span data-stu-id="150e5-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="150e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="150e5-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="150e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="150e5-106">Parameters</span></span>

<span data-ttu-id="150e5-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="150e5-107">*frameNumber* </span></span>  
<span data-ttu-id="150e5-108">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="150e5-108">The specified frame.</span></span>

<span data-ttu-id="150e5-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="150e5-109">*eventID* </span></span>  
<span data-ttu-id="150e5-110">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="150e5-110">The specified event.</span></span>

<span data-ttu-id="150e5-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="150e5-111">*requestCallback* </span></span>  
<span data-ttu-id="150e5-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="150e5-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="150e5-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="150e5-113">*requestCookie* </span></span>  
<span data-ttu-id="150e5-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="150e5-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="150e5-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="150e5-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="150e5-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="150e5-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="150e5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="150e5-117">Return value</span></span>

<span data-ttu-id="150e5-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="150e5-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="150e5-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="150e5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="150e5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="150e5-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="150e5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="150e5-121">Header</span></span></p></td><td><span data-ttu-id="150e5-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="150e5-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="150e5-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="150e5-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="150e5-124">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="150e5-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
