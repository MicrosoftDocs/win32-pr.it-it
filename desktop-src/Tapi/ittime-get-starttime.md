---
description: Il \_ metodo Get StartTime ottiene il valore dell'ora di avvio NTP (Network Time Protocol) a 32 bit. La sessione è considerata attiva da questo momento.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'Metodo ITTime:: get_StartTime (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326767"
---
# <a name="ittimeget_starttime-method"></a><span data-ttu-id="2c75f-104">Metodo ITTime:: Get \_ StartTime</span><span class="sxs-lookup"><span data-stu-id="2c75f-104">ITTime::get\_StartTime method</span></span>

<span data-ttu-id="2c75f-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2c75f-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c75f-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2c75f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2c75f-107">Il metodo **get \_ StartTime** ottiene il valore dell'ora di avvio NTP (Network Time Protocol) a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2c75f-107">The **get\_StartTime** method gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="2c75f-108">La sessione è considerata attiva da questo momento.</span><span class="sxs-lookup"><span data-stu-id="2c75f-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c75f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c75f-109">Syntax</span></span>


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="2c75f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c75f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c75f-111">*pTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2c75f-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c75f-112">Puntatore all'ora di inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="2c75f-112">Pointer to the start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c75f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c75f-113">Return value</span></span>

<span data-ttu-id="2c75f-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2c75f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2c75f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2c75f-115">Return code</span></span>                                                                                   | <span data-ttu-id="2c75f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c75f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2c75f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2c75f-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2c75f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2c75f-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2c75f-120">Il parametro *pTime* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="2c75f-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="2c75f-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2c75f-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c75f-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2c75f-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2c75f-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2c75f-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2c75f-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2c75f-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="2c75f-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2c75f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c75f-127">Requirements</span></span>



| <span data-ttu-id="2c75f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c75f-128">Requirement</span></span> | <span data-ttu-id="2c75f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2c75f-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c75f-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2c75f-130">TAPI version</span></span><br/> | <span data-ttu-id="2c75f-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2c75f-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2c75f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c75f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="2c75f-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c75f-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c75f-134">Library</span></span><br/>      | <dl> <span data-ttu-id="2c75f-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2c75f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2c75f-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="2c75f-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c75f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c75f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c75f-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="2c75f-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="2c75f-140">**ITTime::p \_**</span><span class="sxs-lookup"><span data-stu-id="2c75f-140">**ITTime::put\_StartTime**</span></span>](ittime-put-starttime.md)
</dt> </dl>

 

 




