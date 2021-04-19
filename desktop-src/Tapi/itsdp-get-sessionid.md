---
description: Il \_ metodo get SessionID ottiene il valore NTP (Network Time Protocol) a 32 bit che funge da identificatore di sessione. Viene generato automaticamente quando viene creata la sessione.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Metodo ITSdp:: get_SessionId (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327502"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="92b94-104">Metodo ITSdp:: Get \_ SessionID</span><span class="sxs-lookup"><span data-stu-id="92b94-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="92b94-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92b94-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="92b94-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="92b94-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="92b94-107">Il metodo **get \_ SessionID** ottiene il valore NTP (Network Time Protocol) a 32 bit che funge da identificatore di sessione.</span><span class="sxs-lookup"><span data-stu-id="92b94-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="92b94-108">Viene generato automaticamente quando viene creata la sessione.</span><span class="sxs-lookup"><span data-stu-id="92b94-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b94-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92b94-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="92b94-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="92b94-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b94-111">*pSessionId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92b94-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b94-112">Puntatore all'identificatore di sessione.</span><span class="sxs-lookup"><span data-stu-id="92b94-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b94-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92b94-113">Return value</span></span>

<span data-ttu-id="92b94-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="92b94-114">This method can return one of these values.</span></span>



| <span data-ttu-id="92b94-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="92b94-115">Return code</span></span>                                                                                   | <span data-ttu-id="92b94-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92b94-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="92b94-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="92b94-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="92b94-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="92b94-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="92b94-120">Il parametro *pSessionId* non è valido.</span><span class="sxs-lookup"><span data-stu-id="92b94-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="92b94-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="92b94-122">Il parametro *pSessionId* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="92b94-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="92b94-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="92b94-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="92b94-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="92b94-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="92b94-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="92b94-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="92b94-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="92b94-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="92b94-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="92b94-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="92b94-129">Remarks</span></span>

<span data-ttu-id="92b94-130">Il valore restituito di questo metodo potrebbe essere **ULONG**, ma Visual Basic non supporta il tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="92b94-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="92b94-131">Un **Double** è il tipo più piccolo successivo che comprende l'intero intervallo di valori necessari.</span><span class="sxs-lookup"><span data-stu-id="92b94-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b94-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92b94-132">Requirements</span></span>



| <span data-ttu-id="92b94-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b94-133">Requirement</span></span> | <span data-ttu-id="92b94-134">Valore</span><span class="sxs-lookup"><span data-stu-id="92b94-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92b94-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="92b94-135">TAPI version</span></span><br/> | <span data-ttu-id="92b94-136">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="92b94-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="92b94-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92b94-137">Header</span></span><br/>       | <dl> <span data-ttu-id="92b94-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="92b94-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="92b94-139">Library</span></span><br/>      | <dl> <span data-ttu-id="92b94-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="92b94-141">DLL</span><span class="sxs-lookup"><span data-stu-id="92b94-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="92b94-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b94-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92b94-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b94-144">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="92b94-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




