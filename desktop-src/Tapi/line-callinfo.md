---
description: Il messaggio della linea TAPI \_ CALLINFO viene inviato quando vengono modificate le informazioni relative alla chiamata specificata. L'applicazione può richiamare lineGetCallInfo per determinare le informazioni sulla chiamata corrente.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Messaggio di LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328052"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="d5f3d-104">\_Messaggio linea CALLINFO</span><span class="sxs-lookup"><span data-stu-id="d5f3d-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="d5f3d-105">Il messaggio della **linea TAPI \_ CALLINFO** viene inviato quando vengono modificate le informazioni relative alla chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="d5f3d-106">L'applicazione può richiamare [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) per determinare le informazioni sulla chiamata corrente.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d5f3d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5f3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f3d-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="d5f3d-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f3d-109">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="d5f3d-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="d5f3d-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f3d-111">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="d5f3d-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d5f3d-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f3d-113">Elemento delle informazioni sulla chiamata modificato.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-113">The call information item that has changed.</span></span> <span data-ttu-id="d5f3d-114">Può essere una o più delle [**\_ costanti LINECALLINFOSTATE**](linecallinfostate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d5f3d-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5f3d-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d5f3d-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f3d-116">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d5f3d-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d5f3d-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f3d-118">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f3d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5f3d-119">Return value</span></span>

<span data-ttu-id="d5f3d-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f3d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5f3d-121">Remarks</span></span>

<span data-ttu-id="d5f3d-122">Un messaggio di **riga \_ CALLINFO** con indicazione *NumOwnersIncr*, *NumOwnersDecr* e/o *NumMonitorsChanged* viene inviato ad applicazioni che dispongono già di un handle per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="d5f3d-123">Questo può essere il risultato di un'altra applicazione che modifica la proprietà o il monitoraggio a una chiamata con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)e [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span><span class="sxs-lookup"><span data-stu-id="d5f3d-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="d5f3d-124">Questi messaggi di **riga \_ CALLINFO** non vengono inviati quando viene fornita una notifica di una nuova chiamata in un messaggio di [**\_ CALLSTATE riga**](line-callstate.md) , perché le informazioni sulla chiamata riflettono già il numero corretto di proprietari e monitoraggi al momento dell'invio dei messaggi di riga \_ CALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="d5f3d-125">**Riga \_ di** I messaggi CALLINFO vengono eliminati anche nel caso in cui una chiamata viene offerta da TAPI per monitorare il \_ meccanismo sconosciuto di LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="d5f3d-126">L'applicazione che causa una modifica al numero di proprietari o monitoraggi (ad esempio, richiamando [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) o [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) non riceve un messaggio che indica che la modifica è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="d5f3d-127">Non viene inviato alcun messaggio di **riga \_ CALLINFO** per una chiamata dopo che la chiamata è entrata nello stato di *inattività* .</span><span class="sxs-lookup"><span data-stu-id="d5f3d-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="d5f3d-128">In particolare, le modifiche apportate al numero di proprietari e monitoraggi non vengono segnalate come le applicazioni deallocano gli handle per la chiamata inattiva.</span><span class="sxs-lookup"><span data-stu-id="d5f3d-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f3d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5f3d-129">Requirements</span></span>



| <span data-ttu-id="d5f3d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f3d-130">Requirement</span></span> | <span data-ttu-id="d5f3d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d5f3d-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d5f3d-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d5f3d-132">TAPI version</span></span><br/> | <span data-ttu-id="d5f3d-133">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d5f3d-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d5f3d-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5f3d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="d5f3d-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f3d-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f3d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5f3d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f3d-137">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="d5f3d-138">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="d5f3d-139">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="d5f3d-140">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="d5f3d-141">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="d5f3d-142">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="d5f3d-143">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="d5f3d-144">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="d5f3d-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




