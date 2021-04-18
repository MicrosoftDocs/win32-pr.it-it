---
description: Il \_ metodo Get Event ottiene un \_ descrittore di eventi del partecipante del tipo di evento che si è verificato.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Metodo ITParticipantEvent:: get_Event (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332001"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="abad1-103">Metodo di evento ITParticipantEvent:: Get \_</span><span class="sxs-lookup"><span data-stu-id="abad1-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="abad1-104">\[**ottenere \_ L'evento** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="abad1-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="abad1-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="abad1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="abad1-106">Il metodo **get \_ Event** ottiene un descrittore di [**\_ eventi del partecipante**](participant-event.md) del tipo di evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="abad1-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="abad1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abad1-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="abad1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="abad1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abad1-109">*pParticipantEvent* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="abad1-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abad1-110">Puntatore a un descrittore di [**\_ eventi del partecipante**](participant-event.md) dell'evento.</span><span class="sxs-lookup"><span data-stu-id="abad1-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abad1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abad1-111">Return value</span></span>

<span data-ttu-id="abad1-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="abad1-112">This method can return one of these values.</span></span>



| <span data-ttu-id="abad1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="abad1-113">Value</span></span>                                                                                         | <span data-ttu-id="abad1-114">Significato</span><span class="sxs-lookup"><span data-stu-id="abad1-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="abad1-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abad1-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="abad1-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="abad1-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="abad1-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="abad1-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="abad1-118">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="abad1-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="abad1-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="abad1-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="abad1-120">Il parametro *pParticipantEvent* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="abad1-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="abad1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abad1-121">Requirements</span></span>



| <span data-ttu-id="abad1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="abad1-122">Requirement</span></span> | <span data-ttu-id="abad1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="abad1-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abad1-124">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="abad1-124">TAPI version</span></span><br/> | <span data-ttu-id="abad1-125">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="abad1-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="abad1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abad1-126">Header</span></span><br/>       | <dl> <span data-ttu-id="abad1-127"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="abad1-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="abad1-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="abad1-128">Library</span></span><br/>      | <dl> <span data-ttu-id="abad1-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abad1-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="abad1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="abad1-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="abad1-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abad1-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="abad1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abad1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abad1-133">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="abad1-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="abad1-134">**\_evento partecipante**</span><span class="sxs-lookup"><span data-stu-id="abad1-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 




