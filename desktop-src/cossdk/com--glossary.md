---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glossario COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda1c62c8edee1e15df33b63a9d4894639dd9e5637ed3e87a747d724f9e9040e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638721"
---
# <a name="com-glossary"></a>Glossario COM+

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token di accesso**
</dt> <dd>

Oggetto che descrive il contesto di sicurezza di un processo o di un thread. Le informazioni in un token includono l'identità e i privilegi dell'account utente associato al processo o al thread. Quando un utente esegue l'accesso, il sistema verifica la password dell'utente confrontandolo con le informazioni archiviate in un database di sicurezza. Se la password è autenticata, il sistema produce un token di accesso. Ogni processo eseguito per conto di questo utente dispone di una copia di questo token di accesso.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Proprietà ACID**
</dt> <dd>

Acronimo coniato da processi di elaborazione delle transazioni per operazioni atomiche, coerenti, isolate e durevoli. Queste proprietà assicurano un comportamento prevedibile, rafforzare il ruolo delle transazioni come proposizioni all-or-none progettate per fornire risultati coerenti e prevedibili in un ambiente distribuito quando possono verificarsi errori indipendenti.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**Attivazione**
</dt> <dd>

Catena di eventi che comporta la creazione di un oggetto COM e la restituzione di un puntatore valido a un'interfaccia su tale oggetto. In COM+, un oggetto viene attivato nel proprio contesto o in quello del relativo creatore (un oggetto che ha richiesto l'attivazione dell'oggetto). I servizi COM+ si basano sull'attivazione appropriata di un oggetto in base alla configurazione dell'oggetto. Nel corso dell'attivazione, il sistema determina il contesto in cui viene eseguito l'oggetto, inizializza le proprietà del contesto, controlla le autorizzazioni di accesso e stabilisce un'identità di sicurezza.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**sicurezza dell'attivazione**
</dt> <dd>

Forma di protezione della sicurezza che determina chi può avviare un server. La sicurezza dell'attivazione viene applicata automaticamente da Gestione controllo servizi (SCM) di un computer specifico. Al momento della ricezione di una richiesta da un client per attivare un oggetto, Gestione controllo servizi controlla la richiesta rispetto alle informazioni di sicurezza dell'attivazione archiviate nel registro. Viene verificata anche la sicurezza dell'attivazione per le attivazioni dello stesso computer. Chiamata anche *sicurezza di avvio.*

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo di attivazione**
</dt> <dd>

Categoria di attivazione per un'applicazione COM+ che indica se l'applicazione viene eseguita all'esterno o all'esterno dello spazio di elaborazione del client (a seconda che si tratta rispettivamente di una libreria o di un'applicazione server), nonché se l'applicazione viene eseguita come servizio.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**Attività**
</dt> <dd>

In COM+, thread logico che comprende una o più transazioni e contiene una raccolta di componenti raggruppati in un'applicazione COM+. Ogni oggetto COM appartiene a un'attività. L'associazione tra un oggetto e un'attività non può essere modificata.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processo del modello apartment**
</dt> <dd>

Processo che dispone di due o più apartment a thread singolo e nessun apartment a thread singolo.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy dell'applicazione**
</dt> <dd>

Set di file che contiene informazioni di registrazione che consentono a un client di accedere in remoto a un'applicazione server COM+. Se installato in un computer client, un file proxy dell'applicazione scrive le informazioni sull'applicazione server nel computer client. il client può quindi accedere in remoto all'applicazione server.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Autenticazione**
</dt> <dd>

Processo di sicurezza che determina che un chiamante di un'applicazione è effettivamente chi dichiara di essere, verificando l'autenticità di un'attestazione di identità. Per le applicazioni COM+, l'autenticazione può essere attivata e configurata a livello amministrativo, dopo di che funziona in modo trasparente per l'applicazione.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**Autorizzazione**
</dt> <dd>

Processo di sicurezza che consente di determinare se un chiamante di un'applicazione è autorizzato a eseguire le relative misure.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**memorizzazione nella cache di Resource Manager**
</dt> <dd>

Gestore di risorse che funge da front-end per un altro gestore di risorse e memorizza le informazioni nella cache locale, riducendo il costo di accesso alla risorsa sottostante. A differenza di un gestore di risorse convenzionale, un gestore di risorse di memorizzazione nella cache non partecipa al ripristino perché non archivia mai in modo permanente i dati sottostanti.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**sicurezza delle chiamate**
</dt> <dd>

Forma di protezione della sicurezza che consente di controllare l'accesso ai metodi di un oggetto server dopo l'avvio di un server.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**
</dt> <dd>

Implementazione concreta denominata di una o più interfacce. Una classe COM è identificata da un CLSID e, talvolta, da un ProgID.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**Cloaking**
</dt> <dd>

Capacità di un server di mascherare la propria identità quando si effettuano chiamate per conto di un client. Quando la clonazione è abilitata, le chiamate effettuate dal server che rappresenta il client possono essere effettuate con l'identità del client. Quando la clonazione è disabilitata, le chiamate del server verranno effettuate con l'identità del server.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Applicazione COM+**
</dt> <dd>

Unità principale di amministrazione e sicurezza per Servizi componenti. Un'applicazione COM+ è un gruppo di componenti COM che, in genere, eseguono funzioni correlate. Questi componenti sono costituiti ulteriormente da interfacce e metodi COM.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Pool di applicazioni COM+**
</dt> <dd>

Funzionalità di Servizi componenti che consente la scalabilità dei processi a thread singolo e consente anche di eseguire il ripristino da errori in singoli processi fornendo altri processi in esecuzione in grado di gestire le attivazioni.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Riciclo di applicazioni COM+**
</dt> <dd>

Funzionalità di Servizi componenti che aumenta significativamente la stabilità complessiva delle applicazioni consentendo di arrestare normalmente un processo associato a un'applicazione e riavviarlo.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catalogo COM+** 
</dt> <dd>

Archivio dati che contiene i dati di configurazione COM+. Le prestazioni delle attività di amministrazione COM+ richiedono la lettura e la scrittura dei dati archiviati nel catalogo. È possibile accedere al catalogo solo tramite lo strumento di amministrazione Servizi componenti o la libreria COMAdmin.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventi COM+**
</dt> <dd>

Gli eventi COM+ corrispondono e connettono server di pubblicazione e sottoscrittori tramite un sistema di eventi a controllo libero. Un server di pubblicazione effettua la chiamata al metodo per avviare un evento e un sottoscrittore riceve queste chiamate tramite il sistema di eventi anziché direttamente dal server di pubblicazione. Il servizio Eventi COM+ gestisce l'elenco dei sottoscrittori interessati che ricevono le chiamate e le indirizza senza richiedere la conoscenza del server di pubblicazione.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Applicazione libreria COM+**
</dt> <dd>

Applicazione COM+ eseguita nel processo del client che la crea. Le applicazioni di libreria possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Pool di oggetti COM+**
</dt> <dd>

Servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di se stesso siano mantenute attive in un pool, pronte per essere usate da qualsiasi client che richiede il componente.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partizioni COM+**
</dt> <dd>

Servizio COM+ che consente, in un singolo computer, la creazione di spazi di esecuzione separati per le applicazioni.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Set di partizioni COM+**
</dt> <dd>

Gruppo di partizioni COM+ di cui è stato eseguito il mapping a un ID utente specifico in Active Directory.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componenti in coda COM+**
</dt> <dd>

Un servizio COM+, basato su Microsoft Message Queuing, che fornisce un modo semplice per richiamare ed eseguire i componenti in modo asincrono. L'elaborazione dei messaggi può avvenire indipendentemente dalla disponibilità o dall'accessibilità del mittente o del destinatario.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Applicazione server COM+**
</dt> <dd>

Un'applicazione COM+ che viene eseguita nel proprio processo. Le applicazioni server possono supportare tutti i servizi COM+.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**
</dt> <dd>

Funzionalità di Servizi componenti che consente di esporre un'applicazione COM+ come servizio Web XML. COM+ SOAP consente inoltre di utilizzare un servizio Web XML come componente COM.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**
</dt> <dd>

Unità binaria di codice che include la creazione di pacchetti e il codice di registrazione e che crea oggetti COM. Tutte le applicazioni COM+ sono costituite da uno o più componenti COM.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**albero di commit**
</dt> <dd>

In un sistema di transazioni distribuite, rappresentazione concettuale di una transazione in base alle relazioni gerarchiche tra i singoli gestori transazioni che partecipano a una transazione distribuita. In tale gerarchia sono inclusi i gestori di risorse inseriti associati ai gestori delle transazioni.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Oggetto COM**
</dt> <dd>

Nel modello di programmazione COM una struttura di programmazione che incapsula dati e funzionalità, che vengono definiti e allocati come una singola unità e per cui l'unico accesso pubblico è tramite le interfacce della struttura di programmazione. Un oggetto COM deve supportare almeno l'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) che mantiene l'esistenza dell'oggetto durante l'uso e fornisce l'accesso alle altre interfacce dell'oggetto.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensazione Resource Manager (CRM)**
</dt> <dd>

Funzionalità COM+ che consente alle risorse non transazionali di partecipare a una transazione di commit a due fasi con il Microsoft Distributed Transaction Coordinator (DTC). In genere, i CPM non forniscono le funzionalità di isolamento di gestori di risorse completi, ma offrono atomicità e durabilità transazionali scrivendo in un log.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Strumento di amministrazione Servizi componenti**
</dt> <dd>

Snap-in dell'interfaccia utente tramite il quale amministratori e sviluppatori possono creare, configurare e gestire applicazioni COM+, nonché amministrare transazioni distribuite e database residenti in memoria. Lo strumento di amministrazione Servizi componenti può essere utilizzato anche per visualizzare gli eventi di sistema e gestire i servizi di sistema in locale nel computer in cui è installato lo strumento.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modello concettuale**
</dt> <dd>

Il primo passaggio della fase di progettazione dell'applicazione COM+, in cui lo sviluppatore definisce i problemi aziendali da risolvere e decide quali componenti e servizi sono necessari.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**Concorrenza**
</dt> <dd>

Possibilità di più transazioni o processi di accedere contemporaneamente agli stessi dati. COM+ gestisce in genere la concorrenza tramite la sincronizzazione.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurato**
</dt> <dd>

Componente COM installato in un'applicazione COM+. Dopo l'installazione, il componente viene configurato all'interno del catalogo COM+ per usare i servizi COM+ disponibili.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**Contesto**
</dt> <dd>

Set di proprietà di run-time associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti. Ogni oggetto COM viene eseguito in un singolo contesto dall'attivazione alla disattivazione (sempre all'interno dello stesso apartment). Inizializzato quando viene attivato un oggetto , le proprietà di contesto, ad esempio le proprietà del contesto di sicurezza, rappresentano le esigenze di run-time di un oggetto.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**livello dati**
</dt> <dd>

Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello di accesso DBMS, a cui è possibile accedere tramite il livello intermedio o il livello dei servizi aziendali, e in alcuni casi tramite il livello presentazione o il livello servizi utente. Il livello dati è costituito da componenti di accesso ai dati (anziché connessioni DBMS non elaborati) per facilitare la condivisione delle risorse e consentire la configurazione dei client senza installare le librerie DBMS e i driver ODBC in ogni client. Chiamato anche *livello dei servizi dati*.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Deadlock**
</dt> <dd>

Nelle applicazioni multithreading, un problema di threading che si verifica quando ogni membro di un set di thread è in attesa di un altro membro del set.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegazione**
</dt> <dd>

Forma di rappresentazione che autorizza un server ad agire per conto di un client, offrendo al server la possibilità di rappresentare i client in rete.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transazione distribuita**
</dt> <dd>

Transazione che coinvolge più gestori di risorse, che possono essere nello stesso computer o in computer diversi.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**
</dt> <dd>

Servizio di sistema che gestisce le transazioni e le comunicazioni correlate alle transazioni distribuite tra due o più gestori di risorse in uno o più sistemi per garantire la correttezza delle transazioni ACID.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**cloaking dinamico**
</dt> <dd>

Forma di clonazione in cui l'identità client originale viene individuata come token di accesso del thread del server in ogni chiamata al metodo al server downstream. Anche se l'identità presentata può essere determinata in modo dinamico, il sovraccarico necessario per eseguire questa operazione può essere notevolmente più costoso. Per le applicazioni COM+, la configurazione predefinita è per la funzionalità di clonazione dinamica perché offre la flessibilità generalmente richiesta dalle circostanze che richiedono innanzitutto l'uso della rappresentazione.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**Oggetto enumeratore**
</dt> <dd>

Abilita l'enumerazione di elementi di una raccolta.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**Evento**
</dt> <dd>

Azione riconosciuta da un oggetto, ad esempio quando si fa clic con il mouse o si preme un tasto e per la quale è possibile scrivere codice per rispondere.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**oggetto della classe di evento**
</dt> <dd>

Componente configurato che fornisce un record permanente nel sistema di eventi COM+ per descrivere gli editori e le interfacce di attivazione associate a tali server di pubblicazione.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**metodo event**
</dt> <dd>

Metodo in un'interfaccia COM+ che identifica un evento COM+. I metodi di evento devono essere denominati in modo univoco e possono contenere solo parametri di input. Il valore restituito deve essere **un HRESULT.**

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**oggetto evento**
</dt> <dd>

Oggetto COM in grado di segnalare a uno o più thread che si è verificato un evento. Qualsiasi thread all'interno di un processo può creare un oggetto evento.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**Eccezione**
</dt> <dd>

Condizione o errore anomalo che si verifica durante l'esecuzione di un programma e che richiede l'esecuzione di software al di fuori del normale flusso di controllo.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**Failover**
</dt> <dd>

In un sistema di rete del cluster, il processo di rilocazione di una risorsa sovraccarica o non riuscita, ad esempio un server, un'unità disco o una rete, nel relativo componente di backup.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processo a thread libero**
</dt> <dd>

Processo con apartment a thread singolo e senza apartment a thread singolo.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**coordinatore del commit globale**
</dt> <dd>

In un sistema di transazioni distribuite basato Windows Microsoft, il gestore transazioni radice dell'albero del commit. Questo coordinatore prende la decisione di eseguire il commit o di interrompere una determinata transazione e non è mai in dubbio.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**Rappresentazione**
</dt> <dd>

Possibilità di esecuzione di un thread in un contesto di sicurezza diverso da quello del processo proprietario del thread. Il thread del server usa un token di accesso che rappresenta le credenziali del client e, con questo, può accedere alle risorse a cui il client può accedere.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**livello di rappresentazione**
</dt> <dd>

Impostazione utilizzata dal client per concedere al server un particolare livello di autorità per eseguire azioni per conto del client. In COM+, questa opzione può essere impostata solo per le applicazioni server COM+.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**Intercettazione**
</dt> <dd>

Per un oggetto attivato in un determinato contesto, il processo di gestione delle chiamate a tale oggetto da oltre il limite del contesto. Le chiamate all'interno del contesto vengono gestite con proxy di interfaccia leggeri che gestiranno qualsiasi elemento di aggregazione necessario per modificare l'ambiente di run-time da uno che supporta il chiamante a uno che supporta il chiamato.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**Interfaccia**
</dt> <dd>

Nella programmazione basata su COM, raccolta di funzioni pubbliche correlate che forniscono l'accesso a un oggetto COM. Il set di interfacce in un oggetto COM compone un contratto che specifica in che modo programmi e altri oggetti possono interagire con l'oggetto COM.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy di interfaccia**
</dt> <dd>

Oggetto specifico dell'interfaccia che crea il pacchetto (effettua il marshalling) dei parametri per tale interfaccia in preparazione di una chiamata al metodo remoto e disaccoppia (unmarshal) i valori restituiti dallo stub dell'interfaccia. Un proxy viene eseguito nello spazio indirizzi del mittente e comunica con uno stub corrispondente nello spazio indirizzi del ricevitore.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**stub di interfaccia**
</dt> <dd>

Oggetto specifico dell'interfaccia che annulla il pacchetto dei parametri di cui è stato effettuato il marshalling, chiama il metodo richiesto e i pacchetti (effettuano il marshalling) restituiscono valori dal metodo chiamato. Lo stub viene eseguito nello spazio indirizzi del ricevitore e comunica con un proxy di interfaccia corrispondente nello spazio indirizzi del mittente.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**oggetto interno**
</dt> <dd>

In una gerarchia transazionale, qualsiasi oggetto sotto l'oggetto radice.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**Attivazione JIT (Just-In-Time)**
</dt> <dd>

Servizio automatico fornito da COM+ che consente di usare in modo più produttivo le risorse del server inattive. Quando un componente è configurato come attivato tramite JIT, COM+ può disattivare un'istanza di esso mentre un client contiene ancora un riferimento attivo all'oggetto. Alla successiva chiamata di un metodo sull'oggetto da parte del client, COM+ riattiva l'oggetto in modo trasparente nel client, just-in-time.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente legacy**
</dt> <dd>

Componente non configurato installato in un'applicazione COM+.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Listener**
</dt> <dd>

Elemento architetturale del servizio Componenti in coda COM+. Il listener è un oggetto COM che apre la coda di messaggi associata all'applicazione host e attende l'arrivo dei messaggi. Quando arrivano i messaggi, il listener invia i thread che elaborano i messaggi.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modello logico**
</dt> <dd>

Il secondo passaggio di un processo di progettazione di applicazioni COM+, in cui il modello concettuale è suddiviso nei livelli logici dell'architettura a tre livelli, come indicato di seguito: il livello presentazione o i servizi utente; il livello intermedio o i servizi aziendali; e il livello dati o i servizi dati.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**
</dt> <dd>

Evento il cui mittente (editore) e ricevitore (sottoscrittore) non sono strettamente associati. In un sistema di eventi a controllo libero, ad esempio eventi COM+, le informazioni sugli eventi di diversi autori vengono rese persistenti in un archivio eventi. I Sottoscrittori eseranno query su questo archivio e selezioneranno gli eventi che desiderano ricevere. Se si selezionano le informazioni sull'evento dall'archivio eventi, viene creata una sottoscrizione. Quando si verifica un evento, il sistema di eventi cerca nel database e trova i sottoscrittori interessati, crea un nuovo oggetto di ogni classe interessata e chiama un metodo su tale oggetto.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**Marshalling**
</dt> <dd>

Processo di creazione del pacchetto e decompressione dei parametri del metodo di interfaccia attraverso i limiti del thread o del processo in modo che possa essere eseguita una chiamata di procedura remota.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**spostamento messaggi**
</dt> <dd>

Elemento architetturale del servizio Componenti in coda COM+ che sposta nuovamente i messaggi non riusciti nella coda di input in modo che possano essere ritentati.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-evento**
</dt> <dd>

Tipo di evento utilizzato dal sistema di eventi COM+ per notificare ai sottoscrittori interessati ogni volta che vengono create, modificate o rimosse sottoscrizioni o oggetti della classe di evento.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**Metodo**
</dt> <dd>

Nella programmazione basata su COM, processo eseguito da un oggetto COM quando riceve un messaggio.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**livello intermedio**
</dt> <dd>

Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello che comprende la logica di business e le regole dei dati. I componenti che costituiscono il livello intermedio possono essere usati per applicare regole business, ad esempio algoritmi aziendali, normative legali o governative e regole dei dati, progettate per mantenere coerenti le strutture dei dati all'interno di database specifici o multipli. Poiché questi componenti di livello intermedio non sono associati a un client specifico, possono essere usati da tutte le applicazioni e possono essere spostati in posizioni diverse in base al tempo di risposta e ad altre regole. Detto anche *livello di servizi business o* livello di logica di *business.*

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processo di modello misto**
</dt> <dd>

Processo con apartment a thread singolo e uno o più apartment a thread singolo.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Nome che identifica in modo univoco un oggetto COM. Nello stesso modo in cui un percorso identifica un file nel file system, un moniker identifica un oggetto COM nello spazio dei nomi della directory.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**
</dt> <dd>

File creato dallo strumento di amministrazione Servizi componenti quando si esporta un'applicazione COM+ o un proxy di applicazione per l'installazione in un altro computer. Il file .msi può essere installato in qualsiasi client Windows usando il programma di Windows installazione.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modello di apartment multithreading**
</dt> <dd>

Modello di apartment in cui tutti i thread del processo inizializzati come a thread libero risiedono in un singolo apartment. Non è quindi necessario effettuare il marshalling tra thread. I thread non devono recuperare e inviare messaggi perché COM non usa messaggi finestra in questo modello.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transazione annidata**
</dt> <dd>

Transazione secondaria avviata dall'interno di un limite di transazione primario o padre esistente. Il commit della transazione primaria viene eseguito solo dopo il commit di tutte le transazioni subordinate o annidate. COM+ non supporta le transazioni annidate.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modello di apartment neutro**
</dt> <dd>

Modello di threading in cui gli oggetti seguono le linee guida per gli apartment multithreading, ma possono essere eseguiti in qualsiasi tipo di thread. Il modello di apartment neutro è il modello di threading consigliato per i componenti COM e le applicazioni COM+.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**oggetto persistente**
</dt> <dd>

Oggetto COM che può salvare il proprio stato interno quando richiesto da un client e conforme agli standard definiti da COM tramite i quali i client possono richiedere oggetti da inizializzare, caricare e salvare in e da un archivio dati (ad esempio file flat, archiviazione strutturata o memoria). È responsabilità del client gestire la posizione in cui sono archiviati i dati persistenti dell'oggetto, ma non il formato dei dati.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interfaccia oggetto persistente**
</dt> <dd>

Interfaccia COM implementata da un oggetto persistente. I client usano interfacce di oggetti persistenti per indicare a tali oggetti persistenti quando e dove archiviare il proprio stato.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interfaccia di notifica fase zero**
</dt> <dd>

Interfaccia COM+ che consente alle applicazioni di rilevare quando una transazione è pronta per procedere con un protocollo di commit a due fasi in modo che possa eseguire le operazioni di notifica necessarie e comunicare con la gestione transazioni al termine delle operazioni.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modello fisico**
</dt> <dd>

Il terzo e ultimo passaggio del processo di progettazione delle applicazioni COM+, in cui lo sviluppatore determina dove risiedono fisicamente i componenti e come devono essere codificati.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Giocatore**
</dt> <dd>

Elemento architetturale del servizio Componenti in coda COM+ che recupera il messaggio da una coda e quindi carica l'oggetto server e gli stub di interfaccia standard per annullare il datamarshaling e richiamare i metodi del server. Il lettore esegue l'unmarshaling del contesto di sicurezza del client sul lato server, quindi richiama il componente server ed esegue le stesse chiamate al metodo. Le chiamate al metodo non vengono riprodotte dal lettore fino al completamento del componente client e del commit della transazione che ha registrato il metodo.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**livello presentazione**
</dt> <dd>

Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello che presenta i dati all'utente e facoltativamente consente la manipolazione e l'immissione dei dati. I due tipi principali di interfaccia utente per il livello presentazione sono l'applicazione tradizionale e l'applicazione basata sul Web. Chiamato anche *livello dei servizi utente.*

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token di accesso primario**
</dt> <dd>

Descrive il contesto di sicurezza dell'account utente associato a un processo.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**gestione proxy**
</dt> <dd>

Nel marshalling standard, componente che gestisce tutti i proxy di interfaccia per un singolo oggetto.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-oggetto**
</dt> <dd>

Tipo di oggetto contenuto, ad esempio una selezione utente in un documento, un intervallo di celle in un foglio di calcolo o un intervallo di caratteri in un documento di testo. Questo tipo di oggetto viene chiamato pseudo-oggetto perché non viene considerato come un oggetto distinto fino a quando un utente non contrassegna la selezione.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**Editore**
</dt> <dd>

Mittente di un evento. Nell'architettura degli eventi COM+, il server di pubblicazione effettua la chiamata al metodo per avviare un evento.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker della coda**
</dt> <dd>

Moniker utilizzato per attivare un componente in coda.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**
</dt> <dd>

In un'applicazione multithreading, condizione che si verifica quando più thread accedono a un elemento di dati senza coordinamento, causando eventualmente risultati incoerenti, a seconda del thread che raggiunge per primo l'elemento di dati. COM fornisce alcune funzioni appositamente progettate per evitare race conditions nei server out-of-process.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**Registratore**
</dt> <dd>

Elemento architetturale del servizio componenti in coda COM+ che effettua il marshalling del contesto di sicurezza del client in un messaggio e registra tutte le chiamate al metodo per un oggetto. Il registratore è un gestore proxy fornito dal sistema che seleziona le interfacce dalle interfacce a cui è possibile eseguire l'accodamento nel catalogo COM+.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**distributore di risorse**
</dt> <dd>

Nel modello di programmazione COM+, componente che gestisce lo stato condiviso non modificabile per conto dei componenti dell'applicazione all'interno di un processo. I dispenser di risorse sono simili ai gestori di risorse, ma senza la garanzia di durabilità.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**
</dt> <dd>

Servizio che gestisce dati permanenti o durevoli in database, code di messaggi durevoli o file system transazionali. È il gestore di risorse che sa come archiviare i dati ed eseguire il ripristino di emergenza. Le applicazioni server COM+ usano i gestori di risorse per mantenere lo stato durevole di un'applicazione, ad esempio il record dell'inventario disponibile, gli ordini in sospeso e gli account che è possibile ottenere. I gestori di risorse lavorano in collaborazione con il Microsoft Distributed Transaction Coordinator (DTC) per garantire atomicità e isolamento a un'applicazione.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**sicurezza basata sui ruoli**
</dt> <dd>

Un servizio di sicurezza COM+ fornito per le applicazioni COM+. Un ruolo rappresenta una categoria di utenti definita per un'applicazione COM+ allo scopo di determinare le autorizzazioni di accesso alle risorse dell'applicazione. I ruoli vengono assegnati da uno sviluppatore a componenti, interfacce e metodi. Gli utenti vengono assegnati da un amministratore ai ruoli appropriati, consentendo a un utente all'interno di un determinato ruolo di accedere alle risorse a cui è assegnato tale ruolo.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**oggetto radice**
</dt> <dd>

Primo oggetto di una transazione, denominato radice della transazione, e sempre inserito in un nuovo limite transazionale. In una transazione può essere presente un solo oggetto radice. Tutti gli altri oggetti nella gerarchia transazionale all'interno dell'oggetto radice sono detti oggetti interni.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**gestione transazioni radice**
</dt> <dd>

Gestione transazioni nel sistema che avvia una transazione. La transazione non viene finalizzata fino a quando la gestione transazioni radice non determina lo stato della transazione (di cui è stato eseguito il commit o l'interruzione).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**Semaforo**
</dt> <dd>

Oggetto kernel usato per l'allocazione dell'accesso a una risorsa condivisa.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Service Control Manager (SCM)**
</dt> <dd>

Un processo Windows server microsoft che gestisce tutti i servizi nel Registro Windows sistema.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**gestione proprietà condivise (SPM)**
</dt> <dd>

In Com+, un dispenser di risorse che è possibile usare per condividere lo stato non attivo tra più oggetti all'interno di un processo server.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processo a thread singolo**
</dt> <dd>

Processo costituito da un solo apartment a thread singolo, che a sua volta è costituito esattamente da un thread. Tutti gli oggetti COM presenti in un apartment a thread singolo possono ricevere chiamate al metodo solo da un thread appartenente a tale apartment.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**Sapone**
</dt> <dd>

Protocollo semplice basato su XML per lo scambio di informazioni strutturate e sui tipi sul Web. Il protocollo non contiene alcuna semantica di applicazione o trasporto, che lo rende altamente modulare ed estendibile.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**
</dt> <dd>

Per i componenti che sono già componenti COM esistenti e vengono usati nell'ambiente dei servizi COM+, la disposizione di registrazione in cui l'aspetto COM di base della registrazione viene archiviato nel Registro di sistema di Windows e i nuovi servizi e attributi COM+ (ad esempio, Componenti in coda) vengono archiviati nel database di registrazione COM+. Ogni attributo del componente viene archiviato nel registro Windows o nel database di registrazione COM+. I nuovi componenti COM vengono registrati esclusivamente nel database di registrazione COM+, con alcune duplicazioni nel Registro di sistema Windows in modo che gli strumenti esistenti possano usarli.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**Stateful**
</dt> <dd>

Di un sistema o di un processo che monitora tutti i dettagli dello stato di un'attività a cui partecipa.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**Apolide**
</dt> <dd>

Di un sistema o di un processo che partecipa all'attività senza monitorare tutti i dettagli del relativo stato.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**cloaking statico**
</dt> <dd>

Forma di mascheramento in cui l'identità client originale può essere presentata una sola volta a un server downstream, impostando l'identità client originale una volta nel proxy. Questa identità client viene presentata come token del thread del server che verrà usato nelle chiamate al metodo successive.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Sottoscrittore**
</dt> <dd>

Ricevitore di un evento. Nell'architettura degli eventi COM+, il sottoscrittore riceve le chiamate effettuate dal server di pubblicazione.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**oggetto subscription**
</dt> <dd>

Nel sistema degli eventi COM+, oggetto creato da un sottoscrittore per richiedere e gestire il recapito degli eventi.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**Sincronizzazione**
</dt> <dd>

In COM+, un servizio che passa da un componente a un componente e impedisce a più chiamanti di accedere al componente in un determinato momento. La sincronizzazione determina quando i thread possono inviare chiamate a un oggetto.

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modello architetturale a tre livelli**
</dt> <dd>

Il framework fondamentale per il modello di progettazione logica segmenta i componenti di un'applicazione in tre livelli di servizi, come indicato di seguito: il livello presentazione o i servizi utente. il livello intermedio o i servizi aziendali; e il livello dati o i servizi dati. Questi livelli non corrispondono necessariamente a posizioni fisiche in vari computer in una rete, ma a livelli logici dell'applicazione.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento strettamente accoppiato**
</dt> <dd>

Evento il cui mittente (editore) e ricevitore (sottoscrittore) sono strettamente associati. In un sistema di eventi strettamente associato, al server di pubblicazione viene fornita un'interfaccia sulla quale chiamare un metodo quando si verifica una modifica. Il sottoscrittore conosce il server di pubblicazione da cui richiedere la notifica e le interfacce esposte. Un sistema di eventi strettamente associato richiede che il server di pubblicazione e il sottoscrittore siano sempre in esecuzione.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**log di traccia**
</dt> <dd>

File di log generato automaticamente dal Microsoft Distributed Transaction Coordinator che mostra i dati correlati a una o più transazioni distribuite. Esempi di dati in un log di traccia sono l'ID transazione, l'ora della transazione e i messaggi che indicano il risultato della transazione.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**Transazione**
</dt> <dd>

Unità di lavoro in cui si verifica una serie di operazioni correlate durante un processo dell'applicazione. Una transazione viene eseguita esattamente una volta ed è atomica, ovvero tutte le operazioni vengono eseguite o nessuna.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**TIP (Transaction Internet Protocol)**
</dt> <dd>

Transaction Internet Protocol è un protocollo di commit a due fasi standard che consente a gestori di transazioni eterogenei di coordinare le transazioni distribuite, in particolare tramite Internet. Il protocollo TIP per il commit a due fasi è semplice da implementare ed è indipendente dal protocollo di comunicazione da applicazione ad applicazione, in modo che possa essere usato con qualsiasi protocollo dell'applicazione, ma in particolare con HTTP.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**gestione transazioni**
</dt> <dd>

Parte del Microsoft Distributed Transaction Coordinator (DTC) che viene eseguita in ogni computer che partecipa a una transazione distribuita e gestisce le attività correlate al commit o all'interruzione di tale parte della transazione.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**applicazione di elaborazione delle transazioni**
</dt> <dd>

Raccolta di operazioni di transazione che automatizzano una determinata attività aziendale.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema di elaborazione delle transazioni**
</dt> <dd>

Un sistema completo, costituito sia dall'hardware del computer che dal software, che ospita un'applicazione di elaborazione delle transazioni per eseguire le transazioni di routine necessarie per svolgere attività aziendali.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**protocollo di commit a due fasi**
</dt> <dd>

Un protocollo utilizzato solo nelle transazioni distribuite garantisce che il risultato di una transazione sia coerente tra tutti i gestori transazioni che partecipano alla transazione. Il protocollo opera in due fasi distinte per eseguire il commit o l'interruzione di una transazione: la fase 1 valuta la condizione di ogni gestore di risorse e la fase due completa la transazione.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente non configurato**
</dt> <dd>

Componente COM che non è stato configurato all'interno del catalogo COM+. I componenti non configurati non possono usare i servizi COM+.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Luogo**
</dt> <dd>

Per le transazioni DTC, struttura di dati opaca che rappresenta l'indirizzo del gestore transazioni del gestore di risorse.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfacce XA**
</dt> <dd>

Set standard di interfacce di programmazione che consentono agli sviluppatori di applicazioni COM+ di accedere a database conformi a XA e creare gestori di risorse che operano con database relazionali, accodamento messaggi, file transazionali e database orientati a oggetti. Anche se Microsoft non supporta direttamente il protocollo XA, Microsoft supporta le funzionalità di conversione tra le transazioni OLE e XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Servizi Web XML**
</dt> <dd>

Unità di logica dell'applicazione che forniscono dati e servizi ad altre applicazioni. Le applicazioni accedono ai servizi Web XML tramite protocolli Web standard, ad esempio SOAP.

</dd> </dl>

 

 
