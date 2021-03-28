---
description: Questa classe è la classe padre per gli eventi di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Classe DiskIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966507"
---
# <a name="diskio-class"></a><span data-ttu-id="24f86-104">Classe DiskIo</span><span class="sxs-lookup"><span data-stu-id="24f86-104">DiskIo class</span></span>

<span data-ttu-id="24f86-105">Questa classe è la classe padre per gli eventi di I/O su disco.</span><span class="sxs-lookup"><span data-stu-id="24f86-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="24f86-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="24f86-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f86-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24f86-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="24f86-108">Members</span><span class="sxs-lookup"><span data-stu-id="24f86-108">Members</span></span>

<span data-ttu-id="24f86-109">La classe **DiskIo** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="24f86-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f86-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="24f86-110">Remarks</span></span>

<span data-ttu-id="24f86-111">Per abilitare gli eventi di I/o su disco in una sessione di registrazione del kernel NT, specificare il flag di i  /o del **disco del flag di \_ traccia \_ \_ \_ eventi** nel membro EnableFlags di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="24f86-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="24f86-112">È anche possibile specificare uno o più dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="24f86-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="24f86-113">**i/o \_ \_ \_ disco \_ flag \_ di traccia eventi**</span><span class="sxs-lookup"><span data-stu-id="24f86-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="24f86-114">**\_ \_ driver flag di traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="24f86-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="24f86-115">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di I/O su disco chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**DiskIoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="24f86-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="24f86-116">Usare i tipi di evento seguenti per identificare l'evento di I/O del disco effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="24f86-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="24f86-117">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="24f86-117">Event type</span></span>                                                                      | <span data-ttu-id="24f86-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24f86-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f86-119">**Evento \_ Tipo di traccia \_ \_ io \_ letti**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="24f86-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="24f86-120">Evento Read.</span><span class="sxs-lookup"><span data-stu-id="24f86-120">Read event.</span></span> <span data-ttu-id="24f86-121">La classe MOF [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="24f86-122">**Evento \_ Tipo di traccia \_ \_ io \_ Write**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="24f86-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="24f86-123">Evento Write.</span><span class="sxs-lookup"><span data-stu-id="24f86-123">Write event.</span></span> <span data-ttu-id="24f86-124">La classe MOF [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="24f86-125">**Evento \_ Tipo di traccia \_ \_ io \_ Read \_ init**(il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="24f86-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="24f86-126">Inizializza l'evento di lettura.</span><span class="sxs-lookup"><span data-stu-id="24f86-126">Initialize read event.</span></span> <span data-ttu-id="24f86-127">La classe MOF [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="24f86-128">**Evento \_ Tipo di traccia \_ \_ io \_ Write \_ init**(il valore del tipo di evento è 13)</span><span class="sxs-lookup"><span data-stu-id="24f86-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="24f86-129">Inizializza l'evento di scrittura.</span><span class="sxs-lookup"><span data-stu-id="24f86-129">Initialize write event.</span></span> <span data-ttu-id="24f86-130">La classe MOF [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="24f86-131">**Evento \_ Tipo di traccia \_ \_ io \_ Flush**(il valore del tipo di evento è 14)</span><span class="sxs-lookup"><span data-stu-id="24f86-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="24f86-132">Inizializza l'evento di scrittura.</span><span class="sxs-lookup"><span data-stu-id="24f86-132">Initialize write event.</span></span> <span data-ttu-id="24f86-133">La classe MOF [**DiskIo \_ TypeGroup3**](diskio-typegroup3.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="24f86-134">**Evento \_ Tipo di traccia \_ \_ io \_ Flush \_ init**(il valore del tipo di evento è 15)</span><span class="sxs-lookup"><span data-stu-id="24f86-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="24f86-135">Inizializzare l'evento di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="24f86-135">Initialize flush event.</span></span> <span data-ttu-id="24f86-136">La classe MOF [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="24f86-137">**Evento \_ Tipo di traccia \_ \_ io \_ reindirizzato \_ init**(il valore del tipo di evento è 16)</span><span class="sxs-lookup"><span data-stu-id="24f86-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="24f86-138">Inizializzare l'evento reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="24f86-138">Initialize redirected event.</span></span> <span data-ttu-id="24f86-139">Gli eventi i/o reindirizzati vengono usati per eseguire il mapping di IOs del disco a un formato Windows Imaging (WIM) al nome file all'interno del file WIM.</span><span class="sxs-lookup"><span data-stu-id="24f86-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="24f86-140">Il valore del tipo di evento è 52</span><span class="sxs-lookup"><span data-stu-id="24f86-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="24f86-141">Evento di richiesta completo del driver.</span><span class="sxs-lookup"><span data-stu-id="24f86-141">Driver complete request event.</span></span> <span data-ttu-id="24f86-142">La classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="24f86-143">Il valore del tipo di evento è 53</span><span class="sxs-lookup"><span data-stu-id="24f86-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="24f86-144">Evento restituito della richiesta di completamento del driver.</span><span class="sxs-lookup"><span data-stu-id="24f86-144">Driver complete request return event.</span></span> <span data-ttu-id="24f86-145">La classe MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="24f86-146">Il valore del tipo di evento è 37</span><span class="sxs-lookup"><span data-stu-id="24f86-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="24f86-147">Evento di routine di completamento del driver.</span><span class="sxs-lookup"><span data-stu-id="24f86-147">Driver completion routine event.</span></span> <span data-ttu-id="24f86-148">La classe MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="24f86-149">Il valore del tipo di evento è 34</span><span class="sxs-lookup"><span data-stu-id="24f86-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="24f86-150">Evento di chiamata di funzione principale del driver.</span><span class="sxs-lookup"><span data-stu-id="24f86-150">Driver major function call event.</span></span> <span data-ttu-id="24f86-151">La classe MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="24f86-152">Il valore del tipo di evento è 35</span><span class="sxs-lookup"><span data-stu-id="24f86-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="24f86-153">Evento di chiamata di funzione principale del driver.</span><span class="sxs-lookup"><span data-stu-id="24f86-153">Driver major function call return event.</span></span> <span data-ttu-id="24f86-154">La classe MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="24f86-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="24f86-155">Il provider I/O su disco non è in grado di identificare il file letto o scritto durante un evento di I/O su disco.</span><span class="sxs-lookup"><span data-stu-id="24f86-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="24f86-156">Per recuperare il nome del file associato all'evento di I/O su disco, abilitare il provider di eventi I/0 del file.</span><span class="sxs-lookup"><span data-stu-id="24f86-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="24f86-157">Gli eventi di I/O su disco vengono registrati all'ora di completamento di I/O.</span><span class="sxs-lookup"><span data-stu-id="24f86-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="24f86-158">Per determinare quando è iniziata l'operazione di I/O, utilizzare gli eventi di inizializzazione, ad esempio, il \_ tipo di traccia eventi \_ \_ io \_ Read \_ init.</span><span class="sxs-lookup"><span data-stu-id="24f86-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f86-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24f86-159">Requirements</span></span>



| <span data-ttu-id="24f86-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f86-160">Requirement</span></span> | <span data-ttu-id="24f86-161">Valore</span><span class="sxs-lookup"><span data-stu-id="24f86-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24f86-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f86-162">Minimum supported client</span></span><br/> | <span data-ttu-id="24f86-163">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="24f86-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="24f86-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f86-164">Minimum supported server</span></span><br/> | <span data-ttu-id="24f86-165">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24f86-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24f86-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24f86-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f86-167">**\_TypeGroup1 DiskIo**</span><span class="sxs-lookup"><span data-stu-id="24f86-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="24f86-168">**\_TypeGroup2 DiskIo**</span><span class="sxs-lookup"><span data-stu-id="24f86-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="24f86-169">**\_TypeGroup3 DiskIo**</span><span class="sxs-lookup"><span data-stu-id="24f86-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="24f86-170">**DriverCompleteRequest**</span><span class="sxs-lookup"><span data-stu-id="24f86-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="24f86-171">**DriverCompleteRequestReturn**</span><span class="sxs-lookup"><span data-stu-id="24f86-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="24f86-172">**DriverCompletionRoutine**</span><span class="sxs-lookup"><span data-stu-id="24f86-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="24f86-173">**DriverMajorFunctionCall**</span><span class="sxs-lookup"><span data-stu-id="24f86-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="24f86-174">**DriverMajorFunctionReturn**</span><span class="sxs-lookup"><span data-stu-id="24f86-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
