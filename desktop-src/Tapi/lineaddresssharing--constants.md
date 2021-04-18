---
description: Le \_ costanti del flag di bit LINEADDRESSSHARING descrivono i vari modi in cui un indirizzo può essere condiviso tra le linee.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Costanti LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328417"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="3d4d5-103">\_Costanti LINEADDRESSSHARING</span><span class="sxs-lookup"><span data-stu-id="3d4d5-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="3d4d5-104">Le costanti del flag di bit **LINEADDRESSSHARING \_** descrivono i vari modi in cui un indirizzo può essere condiviso tra le linee.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="3d4d5-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privato**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3d4d5-106">L'indirizzo è privato per la riga dell'utente; non viene assegnato ad altre stazioni.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3d4d5-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**\_BRIDGEDEXCL LINEADDRESSSHARING**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3d4d5-108">L'indirizzo viene colmato a una o più stazioni.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="3d4d5-109">La prima riga per attivare una chiamata sulla riga avrà accesso esclusivo all'indirizzo e alle chiamate che possono esistere.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="3d4d5-110">Altre righe non saranno in grado di usare l'indirizzo con Bridge mentre è in uso.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3d4d5-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**\_BRIDGEDNEW LINEADDRESSSHARING**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3d4d5-112">L'indirizzo viene colmato con una o più stazioni.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="3d4d5-113">La prima riga per attivare una chiamata sulla riga avrà accesso esclusivo solo alla chiamata corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="3d4d5-114">Altre applicazioni che usano l'indirizzo genereranno un aspetto di chiamata nuovo e separato.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3d4d5-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**\_BRIDGEDSHARED LINEADDRESSSHARING**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3d4d5-116">L'indirizzo viene colmato con una o più righe.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="3d4d5-117">Tutte le parti con bridging possono condividere chiamate sull'indirizzo, che quindi funge da conferenza.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3d4d5-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ monitorato**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3d4d5-119">Si tratta di un indirizzo il cui stato di inattività è reso disponibile a questa riga.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d4d5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d4d5-120">Remarks</span></span>

<span data-ttu-id="3d4d5-121">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-121">No extensibility.</span></span> <span data-ttu-id="3d4d5-122">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="3d4d5-123">Il modo in cui un indirizzo viene condiviso tra le righe può influire sul comportamento di tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="3d4d5-124">[**Riga \_ di**](line-callstate.md) I messaggi CALLSTATE e [**line \_ ADDRESSSTATE**](line-addressstate.md) vengono inviati all'applicazione in risposta alle attività da parte delle stazioni di bridging.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="3d4d5-125">Attraverso questi messaggi, un'applicazione può tenere traccia dello stato dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="3d4d5-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4d5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d4d5-126">Requirements</span></span>



| <span data-ttu-id="3d4d5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d4d5-127">Requirement</span></span> | <span data-ttu-id="3d4d5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3d4d5-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3d4d5-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3d4d5-129">TAPI version</span></span><br/> | <span data-ttu-id="3d4d5-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3d4d5-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3d4d5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d4d5-131">Header</span></span><br/>       | <dl> <span data-ttu-id="3d4d5-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4d5-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4d5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d4d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4d5-134">**LINEA \_ ADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="3d4d5-135">**LINEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="3d4d5-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 




