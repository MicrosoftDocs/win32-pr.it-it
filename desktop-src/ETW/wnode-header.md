---
description: La \_ struttura dell'intestazione WNODE è un membro della \_ struttura di proprietà della traccia eventi \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: Struttura WNODE_HEADER (Wmistr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "104982835"
---
# <a name="wnode_header-structure"></a><span data-ttu-id="5fced-103">\_Struttura dell'intestazione WNODE</span><span class="sxs-lookup"><span data-stu-id="5fced-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="5fced-104">La struttura dell' **\_ intestazione WNODE** è un membro della struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="5fced-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fced-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fced-105">Syntax</span></span>


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a><span data-ttu-id="5fced-106">Members</span><span class="sxs-lookup"><span data-stu-id="5fced-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5fced-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="5fced-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-108">Dimensioni totali della memoria allocata, in byte, per le proprietà della sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="5fced-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="5fced-109">La dimensione della memoria deve includere la stanza per la struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , più la stringa del nome di sessione e la stringa del nome del file di log che seguono la struttura in memoria.</span><span class="sxs-lookup"><span data-stu-id="5fced-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-110">**ProviderId**</span><span class="sxs-lookup"><span data-stu-id="5fced-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-111">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="5fced-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-112">**HistoricalContext**</span><span class="sxs-lookup"><span data-stu-id="5fced-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-113">Nell'output, handle per la sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="5fced-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-114">**Versione**</span><span class="sxs-lookup"><span data-stu-id="5fced-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-115">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="5fced-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-116">**Collegamento**</span><span class="sxs-lookup"><span data-stu-id="5fced-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-117">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="5fced-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-118">**KernelHandle**</span><span class="sxs-lookup"><span data-stu-id="5fced-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-119">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="5fced-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-120">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="5fced-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-121">Ora in cui sono state aggiornate le informazioni in questa struttura, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="5fced-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-122">**GUID**</span><span class="sxs-lookup"><span data-stu-id="5fced-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-123">GUID definito per la sessione.</span><span class="sxs-lookup"><span data-stu-id="5fced-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="5fced-124">Per una sessione del logger del kernel NT, impostare questo membro su **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="5fced-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="5fced-125">Se questo membro è impostato su **SystemTraceControlGuid** o **GlobalLoggerGuid**, il logger sarà un logger di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="5fced-126">Per una sessione di logger privata, impostare questo membro sul GUID del provider che si intende abilitare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="5fced-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="5fced-127">Se si avvia una sessione che non è un logger di kernel o una sessione di logger privato, non è necessario specificare un GUID della sessione.</span><span class="sxs-lookup"><span data-stu-id="5fced-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="5fced-128">Se non si specifica un GUID, ETW ne crea uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5fced-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="5fced-129">È necessario specificare un GUID della sessione solo se si desidera modificare le autorizzazioni predefinite associate a una sessione specifica.</span><span class="sxs-lookup"><span data-stu-id="5fced-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="5fced-130">Per informazioni dettagliate, vedere la funzione EventAccessControl.</span><span class="sxs-lookup"><span data-stu-id="5fced-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="5fced-131">Non è possibile avviare più di una sessione con lo stesso GUID della sessione.</span><span class="sxs-lookup"><span data-stu-id="5fced-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="5fced-132">**Prima di Windows Vista:** È possibile avviare più di una sessione con lo stesso GUID della sessione.</span><span class="sxs-lookup"><span data-stu-id="5fced-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="5fced-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-134">Risoluzione del clock da usare quando si registra il timestamp per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="5fced-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="5fced-135">Il valore predefinito è il contatore delle prestazioni delle query (QPC).</span><span class="sxs-lookup"><span data-stu-id="5fced-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="5fced-136">**Prima di Windows Vista:** Il valore predefinito è ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="5fced-137">**Prima di Windows 10, versione 1703:** Non è possibile usare più di 2 tipi di clock distinti simultaneamente da qualsiasi logger di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="5fced-138">**A partire da Windows 10, versione 1703:** La restrizione del tipo di orologio è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="5fced-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="5fced-139">Tutti e tre i tipi di clock possono ora essere usati contemporaneamente dai logger di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="5fced-140">È possibile specificare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5fced-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fced-141">Valore</span><span class="sxs-lookup"><span data-stu-id="5fced-141">Value</span></span></th>
<th><span data-ttu-id="5fced-142">Significato</span><span class="sxs-lookup"><span data-stu-id="5fced-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="5fced-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="5fced-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="5fced-144">Contatore delle prestazioni delle query (QPC).</span><span class="sxs-lookup"><span data-stu-id="5fced-144">Query performance counter (QPC).</span></span> <span data-ttu-id="5fced-145">Il contatore QPC fornisce un timestamp ad alta risoluzione che non è influenzato dalle modifiche apportate al clock di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="5fced-146">Il timestamp archiviato nell'evento è equivalente al valore restituito dall'API QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="5fced-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="5fced-147">Per ulteriori informazioni sulle caratteristiche di questo timestamp, vedere acquisizione di <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">timestamp ad alta risoluzione</a>.</span><span class="sxs-lookup"><span data-stu-id="5fced-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="5fced-148">È consigliabile utilizzare questa soluzione se si dispone di un elevato tasso di eventi o se il consumer unisce eventi da buffer diversi.</span><span class="sxs-lookup"><span data-stu-id="5fced-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="5fced-149">In questi casi, la precisione e la stabilità del timestamp del QPC consentono una maggiore precisione nell'ordinamento degli eventi da buffer diversi.</span><span class="sxs-lookup"><span data-stu-id="5fced-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="5fced-150">Tuttavia, il timestamp QPC non rifletterà gli aggiornamenti al clock di sistema, ad esempio se l'orologio di sistema viene regolato in avanti a causa della sincronizzazione con un server NTP mentre è in corso la traccia, i timestamp QPC nella traccia continueranno a riflettere l'ora come se non si fosse verificato alcun aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5fced-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="5fced-151">Per determinare la risoluzione, usare il membro <strong>PerfFreq</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> durante l'utilizzo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5fced-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="5fced-152">Per convertire il timestamp di un evento in unità 100-ns, usare la formula di conversione seguente:</span><span class="sxs-lookup"><span data-stu-id="5fced-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="5fced-153">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart \* 10000000,0/logfileHeader. PerfFreq. QuadPart</span><span class="sxs-lookup"><span data-stu-id="5fced-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="5fced-154">Si noti che nei computer meno recenti il timestamp potrebbe non essere accurato perché il contatore a volte ignora in avanti a causa di errori hardware.</span><span class="sxs-lookup"><span data-stu-id="5fced-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5fced-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="5fced-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="5fced-156">Ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-156">System time.</span></span> <span data-ttu-id="5fced-157">L'ora di sistema fornisce un timestamp che tiene traccia delle modifiche apportate al clock del sistema, ad esempio se l'orologio di sistema viene regolato in avanti a causa della sincronizzazione con un server NTP mentre è in corso la traccia, i timestamp dell'ora di sistema nella traccia passeranno anche alla nuova impostazione del clock di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="5fced-158">Nei sistemi precedenti a Windows 10, il timestamp archiviato nell'evento è equivalente al valore restituito dall'API GetSystemTimeAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="5fced-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="5fced-159">In Windows 10 o versioni successive, il timestamp archiviato nell'evento è equivalente al valore restituito dall'API GetSystemTimePreciseAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="5fced-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="5fced-160">Prima di Windows 10, la risoluzione di questo timestamp era la risoluzione del tick del clock di sistema, come indicato dal membro TimerResolution di TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="5fced-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="5fced-161">A partire da Windows 10, la risoluzione di questo timestamp è la risoluzione del contatore delle prestazioni, come indicato dal membro PerfFreq di TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="5fced-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="5fced-162">Per convertire il timestamp di un evento in unità 100-ns, usare la formula di conversione seguente:</span><span class="sxs-lookup"><span data-stu-id="5fced-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="5fced-163">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart</span><span class="sxs-lookup"><span data-stu-id="5fced-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="5fced-164">Si noti che quando gli eventi vengono acquisiti in un sistema che esegue un sistema operativo precedente a Windows 10, se il volume degli eventi è elevato, la risoluzione del tempo di sistema potrebbe non essere sufficiente per determinare la sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="5fced-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="5fced-165">In questo caso, un set di eventi avrà lo stesso timestamp, ma l'ordine in cui ETW recapita gli eventi potrebbe non essere corretto.</span><span class="sxs-lookup"><span data-stu-id="5fced-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="5fced-166">A partire da Windows 10, il timestamp viene acquisito con precisione aggiuntiva, anche se è possibile che si verifichi un'instabilità nei casi in cui l'orologio di sistema è stato modificato durante l'acquisizione della traccia.</span><span class="sxs-lookup"><span data-stu-id="5fced-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5fced-167"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="5fced-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="5fced-168">Contatore ciclo CPU.</span><span class="sxs-lookup"><span data-stu-id="5fced-168">CPU cycle counter.</span></span> <span data-ttu-id="5fced-169">Il contatore CPU fornisce il timestamp di risoluzione più elevato ed è il meno intensivo di risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5fced-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="5fced-170">Tuttavia, il contatore della CPU non è affidabile e non deve essere utilizzato nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="5fced-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="5fced-171">Ad esempio, in alcuni computer, i timer cambieranno la frequenza a causa delle modifiche termiche e di risparmio energia, oltre ad arrestare in alcuni Stati.</span><span class="sxs-lookup"><span data-stu-id="5fced-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="5fced-172">Per determinare la risoluzione, usare il membro <strong>CpuSpeedInMHz</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> durante l'utilizzo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5fced-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="5fced-173">Se l'hardware non supporta questo tipo di clock, ETW usa l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="5fced-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="5fced-174"><strong>Windows Server 2003, Windows XP con SP1 e Windows XP:</strong> Questo valore non è supportato, è stato introdotto in Windows Server 2003 con SP1 e Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="5fced-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5fced-175">**Windows 2000:** Il membro **ClientContext** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5fced-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5fced-176">**Flag**</span><span class="sxs-lookup"><span data-stu-id="5fced-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5fced-177">Deve contenere **il \_ \_ \_ GUID tracciato del flag WNODE** per indicare che la struttura contiene informazioni di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="5fced-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fced-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fced-178">Remarks</span></span>

<span data-ttu-id="5fced-179">Assicurarsi di inizializzare la memoria per questa struttura su zero prima di impostare i membri.</span><span class="sxs-lookup"><span data-stu-id="5fced-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="5fced-180">Per convertire un timestamp ETW in un FILETIME, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="5fced-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="5fced-181">Per ogni sessione o file di log in fase di elaborazione (ad esempio per ogni file di log di \_ traccia eventi \_ ), controllare il campo logfile. ProcessTraceMode per determinare se il \_ \_ flag timestamp non elaborato in modalità traccia processo \_ \_ è impostato.</span><span class="sxs-lookup"><span data-stu-id="5fced-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="5fced-182">Per impostazione predefinita, questo flag non è impostato.</span><span class="sxs-lookup"><span data-stu-id="5fced-182">By default, this flag is not set.</span></span> <span data-ttu-id="5fced-183">Se questo flag non è impostato, il runtime ETW convertirà automaticamente il timestamp di ogni record dell'evento \_ in un FILETIME prima di inviare il record dell'evento \_ alla funzione EventRecordCallback, pertanto non sarà necessaria alcuna elaborazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="5fced-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="5fced-184">I passaggi seguenti devono essere utilizzati solo se la traccia viene elaborata con il \_ flag del timestamp RAW della modalità di traccia del processo \_ \_ \_ impostato.</span><span class="sxs-lookup"><span data-stu-id="5fced-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="5fced-185">Per ogni sessione o file di log in fase di elaborazione (ad esempio per ogni file di log di \_ traccia eventi \_ ), controllare il campo logfile. LogfileHeader. ReservedFlags per determinare la scala timestamp per il file di log.</span><span class="sxs-lookup"><span data-stu-id="5fced-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="5fced-186">In base al valore di ReservedFlags, seguire una di queste procedure per determinare il valore da usare per timeStampScale nei passaggi rimanenti:</span><span class="sxs-lookup"><span data-stu-id="5fced-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="5fced-187">a.</span><span class="sxs-lookup"><span data-stu-id="5fced-187">a.</span></span> <span data-ttu-id="5fced-188">Se ReservedFlags = = 1 (QPC): DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart;</span><span class="sxs-lookup"><span data-stu-id="5fced-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="5fced-189">b.</span><span class="sxs-lookup"><span data-stu-id="5fced-189">b.</span></span> <span data-ttu-id="5fced-190">Se ReservedFlags = = 2 (ora di sistema): DOUBLE timeStampScale = 1,0;</span><span class="sxs-lookup"><span data-stu-id="5fced-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="5fced-191">Si noti che i passaggi rimanenti non sono necessari per gli eventi che usano l'ora di sistema, poiché gli eventi forniscono già i timestamp in unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="5fced-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="5fced-192">I passaggi rimanenti funzioneranno ma non saranno necessari e introdurranno un piccolo errore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="5fced-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="5fced-193">c.</span><span class="sxs-lookup"><span data-stu-id="5fced-193">c.</span></span> <span data-ttu-id="5fced-194">Se ReservedFlags = = 3 (contatore cicli CPU): DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz;</span><span class="sxs-lookup"><span data-stu-id="5fced-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="5fced-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fced-195">Requirements</span></span>



| <span data-ttu-id="5fced-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fced-196">Requirement</span></span> | <span data-ttu-id="5fced-197">Valore</span><span class="sxs-lookup"><span data-stu-id="5fced-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5fced-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fced-198">Minimum supported client</span></span><br/> | <span data-ttu-id="5fced-199">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="5fced-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="5fced-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fced-200">Minimum supported server</span></span><br/> | <span data-ttu-id="5fced-201">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5fced-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="5fced-202">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fced-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fced-203"><dt>Wmistr. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fced-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fced-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fced-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fced-205">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="5fced-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="5fced-206">**\_proprietà della traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="5fced-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="5fced-207">**GetTraceLoggerHandle**</span><span class="sxs-lookup"><span data-stu-id="5fced-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="5fced-208">**\_Integer grande**</span><span class="sxs-lookup"><span data-stu-id="5fced-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
