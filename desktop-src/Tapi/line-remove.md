---
description: Il messaggio di rimozione della riga di TAPI \_ viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo a linee.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Messaggio di LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328908"
---
# <a name="line_remove-message"></a><span data-ttu-id="62bb7-103">\_Rimuovi riga messaggio</span><span class="sxs-lookup"><span data-stu-id="62bb7-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="62bb7-104">Il messaggio **di \_ rimozione della riga** di TAPI viene inviato per informare un'applicazione della rimozione (eliminazione dal sistema) di un dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="62bb7-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="62bb7-105">In genere, questo non viene usato per le rimozioni temporanee, ad esempio l'estrazione di dispositivi PCMCIA, ma solo per le rimozioni permanenti in cui il dispositivo non viene più segnalato dal provider di servizi se TAPI è stato reinizializzato.</span><span class="sxs-lookup"><span data-stu-id="62bb7-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="62bb7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62bb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62bb7-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="62bb7-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="62bb7-108">Riservato.</span><span class="sxs-lookup"><span data-stu-id="62bb7-108">Reserved.</span></span> <span data-ttu-id="62bb7-109">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="62bb7-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="62bb7-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="62bb7-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="62bb7-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="62bb7-111">Reserved.</span></span> <span data-ttu-id="62bb7-112">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="62bb7-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="62bb7-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="62bb7-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="62bb7-114">Identificatore del dispositivo a linee che è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="62bb7-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="62bb7-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="62bb7-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="62bb7-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="62bb7-116">Reserved.</span></span> <span data-ttu-id="62bb7-117">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="62bb7-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="62bb7-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="62bb7-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="62bb7-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="62bb7-119">Reserved.</span></span> <span data-ttu-id="62bb7-120">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="62bb7-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62bb7-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62bb7-121">Return value</span></span>

<span data-ttu-id="62bb7-122">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="62bb7-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62bb7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="62bb7-123">Remarks</span></span>

<span data-ttu-id="62bb7-124">Le applicazioni che supportano TAPI 2,0 o versioni successive vengono inviate un messaggio di **\_ rimozione riga** .</span><span class="sxs-lookup"><span data-stu-id="62bb7-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="62bb7-125">In questo modo si informa che il dispositivo è stato rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="62bb7-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="62bb7-126">Il messaggio di **\_ rimozione riga** è preceduto da un messaggio di [**\_ chiusura riga**](line-close.md) su ogni handle di riga, se l'applicazione ha la riga aperta.</span><span class="sxs-lookup"><span data-stu-id="62bb7-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="62bb7-127">Questo messaggio viene inviato a tutte le applicazioni che supportano la versione 2,0 o successiva di TAPI che hanno chiamato [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), inclusi quelli che non dispongono di alcun dispositivo di linea aperto al momento.</span><span class="sxs-lookup"><span data-stu-id="62bb7-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="62bb7-128">Alle applicazioni precedenti viene inviato un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) che specifica LINEDEVSTATE \_ rimosso, seguito da un \_ messaggio di chiusura riga.</span><span class="sxs-lookup"><span data-stu-id="62bb7-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="62bb7-129">Diversamente dal messaggio **di \_ rimozione riga** , tuttavia, queste applicazioni meno recenti possono ricevere questi messaggi solo se la riga è aperta quando viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="62bb7-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="62bb7-130">Se la riga non è aperta, l'unica indicazione che indica che il dispositivo è stato rimosso è la ricezione di un \_ errore LINEERR NODEVICE quando tentano di accedere al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb7-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="62bb7-131">Dopo la rimozione di un dispositivo, qualsiasi tentativo di accedere al dispositivo mediante il relativo identificatore del dispositivo restituisce un \_ errore LINEERR nodevice.</span><span class="sxs-lookup"><span data-stu-id="62bb7-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="62bb7-132">Dopo che tutte le applicazioni TAPI sono state arrestate in modo che TAPI possa essere riavviato e quando viene reinizializzata la funzione TAPI, il dispositivo rimosso non occupa più un identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb7-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="62bb7-133">Implementazione: è TAPI che restituisce questo LINEERR \_ NODEVICE; dopo la ricezione di un messaggio di **\_ rimozione riga** da un provider di servizi, non vengono effettuate ulteriori chiamate a tale provider di servizi tramite tale identificatore del dispositivo di linea.</span><span class="sxs-lookup"><span data-stu-id="62bb7-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62bb7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62bb7-134">Requirements</span></span>



| <span data-ttu-id="62bb7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="62bb7-135">Requirement</span></span> | <span data-ttu-id="62bb7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="62bb7-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="62bb7-137">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="62bb7-137">TAPI version</span></span><br/> | <span data-ttu-id="62bb7-138">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="62bb7-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="62bb7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62bb7-139">Header</span></span><br/>       | <dl> <span data-ttu-id="62bb7-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="62bb7-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62bb7-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62bb7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bb7-142">**\_chiusura riga**</span><span class="sxs-lookup"><span data-stu-id="62bb7-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="62bb7-143">**LINEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="62bb7-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="62bb7-144">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="62bb7-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




