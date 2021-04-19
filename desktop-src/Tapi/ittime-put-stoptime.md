---
description: Il \_ metodo Put StopTime imposta il valore dell'ora di fine del protocollo NTP (Network Time Protocol). Se l'ora di fine è zero, la sessione non è associata.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'ITTime: metodo:p ut_StopTime (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326762"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="9aae8-104">ITTime::p UT \_ StopTime metodo</span><span class="sxs-lookup"><span data-stu-id="9aae8-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="9aae8-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9aae8-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9aae8-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9aae8-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9aae8-107">Il metodo **put \_ StopTime** imposta il valore dell'ora di fine del protocollo NTP (Network Time Protocol).</span><span class="sxs-lookup"><span data-stu-id="9aae8-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="9aae8-108">Se l'ora di fine è zero, la sessione non è associata.</span><span class="sxs-lookup"><span data-stu-id="9aae8-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aae8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9aae8-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="9aae8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9aae8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aae8-111">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9aae8-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aae8-112">Tempo di arresto per la sessione.</span><span class="sxs-lookup"><span data-stu-id="9aae8-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aae8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9aae8-113">Return value</span></span>

<span data-ttu-id="9aae8-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9aae8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9aae8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9aae8-115">Return code</span></span>                                                                                   | <span data-ttu-id="9aae8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aae8-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9aae8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9aae8-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9aae8-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9aae8-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9aae8-120">Il parametro *Time* non è valido.</span><span class="sxs-lookup"><span data-stu-id="9aae8-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="9aae8-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9aae8-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9aae8-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9aae8-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9aae8-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9aae8-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9aae8-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9aae8-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="9aae8-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9aae8-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9aae8-127">Remarks</span></span>

<span data-ttu-id="9aae8-128">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="9aae8-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="9aae8-129">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9aae8-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aae8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9aae8-130">Requirements</span></span>



| <span data-ttu-id="9aae8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aae8-131">Requirement</span></span> | <span data-ttu-id="9aae8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9aae8-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9aae8-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9aae8-133">TAPI version</span></span><br/> | <span data-ttu-id="9aae8-134">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9aae8-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9aae8-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9aae8-135">Header</span></span><br/>       | <dl> <span data-ttu-id="9aae8-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aae8-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="9aae8-137">Library</span></span><br/>      | <dl> <span data-ttu-id="9aae8-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9aae8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9aae8-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="9aae8-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aae8-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aae8-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9aae8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aae8-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="9aae8-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="9aae8-143">**ITTime:: Get \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="9aae8-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




