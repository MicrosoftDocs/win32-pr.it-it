---
description: Il messaggio di rimozione del telefono TAPI \_ viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo telefonico.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Messaggio di PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328047"
---
# <a name="phone_remove-message"></a><span data-ttu-id="7901c-103">Messaggio di rimozione del telefono \_</span><span class="sxs-lookup"><span data-stu-id="7901c-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="7901c-104">Il messaggio **di \_ rimozione del telefono** TAPI viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="7901c-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="7901c-105">In genere, questo non viene usato per le rimozioni temporanee, ad esempio l'estrazione di dispositivi PCMCIA, ma solo per le rimozioni permanenti in cui il dispositivo non viene più segnalato dal provider di servizi se TAPI è stato reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="7901c-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7901c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7901c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7901c-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7901c-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7901c-108">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7901c-108">Reserved.</span></span> <span data-ttu-id="7901c-109">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="7901c-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7901c-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7901c-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7901c-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7901c-111">Reserved.</span></span> <span data-ttu-id="7901c-112">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="7901c-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7901c-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7901c-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7901c-114">Identificatore del dispositivo telefonico che è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="7901c-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="7901c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7901c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7901c-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7901c-116">Reserved.</span></span> <span data-ttu-id="7901c-117">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="7901c-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7901c-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7901c-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7901c-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7901c-119">Reserved.</span></span> <span data-ttu-id="7901c-120">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="7901c-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7901c-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7901c-121">Return value</span></span>

<span data-ttu-id="7901c-122">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7901c-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7901c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7901c-123">Remarks</span></span>

<span data-ttu-id="7901c-124">Per le applicazioni TAPI 2,0 o versioni successive viene inviato un messaggio di **\_ rimozione telefono** .</span><span class="sxs-lookup"><span data-stu-id="7901c-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="7901c-125">In questo modo si informa che il dispositivo è stato rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7901c-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="7901c-126">Il messaggio di **\_ rimozione del telefono** è preceduto da un messaggio di [**\_ chiusura**](phone-close.md) del telefono su ogni handle telefonico, se l'applicazione ha aperto il telefono.</span><span class="sxs-lookup"><span data-stu-id="7901c-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="7901c-127">Questo messaggio viene inviato a tutte le applicazioni che supportano la versione 2,0 o successiva di TAPI che hanno chiamato [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), inclusi quelli che non hanno dispositivi telefonici aperti al momento.</span><span class="sxs-lookup"><span data-stu-id="7901c-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="7901c-128">Alle applicazioni meno recenti (che hanno negoziato la versione 1,4 o precedente) viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) che specifica PHONESTATE \_ rimosso, seguito da un messaggio di [**\_ chiusura del telefono**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="7901c-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="7901c-129">Diversamente dal messaggio **di \_ rimozione del telefono** , tuttavia, queste applicazioni meno recenti possono ricevere questi messaggi solo se hanno il telefono aperto al momento della rimozione.</span><span class="sxs-lookup"><span data-stu-id="7901c-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="7901c-130">Se il telefono non è aperto, l'unica indicazione che indica che il dispositivo è stato rimosso è la ricezione di un PHONEERR \_ NODEVICE quando tentano di accedere al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7901c-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="7901c-131">Dopo la rimozione di un dispositivo, qualsiasi tentativo di accedere al dispositivo mediante il relativo identificatore del dispositivo restituisce un \_ errore PHONEERR nodevice.</span><span class="sxs-lookup"><span data-stu-id="7901c-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="7901c-132">Dopo che tutte le applicazioni TAPI sono state arrestate in modo che TAPI possa essere riavviato e quando viene reinizializzata la funzione TAPI, il dispositivo rimosso non occupa più un identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7901c-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="7901c-133">Implementazione: è TAPI che restituisce questo messaggio PHONEERR \_ NODEVICE dopo la ricezione di un \_ messaggio di rimozione del telefono da un provider di servizi. non vengono effettuate ulteriori chiamate a tale provider di servizi tramite tale identificatore del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="7901c-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7901c-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7901c-134">Requirements</span></span>



| <span data-ttu-id="7901c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7901c-135">Requirement</span></span> | <span data-ttu-id="7901c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7901c-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7901c-137">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7901c-137">TAPI version</span></span><br/> | <span data-ttu-id="7901c-138">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7901c-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7901c-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7901c-139">Header</span></span><br/>       | <dl> <span data-ttu-id="7901c-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7901c-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7901c-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7901c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7901c-142">**\_chiusura telefono**</span><span class="sxs-lookup"><span data-stu-id="7901c-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="7901c-143">**\_stato telefono**</span><span class="sxs-lookup"><span data-stu-id="7901c-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="7901c-144">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="7901c-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="7901c-145">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="7901c-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




