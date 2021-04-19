---
description: Il \_ metodo Put StartTime imposta il valore dell'ora di avvio NTP (Network Time Protocol) a 32 bit. La sessione è considerata attiva da questo momento.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: 'ITTime: metodo:p ut_StartTime (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326764"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="583fc-104">ITTime::p UT \_ Metodo StartTime</span><span class="sxs-lookup"><span data-stu-id="583fc-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="583fc-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="583fc-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="583fc-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="583fc-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="583fc-107">Il metodo **put \_ StartTime** imposta il valore dell'ora di avvio NTP (Network Time Protocol) a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="583fc-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="583fc-108">La sessione è considerata attiva da questo momento.</span><span class="sxs-lookup"><span data-stu-id="583fc-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="583fc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="583fc-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="583fc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="583fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="583fc-111">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="583fc-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583fc-112">Ora di inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="583fc-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="583fc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="583fc-113">Return value</span></span>

<span data-ttu-id="583fc-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="583fc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="583fc-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="583fc-115">Return code</span></span>                                                                                   | <span data-ttu-id="583fc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="583fc-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="583fc-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="583fc-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="583fc-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="583fc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="583fc-120">Il parametro *Tim* e non è valido.</span><span class="sxs-lookup"><span data-stu-id="583fc-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="583fc-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="583fc-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="583fc-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="583fc-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="583fc-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="583fc-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="583fc-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="583fc-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="583fc-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="583fc-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="583fc-127">Remarks</span></span>

<span data-ttu-id="583fc-128">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="583fc-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="583fc-129">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="583fc-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="583fc-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="583fc-130">Requirements</span></span>



| <span data-ttu-id="583fc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="583fc-131">Requirement</span></span> | <span data-ttu-id="583fc-132">Valore</span><span class="sxs-lookup"><span data-stu-id="583fc-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="583fc-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="583fc-133">TAPI version</span></span><br/> | <span data-ttu-id="583fc-134">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="583fc-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="583fc-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="583fc-135">Header</span></span><br/>       | <dl> <span data-ttu-id="583fc-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="583fc-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="583fc-137">Library</span></span><br/>      | <dl> <span data-ttu-id="583fc-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="583fc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="583fc-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="583fc-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="583fc-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="583fc-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="583fc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="583fc-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="583fc-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="583fc-143">**ITTime:: Get \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="583fc-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




