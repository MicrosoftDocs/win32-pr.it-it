---
description: Il \_ metodo Get TTL Ottiene l'ambito TTL (time to Live) per le trasmissioni sugli indirizzi.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'Metodo ITConnection:: get_Ttl (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326503"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="7a14c-103">Metodo ITConnection:: Get \_ TTL</span><span class="sxs-lookup"><span data-stu-id="7a14c-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="7a14c-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7a14c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7a14c-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7a14c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7a14c-106">Il metodo **get \_ TTL** Ottiene l'ambito TTL ( [*time to Live*](t-tapgloss.md) ) per le trasmissioni sugli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7a14c-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a14c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a14c-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="7a14c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a14c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a14c-109">*pTtl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7a14c-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a14c-110">Ambito TTL.</span><span class="sxs-lookup"><span data-stu-id="7a14c-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a14c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a14c-111">Return value</span></span>

<span data-ttu-id="7a14c-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7a14c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7a14c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7a14c-113">Value</span></span>                                                                                         | <span data-ttu-id="7a14c-114">Significato</span><span class="sxs-lookup"><span data-stu-id="7a14c-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7a14c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7a14c-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7a14c-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7a14c-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7a14c-118">Il parametro *pTtl* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="7a14c-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="7a14c-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7a14c-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7a14c-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7a14c-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7a14c-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7a14c-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7a14c-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7a14c-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="7a14c-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="7a14c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a14c-125">Requirements</span></span>



| <span data-ttu-id="7a14c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a14c-126">Requirement</span></span> | <span data-ttu-id="7a14c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7a14c-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a14c-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7a14c-128">TAPI version</span></span><br/> | <span data-ttu-id="7a14c-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7a14c-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7a14c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a14c-130">Header</span></span><br/>       | <dl> <span data-ttu-id="7a14c-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a14c-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a14c-132">Library</span></span><br/>      | <dl> <span data-ttu-id="7a14c-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7a14c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7a14c-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="7a14c-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a14c-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a14c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a14c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a14c-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="7a14c-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




