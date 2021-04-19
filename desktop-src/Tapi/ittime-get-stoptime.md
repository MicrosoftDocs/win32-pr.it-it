---
description: Il \_ metodo Get StopTime ottiene il valore dell'ora di fine NTP (Network Time Protocol). Se l'ora di fine è zero, la sessione non è associata.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'Metodo ITTime:: get_StopTime (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326765"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="2a300-104">Metodo ITTime:: Get \_ StopTime</span><span class="sxs-lookup"><span data-stu-id="2a300-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="2a300-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2a300-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a300-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2a300-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2a300-107">Il metodo **get \_ StopTime** ottiene il valore dell'ora di fine NTP (Network Time Protocol).</span><span class="sxs-lookup"><span data-stu-id="2a300-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="2a300-108">Se l'ora di fine è zero, la sessione non è associata.</span><span class="sxs-lookup"><span data-stu-id="2a300-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a300-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a300-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="2a300-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a300-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a300-111">*pTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2a300-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a300-112">Puntatore all'ora di arresto della sessione.</span><span class="sxs-lookup"><span data-stu-id="2a300-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a300-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a300-113">Return value</span></span>

<span data-ttu-id="2a300-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2a300-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2a300-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2a300-115">Return code</span></span>                                                                                   | <span data-ttu-id="2a300-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a300-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2a300-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2a300-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2a300-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2a300-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2a300-120">Il parametro *pTime* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="2a300-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="2a300-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2a300-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2a300-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a300-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2a300-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2a300-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2a300-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2a300-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="2a300-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2a300-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a300-127">Requirements</span></span>



| <span data-ttu-id="2a300-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a300-128">Requirement</span></span> | <span data-ttu-id="2a300-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2a300-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a300-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2a300-130">TAPI version</span></span><br/> | <span data-ttu-id="2a300-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2a300-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2a300-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a300-132">Header</span></span><br/>       | <dl> <span data-ttu-id="2a300-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a300-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="2a300-134">Library</span></span><br/>      | <dl> <span data-ttu-id="2a300-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2a300-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2a300-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="2a300-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a300-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a300-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a300-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a300-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="2a300-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="2a300-140">**ITTime::p UT \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="2a300-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




