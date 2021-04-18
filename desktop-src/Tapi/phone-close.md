---
description: Il messaggio di \_ chiusura telefono TAPI viene inviato quando un dispositivo telefonico aperto è stato chiuso forzatamente come parte del recupero delle risorse. L'handle del dispositivo non è più valido dopo l'invio del messaggio.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Messaggio di PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329209"
---
# <a name="phone_close-message"></a><span data-ttu-id="7aeab-104">\_Messaggio di chiusura telefono</span><span class="sxs-lookup"><span data-stu-id="7aeab-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="7aeab-105">Il messaggio **di \_ chiusura telefono** TAPI viene inviato quando un dispositivo telefonico aperto è stato chiuso forzatamente come parte del recupero delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7aeab-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="7aeab-106">L'handle del dispositivo non è più valido dopo l'invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7aeab-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7aeab-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7aeab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aeab-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="7aeab-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="7aeab-109">Handle per il dispositivo telefonico aperto che è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="7aeab-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="7aeab-110">L'handle non è più valido dopo l'invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7aeab-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="7aeab-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7aeab-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7aeab-112">Istanza di callback dell'applicazione fornita durante l'apertura del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="7aeab-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="7aeab-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7aeab-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7aeab-114">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7aeab-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7aeab-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7aeab-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7aeab-116">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7aeab-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7aeab-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7aeab-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7aeab-118">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7aeab-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aeab-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7aeab-119">Return value</span></span>

<span data-ttu-id="7aeab-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7aeab-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aeab-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="7aeab-121">Remarks</span></span>

<span data-ttu-id="7aeab-122">Il messaggio di **\_ chiusura del telefono** viene inviato a un'applicazione solo dopo la chiusura forzata di un telefono aperto.</span><span class="sxs-lookup"><span data-stu-id="7aeab-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="7aeab-123">Questa operazione può essere eseguita per impedire a una singola applicazione di monopolizzare un dispositivo telefonico troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="7aeab-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="7aeab-124">Se il telefono può essere riaperto immediatamente dopo una chiusura forzata è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aeab-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="7aeab-125">Un dispositivo telefonico aperto può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione del telefono o del driver.</span><span class="sxs-lookup"><span data-stu-id="7aeab-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="7aeab-126">Se l'utente desidera che le modifiche di configurazione vengano applicate immediatamente (in contrapposizione al successivo riavvio del sistema) e tali modifiche influiscono sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="7aeab-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aeab-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aeab-127">Requirements</span></span>



| <span data-ttu-id="7aeab-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aeab-128">Requirement</span></span> | <span data-ttu-id="7aeab-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7aeab-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7aeab-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7aeab-130">TAPI version</span></span><br/> | <span data-ttu-id="7aeab-131">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7aeab-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7aeab-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7aeab-132">Header</span></span><br/>       | <dl> <span data-ttu-id="7aeab-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aeab-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




