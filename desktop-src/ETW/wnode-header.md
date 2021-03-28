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
# <a name="wnode_header-structure"></a>\_Struttura dell'intestazione WNODE

La struttura dell' **\_ intestazione WNODE** è un membro della struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

## <a name="syntax"></a>Sintassi


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



## <a name="members"></a>Members

<dl> <dt>

**BufferSize**
</dt> <dd>

Dimensioni totali della memoria allocata, in byte, per le proprietà della sessione di traccia eventi. La dimensione della memoria deve includere la stanza per la struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , più la stringa del nome di sessione e la stringa del nome del file di log che seguono la struttura in memoria.

</dd> <dt>

**ProviderId**
</dt> <dd>

Riservato per utilizzo interno.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

Nell'output, handle per la sessione di traccia eventi.

</dd> <dt>

**Versione**
</dt> <dd>

Riservato per utilizzo interno.

</dd> <dt>

**Collegamento**
</dt> <dd>

Riservato per utilizzo interno.

</dd> <dt>

**KernelHandle**
</dt> <dd>

Riservato per utilizzo interno.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Ora in cui sono state aggiornate le informazioni in questa struttura, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.

</dd> <dt>

**GUID**
</dt> <dd>

GUID definito per la sessione.

Per una sessione del logger del kernel NT, impostare questo membro su **SystemTraceControlGuid**.

Se questo membro è impostato su **SystemTraceControlGuid** o **GlobalLoggerGuid**, il logger sarà un logger di sistema.

Per una sessione di logger privata, impostare questo membro sul GUID del provider che si intende abilitare per la sessione.

Se si avvia una sessione che non è un logger di kernel o una sessione di logger privato, non è necessario specificare un GUID della sessione. Se non si specifica un GUID, ETW ne crea uno automaticamente. È necessario specificare un GUID della sessione solo se si desidera modificare le autorizzazioni predefinite associate a una sessione specifica. Per informazioni dettagliate, vedere la funzione EventAccessControl.

Non è possibile avviare più di una sessione con lo stesso GUID della sessione.

**Prima di Windows Vista:** È possibile avviare più di una sessione con lo stesso GUID della sessione.

</dd> <dt>

**ClientContext**
</dt> <dd>

Risoluzione del clock da usare quando si registra il timestamp per ogni evento. Il valore predefinito è il contatore delle prestazioni delle query (QPC).

**Prima di Windows Vista:** Il valore predefinito è ora di sistema.

**Prima di Windows 10, versione 1703:** Non è possibile usare più di 2 tipi di clock distinti simultaneamente da qualsiasi logger di sistema.

**A partire da Windows 10, versione 1703:** La restrizione del tipo di orologio è stata rimossa. Tutti e tre i tipi di clock possono ora essere usati contemporaneamente dai logger di sistema.

È possibile specificare uno dei valori seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>1</dt> </dl></td>
<td>Contatore delle prestazioni delle query (QPC). Il contatore QPC fornisce un timestamp ad alta risoluzione che non è influenzato dalle modifiche apportate al clock di sistema. Il timestamp archiviato nell'evento è equivalente al valore restituito dall'API QueryPerformanceCounter. Per ulteriori informazioni sulle caratteristiche di questo timestamp, vedere acquisizione di <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">timestamp ad alta risoluzione</a>.<br/> È consigliabile utilizzare questa soluzione se si dispone di un elevato tasso di eventi o se il consumer unisce eventi da buffer diversi. In questi casi, la precisione e la stabilità del timestamp del QPC consentono una maggiore precisione nell'ordinamento degli eventi da buffer diversi. Tuttavia, il timestamp QPC non rifletterà gli aggiornamenti al clock di sistema, ad esempio se l'orologio di sistema viene regolato in avanti a causa della sincronizzazione con un server NTP mentre è in corso la traccia, i timestamp QPC nella traccia continueranno a riflettere l'ora come se non si fosse verificato alcun aggiornamento.<br/> Per determinare la risoluzione, usare il membro <strong>PerfFreq</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> durante l'utilizzo dell'evento.<br/> Per convertire il timestamp di un evento in unità 100-ns, usare la formula di conversione seguente: <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart * 10000000,0/logfileHeader. PerfFreq. QuadPart<br/> Si noti che nei computer meno recenti il timestamp potrebbe non essere accurato perché il contatore a volte ignora in avanti a causa di errori hardware.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>Ora di sistema. L'ora di sistema fornisce un timestamp che tiene traccia delle modifiche apportate al clock del sistema, ad esempio se l'orologio di sistema viene regolato in avanti a causa della sincronizzazione con un server NTP mentre è in corso la traccia, i timestamp dell'ora di sistema nella traccia passeranno anche alla nuova impostazione del clock di sistema. <br/>
<ul>
<li>Nei sistemi precedenti a Windows 10, il timestamp archiviato nell'evento è equivalente al valore restituito dall'API GetSystemTimeAsFileTime.</li>
<li>In Windows 10 o versioni successive, il timestamp archiviato nell'evento è equivalente al valore restituito dall'API GetSystemTimePreciseAsFileTime.</li>
</ul>
Prima di Windows 10, la risoluzione di questo timestamp era la risoluzione del tick del clock di sistema, come indicato dal membro TimerResolution di TRACE_LOGFILE_HEADER. A partire da Windows 10, la risoluzione di questo timestamp è la risoluzione del contatore delle prestazioni, come indicato dal membro PerfFreq di TRACE_LOGFILE_HEADER.<br/> Per convertire il timestamp di un evento in unità 100-ns, usare la formula di conversione seguente: <br/> scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart<br/> Si noti che quando gli eventi vengono acquisiti in un sistema che esegue un sistema operativo precedente a Windows 10, se il volume degli eventi è elevato, la risoluzione del tempo di sistema potrebbe non essere sufficiente per determinare la sequenza di eventi. In questo caso, un set di eventi avrà lo stesso timestamp, ma l'ordine in cui ETW recapita gli eventi potrebbe non essere corretto. A partire da Windows 10, il timestamp viene acquisito con precisione aggiuntiva, anche se è possibile che si verifichi un'instabilità nei casi in cui l'orologio di sistema è stato modificato durante l'acquisizione della traccia.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>3</dt> </dl></td>
<td>Contatore ciclo CPU. Il contatore CPU fornisce il timestamp di risoluzione più elevato ed è il meno intensivo di risorse da recuperare. Tuttavia, il contatore della CPU non è affidabile e non deve essere utilizzato nell'ambiente di produzione. Ad esempio, in alcuni computer, i timer cambieranno la frequenza a causa delle modifiche termiche e di risparmio energia, oltre ad arrestare in alcuni Stati.<br/> Per determinare la risoluzione, usare il membro <strong>CpuSpeedInMHz</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> durante l'utilizzo dell'evento.<br/> Se l'hardware non supporta questo tipo di clock, ETW usa l'ora di sistema.<br/> <strong>Windows Server 2003, Windows XP con SP1 e Windows XP:</strong> Questo valore non è supportato, è stato introdotto in Windows Server 2003 con SP1 e Windows XP con SP2.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000:** Il membro **ClientContext** non è supportato.

</dd> <dt>

**Flag**
</dt> <dd>

Deve contenere **il \_ \_ \_ GUID tracciato del flag WNODE** per indicare che la struttura contiene informazioni di traccia eventi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Assicurarsi di inizializzare la memoria per questa struttura su zero prima di impostare i membri.

Per convertire un timestamp ETW in un FILETIME, attenersi alla procedura seguente:

<dl> 1. Per ogni sessione o file di log in fase di elaborazione (ad esempio per ogni file di log di \_ traccia eventi \_ ), controllare il campo logfile. ProcessTraceMode per determinare se il \_ \_ flag timestamp non elaborato in modalità traccia processo \_ \_ è impostato. Per impostazione predefinita, questo flag non è impostato. Se questo flag non è impostato, il runtime ETW convertirà automaticamente il timestamp di ogni record dell'evento \_ in un FILETIME prima di inviare il record dell'evento \_ alla funzione EventRecordCallback, pertanto non sarà necessaria alcuna elaborazione aggiuntiva. I passaggi seguenti devono essere utilizzati solo se la traccia viene elaborata con il \_ flag del timestamp RAW della modalità di traccia del processo \_ \_ \_ impostato.  
2. Per ogni sessione o file di log in fase di elaborazione (ad esempio per ogni file di log di \_ traccia eventi \_ ), controllare il campo logfile. LogfileHeader. ReservedFlags per determinare la scala timestamp per il file di log. In base al valore di ReservedFlags, seguire una di queste procedure per determinare il valore da usare per timeStampScale nei passaggi rimanenti: <dl> a. Se ReservedFlags = = 1 (QPC): DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart;  
b. Se ReservedFlags = = 2 (ora di sistema): DOUBLE timeStampScale = 1,0;  
Si noti che i passaggi rimanenti non sono necessari per gli eventi che usano l'ora di sistema, poiché gli eventi forniscono già i timestamp in unità di tempo. I passaggi rimanenti funzioneranno ma non saranno necessari e introdurranno un piccolo errore di arrotondamento.  
c. Se ReservedFlags = = 3 (contatore cicli CPU): DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                   |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Wmistr. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**\_proprietà della traccia eventi \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**\_Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
