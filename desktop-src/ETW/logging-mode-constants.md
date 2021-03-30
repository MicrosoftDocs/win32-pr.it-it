---
description: Le costanti seguenti rappresentano le possibili modalità di registrazione per una sessione di traccia eventi.
ms.assetid: d12aaecb-776a-4476-9ba4-16af30fde9c2
title: Costanti della modalità di registrazione
ms.topic: article
ms.date: 06/03/2020
ms.openlocfilehash: daa0233346718040653edbc75a10615f9fd31765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977826"
---
# <a name="logging-mode-constants"></a>Costanti della modalità di registrazione

Le costanti seguenti rappresentano le possibili modalità di registrazione per una sessione di traccia eventi.

Le costanti vengono usate nei membri **LogFileMode** del file di [**\_ \_ log di traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea), delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) e delle strutture di [**\_ \_ intestazione del file di log di traccia**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header) . Queste costanti sono definite nel file di intestazione *Evntrace. h* .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NONE</strong> (0x00000000)</td>
<td>Uguale a <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> senza dimensioni massime del file specificato.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> (0x00000001)</td>
<td>Scrive gli eventi in un file di log in sequenza; si interrompe quando il file raggiunge le dimensioni massime. Non usare con <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> o <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> (0x00000002)</td>
<td>Scrive gli eventi in un file di log. Quando il file raggiunge le dimensioni massime, gli eventi meno recenti vengono sostituiti con gli eventi in ingresso. Si noti che il contenuto del file di log circolare potrebbe non essere più ordinato nei computer multiprocessore.<br/> Non usare con <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>o <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_APPEND</strong> (0x00000004)</td>
<td>Accoda gli eventi a un file di log sequenziale esistente. Se il file non esiste, viene creato. Usare solo se si specifica l' <a href="wnode-header.md"><strong>ora di sistema</strong></a> per la risoluzione dell'orologio; in caso contrario, <a href="/windows/win32/api/evntrace/nf-evntrace-processtrace"><strong>ProcessTrace</strong></a> restituirà gli eventi con timestamp non corretti. Quando si utilizza <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, i valori per <strong>bufferSize</strong>, <strong>NumberOfProcessors</strong>e <strong>ClockType</strong> devono essere specificati in modo esplicito e devono essere identici sia nel logger che nel file da accodare.<br/> Non usare con <strong>EVENT_TRACE_REAL_TIME_MODE</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>o <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>.<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> (0x00000008)</td>
<td>Passa automaticamente a un nuovo file di log quando il file raggiunge le dimensioni massime. È necessario impostare il membro <strong>maximumFileSize</strong> del <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a> . Il nome file specificato deve essere una stringa formattata, ad esempio la stringa contiene% d, ad esempio c:\test%d.etl. Ogni volta che viene creato un nuovo file, viene incrementato un contatore e viene utilizzato il relativo valore, viene aggiornata la stringa formattata e la stringa risultante viene utilizzata come nome file.<br/> Questa opzione non è consentita per le sessioni di traccia eventi privati e non deve essere usata per le sessioni del logger di kernel NT.<br/> Non usare con <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> o <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_PREALLOCATE</strong>(0x00000020)</td>
<td>Riserva <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a> di byte di spazio su disco per il file di log in anticipo. Il file occupa l'intero spazio durante la registrazione, sia per i file di log circolari che per quelli sequenziali. Quando si arresta la sessione, il file di log viene ridotto alle dimensioni necessarie. È necessario impostare <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a>.<br/> Non è possibile usare la modalità per le sessioni di traccia eventi privati.<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NONSTOPPABLE_MODE</strong>(0x00000040)</td>
<td>Impossibile arrestare la sessione di registrazione. Questa modalità è supportata solo da autologger. questa opzione è supportata in Windows Vista e versioni successive.<br/>.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_SECURE_MODE</strong> (0X00000080)</td>
<td>Limita gli utenti che possono registrare gli eventi della sessione a quelli con autorizzazione <a href="/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol"><strong>TRACELOG_LOG_EVENT</strong></a> . Questa opzione è supportata in Windows Vista e versioni successive.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_REAL_TIME_MODE</strong> (0x00000100)</td>
<td>Recapita gli eventi agli utenti in tempo reale. Gli eventi vengono recapitati quando i buffer vengono scaricati, non nel momento in cui il provider scrive l'evento. Non è consigliabile abilitare la modalità in tempo reale se non sono presenti consumer per l'utilizzo degli eventi, in quanto le chiamate agli eventi di log avranno esito negativo quando i buffer diventano pieni. Prima di Windows Vista, se gli eventi non venivano utilizzati, gli eventi venivano eliminati. Non specificare più di un consumer in tempo reale in un processo in Windows XP Windows Server 2003. Al contrario, un thread utilizza gli eventi e distribuisce gli eventi ad altri utenti.<br/> <strong>Prima di Windows Vista:</strong> Non usare la modalità in tempo reale perché la frequenza degli eventi supportata è molto inferiore alla lettura dal file di log (gli eventi possono essere eliminati). Inoltre, l'ordine degli eventi non è garantito nei computer con più processori. La modalità in tempo reale è più adatta per gli eventi di tipo di notifica con traffico ridotto.<br/> <br/> È possibile combinare questa modalità con altre modalità file di registro; Tuttavia, non usare questa modalità con EVENT_TRACE_PRIVATE_LOGGER_MODE. Si noti che se si combina questa modalità con altre modalità file di log, i buffer verranno scaricati una volta al secondo, con conseguente scrittura di buffer riempiti parzialmente nel file di log. Se ad esempio si usano buffer 64K e la frequenza di registrazione è di 1 evento ogni secondo, il servizio scriverà 64K al secondo nel file di log.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_DELAY_OPEN_FILE_MODE</strong>(0x00000200)</td>
<td>Questa modalità viene utilizzata per ritardare l'apertura del file di log fino a quando non si verifica un evento. <br/>
<blockquote>
<strong>Nota:</strong><br />
In Windows Vista o versioni successive questa modalità non è applicabile.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_BUFFERING_MODE</strong> (0x00000400)</td>
<td>Questa modalità scrive gli eventi in un buffer di memoria circolare. Gli eventi scritti oltre la dimensione totale del buffer eliminano gli eventi meno recenti ancora rimanenti nel buffer. La dimensione del buffer di memoria è il prodotto di <strong>MinimumBuffers</strong> e <strong>BufferSize</strong> (vedere <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>). Come conseguenza di questa formula, qualsiasi buffer che usa <strong>EVENT_TRACE_BUFFERING_MODE</strong> ignorerà il valore <strong>MaximumBuffers</strong> .<br/> Gli eventi non vengono scritti in un file di log o recapitati in tempo reale e ETW non Scarica i buffer. Per ottenere uno snapshot del buffer, chiamare la funzione <a href="/windows/win32/api/evntrace/nf-evntrace-flushtracea"><strong>FlushTrace</strong></a> .<br/> Questa modalità è particolarmente utile per il debug dei driver di dispositivo insieme alla possibilità di visualizzare il contenuto dei buffer in memoria con l'estensione del debugger del kernel <a href="/windows-hardware/drivers/devtest/trace-session">WMITrace</a> .<br/> Non usare con <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>o <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> (0x00000800)</td>
<td>Crea una sessione di traccia eventi in modalità utente che viene eseguita nello stesso processo del provider di traccia eventi. La memoria per i buffer deriva dalla memoria del processo. I processi che non richiedono dati dal kernel possono eliminare il sovraccarico associato alle transizioni in modalità kernel utilizzando una sessione di traccia eventi privata.<br/> Se il provider è registrato da più processi, ETW aggiunge l'identificatore del processo al nome del file di log per creare un nome di file di log univoco. Se, ad esempio, il controller specifica i nomi dei file di log come c:\mylogs\myprivatelog.ETL, ETW crea il file di log come c:\Mylogs\ myprivatelog.etl_nnnn, dove nnnn è l'identificatore del processo. L'identificatore di processo non viene aggiunto al primo processo che registra il provider, viene aggiunto solo ai processi successivi che registrano il provider.<br/> Le sessioni di traccia eventi privati presentano le limitazioni seguenti:<br/>
<ul>
<li>Una sessione privata può registrare gli eventi solo per i thread del processo in cui è in esecuzione.</li>
<li>È possibile eseguire fino a otto sessioni private per processo.</li>
<li>Le sessioni private non possono essere usate con il recapito in tempo reale.</li>
<li>Gli eventi generati da una sessione privata non includono il tempo di esecuzione per le istruzioni in modalità kernel rispetto a quelle della modalità utente o i dettagli a livello di thread del tempo di CPU usato.</li>
</ul>
I filtri di ID processo e i filtri dei nomi eseguibili possono ora essere passati alle API del controllo della sessione quando vengono avviati i logger privati a livello di sistema. Per ottenere risultati ottimali negli scenari tra processi, è necessario passare gli stessi filtri a ogni operazione di controllo durante la sessione, incluse le chiamate Enable/diasble del provider. Si noti che i filtri hanno lo stesso formato di quelli usati da <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a>. <br/> Questa modalità può essere usata in combinazione con la modalità <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> .<br/> <strong>Prima di Windows 10, versione 1703:</strong> Solo LocalSystem, l'amministratore e gli utenti del gruppo Administrator eseguiti in un processo con privilegi elevati possono creare una sessione privata. Se si include il flag di <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> , qualsiasi utente può creare una sessione privata in-process. Nelle versioni precedenti di Windows, inoltre, può essere presente una sola sessione privata per processo, a meno che non sia specificata anche la modalità di EVENT_TRACE_PRIVATE_IN_PROC, nel qual caso è possibile creare fino a tre sessioni private in-process. <br/> <strong>Prima di Windows Vista:</strong> Gli utenti del gruppo Performance Log Users possono anche creare una sessione privata.<br/> <br/> Non usare con EVENT_TRACE_REAL_TIME_MODE.<br/> <strong>Prima di Windows 7 e Windows Server 2008 R2:</strong> Non usare con EVENT_TRACE_FILE_MODE_NEWFILE.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_ADD_HEADER_MODE</strong>(0x00001000)</td>
<td>Questa opzione consente di aggiungere un'intestazione al file di log.<br/>
<blockquote>
<strong>Nota:</strong><br />
In Windows Vista o versioni successive questa modalità non è applicabile.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_KBYTES_FOR_SIZE</strong>(0x00002000)</td>
<td>Utilizzare kilobyte come unità di misura per specificare le dimensioni di un file. L'unità di misura predefinita è megabyte. Questa modalità si applica al valore del registro di sistema <strong>MaxFileSize</strong> per una sessione di <a href="configuring-and-starting-an-autologger-session.md">autologger</a> e al membro <strong>maximumFileSize</strong> del <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>. Questa opzione è supportata in Windows Vista e versioni successive.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong>(0x00004000)</td>
<td>Usa numeri di sequenza univoci tra le sessioni di traccia eventi. Questa modalità si applica solo agli eventi registrati tramite la funzione <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Per ulteriori informazioni, vedere <strong>TraceMessage</strong> per i dettagli di utilizzo.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> e <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> si escludono a vicenda.<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> (0x00008000)</td>
<td>Usa numeri di sequenza univoci solo per una singola sessione di traccia eventi. Questa modalità si applica solo agli eventi registrati tramite la funzione <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Per ulteriori informazioni, vedere <strong>TraceMessage</strong> per i dettagli di utilizzo.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> e <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> si escludono a vicenda.<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_RELOG_MODE</strong> (0x00010000)</td>
<td>Registra l'evento senza includere <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_header"><strong>EVENT_TRACE_HEADER</strong></a>.
<blockquote>
<strong>Nota:</strong><br />
Questa modalità non deve essere utilizzata. È riservata per uso interno.
</blockquote>
<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> (0x00020000)</td>
<td>Usare insieme alla modalità <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> per avviare una sessione privata. Questa modalità impone che solo il processo che ha registrato il GUID del provider possa avviare la sessione del logger con tale GUID.<br/> È possibile creare fino a tre sessioni private in-process per processo.<br/> Questa opzione è supportata in Windows Vista e versioni successive.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_MODE_RESERVED</strong>(0x00100000)</td>
<td>Questa opzione viene utilizzata per segnalare l'heap e la traccia della sezione critica. Questa opzione è supportata in Windows Vista e versioni successive.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong>(0x00400000)</td>
<td>Questa opzione arresta la registrazione all'arresto ibrido. Se non si specifica né <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> né <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> , ETW sceglierà un valore predefinito a seconda che il chiamante provenga dalla sessione 0 o meno. Questa opzione è supportata in Windows 8 e Windows Server 2012. <br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong>(0x00800000)</td>
<td>Questa opzione continua ad accedere all'arresto ibrido. Se non si specifica né <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> né <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> , ETW sceglierà un valore predefinito a seconda che il chiamante provenga dalla sessione 0 o meno. Questa opzione è supportata in Windows 8 e Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_PAGED_MEMORY</strong> (0x01000000)</td>
<td>Usa la memoria di paging. Questa impostazione è consigliata in modo che gli eventi non usino la memoria non di paging. I buffer non di paging utilizzano la memoria non di paging per lo spazio del buffer. Poiché i buffer non di paging non vengono mai sottopaginati, una sessione di registrazione viene eseguita correttamente. L'uso di buffer paginabili comporta un minor utilizzo di risorse.<br/> I provider in modalità kernel e i logger di sistema non possono registrare gli eventi in sessioni che specificano questa modalità di registrazione.<br/> Questa modalità viene ignorata se è impostato <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> .<br/> Non è possibile usare questa modalità con il logger di kernel NT.<br/> <strong>Windows 2000:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_SYSTEM_LOGGER_MODE</strong>(0x02000000)</td>
<td>Questa opzione riceverà gli eventi da SystemTraceProvider. Se il parametro <a href="/windows/win32/api/evntrace/nf-evntrace-starttracea"><strong>StartTrace</strong></a><em>Properties</em> <strong>LogFileMode</strong> include questo flag, il logger sarà un logger di sistema. Questa opzione è supportata in Windows 8 e Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_INDEPENDENT_SESSION_MODE</strong>(0x08000000)</td>
<td>Indica che una sessione di registrazione non deve essere interessata da errori <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> in altre sessioni. Senza questo flag, se non è possibile pubblicare un evento in una delle sessioni in cui è abilitato un provider, l'evento non verrà pubblicato in nessuna delle sessioni. Quando questo flag è impostato, un errore di scrittura di un evento in una sessione non comporterà la restituzione di un codice di errore in altre sessioni da parte della funzione <strong>EventWrite</strong> . <br/> Non usare con <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>. <br/> Questa opzione è supportata in Windows 8.1, Windows Server 2012 R2 e versioni successive.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING</strong> (0x10000000)</td>
<td>Scrive gli eventi che sono stati registrati su processori diversi in un buffer comune. L'uso di questa modalità consente di eliminare il problema degli eventi che risultano non ordinati quando gli eventi vengono pubblicati su processori diversi usando l'ora di sistema. Questa modalità consente inoltre di eliminare il problema con i log circolari visualizzati per eliminare gli eventi in più computer del processore.<br/> Se non si utilizza questa modalità e si utilizza l'ora di sistema, è possibile che gli eventi non vengano visualizzati in ordine su più computer del processore. Questo perché i buffer ETW sono associati a un processore invece che a un thread. Di conseguenza, se un thread viene passato da una CPU a un'altra, il buffer associato alla seconda CPU può essere scaricato su disco prima di quello associato alla CPU precedente.<br/> Se si prevede un volume elevato di eventi (ad esempio, più di 1.000 eventi al secondo), non usare questa modalità.<br/> Si noti che il numero di processore non è incluso nell'evento.<br/> Questa opzione è supportata in Windows 7, Windows Server 2008 R2 e versioni successive.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_ADDTO_TRIAGE_DUMP</strong>(0x80000000)</td>
<td>Questa opzione aggiunge buffer ETW ai dump della valutazione. Questa opzione è supportata in Windows 8 e Windows Server 2012. <br/></td>
</tr>
</tbody>
</table>
