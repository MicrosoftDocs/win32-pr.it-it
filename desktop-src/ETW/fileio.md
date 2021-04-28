---
description: 'Classe FileIo: questa classe è la classe padre per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Classe FileIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106529"
---
# <a name="fileio-class"></a><span data-ttu-id="76b36-104">Classe FileIo</span><span class="sxs-lookup"><span data-stu-id="76b36-104">FileIo class</span></span>

<span data-ttu-id="76b36-105">Questa classe è la classe padre per gli eventi di I/O di file.</span><span class="sxs-lookup"><span data-stu-id="76b36-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="76b36-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="76b36-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b36-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76b36-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="76b36-108">Members</span><span class="sxs-lookup"><span data-stu-id="76b36-108">Members</span></span>

<span data-ttu-id="76b36-109">La **classe FileIo** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="76b36-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="76b36-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="76b36-110">Remarks</span></span>

<span data-ttu-id="76b36-111">Per abilitare gli eventi di I/O di file in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG DISK FILE \_ \_ \_ \_ \_ IO** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="76b36-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="76b36-112">È anche possibile specificare uno o più dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="76b36-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="76b36-113">**\_I/O DEL FILE DEL FLAG DI TRACCIA \_ \_ \_ EVENTI**</span><span class="sxs-lookup"><span data-stu-id="76b36-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="76b36-114">**FILE \_ DEL FLAG DI TRACCIA EVENTI IO \_ \_ \_ \_ INIT**</span><span class="sxs-lookup"><span data-stu-id="76b36-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="76b36-115">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di I/O di file chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**FileIoGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="76b36-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="76b36-116">Usare i tipi di evento seguenti per identificare l'evento effettivo quando si usano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="76b36-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="76b36-117">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="76b36-117">Event type</span></span>             | <span data-ttu-id="76b36-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76b36-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b36-119">Il valore del tipo di evento è 0</span><span class="sxs-lookup"><span data-stu-id="76b36-119">Event type value is 0</span></span>  | <span data-ttu-id="76b36-120">Evento nome file.</span><span class="sxs-lookup"><span data-stu-id="76b36-120">File name event.</span></span> <span data-ttu-id="76b36-121">La [**classe MOF FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="76b36-122">Il valore del tipo di evento è 32</span><span class="sxs-lookup"><span data-stu-id="76b36-122">Event type value is 32</span></span> | <span data-ttu-id="76b36-123">Evento di creazione file.</span><span class="sxs-lookup"><span data-stu-id="76b36-123">File create event.</span></span> <span data-ttu-id="76b36-124">La [**classe MOF FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="76b36-125">Il valore del tipo di evento è 35</span><span class="sxs-lookup"><span data-stu-id="76b36-125">Event type value is 35</span></span> | <span data-ttu-id="76b36-126">Evento di eliminazione file.</span><span class="sxs-lookup"><span data-stu-id="76b36-126">File delete event.</span></span> <span data-ttu-id="76b36-127">La classe MOF [**FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="76b36-128">Il valore del tipo di evento è 36</span><span class="sxs-lookup"><span data-stu-id="76b36-128">Event type value is 36</span></span> | <span data-ttu-id="76b36-129">Evento di rundown del file.</span><span class="sxs-lookup"><span data-stu-id="76b36-129">File rundown event.</span></span> <span data-ttu-id="76b36-130">Enumera tutti i file aperti nel computer alla fine della sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="76b36-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="76b36-131">La classe MOF [**FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="76b36-132">Il valore del tipo di evento è 64</span><span class="sxs-lookup"><span data-stu-id="76b36-132">Event type value is 64</span></span> | <span data-ttu-id="76b36-133">Evento di creazione file.</span><span class="sxs-lookup"><span data-stu-id="76b36-133">File create event.</span></span> <span data-ttu-id="76b36-134">La [**classe FileIo \_ Create**](fileio-create.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="76b36-135">Il valore del tipo di evento è 72</span><span class="sxs-lookup"><span data-stu-id="76b36-135">Event type value is 72</span></span> | <span data-ttu-id="76b36-136">Evento di enumerazione della directory.</span><span class="sxs-lookup"><span data-stu-id="76b36-136">Directory enumeration event.</span></span> <span data-ttu-id="76b36-137">La [**classe MOF FileIo \_ DirEnum**](fileio-direnum.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="76b36-138">Il valore del tipo di evento è 77</span><span class="sxs-lookup"><span data-stu-id="76b36-138">Event type value is 77</span></span> | <span data-ttu-id="76b36-139">Evento di notifica della directory.</span><span class="sxs-lookup"><span data-stu-id="76b36-139">Directory notification event.</span></span> <span data-ttu-id="76b36-140">La [**classe MOF FileIo \_ DirEnum**](fileio-direnum.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="76b36-141">Il valore del tipo di evento è 69</span><span class="sxs-lookup"><span data-stu-id="76b36-141">Event type value is 69</span></span> | <span data-ttu-id="76b36-142">Evento di impostazione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="76b36-142">Set information event.</span></span> <span data-ttu-id="76b36-143">La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="76b36-144">Il valore del tipo di evento è 70</span><span class="sxs-lookup"><span data-stu-id="76b36-144">Event type value is 70</span></span> | <span data-ttu-id="76b36-145">Evento di eliminazione del file.</span><span class="sxs-lookup"><span data-stu-id="76b36-145">Delete file event.</span></span> <span data-ttu-id="76b36-146">La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="76b36-147">Il valore del tipo di evento è 71</span><span class="sxs-lookup"><span data-stu-id="76b36-147">Event type value is 71</span></span> | <span data-ttu-id="76b36-148">Rinominare l'evento del file.</span><span class="sxs-lookup"><span data-stu-id="76b36-148">Rename file event.</span></span> <span data-ttu-id="76b36-149">La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="76b36-150">Il valore del tipo di evento è 74</span><span class="sxs-lookup"><span data-stu-id="76b36-150">Event type value is 74</span></span> | <span data-ttu-id="76b36-151">Eseguire query sull'evento di informazioni sul file.</span><span class="sxs-lookup"><span data-stu-id="76b36-151">Query file information event.</span></span> <span data-ttu-id="76b36-152">La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="76b36-153">Il valore del tipo di evento è 75</span><span class="sxs-lookup"><span data-stu-id="76b36-153">Event type value is 75</span></span> | <span data-ttu-id="76b36-154">Evento di controllo del file system.</span><span class="sxs-lookup"><span data-stu-id="76b36-154">File system control event.</span></span> <span data-ttu-id="76b36-155">La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="76b36-156">Il valore del tipo di evento è 76</span><span class="sxs-lookup"><span data-stu-id="76b36-156">Event type value is 76</span></span> | <span data-ttu-id="76b36-157">Evento di fine operazione.</span><span class="sxs-lookup"><span data-stu-id="76b36-157">End of operation event.</span></span> <span data-ttu-id="76b36-158">La [**classe MOF FileIo \_ OpEnd**](fileio-opend.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="76b36-159">Il valore del tipo di evento è 67</span><span class="sxs-lookup"><span data-stu-id="76b36-159">Event type value is 67</span></span> | <span data-ttu-id="76b36-160">Evento di lettura file.</span><span class="sxs-lookup"><span data-stu-id="76b36-160">File read event.</span></span> <span data-ttu-id="76b36-161">La [**classe MOF FileIo \_ ReadWrite**](fileio-readwrite.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="76b36-162">Il valore del tipo di evento è 68</span><span class="sxs-lookup"><span data-stu-id="76b36-162">Event type value is 68</span></span> | <span data-ttu-id="76b36-163">Evento di scrittura file.</span><span class="sxs-lookup"><span data-stu-id="76b36-163">File write event.</span></span> <span data-ttu-id="76b36-164">La [**classe MOF FileIo \_ ReadWrite**](fileio-readwrite.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="76b36-165">Il valore del tipo di evento è 65</span><span class="sxs-lookup"><span data-stu-id="76b36-165">Event type value is 65</span></span> | <span data-ttu-id="76b36-166">Evento di pulizia.</span><span class="sxs-lookup"><span data-stu-id="76b36-166">Clean up event.</span></span> <span data-ttu-id="76b36-167">L'evento viene generato quando viene rilasciato l'ultimo handle per il file.</span><span class="sxs-lookup"><span data-stu-id="76b36-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="76b36-168">La [**classe MOF FileIo \_ SimpleOp**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="76b36-169">Il valore del tipo di evento è 66</span><span class="sxs-lookup"><span data-stu-id="76b36-169">Event type value is 66</span></span> | <span data-ttu-id="76b36-170">Evento di chiusura.</span><span class="sxs-lookup"><span data-stu-id="76b36-170">Close event.</span></span> <span data-ttu-id="76b36-171">L'evento viene generato quando l'oggetto file viene liberato.</span><span class="sxs-lookup"><span data-stu-id="76b36-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="76b36-172">La [**classe MOF FileIo \_ SimpleOp**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="76b36-173">Il valore del tipo di evento è 73</span><span class="sxs-lookup"><span data-stu-id="76b36-173">Event type value is 73</span></span> | <span data-ttu-id="76b36-174">Evento Flush.</span><span class="sxs-lookup"><span data-stu-id="76b36-174">Flush event.</span></span> <span data-ttu-id="76b36-175">Questo evento viene generato quando i buffer dei file vengono scaricati completamente su disco.</span><span class="sxs-lookup"><span data-stu-id="76b36-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="76b36-176">La [**classe MOF FileIo \_ SimpleOp**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="76b36-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="76b36-177">Gli eventi di I/O di file vengono registrati all'inizio dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="76b36-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b36-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76b36-178">Requirements</span></span>



| <span data-ttu-id="76b36-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="76b36-179">Requirement</span></span> | <span data-ttu-id="76b36-180">Valore</span><span class="sxs-lookup"><span data-stu-id="76b36-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76b36-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76b36-181">Minimum supported client</span></span><br/> | <span data-ttu-id="76b36-182">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76b36-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76b36-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76b36-183">Minimum supported server</span></span><br/> | <span data-ttu-id="76b36-184">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="76b36-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76b36-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76b36-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b36-186">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="76b36-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="76b36-187">**FileIo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="76b36-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="76b36-188">**FileIo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="76b36-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
