---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glossario COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483157"
---
# <a name="com-glossary"></a>Glossario COM+

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token di accesso**
</dt> <dd>

Oggetto che descrive il contesto di sicurezza di un processo o di un thread. Le informazioni contenute in un token includono l'identità e i privilegi dell'account utente associato al processo o al thread. Quando un utente esegue l'accesso, il sistema verifica la password dell'utente confrontandolo con le informazioni archiviate in un database di sicurezza. Se la password viene autenticata, il sistema produce un token di accesso. Ogni processo eseguito per conto di questo utente ha una copia di questo token di accesso.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Proprietà ACID**
</dt> <dd>

Acronimo coniato da pionieri dell'elaborazione delle transazioni per atomicità, coerenza, isolamento e durevolezza. Queste proprietà garantiscono un comportamento prevedibile, potenziando il ruolo delle transazioni come proposizioni All-or-none progettate per fornire risultati coerenti e prevedibili in un ambiente distribuito quando possono verificarsi errori indipendenti.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**attivazione**
</dt> <dd>

Catena di eventi che determina la creazione di un oggetto COM e la restituzione di un puntatore valido a un'interfaccia su tale oggetto. In COM+, un oggetto viene attivato nel relativo contesto o in quello del creatore (un oggetto che ha richiesto l'attivazione dell'oggetto). I servizi COM+ si basano sull'attivazione appropriata di un oggetto in base alla configurazione dell'oggetto. Nel corso dell'attivazione, il sistema determina il contesto in cui viene eseguito l'oggetto, Inizializza le proprietà di contesto, verifica le autorizzazioni di accesso e stabilisce un'identità di sicurezza.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**sicurezza attivazione**
</dt> <dd>

Un modulo di protezione della sicurezza che determina chi può avviare un server. La sicurezza per l'attivazione viene applicata automaticamente da Gestione controllo servizi (SCM) di un determinato computer. Al momento della ricezione di una richiesta da parte di un client per l'attivazione di un oggetto, SCM controlla la richiesta in base alle informazioni di sicurezza di attivazione archiviate nel registro di sistema. Viene verificata anche la sicurezza dell'attivazione per le attivazioni dello stesso computer. Detto anche *sicurezza di avvio*.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo di attivazione**
</dt> <dd>

Categoria di attivazione per un'applicazione COM+ che indica se l'applicazione viene eseguita all'interno o all'esterno dello spazio di elaborazione del client (a seconda che si tratti di una libreria o di un'applicazione server, rispettivamente) e che l'applicazione venga eseguita come servizio.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**attività**
</dt> <dd>

In COM+, thread logico che comprende una o più transazioni e contenente una raccolta di componenti raggruppati in un'applicazione COM+. Ogni oggetto COM appartiene a un'attività. Non è possibile modificare l'associazione tra un oggetto e un'attività.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processo del modello Apartment**
</dt> <dd>

Un processo che ha due o più Apartment a thread singolo e nessun Apartment multithread.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy di applicazione**
</dt> <dd>

Set di file contenente le informazioni di registrazione che consentono a un client di accedere in remoto a un'applicazione server COM+. Quando viene installato in un computer client, un file proxy di applicazione scrive le informazioni relative all'applicazione server nel computer client. il client può quindi accedere in remoto all'applicazione server.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**autenticazione**
</dt> <dd>

Il processo di sicurezza che determina che un chiamante di un'applicazione è in realtà colui che dichiara di essere, verificando l'autenticità di un'attestazione di identità. Per le applicazioni COM+, l'autenticazione può essere attivata e configurata in modo amministrativo, dopo la quale funziona in modo trasparente per l'applicazione.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**autorizzazione**
</dt> <dd>

Processo di sicurezza che determina se un chiamante di un'applicazione è autorizzato a eseguire le operazioni richieste.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Gestione risorse di Caching**
</dt> <dd>

Un gestore di risorse che funge da front-end per un altro gestore di risorse e che memorizza nella cache le informazioni in locale, riducendo il costo di accesso alla risorsa sottostante. A differenza di un gestore di risorse convenzionale, un gestore di risorse di Caching non partecipa al ripristino perché non archivia mai in modo permanente i dati sottostanti.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**sicurezza delle chiamate**
</dt> <dd>

Un modulo di protezione della sicurezza che consente di controllare l'accesso ai metodi di un oggetto server dopo l'avvio di un server.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**Classe (COM)**
</dt> <dd>

Implementazione concreta denominata di una o più interfacce. Una classe COM è identificata da un CLSID e, a volte, un ProgID.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**
</dt> <dd>

Capacità del server di mascherare la propria identità quando si effettuano chiamate per conto di un client. Quando il mascheramento è abilitato, le chiamate effettuate dal server che rappresenta il client possono essere effettuate con l'identità del client. Quando il mascheramento è disabilitato, le chiamate dal server verranno effettuate nell'identità del server.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Applicazione COM+**
</dt> <dd>

Unità principale di amministrazione e protezione per i servizi componenti. Un'applicazione COM+ è un gruppo di componenti COM che, in genere, eseguono funzioni correlate. Questi componenti sono ulteriormente costituiti da interfacce e metodi COM.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Pool di applicazioni COM+**
</dt> <dd>

Funzionalità di Servizi componenti che consente la scalabilità dei processi a thread singolo e consente inoltre di eseguire il recupero dagli errori nei singoli processi fornendo altri processi in esecuzione in grado di gestire le attivazioni.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Riciclo di applicazioni COM+**
</dt> <dd>

Funzionalità di Servizi componenti che aumenta significativamente la stabilità complessiva delle applicazioni, consentendo di arrestare normalmente un processo associato a un'applicazione e di riavviarlo.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catalogo COM+** 
</dt> <dd>

Archivio dati che include i dati di configurazione COM+. Le prestazioni delle attività di amministrazione COM+ richiedono la lettura e la scrittura dei dati archiviati nel catalogo. È possibile accedere al catalogo solo tramite lo strumento di amministrazione Servizi componenti o tramite la libreria COMAdmin.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventi COM+**
</dt> <dd>

Gli eventi COM+ corrispondono e collegano i Publisher e i sottoscrittori tramite un sistema di eventi a regime di controllo libero. Un server di pubblicazione esegue la chiamata al metodo per avviare un evento e un sottoscrittore riceve queste chiamate tramite il sistema di eventi anziché direttamente dal server di pubblicazione. Il servizio eventi COM+ gestisce l'elenco di sottoscrittori interessati che ricevono le chiamate e indirizza tali chiamate senza richiedere la conoscenza del server di pubblicazione.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Applicazione libreria COM+**
</dt> <dd>

Applicazione COM+ eseguita nel processo del client che la crea. Le applicazioni di libreria possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Pool di oggetti COM+**
</dt> <dd>

Servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di siano mantenute attive in un pool, pronte per essere utilizzate da qualsiasi client che richiede il componente.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partizioni COM+**
</dt> <dd>

Servizio COM+ che consente di creare spazi di esecuzione separati per le applicazioni in un singolo computer.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Set di partizioni COM+**
</dt> <dd>

Gruppo di partizioni COM+ mappato a un determinato ID utente in Active Directory.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componenti in coda COM+**
</dt> <dd>

Un servizio COM+, basato su Microsoft Message Queuing, che fornisce un modo semplice per richiamare ed eseguire i componenti in modo asincrono. L'elaborazione dei messaggi può essere eseguita indipendentemente dalla disponibilità o dall'accessibilità del mittente o del destinatario.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Applicazione server COM+**
</dt> <dd>

Applicazione COM+ che viene eseguita nel proprio processo. Le applicazioni server possono supportare tutti i servizi COM+.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**
</dt> <dd>

Funzionalità di Servizi componenti che consente di esporre un'applicazione COM+ come un servizio Web XML. Il protocollo SOAP COM+ consente inoltre di utilizzare un servizio Web XML come componente COM.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**
</dt> <dd>

Unità binaria di codice che include la creazione di pacchetti e il codice di registrazione e che crea oggetti COM. Tutte le applicazioni COM+ sono costituite da uno o più componenti COM.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**albero commit**
</dt> <dd>

In un sistema di transazioni distribuite, rappresentazione concettuale di una transazione basata sulle relazioni gerarchiche tra i singoli gestori di transazioni che partecipano a una transazione distribuita. In tale gerarchia sono inclusi i gestori delle risorse integrate associati ai gestori delle transazioni.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Oggetto COM**
</dt> <dd>

Nel modello di programmazione COM, una struttura di programmazione che incapsula i dati e le funzionalità, che vengono definiti e allocati come una singola unità e per cui l'unico accesso pubblico è attraverso le interfacce della struttura di programmazione. Un oggetto COM deve supportare come minimo l'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , che mantiene l'esistenza dell'oggetto mentre viene utilizzata e fornisce l'accesso alle altre interfacce dell'oggetto.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Gestione risorse di compensazione (CRM)**
</dt> <dd>

Funzionalità COM+ che consente alle risorse non transazionali di partecipare a una transazione di commit in due fasi con Microsoft Distributed Transaction Coordinator (DTC). In genere, dispongono non forniscono le funzionalità di isolamento dei gestori di risorse completi, ma forniscono atomicità transazionale e durabilità scrivendo in un log.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Strumento di amministrazione Servizi componenti**
</dt> <dd>

Uno snap-in di interfaccia utente tramite il quale gli amministratori e gli sviluppatori possono creare, configurare e gestire le applicazioni COM+, nonché amministrare le transazioni distribuite e i database residenti in memoria. Lo strumento di amministrazione Servizi componenti può essere utilizzato anche per visualizzare gli eventi di sistema e gestire i servizi di sistema in locale nel computer in cui è installato lo strumento.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modello concettuale**
</dt> <dd>

Il primo passaggio della fase di progettazione dell'applicazione COM+, in cui lo sviluppatore definisce i problemi aziendali da risolvere e stabilisce quali componenti e servizi sono necessari.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concorrenza**
</dt> <dd>

Capacità di più di una transazione o di un processo di accedere contemporaneamente agli stessi dati. COM+ gestisce in genere la concorrenza tramite la sincronizzazione.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurato**
</dt> <dd>

Componente COM che è stato installato in un'applicazione COM+. Una volta installato, il componente viene configurato nel catalogo COM+ per utilizzare i servizi COM+ disponibili.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**contesto**
</dt> <dd>

Set di proprietà della fase di esecuzione associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti. Ogni oggetto COM viene eseguito in un singolo contesto dall'attivazione alla disattivazione (sempre all'interno dello stesso Apartment). Inizializzata quando un oggetto viene attivato, le proprietà di contesto, ad esempio le proprietà del contesto di sicurezza, rappresentano le esigenze di runtime di un oggetto.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**livello dati**
</dt> <dd>

Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello di accesso DBMS, a cui è possibile accedere tramite il livello intermedio o il livello dei servizi aziendali, a volte tramite il livello di presentazione o il livello dei servizi utente. Il livello dati è costituito da componenti di accesso ai dati, anziché da connessioni DBMS non elaborate, per facilitare la condivisione delle risorse e consentire la configurazione dei client senza installare le librerie DBMS e i driver ODBC in ogni client. Detto anche *livello dei servizi dati*.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**
</dt> <dd>

Nelle applicazioni multithread, problema di threading che si verifica quando ogni membro di un set di thread è in attesa di un altro membro del set.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegazione**
</dt> <dd>

Una forma di rappresentazione che autorizza un server a agire per conto di un cliente, offrendo al server la possibilità di rappresentare i client in rete.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transazione distribuita**
</dt> <dd>

Transazione che coinvolge più gestori di risorse, che possono trovarsi nello stesso computer o in computer diversi.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**
</dt> <dd>

Servizio di sistema che gestisce le transazioni e le comunicazioni relative alle transazioni distribuite tra due o più gestori di risorse in uno o più sistemi per garantire le transazioni ACID corrette.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**mascheramento dinamico**
</dt> <dd>

Forma di mascheramento in cui l'identità client originale viene individuata come token di accesso del thread server per ogni chiamata al server downstream. Sebbene l'identità presentata possa essere determinata in modo dinamico, l'overhead necessario per eseguire questa operazione può essere notevolmente più oneroso. Per le applicazioni COM+, la configurazione predefinita è per la funzionalità di mascheramento dinamico, perché fornisce la flessibilità che in genere è necessaria per circostanze che richiedono l'uso della rappresentazione.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumeratore (oggetto)**
</dt> <dd>

Abilita l'enumerazione di elementi di una raccolta.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**evento**
</dt> <dd>

Azione riconosciuta da un oggetto, ad esempio il clic del mouse o la pressione di un tasto, per la quale è possibile scrivere codice per rispondere.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**oggetto classe di evento**
</dt> <dd>

Componente configurato che fornisce un record persistente nel sistema di eventi COM+ per descrivere i Publisher e le interfacce di attivazione associate a tali autori.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**Metodo Event**
</dt> <dd>

Metodo in un'interfaccia COM+ che identifica un evento COM+. I metodi di evento devono essere denominati in modo univoco e possono contenere solo parametri di input. Il valore restituito deve essere un valore **HRESULT**.

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**oggetto Event**
</dt> <dd>

Oggetto COM in grado di segnalare uno o più thread in cui si è verificato un evento. Qualsiasi thread all'interno di un processo può creare un oggetto evento.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**eccezione**
</dt> <dd>

Condizione o errore anomalo che si verifica durante l'esecuzione di un programma e che richiede l'esecuzione del software al di fuori del normale flusso di controllo.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**
</dt> <dd>

In un sistema di rete cluster, il processo di rilocazione di una risorsa di overload o di errore, ad esempio un server, un'unità disco o una rete, al relativo componente di backup.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processo a thread libero**
</dt> <dd>

Un processo con un Apartment a thread multipli e nessun Apartment a thread singolo.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Coordinatore commit globale**
</dt> <dd>

In un sistema di transazioni distribuite basato su Microsoft Windows, la gestione transazioni radice dell'albero di commit. Questo coordinatore decide di eseguire il commit o l'interruzione di una determinata transazione e non è mai in dubbio.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**rappresentazione**
</dt> <dd>

Possibilità che un thread venga eseguito in un contesto di sicurezza diverso da quello del processo proprietario del thread. Il thread del server utilizza un token di accesso che rappresenta le credenziali del client e, con questo, può accedere alle risorse a cui il client può accedere.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**livello di rappresentazione**
</dt> <dd>

Impostazione utilizzata dal client per concedere al server un particolare livello di autorità per eseguire azioni per conto del client. In COM+ è possibile impostare questa impostazione solo per le applicazioni server COM+.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**intercettazione**
</dt> <dd>

Per un oggetto attivato in un determinato contesto, il processo di gestione delle chiamate a tale oggetto da oltre il limite del contesto. Le chiamate all'interno del contesto vengono gestite con proxy di interfaccia semplici che gestiranno la mediazione necessaria per modificare l'ambiente di runtime da uno che consente di ospitare il chiamante a uno che soddisfa il chiamato.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interfaccia**
</dt> <dd>

Nella programmazione basata su COM, raccolta di funzioni pubbliche correlate che forniscono l'accesso a un oggetto COM. Il set di interfacce in un oggetto COM compone un contratto che specifica il modo in cui i programmi e altri oggetti possono interagire con l'oggetto COM.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy di interfaccia**
</dt> <dd>

Oggetto specifico dell'interfaccia che consente di creare un pacchetto di parametri (marshalling) per l'interfaccia in preparazione per una chiamata al metodo remoto e di decreare (annullare il marshalling) i valori restituiti dallo stub dell'interfaccia. Un proxy viene eseguito nello spazio degli indirizzi del mittente e comunica con uno stub corrispondente nello spazio degli indirizzi del destinatario.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**Stub interfaccia**
</dt> <dd>

Oggetto specifico dell'interfaccia che consente di annullare il pacchetto dei parametri sottoposti a marshalling, chiamare il metodo richiesto e i pacchetti (marshalling) restituiscono valori dal metodo chiamato. Lo stub viene eseguito nello spazio degli indirizzi del destinatario e comunica con un proxy di interfaccia corrispondente nello spazio degli indirizzi del mittente.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**oggetto interno**
</dt> <dd>

In una gerarchia transazionale, qualsiasi oggetto sotto l'oggetto radice.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**attivazione JIT (just-in-Time)**
</dt> <dd>

Servizio automatico fornito da COM+ che consente l'utilizzo più produttivo delle risorse inattive del server. Quando un componente viene configurato come JIT attivato, COM+ può disattivare un'istanza del componente mentre un client conserva ancora un riferimento attivo all'oggetto. La volta successiva che il client chiama un metodo sull'oggetto, COM+ riattiva l'oggetto in modo trasparente al client, solo nel tempo.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente legacy**
</dt> <dd>

Componente non configurato installato in un'applicazione COM+.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**
</dt> <dd>

Elemento dell'architettura del servizio componenti in coda COM+. Il listener è un oggetto COM che apre la coda di messaggi associata all'applicazione host e attende l'arrivo dei messaggi. Quando arrivano i messaggi, il listener invia i thread che elaborano i messaggi.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modello logico**
</dt> <dd>

Il secondo passaggio del processo di progettazione di un'applicazione COM+, in cui il modello concettuale è suddiviso nei livelli logici dell'architettura a tre livelli, come indicato di seguito: il livello di presentazione o i servizi utente; livello intermedio o servizi aziendali; e il livello dati o i servizi dati.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento a regime di controllo libero**
</dt> <dd>

Un evento il cui mittente (server di pubblicazione) e il destinatario (Sottoscrittore) non sono strettamente associati. In un sistema di eventi a regime di controllo libero, ad esempio gli eventi COM+, le informazioni sugli eventi di autori diversi vengono rese permanente in un archivio eventi. I Sottoscrittori eseguono una query su questo archivio e selezionano gli eventi che desiderano ricevere. Quando si selezionano le informazioni sull'evento dall'archivio eventi, viene creata una sottoscrizione. Quando si verifica un evento, il sistema di eventi Cerca nel database e trova i sottoscrittori interessati, crea un nuovo oggetto di ogni classe interessata e chiama un metodo su tale oggetto.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshalling**
</dt> <dd>

Il processo di creazione di pacchetti e annullamento del packaging dei parametri del metodo di interfaccia attraverso i limiti del thread o del processo, in modo da poter eseguire una chiamata di procedura remota.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**motore messaggi**
</dt> <dd>

Elemento dell'architettura del servizio componenti in coda COM+ che sposta i messaggi non riusciti nella coda di input in modo che possano essere ripetuti.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta evento**
</dt> <dd>

Tipo di evento utilizzato dal sistema di eventi COM+ per notificare ai sottoscrittori interessati ogni volta che vengono creati, modificati o rimossi sottoscrizioni o oggetti della classe di evento.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**Metodo**
</dt> <dd>

Nella programmazione basata su COM, un processo eseguito da un oggetto COM quando riceve un messaggio.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**livello intermedio**
</dt> <dd>

Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello che comprende la logica di business e le regole dei dati. I componenti che costituiscono il livello intermedio possono essere utilizzati per applicare le regole di business, ad esempio gli algoritmi aziendali, le normative legali o governative e le regole dei dati, progettate per garantire la coerenza delle strutture di dati all'interno di database specifici o multipli. Poiché questi componenti di livello intermedio non sono collegati a un client specifico, possono essere utilizzati da tutte le applicazioni e possono essere spostati in posizioni diverse, ad esempio il tempo di risposta e le altre regole richieste. Detto anche livello *Business Services* o *livello di logica di business*.

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processo di modello misto**
</dt> <dd>

Processo con un Apartment a thread multipli e uno o più Apartment a thread singolo.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**
</dt> <dd>

Nome che identifica in modo univoco un oggetto COM. Nello stesso modo in cui un percorso identifica un file nel file system, un moniker identifica un oggetto COM nello spazio dei nomi della directory.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**file con estensione msi**
</dt> <dd>

Un file creato dallo strumento di amministrazione Servizi componenti quando si esporta un'applicazione COM+ o un proxy di applicazione per l'installazione in un altro computer. Il file con estensione msi può essere installato in qualsiasi client basato su Windows utilizzando Windows Installer.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modello di Apartment a thread multipli**
</dt> <dd>

Modello di Apartment in cui tutti i thread del processo che sono stati inizializzati come a thread libero si trovano in un unico Apartment. Non è pertanto necessario effettuare il marshalling tra thread. I thread non devono recuperare e inviare messaggi perché COM non usa i messaggi di finestra in questo modello.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transazione nidificata**
</dt> <dd>

Una transazione secondaria è stata avviata dall'interno di un limite di transazione primario o padre esistente. Il commit della transazione primaria non viene eseguito fino a quando non viene eseguito il commit di tutte le transazioni subordinate o nidificate. COM+ non supporta le transazioni nidificate.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modello di Apartment neutro**
</dt> <dd>

Modello di threading in cui gli oggetti seguono le linee guida per gli Apartment a thread multipli ma possono essere eseguiti su qualsiasi tipo di thread. Il modello di Apartment neutro è il modello di threading consigliato per i componenti COM e le applicazioni COM+.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**oggetto persistente**
</dt> <dd>

Oggetto COM che può salvare lo stato interno quando viene richiesto da un client e che è conforme agli standard definiti da COM attraverso i quali i client possono richiedere l'inizializzazione, il caricamento e il salvataggio di oggetti da e verso un archivio dati (ad esempio file flat, archiviazione strutturata o memoria). È responsabilità del cliente gestire la posizione in cui vengono archiviati i dati persistenti dell'oggetto, ma non il formato dei dati.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interfaccia oggetto permanente**
</dt> <dd>

Interfaccia COM implementata da un oggetto persistente. I client utilizzano interfacce oggetto permanenti per indicare agli oggetti permanenti quando e dove archiviare il proprio stato.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interfaccia di notifica della fase zero**
</dt> <dd>

Interfaccia COM+ che consente alle applicazioni di rilevare quando una transazione è pronta per procedere con un protocollo di commit in due fasi, in modo da poter eseguire le operazioni di notifica necessarie e comunicare con la gestione transazioni quando le operazioni sono state completate.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modello fisico**
</dt> <dd>

Il terzo e ultimo passaggio del processo di progettazione dell'applicazione COM+, in cui lo sviluppatore determina dove risiedono fisicamente i componenti e il modo in cui devono essere codificati.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Player**
</dt> <dd>

Elemento dell'architettura del servizio COM+ Queued Components che recupera il messaggio da una coda e quindi carica l'oggetto server e gli stub di interfaccia standard per eseguire l'unmarshalling dei dati e richiamare i metodi del server. Il giocatore esegue l'unmarshalling del contesto di sicurezza del client sul lato server e quindi richiama il componente server e effettua le stesse chiamate al metodo. Le chiamate al metodo non vengono riprodotte dal lettore finché il componente client non viene completato e la transazione che ha registrato il metodo chiama commit.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**livello presentazione**
</dt> <dd>

Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello che presenta i dati all'utente e, facoltativamente, consente la manipolazione e l'immissione di dati. I due tipi principali di interfaccia utente per il livello presentazione sono l'applicazione tradizionale e l'applicazione basata sul Web. Detto anche *livello dei servizi utente*.

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

Tipo di oggetto contenuto, ad esempio la selezione di un utente in un documento, un intervallo di celle in un foglio di calcolo o un intervallo di caratteri in un documento di testo. Questo tipo di oggetto viene definito pseudo-oggetto perché non viene considerato come un oggetto distinto finché un utente non contrassegna la selezione.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**pubblicazione**
</dt> <dd>

Mittente di un evento. Nell'architettura degli eventi COM+, il server di pubblicazione effettua la chiamata al metodo per avviare un evento.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker della coda**
</dt> <dd>

Moniker utilizzato per attivare un componente in coda.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**
</dt> <dd>

In un'applicazione multithread, condizione che si verifica quando più thread accedono a un elemento dati senza coordinamento, causando probabilmente risultati incoerenti, a seconda del thread che raggiunge prima l'elemento dati. COM fornisce alcune funzioni progettate appositamente per evitare race condition nei server out-of-process.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**registrazione**
</dt> <dd>

Elemento dell'architettura del servizio COM+ Queued Components che effettua il marshalling del contesto di sicurezza del client in un messaggio e registra tutte le chiamate al metodo per un oggetto. Il registratore è una gestione proxy fornita dal sistema che seleziona le interfacce dalle interfacce accodabili nel catalogo COM+.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispenser di risorse**
</dt> <dd>

Nel modello di programmazione COM+, componente che gestisce lo stato condiviso non durevole per conto dei componenti dell'applicazione all'interno di un processo. I dispenser di risorse sono simili ai gestori di risorse, ma senza la garanzia di durabilità.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Resource Manager**
</dt> <dd>

Servizio che gestisce dati permanenti o durevoli nei database, nelle code di messaggi durevoli o nei file system transazionali. Si tratta del Resource Manager che sa come archiviare i dati ed eseguire il ripristino di emergenza. Le applicazioni server COM+ utilizzano i gestori di risorse per mantenere lo stato durevole di un'applicazione, ad esempio il record dell'inventario a mano, gli ordini in sospeso e gli account di credito. I gestori di risorse operano in collaborazione con Microsoft Distributed Transaction Coordinator (DTC) per garantire atomicità e isolamento a un'applicazione.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**sicurezza basata sui ruoli**
</dt> <dd>

Servizio di sicurezza COM+ fornito per le applicazioni COM+. Un ruolo rappresenta una categoria di utenti definiti per un'applicazione COM+ allo scopo di determinare le autorizzazioni di accesso alle risorse dell'applicazione. I ruoli vengono assegnati da uno sviluppatore a componenti, interfacce e metodi. Gli utenti vengono assegnati da un amministratore ai ruoli appropriati, consentendo a un utente all'interno di un determinato ruolo di accedere a tutte le risorse a cui è assegnato il ruolo.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**oggetto radice**
</dt> <dd>

Primo oggetto di una transazione, denominato radice della transazione, che viene sempre inserito in un nuovo limite transazionale. In una transazione può essere presente un solo oggetto radice. Tutti gli altri oggetti nella gerarchia transazionale sotto l'oggetto radice sono detti oggetti interni.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**gestione transazioni radice**
</dt> <dd>

Gestione transazioni nel sistema che avvia una transazione. La transazione non viene finalizzata finché la gestione transazioni radice non determina lo stato della transazione (commit o interrotto).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaforo**
</dt> <dd>

Oggetto kernel utilizzato per l'accesso a una risorsa condivisa.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Gestione controllo servizi**
</dt> <dd>

Un processo di Microsoft Windows Server che gestisce tutti i servizi nel registro di sistema di Windows.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Gestione proprietà condivise (SPM)**
</dt> <dd>

In com+, un dispenser di risorse che è possibile utilizzare per condividere lo stato non persistente tra più oggetti all'interno di un processo server.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processo a thread singolo**
</dt> <dd>

Un processo costituito da un solo Apartment a thread singolo, che a sua volta è costituito da un solo thread. Tutti gli oggetti COM che si trovano in un Apartment a thread singolo possono ricevere chiamate al metodo solo da un thread che appartiene a tale Apartment.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**
</dt> <dd>

Semplice protocollo basato su XML per lo scambio di informazioni strutturate e di tipo sul Web. Il protocollo non contiene alcuna semantica dell'applicazione o del trasporto, che lo rende altamente modulare ed estendibile.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**suddivisione registrazione**
</dt> <dd>

Per i componenti che sono già componenti COM esistenti e utilizzati nell'ambiente dei servizi COM+, la disposizione di registrazione in cui l'aspetto COM di base della registrazione viene archiviato nel registro di sistema di Windows e i nuovi servizi e attributi COM+, ad esempio i componenti in coda, vengono archiviati nel database di registrazione COM+. Ogni attributo Component viene archiviato nel registro di sistema di Windows o nel database di registrazione COM+. I nuovi componenti COM vengono registrati esclusivamente nel database di registrazione COM+, con alcune duplicazioni nel registro di sistema di Windows, in modo che gli strumenti esistenti possano usarli.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**con stato**
</dt> <dd>

O che si riferisce a un sistema o a un processo che monitora tutti i dettagli dello stato di un'attività a cui partecipa.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**senza stato**
</dt> <dd>

O che si riferisce a un sistema o a un processo che fa parte di un'attività senza monitorare tutti i dettagli dello stato.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**mascheramento statico**
</dt> <dd>

Una forma di mascheramento in cui l'identità client originale può essere presentata una volta a un server downstream, impostando l'identità del client originale una volta sul proxy. Questa identità client viene presentata come token del thread del server che verrà usato nelle chiamate al metodo successive.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Sottoscrittore**
</dt> <dd>

Destinatario di un evento. Nell'architettura degli eventi COM+, il sottoscrittore riceve le chiamate eseguite dal server di pubblicazione.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**oggetto Subscription**
</dt> <dd>

Nel sistema degli eventi COM+, oggetto creato da un Sottoscrittore per richiedere e gestire il recapito degli eventi.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**sincronizzazione**
</dt> <dd>

In COM+, un servizio che passa da componente a componente e impedisce a più di un chiamante di immettere il componente in un determinato momento. La sincronizzazione determina quando i thread possono inviare chiamate a un oggetto.

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modello architetturale a tre livelli**
</dt> <dd>

Il Framework fondamentale per il modello di progettazione logica, segmenta i componenti di un'applicazione in tre livelli di servizi, come indicato di seguito: il livello di presentazione o i servizi utente; livello intermedio o servizi aziendali; e il livello dati o i servizi dati. Questi livelli non corrispondono necessariamente a posizioni fisiche su diversi computer in una rete, ma piuttosto a livelli logici dell'applicazione.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento strettamente associato**
</dt> <dd>

Un evento il cui mittente (server di pubblicazione) e ricevitore (Sottoscrittore) sono strettamente associati. In un sistema di eventi strettamente accoppiato, il server di pubblicazione viene fornito con un'interfaccia in cui chiamare un metodo quando si verifica una modifica. Il Sottoscrittore conosce l'autore da cui richiedere la notifica e le interfacce esposte. Per un sistema di eventi strettamente associato è necessario che sia il server di pubblicazione che il Sottoscrittore siano sempre in esecuzione.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Registro di traccia**
</dt> <dd>

Un file di log generato automaticamente dal Distributed Transaction Coordinator Microsoft che mostra i dati relativi a una o più transazioni distribuite. Esempi di dati in un log di traccia sono ID transazione, tempo transazione e messaggi che indicano il risultato della transazione.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transazione**
</dt> <dd>

Unità di lavoro in cui si verifica una serie di operazioni correlate durante un processo dell'applicazione. Una transazione viene eseguita una sola volta ed è atomica, ovvero tutto il lavoro viene eseguito o nessuno di essi.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocollo di transazione Internet (TIP)**
</dt> <dd>

Transaction Internet Protocol è un protocollo di commit in due fasi standard che consente ai gestori di transazioni eterogenei di coordinare le transazioni distribuite, in particolare su Internet. Il protocollo di commit a due fasi è semplice da implementare ed è indipendente dal protocollo di comunicazione da applicazione ad applicazione, in modo che possa essere utilizzato con qualsiasi protocollo dell'applicazione, ma in particolare HTTP.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**gestione transazioni**
</dt> <dd>

Parte di Microsoft Distributed Transaction Coordinator (DTC) eseguita su ogni computer che partecipa a una transazione distribuita e gestisce le attività relative al commit o all'interruzione di tale parte della transazione.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**applicazione di elaborazione delle transazioni**
</dt> <dd>

Raccolta di operazioni di transazione che automatizzano una determinata attività aziendale.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema di elaborazione delle transazioni**
</dt> <dd>

Sistema completo, che comprende sia l'hardware che il software del computer, che ospita un'applicazione di elaborazione delle transazioni per eseguire le transazioni di routine necessarie per condurre le attività aziendali.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**protocollo di commit in due fasi**
</dt> <dd>

Un protocollo utilizzato solo nelle transazioni distribuite garantisce che il risultato di una transazione sia coerente in tutti i gestori di transazioni che partecipano alla transazione. Il protocollo viene eseguito in due fasi distinte per il commit o l'interruzione di una transazione: fase 1 valuta la condizione di ogni Resource Manager e la fase due completa la transazione.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente non configurato**
</dt> <dd>

Componente COM che non è stato configurato nel catalogo COM+. I componenti non configurati non possono utilizzare i servizi COM+.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Whereabouts**
</dt> <dd>

Per le transazioni DTC, struttura di dati opaca che rappresenta l'indirizzo del gestore delle transazioni di Resource Manager.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfacce XA**
</dt> <dd>

Set standard di interfacce di programmazione che consentono agli sviluppatori di applicazioni COM+ di accedere ai database conformi a XA e creare gestori di risorse che operano con database relazionali, Accodamento messaggi, file transazionali e database orientati a oggetti. Sebbene Microsoft non supporti direttamente il protocollo XA, Microsoft supporta le funzionalità di traduzione tra le transazioni OLE e XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Servizi Web XML**
</dt> <dd>

Unità della logica dell'applicazione che fornisce dati e servizi ad altre applicazioni. Le applicazioni accedono ai servizi Web XML tramite protocolli Web standard, ad esempio SOAP.

</dd> </dl>

 

 
