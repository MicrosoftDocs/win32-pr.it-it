---
description: Le \_ costanti del flag di bit LINEADDRESSSTATE descrivono diversi elementi di stato dell'indirizzo.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Costanti LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332916"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="dafe0-103">\_Costanti LINEADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="dafe0-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="dafe0-104">Le costanti del flag di bit **LINEADDRESSSTATE \_** descrivono diversi elementi di stato dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="dafe0-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="dafe0-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**\_CAPSCHANGE LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-106">Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) per l'indirizzo sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="dafe0-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="dafe0-107">Per leggere la struttura aggiornata, l'applicazione deve usare [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="dafe0-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="dafe0-108">Se un provider di servizi invia un messaggio di [**riga \_ ADDRESSSTATE**](line-addressstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni che hanno negoziato la versione di TAPI 1,4 o versioni successive. le applicazioni che trattano una versione precedente dell'API riceveranno i messaggi di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) specificando LINEDEVSTATE \_ reinit, richiedendo di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="dafe0-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**\_DEVSPECIFIC LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-110">L'elemento specifico del dispositivo dello stato dell'indirizzo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="dafe0-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ in futuro**</span><span class="sxs-lookup"><span data-stu-id="dafe0-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-112">Lo stato di avanzamento dell'indirizzo è stato modificato, incluso probabilmente il numero di anelli per determinare una condizione di nessuna risposta.</span><span class="sxs-lookup"><span data-stu-id="dafe0-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="dafe0-113">L'applicazione deve controllare lo stato dell'indirizzo per determinare i dettagli relativi allo stato di avanzamento corrente dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="dafe0-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**\_INUSEMANY LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-115">L'indirizzo monitorato o con bridging è stato modificato in modo da essere utilizzato da una stazione per essere utilizzato da più di una stazione.</span><span class="sxs-lookup"><span data-stu-id="dafe0-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**\_INUSEONE LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-117">L'indirizzo è stato modificato da inattivo o utilizzato da molte stazioni con Bridge per essere utilizzato da una sola stazione.</span><span class="sxs-lookup"><span data-stu-id="dafe0-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**\_INUSEZERO LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-119">L'indirizzo è stato modificato in inattivo (non è utilizzato da alcuna stazione).</span><span class="sxs-lookup"><span data-stu-id="dafe0-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**\_NUMCALLS LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-121">Il numero di chiamate sull'indirizzo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="dafe0-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="dafe0-122">Questo è il risultato di eventi quali una nuova chiamata in ingresso, una chiamata in uscita sull'indirizzo o una chiamata che modifica lo stato di attesa.</span><span class="sxs-lookup"><span data-stu-id="dafe0-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="dafe0-123">Questo flag copre le modifiche apportate ai membri **dwNumActiveCalls**, **dwNumOnHoldCalls** e **dwNumOnHoldPendingCalls** nella struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="dafe0-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="dafe0-124">L'applicazione deve controllare tutti e tre i membri quando riceve un messaggio di [**riga \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).</span><span class="sxs-lookup"><span data-stu-id="dafe0-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ altro**</span><span class="sxs-lookup"><span data-stu-id="dafe0-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-126">Gli elementi di stato Address diversi da quelli elencati di seguito sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="dafe0-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="dafe0-127">L'applicazione deve controllare lo stato dell'indirizzo corrente per determinare quali elementi sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="dafe0-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dafe0-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminali LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dafe0-129">Le impostazioni del terminale per l'indirizzo sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="dafe0-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dafe0-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="dafe0-130">Remarks</span></span>

<span data-ttu-id="dafe0-131">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="dafe0-131">No extensibility.</span></span> <span data-ttu-id="dafe0-132">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="dafe0-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="dafe0-133">Un'applicazione riceve una notifica sulle modifiche apportate a questi elementi di stato nel messaggio di [**riga \_ ADDRESSSTATE**](line-addressstate.md) .</span><span class="sxs-lookup"><span data-stu-id="dafe0-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="dafe0-134">Le funzionalità del dispositivo dell'indirizzo indicano quali modifiche allo stato dell'indirizzo possono essere segnalate per questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="dafe0-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="dafe0-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dafe0-135">Requirements</span></span>



| <span data-ttu-id="dafe0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="dafe0-136">Requirement</span></span> | <span data-ttu-id="dafe0-137">Valore</span><span class="sxs-lookup"><span data-stu-id="dafe0-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dafe0-138">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="dafe0-138">TAPI version</span></span><br/> | <span data-ttu-id="dafe0-139">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dafe0-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dafe0-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dafe0-140">Header</span></span><br/>       | <dl> <span data-ttu-id="dafe0-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dafe0-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dafe0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dafe0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dafe0-143">**LINEA \_ ADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="dafe0-144">**LINEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="dafe0-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="dafe0-145">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="dafe0-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="dafe0-146">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="dafe0-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="dafe0-147">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="dafe0-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




