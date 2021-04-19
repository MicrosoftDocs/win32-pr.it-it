---
description: TAPI invia il \_ messaggio di stato del telefono a un'applicazione ogni volta che lo stato di un dispositivo telefonico viene modificato.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Messaggio di PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324125"
---
# <a name="phone_state-message"></a><span data-ttu-id="301f4-103">\_Messaggio di stato telefono</span><span class="sxs-lookup"><span data-stu-id="301f4-103">PHONE\_STATE message</span></span>

<span data-ttu-id="301f4-104">TAPI invia il messaggio di **\_ stato del telefono** a un'applicazione ogni volta che lo stato di un dispositivo telefonico viene modificato.</span><span class="sxs-lookup"><span data-stu-id="301f4-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="301f4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="301f4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301f4-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="301f4-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="301f4-107">Handle per il dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="301f4-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="301f4-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="301f4-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="301f4-109">Istanza di callback dell'applicazione fornita all'apertura del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="301f4-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="301f4-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="301f4-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="301f4-111">Stato del telefono che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="301f4-111">The phone state that has changed.</span></span> <span data-ttu-id="301f4-112">Questo parametro usa una delle [**\_ costanti PHONESTATE**](phonestate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="301f4-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="301f4-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="301f4-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="301f4-114">Informazioni dipendenti dallo stato del telefono che descrivono in dettaglio la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="301f4-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="301f4-115">Questo parametro non viene utilizzato se più flag sono impostati in *dwParam1*, perché sono stati modificati più elementi di stato.</span><span class="sxs-lookup"><span data-stu-id="301f4-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="301f4-116">L'applicazione deve richiamare [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) per ottenere un set completo di informazioni.</span><span class="sxs-lookup"><span data-stu-id="301f4-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="301f4-117">Se *dwParam1* è PHONESTATE \_ Owner, *dwParam2* contiene il nuovo numero di proprietari.</span><span class="sxs-lookup"><span data-stu-id="301f4-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="301f4-118">Se *dwParam1* è PHONESTATE \_ monitoraggi, *dwParam2* contiene il nuovo numero di monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="301f4-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="301f4-119">Se *dwParam1* è PHONESTATE \_ Lamp, *dwParam2* contiene l'identificatore del pulsante o della lampada della lampada che è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="301f4-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="301f4-120">Se *dwParam1* è PHONESTATE \_ RINGMODE, *dwParam2* contiene la nuova modalità ring.</span><span class="sxs-lookup"><span data-stu-id="301f4-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="301f4-121">Se *dwParam1* è PHONESTATE \_ handset, speaker o headset, *dwParam2* contiene la nuova modalità hookswitch del dispositivo hookswitch.</span><span class="sxs-lookup"><span data-stu-id="301f4-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="301f4-122">Questo parametro usa una delle [**\_ costanti PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="301f4-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="301f4-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="301f4-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="301f4-124">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="301f4-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301f4-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="301f4-125">Return value</span></span>

<span data-ttu-id="301f4-126">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="301f4-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="301f4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="301f4-127">Remarks</span></span>

<span data-ttu-id="301f4-128">L'invio del messaggio di **\_ stato telefonico** all'applicazione può essere controllato e sottoposto a query usando [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) e [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="301f4-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="301f4-129">Per impostazione predefinita, questo messaggio è disabilitato per tutte le modifiche di stato ad eccezione di PHONESTATE \_ reinit, che non può essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="301f4-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="301f4-130">Questo messaggio viene inviato a tutte le applicazioni che dispongono di un handle per il telefono, incluse quelle che hanno chiamato [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con il parametro *DWPRIVILEGES* impostato su PHONEPRIVILEGE \_ owner o PHONEPRIVILEGE \_ monitor.</span><span class="sxs-lookup"><span data-stu-id="301f4-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="301f4-131">Un messaggio di **\_ stato del telefono** con un proprietario e/o un'indicazione relativa ai monitoraggi viene inviato alle applicazioni che dispongono già di un handle per il telefono.</span><span class="sxs-lookup"><span data-stu-id="301f4-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="301f4-132">Questo può essere il risultato di un'altra applicazione che modifica la proprietà o il monitoraggio del dispositivo telefonico con [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) o [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span><span class="sxs-lookup"><span data-stu-id="301f4-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="301f4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="301f4-133">Requirements</span></span>



| <span data-ttu-id="301f4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="301f4-134">Requirement</span></span> | <span data-ttu-id="301f4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="301f4-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="301f4-136">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="301f4-136">TAPI version</span></span><br/> | <span data-ttu-id="301f4-137">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="301f4-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="301f4-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="301f4-138">Header</span></span><br/>       | <dl> <span data-ttu-id="301f4-139"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="301f4-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="301f4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="301f4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301f4-141">**\_chiusura telefono**</span><span class="sxs-lookup"><span data-stu-id="301f4-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="301f4-142">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="301f4-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="301f4-143">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="301f4-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="301f4-144">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="301f4-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="301f4-145">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="301f4-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="301f4-146">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="301f4-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="301f4-147">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="301f4-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="301f4-148">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="301f4-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="301f4-149">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="301f4-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="301f4-150">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="301f4-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="301f4-151">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="301f4-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




