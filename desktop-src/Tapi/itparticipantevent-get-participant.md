---
description: Il \_ metodo Get partecipante ottiene un puntatore a una matrice di interfacce ITParticipant che rappresenta i partecipanti coinvolti nell'evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Metodo ITParticipantEvent:: get_Participant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329088"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="dcc95-103">Metodo ITParticipantEvent:: Get \_ partecipante</span><span class="sxs-lookup"><span data-stu-id="dcc95-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="dcc95-104">\[**ottenere \_ Il partecipante** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dcc95-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dcc95-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="dcc95-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dcc95-106">Il metodo **get \_ partecipante** ottiene un puntatore a una matrice di interfacce [**ITParticipant**](itparticipant.md) che rappresenta i partecipanti coinvolti nell'evento.</span><span class="sxs-lookup"><span data-stu-id="dcc95-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc95-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcc95-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="dcc95-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcc95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc95-109">*ppParticipant* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dcc95-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc95-110">Puntatore alla matrice di interfacce [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc95-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc95-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcc95-111">Return value</span></span>

<span data-ttu-id="dcc95-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="dcc95-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dcc95-113">Valore</span><span class="sxs-lookup"><span data-stu-id="dcc95-113">Value</span></span>                                                                                           | <span data-ttu-id="dcc95-114">Significato</span><span class="sxs-lookup"><span data-stu-id="dcc95-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcc95-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="dcc95-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dcc95-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="dcc95-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="dcc95-118">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="dcc95-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="dcc95-119"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="dcc95-120">Nessun partecipante associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="dcc95-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="dcc95-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="dcc95-122">Il parametro *ppParticipant* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="dcc95-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dcc95-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcc95-123">Requirements</span></span>



| <span data-ttu-id="dcc95-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc95-124">Requirement</span></span> | <span data-ttu-id="dcc95-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dcc95-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc95-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="dcc95-126">TAPI version</span></span><br/> | <span data-ttu-id="dcc95-127">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dcc95-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dcc95-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcc95-128">Header</span></span><br/>       | <dl> <span data-ttu-id="dcc95-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="dcc95-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcc95-130">Library</span></span><br/>      | <dl> <span data-ttu-id="dcc95-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dcc95-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc95-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="dcc95-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcc95-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dcc95-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcc95-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc95-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="dcc95-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="dcc95-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="dcc95-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




