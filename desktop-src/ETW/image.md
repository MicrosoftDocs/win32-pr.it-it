---
description: Questa classe è la classe padre per gli eventi di immagine. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Classe Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979871"
---
# <a name="image-class"></a><span data-ttu-id="3fd92-104">Classe Image</span><span class="sxs-lookup"><span data-stu-id="3fd92-104">Image class</span></span>

<span data-ttu-id="3fd92-105">Questa classe è la classe padre per gli eventi di immagine.</span><span class="sxs-lookup"><span data-stu-id="3fd92-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="3fd92-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3fd92-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd92-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fd92-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3fd92-108">Members</span><span class="sxs-lookup"><span data-stu-id="3fd92-108">Members</span></span>

<span data-ttu-id="3fd92-109">La classe **Image** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="3fd92-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd92-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd92-110">Remarks</span></span>

<span data-ttu-id="3fd92-111">Per abilitare gli eventi di immagine in una sessione di registrazione del kernel NT, specificare il flag di caricamento dell'  **immagine del flag di \_ traccia \_ \_ \_ eventi** nel membro EnableFlags della struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="3fd92-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="3fd92-112">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di caricamento dell'immagine chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="3fd92-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3fd92-113">Usare i tipi di eventi seguenti per identificare gli eventi di caricamento delle immagini quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="3fd92-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="3fd92-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="3fd92-114">Event type</span></span>                                                          | <span data-ttu-id="3fd92-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fd92-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd92-116">**Evento \_ \_ \_ Caricamento del tipo di traccia**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="3fd92-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="3fd92-117">Evento di caricamento dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="3fd92-117">Image load event.</span></span> <span data-ttu-id="3fd92-118">Generato quando viene caricato un file eseguibile o una DLL.</span><span class="sxs-lookup"><span data-stu-id="3fd92-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="3fd92-119">Il provider genera un solo evento per la prima volta che una determinata DLL viene caricata.</span><span class="sxs-lookup"><span data-stu-id="3fd92-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="3fd92-120">La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="3fd92-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="3fd92-121">**Evento \_ \_ \_ Fine tipo di traccia**(il valore del tipo di evento è 2)</span><span class="sxs-lookup"><span data-stu-id="3fd92-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="3fd92-122">Evento di scaricamento immagine.</span><span class="sxs-lookup"><span data-stu-id="3fd92-122">Image unload event.</span></span> <span data-ttu-id="3fd92-123">Generato quando viene scaricato un file eseguibile o una DLL.</span><span class="sxs-lookup"><span data-stu-id="3fd92-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="3fd92-124">Il provider genera un solo evento per l'ultima volta in cui una determinata DLL viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="3fd92-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="3fd92-125">La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="3fd92-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3fd92-126">**Evento \_ Tipo di traccia \_ \_ DC \_ Start**(il valore del tipo di evento è 3)</span><span class="sxs-lookup"><span data-stu-id="3fd92-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="3fd92-127">Evento di avvio raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="3fd92-127">Data collection start event.</span></span> <span data-ttu-id="3fd92-128">Enumera tutte le immagini caricate all'inizio della traccia.</span><span class="sxs-lookup"><span data-stu-id="3fd92-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="3fd92-129">La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="3fd92-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="3fd92-130">**Evento \_ Tipo di traccia \_ \_ DC \_ end**(il valore del tipo di evento è 4)</span><span class="sxs-lookup"><span data-stu-id="3fd92-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="3fd92-131">Evento di fine raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="3fd92-131">Data collection end event.</span></span> <span data-ttu-id="3fd92-132">Enumera tutte le immagini caricate alla fine della traccia.</span><span class="sxs-lookup"><span data-stu-id="3fd92-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="3fd92-133">La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="3fd92-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="3fd92-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd92-134">Requirements</span></span>



| <span data-ttu-id="3fd92-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd92-135">Requirement</span></span> | <span data-ttu-id="3fd92-136">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd92-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fd92-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd92-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd92-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fd92-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3fd92-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd92-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd92-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fd92-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fd92-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fd92-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd92-142">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="3fd92-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="3fd92-143">**\_Caricamento immagine**</span><span class="sxs-lookup"><span data-stu-id="3fd92-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="3fd92-144">**Immagine \_ V0**</span><span class="sxs-lookup"><span data-stu-id="3fd92-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="3fd92-145">**Immagine \_ V1**</span><span class="sxs-lookup"><span data-stu-id="3fd92-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
