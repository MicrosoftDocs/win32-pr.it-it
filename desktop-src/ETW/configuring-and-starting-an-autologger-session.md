---
description: La sessione di traccia eventi di autologger registra gli eventi che si verificano all'inizio del processo di avvio del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurazione e avvio di una sessione di autologger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980954"
---
# <a name="configuring-and-starting-an-autologger-session"></a>Configurazione e avvio di una sessione di autologger

La sessione di traccia eventi di autologger registra gli eventi che si verificano all'inizio del processo di avvio del sistema operativo. Le applicazioni e i driver di dispositivo possono usare la sessione autologger per acquisire tracce prima che l'utente effettui l'accesso. Si noti che alcuni driver di dispositivo, ad esempio i driver dei dispositivi disco, non vengono caricati al momento dell'avvio della sessione autologger.

Il logger automatico differisce dal logger globale nei modi seguenti:

-   È possibile specificare una o più sessioni di autologger (il logger globale è una singola sessione a cui sono stati registrati tutti gli eventi).
-   Autologger invia una notifica di abilitazione ai provider all'avvio della sessione (il logger globale non ha inviato una notifica di abilitazione ai provider, quindi i provider devono basarsi su altri modi per verificare se la sessione del logger globale è stata avviata per iniziare la registrazione degli eventi).
-   Autologger non supporta la registrazione degli eventi del logger di kernel NT (vedere il membro **EnableFlags** delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Per registrare gli eventi del logger del kernel NT, è necessario usare il [logger globale](configuring-and-starting-the-global-logger-session.md).

Per ulteriori informazioni sulla visualizzazione del logger globale, vedere la pagina relativa alla [configurazione e all'avvio della sessione Global Logger](configuring-and-starting-the-global-logger-session.md).

> [!Note]  
> ETW supporta autologger in Windows Vista e versioni successive. Usare il [logger globale](configuring-and-starting-the-global-logger-session.md) nei sistemi operativi precedenti.

 

Usare il registro di sistema per configurare la sessione di autologger. Aggiungere la seguente chiave del registro di sistema, se non è già presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

Sotto la chiave **autologger** creare una chiave per ogni sessione di autologger che si desidera configurare, come illustrato nell'esempio seguente.

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

Per ogni sessione, creare una chiave per ogni provider che si desidera abilitare per la sessione. Utilizzare il GUID del provider come chiave.

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

La tabella seguente descrive i valori che è possibile definire per ogni sessione di autologger. Per specificare questi valori del registro di sistema, è necessario disporre dei privilegi di amministratore. Il valore **iniziale** e **GUID** sono gli unici valori necessari per avviare la sessione di autologger. tutti gli altri valori hanno impostazioni predefinite che vengono usate se il valore non è presente nel registro di sistema. In genere, è consigliabile usare i valori predefiniti. Se si specifica un valore che ETW non supporta, ETW eseguirà l'override del valore.



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
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Timer da usare per registrare il timestamp per ogni evento.
<ul>
<li>1 = valore del contatore delle prestazioni (alta risoluzione)</li>
<li>2 = timer di sistema</li>
<li>3 = contatore cicli CPU</li>
</ul>
Per una descrizione di ogni tipo di orologio, vedere il membro <strong>ClientContext</strong> di <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> Il valore predefinito è 1 (valore del contatore delle prestazioni) in Windows Vista e versioni successive. Prima di Windows Vista, il valore predefinito è 2 (timer di sistema).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Per disabilitare la persistenza in tempo reale, impostare questo valore su 1. Il valore predefinito è 0 (abilitato) per le sessioni in tempo reale.<br/> Se è abilitata la persistenza in tempo reale, gli eventi in tempo reale che non sono stati recapitati nel momento in cui il computer è stato arrestato verranno resi persistenti. Gli eventi verranno quindi recapitati al consumer alla successiva connessione del consumer alla sessione. <br/></td>
</tr>
<tr class="even">
<td><strong>Filecounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Non impostare o modificare questo valore. Questo valore è il numero di serie usato per incrementare il nome del file di log se è specificato <strong>FileMax</strong> . Se il valore non è valido, verrà utilizzato 1.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Percorso completo del file di log. Il percorso di questo file deve esistere. Il file di log è un file di log sequenziale. Il percorso è limitato a 1024 caratteri.<br/> Se <strong>filename</strong> non è specificato, gli eventi vengono scritti in%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . etl. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero massimo di istanze del file di log creato da ETW. Se il file di log specificato in <strong>filename</strong> esiste, ETW aggiunge il valore <strong>filecounter</strong> al nome del file. Se, ad esempio, viene utilizzato il nome del file di log predefinito, il form è%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . etl. NNNN. <br/> La prima volta che il computer viene avviato, il nome del file è <sessionname> . etl. 0001, la seconda volta il nome del file è <sessionname> . etl. 0002 e così via. Se <strong>FileMax</strong> è 3, al quarto riavvio del computer, ETW Reimposta il contatore su 1 e sovrascrive <sessionname> . etl. 0001, se esistente.<br/> Il numero massimo di istanze del file di log supportato è 16.<br/> Non usare questa funzionalità con la modalità file di registro <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Con quale frequenza, in secondi, i buffer di traccia vengono scaricati forzatamente. Il tempo di svuotamento minimo è 1 secondo. Questo svuotamento forzato è in aggiunta allo scaricamento automatico che si verifica quando un buffer è pieno e quando la sessione di traccia viene arrestata. <br/> Per il caso di un logger in tempo reale, un valore pari a zero (valore predefinito) indica che il tempo di scaricamento verrà impostato su 1 secondo. Un logger in tempo reale è quando <strong>LogFileMode</strong> è impostato su <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> Il valore predefinito è 0. Per impostazione predefinita, i buffer vengono scaricati solo quando sono pieni. <br/></td>
</tr>
<tr class="even">
<td><strong>GUID</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Stringa contenente un GUID che identifica in modo univoco la sessione. Questo valore è obbligatorio.</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Specificare una o più modalità di registrazione. Per i valori possibili, vedere <a href="logging-mode-constants.md">costanti della modalità di registrazione</a>. Il valore predefinito è <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. Invece di scrivere in un file di log, è possibile specificare <strong>EVENT_TRACE_BUFFERING_MODE</strong> o <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> Specificando <strong>EVENT_TRACE_BUFFERING_MODE</strong> si evita il costo di scaricamento del contenuto della sessione su disco quando il file System diventa disponibile. <br/> Si noti che se si usa <strong>EVENT_TRACE_BUFFERING_MODE</strong> il sistema ignorerà il valore <strong>MaximumBuffers</strong> , perché la dimensione del buffer è invece il prodotto di <strong>MinimumBuffers</strong> e <strong>bufferSize</strong>.<br/> Le sessioni autologger non supportano la modalità di registrazione <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .<br/> Se <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> viene specificato, <strong>bufferSize</strong> deve essere specificato in modo esplicito e deve essere lo stesso sia nel logger che nel file da accodare.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Dimensioni massime del file di log, in megabyte. La sessione viene chiusa quando viene raggiunta la dimensione massima, a meno che non ci si trovi in modalità file di registro circolare. Per specificare nessun limite, impostare il valore su 0. Il valore predefinito è 100 MB, se non è impostato. Il comportamento che si verifica quando viene raggiunta la dimensione massima del file dipende dal valore di <strong>LogFileMode</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero massimo di buffer da allocare. In genere, questo valore è il numero minimo di buffer più venti. ETW usa le dimensioni del buffer e le dimensioni della memoria fisica per calcolare questo valore. Questo valore deve essere maggiore o uguale al valore di <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Numero minimo di buffer da allocare all'avvio. Il numero minimo di buffer che è possibile specificare è costituito da due buffer per processore. Ad esempio, in un computer a processore singolo, il numero minimo di buffer è due.<br/></td>
</tr>
<tr class="odd">
<td><strong>Inizia</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Per fare in modo che la sessione autologger venga avviata al successivo riavvio del computer, impostare questo valore su 1; in caso contrario, impostare questo valore su 0.<br/></td>
</tr>
<tr class="even">
<td><strong>Status</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Stato di avvio di autologger. Se non è stato possibile avviare autologger, il valore di questa chiave è il codice di errore Win32 appropriato. Se il logger automatico è stato avviato correttamente, il valore di questa chiave è <strong>ERROR_SUCCESS</strong> (0).<br/></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono descritti i valori che è possibile definire per ogni provider che si desidera abilitare per la sessione. Per specificare questi valori del registro di sistema, è necessario disporre dei privilegi di amministratore. Se si specifica un valore che ETW non supporta, ETW eseguirà l'override del valore.



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
<td>Valore definito dal provider che specifica la classe degli eventi per i quali il provider genera eventi. Per informazioni dettagliate, vedere il parametro <em>EnableFlags</em> della funzione <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> . Specificare il nome del valore se il provider non supporta <strong>MatchAnyKeyword</strong> o <strong>MatchAllKeyword</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valore definito dal provider che specifica il livello di dettaglio incluso nell'evento. Ad esempio, è possibile usare questo valore per indicare il livello di gravità degli eventi (informativi, di avviso, di errore) generati dal provider. Per un elenco di livelli predefiniti, vedere il parametro <em>Level</em> della funzione <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Utilizzare questo valore per includere uno o più degli elementi seguenti nel file di log:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = include nei dati estesi l'ID di sicurezza (SID) dell'utente.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = include nei dati estesi l'identificatore della sessione terminale.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = include nei dati estesi una traccia dello stack di chiamate per gli eventi scritti usando <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra tutti gli eventi per i quali non è specificata una parola chiave diversa da zero.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica che la chiamata a <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> deve abilitare un <a href="provider-traits.md">gruppo di provider</a> anziché un singolo provider di eventi.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = include la chiave di inizio del processo nei dati estesi.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = include la chiave evento nei dati estesi.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = esclude tutti gli eventi contrassegnati come un evento InPrivate o provengono da un processo contrassegnato come InPrivate.</li>
</ul>
Per ulteriori informazioni su questi elementi, vedere <strong>EnableProperty</strong> della struttura <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Maschera di maschera delle parole chiave che determinano la categoria di eventi che si desidera vengano scritti dal provider. Il provider scrive l'evento se uno dei bit della parola chiave dell'evento corrisponde a uno qualsiasi dei bit impostati in questa maschera. Per specificare che il provider scrive tutti gli eventi, impostare questo valore su zero. Per un esempio, vedere la sezione Osservazioni della funzione <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Questa maschera di maschera è facoltativa. Questa maschera limita ulteriormente la categoria di eventi che si desidera vengano scritti dal provider. Se la parola chiave dell'evento soddisfa la condizione <em>MatchAnyKeyword</em> , il provider scriverà l'evento solo se tutti i bit in questa maschera sono presenti nella parola chiave dell'evento. Questa maschera non viene utilizzata se <em>MatchAnyKeyword</em> è zero. Per un esempio, vedere la sezione Osservazioni della funzione <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
</tbody>
</table>



 

Dopo che il registro di sistema è stato modificato, la sessione autologger viene avviata al successivo riavvio del computer. La sessione autologger chiama la funzione [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) per abilitare i provider.

Le sessioni autologger aumentano l'ora di avvio del sistema e devono essere usate con moderazione. Per i servizi che vogliono acquisire informazioni durante il processo di avvio è consigliabile aggiungere la logica del controller a se stessa, anziché usare la sessione autologger.

Per arrestare una sessione di autologger, chiamare la funzione [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) . Il nome della sessione passato alla funzione è il nome della chiave del registro di sistema utilizzata per definire la sessione nel registro di sistema.

In Windows 8.1, Windows Server 2012 R2 e versioni successive, il payload dell'evento, l'ambito e i filtri di percorso stack possono essere utilizzati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**enable \_ trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descrittore filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione logger. Per ulteriori informazioni sui filtri di payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **enable \_ trace \_ Parameters**, **Event \_ Filter \_ descrittor** e [**payload \_ Filter \_ predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger privata, vedere [configurazione e avvio di una sessione di logger privati](configuring-and-starting-a-private-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione del logger di kernel NT, vedere [configurazione e avvio della sessione del logger di kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione di logger privata](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Abilita \_ parametri di traccia \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_descrittore filtro eventi \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_predicato filtro payload \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>
