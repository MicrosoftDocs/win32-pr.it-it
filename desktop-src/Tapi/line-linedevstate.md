---
description: Il messaggio della linea TAPI \_ LINEDEVSTATE viene inviato quando lo stato di un dispositivo a linee è cambiato. L'applicazione può richiamare lineGetLineDevStatus per determinare il nuovo stato della riga.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Messaggio di LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327404"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="f4494-104">\_Messaggio linea LINEDEVSTATE</span><span class="sxs-lookup"><span data-stu-id="f4494-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="f4494-105">Il messaggio della **linea TAPI \_ LINEDEVSTATE** viene inviato quando lo stato di un dispositivo a linee è cambiato.</span><span class="sxs-lookup"><span data-stu-id="f4494-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="f4494-106">L'applicazione può richiamare [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) per determinare il nuovo stato della riga.</span><span class="sxs-lookup"><span data-stu-id="f4494-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f4494-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4494-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4494-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f4494-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f4494-109">Handle per il dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="f4494-109">A handle to the line device.</span></span> <span data-ttu-id="f4494-110">Questo parametro è **null** se *dwParam1* è LINEDEVSTATE \_ reinit.</span><span class="sxs-lookup"><span data-stu-id="f4494-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="f4494-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f4494-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f4494-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="f4494-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="f4494-113">Se il parametro *dwParam1* è LINEDEVSTATE \_ reinit, il parametro *dwCallbackInstance* non è valido e è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="f4494-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4494-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f4494-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f4494-115">Elemento di stato del dispositivo di linea modificato.</span><span class="sxs-lookup"><span data-stu-id="f4494-115">The line device status item that has changed.</span></span> <span data-ttu-id="f4494-116">Il parametro può essere costituito da una o [**più \_ costanti LINEDEVSTATE**](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f4494-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4494-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f4494-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f4494-118">L'interpretazione di questo parametro dipende dal valore di *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="f4494-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="f4494-119">Se *dwParam1* è LINEDEVSTATE \_ Ringing, *dwParam2* contiene la modalità ring con cui l'opzione indica alla riga di squillare.</span><span class="sxs-lookup"><span data-stu-id="f4494-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="f4494-120">Le modalità anello valide sono numeri nell'intervallo da uno a **dwNumRingModes**, dove **dwNumRingModes** è una funzionalità di dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="f4494-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="f4494-121">Se *dwParam1* è LINEDEVSTATE \_ reinit e il messaggio è stato emesso da TAPI come risultato della conversione di un nuovo messaggio API in un messaggio reinit, *DwParam2* contiene il parametro *dwMsg* del messaggio originale (ad esempio, [**riga \_ creazione**](line-create.md) o riga \_ LINEDEVSTATE).</span><span class="sxs-lookup"><span data-stu-id="f4494-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="f4494-122">Se *dwParam2* è zero, questo indica che il messaggio reinit è un messaggio "Real" reinit che richiede che l'applicazione chiami [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) alla prima convenienza.</span><span class="sxs-lookup"><span data-stu-id="f4494-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="f4494-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f4494-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f4494-124">L'interpretazione di questo parametro dipende dal valore di *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="f4494-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="f4494-125">Se *dwParam1* è LINEDEVSTATE \_ Ringing, *dwParam3* contiene il numero di squilli per questo evento ring.</span><span class="sxs-lookup"><span data-stu-id="f4494-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="f4494-126">Il numero di squilli inizia da zero.</span><span class="sxs-lookup"><span data-stu-id="f4494-126">The ring count starts at zero.</span></span>

<span data-ttu-id="f4494-127">Se *dwParam1* è LINEDEVSTATE \_ reinit e il messaggio è stato emesso da TAPI come risultato della conversione di un nuovo messaggio API in un messaggio reinit, *DwParam3* contiene il parametro *dwParam1* del messaggio originale (ad esempio, LINEDEVSTATE \_ TRANSLATECHANGE o un altro \_ valore LINEDEVSTATE, se *dwParam2* è la riga LINEDEVSTATE o \_ il nuovo identificatore di dispositivo, se *dwParam2* è [**line \_ create**](line-create.md)).</span><span class="sxs-lookup"><span data-stu-id="f4494-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4494-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4494-128">Return value</span></span>

<span data-ttu-id="f4494-129">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f4494-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4494-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4494-130">Remarks</span></span>

<span data-ttu-id="f4494-131">L'invio del messaggio di **riga \_ LINEDEVSTATE** può essere controllato con [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="f4494-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="f4494-132">Un'applicazione può indicare le modifiche degli elementi di stato per le quali si desidera ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="f4494-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="f4494-133">Per impostazione predefinita, tutti i rapporti di stato sono disabilitati, ad eccezione di LINEDEVSTATE \_ reinit, che non può essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f4494-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="f4494-134">Questo messaggio viene inviato a tutte le applicazioni che dispongono di un handle per la riga, inclusi quelli che hanno chiamato [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con il parametro *DWPRIVILEGES* impostato su LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ monitor o combinazioni consentite di questi.</span><span class="sxs-lookup"><span data-stu-id="f4494-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4494-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4494-135">Requirements</span></span>



| <span data-ttu-id="f4494-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4494-136">Requirement</span></span> | <span data-ttu-id="f4494-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f4494-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f4494-138">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f4494-138">TAPI version</span></span><br/> | <span data-ttu-id="f4494-139">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f4494-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f4494-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4494-140">Header</span></span><br/>       | <dl> <span data-ttu-id="f4494-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4494-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4494-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4494-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4494-143">**\_chiusura riga**</span><span class="sxs-lookup"><span data-stu-id="f4494-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="f4494-144">**\_creazione linea**</span><span class="sxs-lookup"><span data-stu-id="f4494-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="f4494-145">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="f4494-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="f4494-146">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f4494-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="f4494-147">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="f4494-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="f4494-148">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="f4494-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="f4494-149">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="f4494-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="f4494-150">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="f4494-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="f4494-151">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="f4494-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="f4494-152">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="f4494-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="f4494-153">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="f4494-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="f4494-154">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="f4494-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




