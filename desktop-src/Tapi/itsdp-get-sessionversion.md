---
description: Il \_ metodo Get SessionVersion ottiene il valore 32 bit (idealmente Network Time Protocol o NTP) che funge da versione della sessione.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Metodo ITSdp:: get_SessionVersion (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333958"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="7d9a5-103">Metodo ITSdp:: Get \_ SessionVersion</span><span class="sxs-lookup"><span data-stu-id="7d9a5-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="7d9a5-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7d9a5-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7d9a5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7d9a5-106">Il metodo **get \_ SessionVersion** ottiene il valore 32 bit (idealmente Network Time Protocol o NTP) che funge da versione della sessione.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="7d9a5-107">Sebbene venga generato automaticamente quando viene creata la sessione, l'utente è responsabile della sua modifica quando il SDP viene modificato.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d9a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d9a5-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="7d9a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d9a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d9a5-110">*pSessionVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7d9a5-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d9a5-111">Puntatore all'identificatore della versione della sessione.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d9a5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d9a5-112">Return value</span></span>

<span data-ttu-id="7d9a5-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7d9a5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7d9a5-114">Return code</span></span>                                                                                   | <span data-ttu-id="7d9a5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d9a5-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d9a5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7d9a5-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="7d9a5-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7d9a5-119">Il parametro *pSessionVersion* non è valido.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="7d9a5-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7d9a5-121">Il parametro *pSessionVersion* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="7d9a5-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7d9a5-123">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="7d9a5-124"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7d9a5-125">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="7d9a5-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7d9a5-127">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="7d9a5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d9a5-128">Remarks</span></span>

<span data-ttu-id="7d9a5-129">Il valore restituito di questo metodo potrebbe essere **ULONG**, ma Visual Basic non supporta il tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="7d9a5-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="7d9a5-130">Un **Double** è il tipo più piccolo successivo che comprende l'intero intervallo di valori necessari.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9a5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d9a5-131">Requirements</span></span>



| <span data-ttu-id="7d9a5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d9a5-132">Requirement</span></span> | <span data-ttu-id="7d9a5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="7d9a5-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9a5-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7d9a5-134">TAPI version</span></span><br/> | <span data-ttu-id="7d9a5-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7d9a5-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7d9a5-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d9a5-136">Header</span></span><br/>       | <dl> <span data-ttu-id="7d9a5-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d9a5-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d9a5-138">Library</span></span><br/>      | <dl> <span data-ttu-id="7d9a5-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7d9a5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7d9a5-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="7d9a5-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d9a5-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d9a5-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d9a5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9a5-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="7d9a5-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="7d9a5-144">**ITSdp::p UT \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="7d9a5-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




