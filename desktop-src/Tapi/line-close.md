---
description: Il messaggio di chiusura della riga di TAPI \_ viene inviato quando il dispositivo a linee specificato è stato chiuso forzatamente. Quando il messaggio è stato inviato, l'handle di dispositivo linea o qualsiasi handle di chiamata per le chiamate sulla riga non sono più validi.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Messaggio di LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327497"
---
# <a name="line_close-message"></a><span data-ttu-id="5a9ff-104">\_Messaggio di chiusura riga</span><span class="sxs-lookup"><span data-stu-id="5a9ff-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="5a9ff-105">Il messaggio **di \_ chiusura della riga** di TAPI viene inviato quando il dispositivo a linee specificato è stato chiuso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="5a9ff-106">Quando il messaggio è stato inviato, l'handle di dispositivo linea o qualsiasi handle di chiamata per le chiamate sulla riga non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5a9ff-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a9ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9ff-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="5a9ff-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9ff-109">Handle per il dispositivo della linea che è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="5a9ff-110">Questo handle non è più valido.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="5a9ff-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="5a9ff-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9ff-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="5a9ff-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5a9ff-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9ff-114">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="5a9ff-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5a9ff-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9ff-116">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="5a9ff-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5a9ff-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9ff-118">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9ff-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a9ff-119">Return value</span></span>

<span data-ttu-id="5a9ff-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9ff-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a9ff-121">Remarks</span></span>

<span data-ttu-id="5a9ff-122">Il messaggio di **\_ chiusura riga** viene inviato a qualsiasi applicazione solo dopo che il provider di servizi TAPI (TSP) ha chiuso forzatamente una linea aperta.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="5a9ff-123">Indica se la riga può essere riaperta immediatamente dopo una chiusura forzata è specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="5a9ff-124">La condizione che provoca la causa può essere una modifica significativa dello stato, un errore hardware, una perdita di connessione a un server o anche potenzialmente impedire a una singola applicazione di monopolizzare un dispositivo a linee troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="5a9ff-125">Un dispositivo A linee può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione di tale riga o del relativo driver.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="5a9ff-126">Se l'utente desidera che le modifiche di configurazione vengano applicate immediatamente (a differenza di dopo il successivo riavvio del sistema) e influiscono sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="5a9ff-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9ff-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a9ff-127">Requirements</span></span>



| <span data-ttu-id="5a9ff-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a9ff-128">Requirement</span></span> | <span data-ttu-id="5a9ff-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5a9ff-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5a9ff-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5a9ff-130">TAPI version</span></span><br/> | <span data-ttu-id="5a9ff-131">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5a9ff-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5a9ff-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a9ff-132">Header</span></span><br/>       | <dl> <span data-ttu-id="5a9ff-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9ff-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




