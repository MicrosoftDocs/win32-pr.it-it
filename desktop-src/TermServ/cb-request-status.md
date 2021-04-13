---
title: Enumerazione CB_REQUEST_STATUS (Cbclient. h)
description: Specifica lo stato di una richiesta asincrona.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Enumerazione CB_REQUEST_STATUS Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340533"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="9b75d-104">\_ \_ Enumerazione dello stato della richiesta CB</span><span class="sxs-lookup"><span data-stu-id="9b75d-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="9b75d-105">Specifica lo stato di una richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="9b75d-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="9b75d-106">Questa enumerazione viene utilizzata con il metodo [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="9b75d-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b75d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b75d-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="9b75d-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="9b75d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9b75d-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_stato CB \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="9b75d-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-110">L'oggetto Request non è inizializzato.</span><span class="sxs-lookup"><span data-stu-id="9b75d-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_richiesta di \_ avvio stato \_ CB**</span><span class="sxs-lookup"><span data-stu-id="9b75d-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b75d-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_richiesta di stato CB \_ \_ completata**</span><span class="sxs-lookup"><span data-stu-id="9b75d-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-114">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9b75d-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_richiesta di stato CB \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="9b75d-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-116">Richiesta non riuscita.</span><span class="sxs-lookup"><span data-stu-id="9b75d-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_richiesta di stato CB \_ \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="9b75d-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-118">La richiesta è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="9b75d-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_ \_ destinazione ricerca stato \_ CB**</span><span class="sxs-lookup"><span data-stu-id="9b75d-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b75d-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_ \_ destinazione caricamento stato \_ CB**</span><span class="sxs-lookup"><span data-stu-id="9b75d-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b75d-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**stato CB che \_ \_ porta la \_ sessione \_ online**</span><span class="sxs-lookup"><span data-stu-id="9b75d-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b75d-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b75d-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_Reindirizzamento stato CB \_ \_ a \_ destinazione**</span><span class="sxs-lookup"><span data-stu-id="9b75d-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="9b75d-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b75d-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b75d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b75d-127">Requirements</span></span>



| <span data-ttu-id="9b75d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b75d-128">Requirement</span></span> | <span data-ttu-id="9b75d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9b75d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b75d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b75d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9b75d-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b75d-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="9b75d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b75d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9b75d-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b75d-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="9b75d-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b75d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b75d-135"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b75d-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b75d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b75d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b75d-137">**IConnectionBrokerRequest:: CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="9b75d-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





