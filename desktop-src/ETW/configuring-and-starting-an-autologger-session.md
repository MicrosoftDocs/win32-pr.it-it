---
description: La sessione di traccia eventi autologger registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurazione e avvio di una sessione di autologger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102040"
---
# <a name="configuring-and-starting-an-autologger-session"></a>Configurazione e avvio di una sessione di autologger

La sessione di traccia eventi autologger registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo. Le applicazioni e i driver di dispositivo possono usare la sessione AutoLogger per acquisire le tracce prima che l'utente esezioni l'accesso. Si noti che alcuni driver di dispositivo, ad esempio i driver di dispositivo del disco, non vengono caricati all'inizio della sessione di AutoLogger.

AutoLogger differisce dal logger globale nei modi seguenti:

-   È possibile specificare una o più sessioni autologger (il logger globale è una singola sessione in cui tutti gli utenti hanno registrato gli eventi).
-   AutoLogger invia una notifica di abilitazione ai provider all'avvio della sessione (il logger globale non ha inviato una notifica di abilitazione ai provider, quindi i provider dovevano basarsi su altri mezzi per sapere se la sessione del logger globale è stata avviata per iniziare a registrare gli eventi).
-   AutoLogger non supporta la registrazione degli eventi del logger del kernel NT (vedere il **membro EnableFlags** di [**EVENT TRACE \_ \_ PROPERTIES).**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Per registrare gli eventi del logger del kernel NT, è necessario usare [il logger globale](configuring-and-starting-the-global-logger-session.md).

Per altre informazioni sulla seesion del logger globale, vedere [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).

> [!Note]  
> ETW supporta autologger in Windows Vista e versioni successive. Usare il [logger globale](configuring-and-starting-the-global-logger-session.md) nei sistemi operativi precedenti.

 

Usare il Registro di sistema per configurare la sessione autologger. Aggiungere la chiave del Registro di sistema seguente, se non è già presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

Nella chiave **Autologger** creare una chiave per ogni sessione di AutoLogger che si vuole configurare, come illustrato nell'esempio seguente.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

Per ogni sessione, creare una chiave per ogni provider che si desidera abilitare per la sessione. Usare il GUID del provider come chiave.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

Nella tabella seguente vengono descritti i valori che è possibile definire per ogni sessione di AutoLogger. Per specificare questi valori del Registro di sistema, è necessario disporre dei privilegi di amministratore. I **valori Start** e **Guid** sono gli unici valori necessari per avviare la sessione di AutoLogger. Tutti gli altri valori hanno impostazioni predefinite che vengono usate se il valore non è presente nel Registro di sistema. In genere, è consigliabile usare i valori predefiniti. Se si specifica un valore che ETW non può supportare, ETW eseguirà l'override del valore.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Dimensioni di ogni buffer, in kilobyte. Deve essere minore di un megabyte. ETW usa le dimensioni della memoria fisica per calcolare questo valore.<br/></td>
</tr>
<tr class="even">
<td><strong>Tipo di orologio</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Timer da usare per la registrazione del timestamp per ogni evento.
<ul>
<li>1 = Valore del contatore delle prestazioni (risoluzione elevata)</li>
<li>2 = Timer di sistema</li>
<li>3 = Contatore ciclo CPU</li>
</ul>
Per una descrizione di ogni tipo di orologio, vedere il <strong>membro ClientContext</strong> <a href="wnode-header.md"><strong>di WNODE_HEADER</strong></a>.<br/> Il valore predefinito è 1 (valore del contatore delle prestazioni) in Windows Vista e versioni successive. Prima di Windows Vista, il valore predefinito è 2 (timer di sistema).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Per disabilitare la persistenza in tempo reale, impostare questo valore su 1. Il valore predefinito è 0 (abilitato) per le sessioni in tempo reale.<br/> Se è abilitata la persistenza in tempo reale, gli eventi in tempo reale che non sono stati recapitati al momento dell'arresto del computer verranno resi persistenti. Gli eventi verranno quindi recapitati al consumer alla successiva connessione del consumer alla sessione. <br/></td>
</tr>
<tr class="even">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Non impostare o modificare questo valore. Questo valore è il numero di serie usato per incrementare il nome del file di log se <strong>è specificato FileMax.</strong> Se il valore non è valido, verrà utilizzato 1.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Percorso completo del file di log. Il percorso di questo file deve esistere. Il file di log è un file di log sequenziale. Il percorso è limitato a 1024 caratteri.<br/> Se <strong>FileName</strong> non viene specificato, gli eventi vengono scritti in %SystemRoot%\System32\LogFiles\WMI \& lt;sessionname &gt; .etl. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero massimo di istanze del file di log create da ETW. Se il file di log specificato in <strong>FileName</strong> esiste, ETW aggiunge il <strong>valore FileCounter</strong> al nome del file. Ad esempio, se si usa il nome del file di log predefinito, il formato sarà %SystemRoot%\System32\LogFiles\WMI \& lt;nome sessione &gt; .etl. Nnnn. <br/> La prima volta che il computer viene avviato, il nome del file è sessionname .etl.0001, la seconda volta il nome del file è &lt; &gt; &lt; sessionname &gt; .etl.0002 e così via. Se <strong>FileMax</strong> è 3, al quarto riavvio del computer ETW reimposta il contatore su 1 e sovrascrive il nome sessione &lt; &gt; .etl.0001, se esistente.<br/> Il numero massimo di istanze del file di log supportate è 16.<br/> Non utilizzare questa funzionalità con la modalità <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> file di log.<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Frequenza, in secondi, con cui i buffer di traccia vengono scaricati forzatamente. Il tempo di scaricamento minimo è di 1 secondo. Questo scaricamento forzato si aggiunge allo scaricamento automatico che si verifica quando un buffer è pieno e quando la sessione di traccia si arresta. <br/> Nel caso di un logger in tempo reale, un valore pari a zero (valore predefinito) indica che l'ora di scaricamento verrà impostata su 1 secondo. Un logger in tempo reale è quando <strong>LogFileMode è</strong> impostato <strong>su EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> Il valore predefinito è 0. Per impostazione predefinita, i buffer vengono scaricati solo quando sono pieni. <br/></td>
</tr>
<tr class="even">
<td><strong>Guid</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Stringa contenente un GUID che identifica in modo univoco la sessione. Questo valore è obbligatorio.</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Specificare una o più modalità di log. Per i valori possibili, vedere <a href="logging-mode-constants.md">Costanti della modalità di registrazione.</a> Il valore predefinito <strong>è EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. Anziché scrivere in un file di log, è possibile specificare EVENT_TRACE_BUFFERING_MODE <strong>o</strong> <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> Specificando <strong>EVENT_TRACE_BUFFERING_MODE</strong> si evita il costo dello scaricamento del contenuto della sessione su disco quando il file system diventa disponibile. <br/> Si noti che <strong>EVENT_TRACE_BUFFERING_MODE</strong> il sistema ignorerà il valore <strong>MaximumBuffers,</strong> perché le dimensioni del buffer sono invece il prodotto di <strong>MinimumBuffers</strong> e <strong>BufferSize.</strong><br/> Le sessioni autologger non supportano la <strong>modalità EVENT_TRACE_FILE_MODE_NEWFILE</strong> registrazione automatica.<br/> Se <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> specificato, <strong>BufferSize</strong> deve essere specificato in modo esplicito e deve essere lo stesso sia nel logger che nel file da aggiungere.<br/></td>
</tr>
<tr class="even">
<td><strong>Maxfilesize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Dimensioni massime del file di log, in megabyte. La sessione viene chiusa quando viene raggiunta la dimensione massima, a meno che non si sia in modalità file di log circolare. Per non specificare alcun limite, impostare il valore su 0. Il valore predefinito è 100 MB, se non impostato. Il comportamento che si verifica quando viene raggiunta la dimensione massima del file dipende dal valore di <strong>LogFileMode</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero massimo di buffer da allocare. In genere, questo valore è il numero minimo di buffer più venti. ETW usa le dimensioni del buffer e la dimensione della memoria fisica per calcolare questo valore. Questo valore deve essere maggiore o uguale al valore per <strong>MinimumBuffers.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero minimo di buffer da allocare all'avvio. Il numero minimo di buffer che è possibile specificare è due buffer per processore. In un computer a processore singolo, ad esempio, il numero minimo di buffer è due.<br/></td>
</tr>
<tr class="odd">
<td><strong>Inizia</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Per fare in modo che la sessione autologger venga avviata al successivo riavvio del computer, impostare questo valore su 1. In caso contrario, impostare questo valore su 0.<br/></td>
</tr>
<tr class="even">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Stato di avvio di AutoLogger. Se l'avvio di AutoLogger non è riuscito, il valore di questa chiave è il codice di errore Win32 appropriato. Se AutoLogger è stato avviato correttamente, <strong></strong> il valore di questa chiave ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono descritti i valori che è possibile definire per ogni provider che si desidera abilitare per la sessione. Per specificare questi valori del Registro di sistema, è necessario disporre dei privilegi di amministratore. Se si specifica un valore che ETW non può supportare, ETW eseguirà l'override del valore.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Enabled</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Determina se il provider è abilitato. Per abilitare il provider, impostare questo valore su 1. Per disabilitare il provider, impostare questo valore su 0. Il valore predefinito è 0.</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valore definito dal provider che specifica la classe di eventi per cui il provider genera eventi. Per informazioni dettagliate, <em>vedere il parametro EnableFlags</em> della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>funzione EnableTrace.</strong></a> Specificare questo nome di valore se il provider non supporta <strong>MatchAnyKeyword</strong> <strong>o MatchAllKeyword</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valore definito dal provider che specifica il livello di dettaglio incluso nell'evento. Ad esempio, è possibile utilizzare questo valore per indicare il livello di gravità degli eventi (informativo, di avviso, di errore) generati dal provider. Per un elenco dei livelli predefiniti, vedere il <em>parametro level</em> della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>funzione EnableTraceEx.</strong></a></td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Usare questo valore per includere uno o più degli elementi seguenti nel file di log:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Includere nei dati estesi l'ID di sicurezza (SID) dell'utente.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include nei dati estesi l'identificatore di sessione del terminale.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include nei dati estesi un'analisi dello stack di chiamate per gli eventi scritti usando <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite.</strong></a></li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filtra tutti gli eventi per cui non è specificata una parola chiave diverso da zero.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica che questa chiamata <a href="provider-traits.md">a</a> <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> deve abilitare un gruppo di provider anziché un singolo provider di eventi.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Includere la chiave di avvio del processo nei dati estesi.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Includere la chiave evento nei dati estesi.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filtra tutti gli eventi contrassegnati come evento InPrivate o provenienti da un processo contrassegnato come InPrivate.</li>
</ul>
Per altre informazioni su questi elementi, vedere <strong>EnableProperty</strong> della <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> struttura .<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Maschera di bit di parole chiave che determinano la categoria di eventi che il provider deve scrivere. Il provider scrive l'evento se uno dei bit della parola chiave dell'evento corrisponde a uno dei bit impostati in questa maschera. Per specificare che il provider deve scrivere tutti gli eventi, impostare questo valore su zero. Per un esempio, vedere la sezione Osservazioni della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>funzione EnableTraceEx.</strong></a></td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Questa maschera di bit è facoltativa. Questa maschera limita ulteriormente la categoria di eventi che il provider deve scrivere. Se la parola chiave dell'evento soddisfa la condizione <em>MatchAnyKeyword,</em> il provider scriverà l'evento solo se tutti i bit in questa maschera sono presenti nella parola chiave dell'evento. Questa maschera non viene usata se <em>MatchAnyKeyword</em> è zero. Per un esempio, vedere la sezione Osservazioni della <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>funzione EnableTraceEx.</strong></a></td>
</tr>
</tbody>
</table>



 

Dopo la modifica del Registro di sistema, la sessione autologger viene avviata al successivo riavvio del computer. La sessione AutoLogger chiama la [**funzione EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) per abilitare i provider.

Le sessioni autologger aumentano il tempo di avvio del sistema e devono essere usate con moderamento. I servizi che vogliono acquisire informazioni durante il processo di avvio devono prendere in considerazione l'aggiunta della logica del controller a se stessa anziché usare la sessione autologger.

Per arrestare una sessione di AutoLogger, chiamare la [**funzione ControlTrace.**](/windows/win32/api/evntrace/nf-evntrace-controltracea) Il nome della sessione passato alla funzione è il nome della chiave del Registro di sistema usata per definire la sessione nel Registro di sistema.

In Windows 8.1, Windows Server 2012 R2 e versioni successive, il payload dell'evento, l'ambito e i filtri di percorso dello stack possono essere usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger. Per altre informazioni sui filtri di payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** e [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [Configurazione e avvio di una sessione di traccia eventi.](configuring-and-starting-an-event-tracing-session.md)

Per informazioni dettagliate sull'avvio di una sessione di logger privata, vedere [Configurazione e avvio di una sessione privata del logger.](configuring-and-starting-a-private-logger-session.md)

Per informazioni dettagliate sull'avvio di una sessione di logger del kernel NT, vedere [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione privata del logger](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**ABILITARE \_ I PARAMETRI DI \_ TRACCIA**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**DESCRITTORE \_ DEL \_ FILTRO EVENTI**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PREDICATO \_ DEL \_ FILTRO DI PAYLOAD**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>
