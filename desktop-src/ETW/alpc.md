---
description: Questa classe è la classe padre per gli eventi di chiamata di procedura locale avanzati. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977727"
---
# <a name="alpc-class"></a><span data-ttu-id="6f10a-104">Classe ALPC</span><span class="sxs-lookup"><span data-stu-id="6f10a-104">ALPC class</span></span>

<span data-ttu-id="6f10a-105">Questa classe è la classe padre per gli eventi di chiamata di procedura locale avanzati.</span><span class="sxs-lookup"><span data-stu-id="6f10a-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="6f10a-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="6f10a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f10a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f10a-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="6f10a-108">Members</span><span class="sxs-lookup"><span data-stu-id="6f10a-108">Members</span></span>

<span data-ttu-id="6f10a-109">La classe **ALPC** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="6f10a-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f10a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f10a-110">Remarks</span></span>

<span data-ttu-id="6f10a-111">Per abilitare gli eventi di chiamata della procedura locale avanzata in una sessione di registrazione del kernel NT, specificare il flag di **\_ traccia eventi \_ \_ ALPC** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="6f10a-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="6f10a-112">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi ALPC chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ALPCGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="6f10a-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="6f10a-113">Usare i tipi di evento seguenti per identificare l'evento ALPC effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="6f10a-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="6f10a-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="6f10a-114">Event type</span></span>           | <span data-ttu-id="6f10a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f10a-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f10a-116">Valore del tipo di evento, 33</span><span class="sxs-lookup"><span data-stu-id="6f10a-116">Event type value, 33</span></span> | <span data-ttu-id="6f10a-117">Evento Send Message.</span><span class="sxs-lookup"><span data-stu-id="6f10a-117">Send message event.</span></span> <span data-ttu-id="6f10a-118">La classe MOF del [**\_ \_ messaggio Send ALPC**](alpc-send-message.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="6f10a-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="6f10a-119">Valore del tipo di evento, 34</span><span class="sxs-lookup"><span data-stu-id="6f10a-119">Event type value, 34</span></span> | <span data-ttu-id="6f10a-120">Evento Receive Message.</span><span class="sxs-lookup"><span data-stu-id="6f10a-120">Receive message event.</span></span> <span data-ttu-id="6f10a-121">La classe MOF del [**\_ \_ messaggio di ricezione ALPC**](alpc-receive-message.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="6f10a-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="6f10a-122">Valore del tipo di evento, 35</span><span class="sxs-lookup"><span data-stu-id="6f10a-122">Event type value, 35</span></span> | <span data-ttu-id="6f10a-123">Attendere l'evento di risposta.</span><span class="sxs-lookup"><span data-stu-id="6f10a-123">Wait for reply event.</span></span> <span data-ttu-id="6f10a-124">La classe [**ALPC \_ Wait \_ for \_ Reply**](alpc-wait-for-reply.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="6f10a-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="6f10a-125">Valore del tipo di evento, 36</span><span class="sxs-lookup"><span data-stu-id="6f10a-125">Event type value, 36</span></span> | <span data-ttu-id="6f10a-126">Attendere l'evento nuovo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f10a-126">Wait for new message event.</span></span> <span data-ttu-id="6f10a-127">La classe [**ALPC \_ Wait \_ for \_ New \_ Message**](alpc-wait-for-new-message.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="6f10a-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="6f10a-128">Valore del tipo di evento, 37</span><span class="sxs-lookup"><span data-stu-id="6f10a-128">Event type value, 37</span></span> | <span data-ttu-id="6f10a-129">Arresta l'evento in attesa.</span><span class="sxs-lookup"><span data-stu-id="6f10a-129">Stop waiting event.</span></span> <span data-ttu-id="6f10a-130">La classe [**ALPC \_ Unwait**](alpc-unwait.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="6f10a-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="6f10a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f10a-131">Requirements</span></span>



| <span data-ttu-id="6f10a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f10a-132">Requirement</span></span> | <span data-ttu-id="6f10a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6f10a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f10a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f10a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6f10a-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f10a-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f10a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f10a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6f10a-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f10a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

