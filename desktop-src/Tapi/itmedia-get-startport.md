---
description: Il \_ metodo Get presenta ottiene il valore della porta a 16 bit per la prima porta.
ms.assetid: 203b51ea-8e0c-47d2-b267-36a0bf3bff72
title: 'Metodo ITMedia:: get_StartPort (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c5cf50f4a8beb0a1694bd1ceaf000620c69b69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324886"
---
# <a name="itmediaget_startport-method"></a><span data-ttu-id="2f383-103">Metodo ITMedia:: Get \_ presenta</span><span class="sxs-lookup"><span data-stu-id="2f383-103">ITMedia::get\_StartPort method</span></span>

<span data-ttu-id="2f383-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2f383-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f383-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2f383-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2f383-106">Il metodo **get \_ presenta** ottiene il valore della porta a 16 bit per la prima porta.</span><span class="sxs-lookup"><span data-stu-id="2f383-106">The **get\_StartPort** method gets the 16-bit port value for the first port.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f383-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f383-107">Syntax</span></span>


```C++
HRESULT get_StartPort(
  [out] LONG *pStartPort
);
```



## <a name="parameters"></a><span data-ttu-id="2f383-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f383-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f383-109">*pStartPort* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f383-109">*pStartPort* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f383-110">Valore della prima porta.</span><span class="sxs-lookup"><span data-stu-id="2f383-110">Value of the first port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f383-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f383-111">Return value</span></span>

<span data-ttu-id="2f383-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2f383-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2f383-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2f383-113">Return code</span></span>                                                                                   | <span data-ttu-id="2f383-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f383-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2f383-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2f383-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2f383-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2f383-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2f383-118">Il parametro *pStartPort* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="2f383-118">The *pStartPort* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="2f383-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2f383-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2f383-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2f383-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2f383-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2f383-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2f383-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2f383-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="2f383-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2f383-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f383-125">Requirements</span></span>



| <span data-ttu-id="2f383-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f383-126">Requirement</span></span> | <span data-ttu-id="2f383-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2f383-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f383-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2f383-128">TAPI version</span></span><br/> | <span data-ttu-id="2f383-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2f383-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2f383-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f383-130">Header</span></span><br/>       | <dl> <span data-ttu-id="2f383-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f383-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f383-132">Library</span></span><br/>      | <dl> <span data-ttu-id="2f383-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2f383-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2f383-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="2f383-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f383-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f383-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f383-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f383-137">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="2f383-137">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




