---
description: Il \_ metodo Get bandwidth ottiene il valore della larghezza di banda.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: 'Metodo ITConnection:: get_Bandwidth (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ff4d5902a3434839167ffd28fad2b7552e5c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333558"
---
# <a name="itconnectionget_bandwidth-method"></a><span data-ttu-id="df3bf-103">Metodo ITConnection:: Get \_ Bandwidth</span><span class="sxs-lookup"><span data-stu-id="df3bf-103">ITConnection::get\_Bandwidth method</span></span>

<span data-ttu-id="df3bf-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="df3bf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df3bf-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="df3bf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="df3bf-106">Il metodo **get \_ Bandwidth** ottiene il valore della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="df3bf-106">The **get\_Bandwidth** method gets the bandwidth value.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3bf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df3bf-107">Syntax</span></span>


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="df3bf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df3bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df3bf-109">*pBandwidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df3bf-109">*pBandwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df3bf-110">Valore della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="df3bf-110">Bandwidth value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df3bf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df3bf-111">Return value</span></span>

<span data-ttu-id="df3bf-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="df3bf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="df3bf-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="df3bf-113">Return code</span></span>                                                                                   | <span data-ttu-id="df3bf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df3bf-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="df3bf-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df3bf-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="df3bf-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="df3bf-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="df3bf-118">Il parametro *pBandwidth* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="df3bf-118">The *pBandwidth* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="df3bf-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df3bf-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="df3bf-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="df3bf-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="df3bf-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="df3bf-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="df3bf-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="df3bf-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="df3bf-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="df3bf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df3bf-125">Requirements</span></span>



| <span data-ttu-id="df3bf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="df3bf-126">Requirement</span></span> | <span data-ttu-id="df3bf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="df3bf-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df3bf-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="df3bf-128">TAPI version</span></span><br/> | <span data-ttu-id="df3bf-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="df3bf-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="df3bf-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df3bf-130">Header</span></span><br/>       | <dl> <span data-ttu-id="df3bf-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="df3bf-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="df3bf-132">Library</span></span><br/>      | <dl> <span data-ttu-id="df3bf-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df3bf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="df3bf-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="df3bf-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df3bf-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df3bf-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df3bf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3bf-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="df3bf-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




