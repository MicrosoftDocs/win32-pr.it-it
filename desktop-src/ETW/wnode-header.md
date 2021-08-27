---
description: La struttura WNODE \_ HEADER è un membro della struttura EVENT TRACE \_ \_ PROPERTIES.
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER struttura (Wmistr.h)
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
ms.openlocfilehash: 93cecb900b0c62084a3b5ea4e4a7789575c20c27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480687"
---
# <a name="wnode_header-structure"></a>Struttura WNODE \_ HEADER

La **struttura WNODE \_ HEADER** è un membro della [**struttura EVENT TRACE \_ \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

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

Dimensione totale della memoria allocata, in byte, per le proprietà della sessione di traccia eventi. Le dimensioni della memoria devono includere lo spazio per la struttura [**EVENT \_ TRACE \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) più la stringa del nome della sessione e la stringa del nome del file di log che seguono la struttura in memoria.

</dd> <dt>

**ProviderId**
</dt> <dd>

Riservato per utilizzo interno.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

Nell'output, handle per la sessione di traccia eventi.

</dd> <dt>

**Version**
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

**Timestamp**
</dt> <dd>

Ora in cui le informazioni in questa struttura sono state aggiornate, a intervalli di 100 nanosecondi dalla mezzanotte del 1° gennaio 1601.

</dd> <dt>

**Guid**
</dt> <dd>

GUID definito per la sessione.

Per una sessione del logger del kernel NT, impostare questo membro **su SystemTraceControlGuid**.

Se questo membro è impostato su **SystemTraceControlGuid** o **GlobalLoggerGuid,** il logger sarà un logger di sistema.

Per una sessione di logger privata, impostare questo membro sul GUID del provider che si desidera abilitare per la sessione.

Se si avvia una sessione che non è un logger del kernel o una sessione privata del logger, non è necessario specificare un GUID di sessione. Se non si specifica un GUID, ETW ne crea uno automaticamente. È necessario specificare un GUID di sessione solo se si desidera modificare le autorizzazioni predefinite associate a una sessione specifica. Per informazioni dettagliate, vedere la funzione EventAccessControl.

Non è possibile avviare più di una sessione con lo stesso GUID di sessione.

**Prima di Windows Vista:** È possibile avviare più di una sessione con lo stesso GUID di sessione.

</dd> <dt>

**ClientContext**
</dt> <dd>

Risoluzione del clock da utilizzare per la registrazione del timestamp per ogni evento. Il valore predefinito è Query performance counter (QPC).

**Prima di Windows Vista:** Il valore predefinito è l'ora di sistema.

**Prima di Windows 10, versione 1703:** Nessun logger di sistema può usare contemporaneamente più di 2 tipi di clock distinti.

**A partire Windows 10, versione 1703:** La restrizione del tipo di orologio è stata rimossa. Tutti e tre i tipi di clock possono ora essere usati contemporaneamente dai logger di sistema.

È possibile specificare uno dei valori seguenti.




| valore | Significato | 
|-------|---------|
| <dl><dt>1</dt></dl> | Contatore delle prestazioni delle query (QPC). Il contatore QPC fornisce un timestamp ad alta risoluzione che non è interessato dalle modifiche all'orologio di sistema. Il timestamp archiviato nell'evento è equivalente al valore restituito dall'API QueryPerformanceCounter. Per altre informazioni sulle caratteristiche di questo timestamp, vedere Acquisizione di timestamp ad <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">alta risoluzione.</a><br /> È consigliabile usare questa risoluzione se si hanno frequenze di eventi elevate o se il consumer unisce eventi da buffer diversi. In questi casi, la precisione e la stabilità del timestamp QPC consentono una migliore accuratezza nell'ordinamento degli eventi da buffer diversi. Tuttavia, il timestamp QPC non rifletterà gli aggiornamenti all'orologio di sistema, ad esempio se l'orologio di sistema viene regolato in avanti a causa della sincronizzazione con un server NTP mentre la traccia è in corso, i timestamp QPC nella traccia continueranno a riflettere l'ora come se non fosse stato fatto alcun aggiornamento.<br /> Per determinare la risoluzione, usare il <strong>membro PerfFreq</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> quando si utilizza l'evento.<br /> Per convertire il timestamp di un evento in unità da 100 ns, usare la formula di conversione seguente: <br /> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart * 10000000.0 / logfileHeader.PerfFreq.QuadPart<br /> Si noti che nei computer meno recenti il timestamp potrebbe non essere accurato perché a volte il contatore viene ignorato a causa di errori hardware.<br /> | 
| <dl><dt>2</dt></dl> | Ora di sistema. L'ora di sistema fornisce un timestamp che tiene traccia delle modifiche apportate all'orologio del sistema, ad esempio se l'orologio di sistema viene regolato in avanti a causa della sincronizzazione con un server NTP mentre la traccia è in corso, anche i timestamp di sistema nella traccia salteranno in avanti per corrispondere alla nuova impostazione dell'orologio di sistema. <br /><ul><li>Nei sistemi precedenti Windows 10, il timestamp archiviato nell'evento è equivalente al valore restituito dall'API GetSystemTimeAsFileTime.</li><li>In Windows 10 versione successiva, il timestamp archiviato nell'evento è equivalente al valore restituito dall'API GetSystemTimePreciseAsFileTime.</li></ul>Prima di Windows 10, la risoluzione di questo timestamp era la risoluzione di un tick del clock di sistema, come indicato dal membro TimerResolution di TRACE_LOGFILE_HEADER. A partire Windows 10, la risoluzione di questo timestamp è la risoluzione del contatore delle prestazioni, come indicato dal membro PerfFreq di TRACE_LOGFILE_HEADER.<br /> Per convertire il timestamp di un evento in unità da 100 ns, usare la formula di conversione seguente: <br /> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart<br /> Si noti che quando gli eventi vengono acquisiti in un sistema che esegue un sistema operativo prima di Windows 10, se il volume di eventi è elevato, la risoluzione dell'ora di sistema potrebbe non essere sufficiente per determinare la sequenza di eventi. In questo caso, un set di eventi avrà lo stesso timestamp, ma l'ordine in cui ETW recapita gli eventi potrebbe non essere corretto. A partire da Windows 10, il timestamp viene acquisito con una precisione aggiuntiva, anche se potrebbe verificarsi una certa instabilità nei casi in cui l'orologio di sistema è stato regolato durante l'acquisizione della traccia.<br /> | 
| <dl><dt>3</dt></dl> | Contatore ciclo CPU. Il contatore CPU fornisce il timestamp di risoluzione più elevato ed è il meno elevato di risorse da recuperare. Tuttavia, il contatore della CPU non è affidabile e non deve essere usato nell'ambiente di produzione. Ad esempio, in alcuni computer, i timer cambieranno frequenza a causa di variazioni termiche e di alimentazione, oltre all'arresto in alcuni stati.<br /> Per determinare la risoluzione, usare il <strong>membro CpuSpeedInMHz</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>di TRACE_LOGFILE_HEADER</strong></a> quando si utilizza l'evento.<br /> Se l'hardware non supporta questo tipo di clock, ETW usa l'ora di sistema.<br /><strong>Windows Server 2003, Windows XP con SP1 e Windows XP:</strong> Questo valore non è supportato, è stato introdotto in Windows Server 2003 con SP1 e Windows XP con SP2.<br /> | 




 

**Windows 2000:** Il **membro ClientContext** non è supportato.

</dd> <dt>

**Flag**
</dt> <dd>

Deve contenere **WNODE \_ FLAG \_ TRACED \_ GUID** per indicare che la struttura contiene informazioni di traccia eventi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Assicurarsi di inizializzare la memoria per questa struttura su zero prima di impostare i membri.

Per convertire un timestamp ETW in fileTIME, usare la procedura seguente:

<dl> 1. Per ogni sessione o file di log in fase di elaborazione, ad esempio per ogni EVENT TRACE LOGFILE, controllare il campo \_ \_ logFile.ProcessTraceMode per determinare se il flag PROCESS TRACE MODE RAW TIMESTAMP è \_ \_ \_ \_ impostato. Per impostazione predefinita, questo flag non è impostato. Se questo flag non è impostato, il runtime ETW convertirà automaticamente il timestamp di ogni RECORD DI EVENTO in UN FILETIME prima di inviare il RECORD DI EVENTO alla funzione \_ EventRecordCallback, quindi non è necessaria alcuna elaborazione \_ aggiuntiva. I passaggi seguenti devono essere utilizzati solo se la traccia viene elaborata con il flag RAW TIMESTAMP DI PROCESS \_ TRACE \_ MODE \_ \_ impostato.  
2. Per ogni sessione o file di log in fase di elaborazione, ad esempio per ogni EVENT TRACE LOGFILE, controllare il campo \_ logFile.LogfileHeader.ReservedFlags per determinare la scala del timestamp per il \_ file di log. In base al valore di ReservedFlags, seguire uno di questi passaggi per determinare il valore da usare per timeStampScale nei passaggi rimanenti: <dl> a. If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;  
b. If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;  
Si noti che i passaggi rimanenti non sono necessari per gli eventi che usano l'ora di sistema, poiché gli eventi forniscono già i timestamp in unità FILETIME. I passaggi rimanenti funzioneranno ma non saranno necessari e introdurranno un piccolo errore di arrotondamento.  
c. If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                   |
| Server minimo supportato<br/> | Windows 2000 Server desktop apps UWP apps (App desktop UWP di Windows 2000 \[ \| Server)\]<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Wmistr.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[*Metodo ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**PROPRIETÀ \_ DI TRACCIA \_ EVENTI**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**LARGE \_ INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
