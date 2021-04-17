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
# <a name="com-glossary"></a><span data-ttu-id="c2606-103">Glossario COM+</span><span class="sxs-lookup"><span data-stu-id="c2606-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="c2606-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token di accesso**</span><span class="sxs-lookup"><span data-stu-id="c2606-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-105">Oggetto che descrive il contesto di sicurezza di un processo o di un thread.</span><span class="sxs-lookup"><span data-stu-id="c2606-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="c2606-106">Le informazioni contenute in un token includono l'identità e i privilegi dell'account utente associato al processo o al thread.</span><span class="sxs-lookup"><span data-stu-id="c2606-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="c2606-107">Quando un utente esegue l'accesso, il sistema verifica la password dell'utente confrontandolo con le informazioni archiviate in un database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c2606-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="c2606-108">Se la password viene autenticata, il sistema produce un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="c2606-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="c2606-109">Ogni processo eseguito per conto di questo utente ha una copia di questo token di accesso.</span><span class="sxs-lookup"><span data-stu-id="c2606-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Proprietà ACID**</span><span class="sxs-lookup"><span data-stu-id="c2606-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-111">Acronimo coniato da pionieri dell'elaborazione delle transazioni per atomicità, coerenza, isolamento e durevolezza.</span><span class="sxs-lookup"><span data-stu-id="c2606-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="c2606-112">Queste proprietà garantiscono un comportamento prevedibile, potenziando il ruolo delle transazioni come proposizioni All-or-none progettate per fornire risultati coerenti e prevedibili in un ambiente distribuito quando possono verificarsi errori indipendenti.</span><span class="sxs-lookup"><span data-stu-id="c2606-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**attivazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-114">Catena di eventi che determina la creazione di un oggetto COM e la restituzione di un puntatore valido a un'interfaccia su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="c2606-115">In COM+, un oggetto viene attivato nel relativo contesto o in quello del creatore (un oggetto che ha richiesto l'attivazione dell'oggetto).</span><span class="sxs-lookup"><span data-stu-id="c2606-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="c2606-116">I servizi COM+ si basano sull'attivazione appropriata di un oggetto in base alla configurazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="c2606-117">Nel corso dell'attivazione, il sistema determina il contesto in cui viene eseguito l'oggetto, Inizializza le proprietà di contesto, verifica le autorizzazioni di accesso e stabilisce un'identità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c2606-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**sicurezza attivazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-119">Un modulo di protezione della sicurezza che determina chi può avviare un server.</span><span class="sxs-lookup"><span data-stu-id="c2606-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="c2606-120">La sicurezza per l'attivazione viene applicata automaticamente da Gestione controllo servizi (SCM) di un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="c2606-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="c2606-121">Al momento della ricezione di una richiesta da parte di un client per l'attivazione di un oggetto, SCM controlla la richiesta in base alle informazioni di sicurezza di attivazione archiviate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c2606-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="c2606-122">Viene verificata anche la sicurezza dell'attivazione per le attivazioni dello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="c2606-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="c2606-123">Detto anche *sicurezza di avvio*.</span><span class="sxs-lookup"><span data-stu-id="c2606-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo di attivazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-125">Categoria di attivazione per un'applicazione COM+ che indica se l'applicazione viene eseguita all'interno o all'esterno dello spazio di elaborazione del client (a seconda che si tratti di una libreria o di un'applicazione server, rispettivamente) e che l'applicazione venga eseguita come servizio.</span><span class="sxs-lookup"><span data-stu-id="c2606-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**attività**</span><span class="sxs-lookup"><span data-stu-id="c2606-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-127">In COM+, thread logico che comprende una o più transazioni e contenente una raccolta di componenti raggruppati in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="c2606-128">Ogni oggetto COM appartiene a un'attività.</span><span class="sxs-lookup"><span data-stu-id="c2606-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="c2606-129">Non è possibile modificare l'associazione tra un oggetto e un'attività.</span><span class="sxs-lookup"><span data-stu-id="c2606-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processo del modello Apartment**</span><span class="sxs-lookup"><span data-stu-id="c2606-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-131">Un processo che ha due o più Apartment a thread singolo e nessun Apartment multithread.</span><span class="sxs-lookup"><span data-stu-id="c2606-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy di applicazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-133">Set di file contenente le informazioni di registrazione che consentono a un client di accedere in remoto a un'applicazione server COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="c2606-134">Quando viene installato in un computer client, un file proxy di applicazione scrive le informazioni relative all'applicazione server nel computer client. il client può quindi accedere in remoto all'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c2606-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**autenticazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-136">Il processo di sicurezza che determina che un chiamante di un'applicazione è in realtà colui che dichiara di essere, verificando l'autenticità di un'attestazione di identità.</span><span class="sxs-lookup"><span data-stu-id="c2606-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="c2606-137">Per le applicazioni COM+, l'autenticazione può essere attivata e configurata in modo amministrativo, dopo la quale funziona in modo trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**autorizzazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-139">Processo di sicurezza che determina se un chiamante di un'applicazione è autorizzato a eseguire le operazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="c2606-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Gestione risorse di Caching**</span><span class="sxs-lookup"><span data-stu-id="c2606-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-141">Un gestore di risorse che funge da front-end per un altro gestore di risorse e che memorizza nella cache le informazioni in locale, riducendo il costo di accesso alla risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="c2606-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="c2606-142">A differenza di un gestore di risorse convenzionale, un gestore di risorse di Caching non partecipa al ripristino perché non archivia mai in modo permanente i dati sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c2606-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**sicurezza delle chiamate**</span><span class="sxs-lookup"><span data-stu-id="c2606-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-144">Un modulo di protezione della sicurezza che consente di controllare l'accesso ai metodi di un oggetto server dopo l'avvio di un server.</span><span class="sxs-lookup"><span data-stu-id="c2606-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**Classe (COM)**</span><span class="sxs-lookup"><span data-stu-id="c2606-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-146">Implementazione concreta denominata di una o più interfacce.</span><span class="sxs-lookup"><span data-stu-id="c2606-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="c2606-147">Una classe COM è identificata da un CLSID e, a volte, un ProgID.</span><span class="sxs-lookup"><span data-stu-id="c2606-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span><span class="sxs-lookup"><span data-stu-id="c2606-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-149">Capacità del server di mascherare la propria identità quando si effettuano chiamate per conto di un client.</span><span class="sxs-lookup"><span data-stu-id="c2606-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="c2606-150">Quando il mascheramento è abilitato, le chiamate effettuate dal server che rappresenta il client possono essere effettuate con l'identità del client.</span><span class="sxs-lookup"><span data-stu-id="c2606-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="c2606-151">Quando il mascheramento è disabilitato, le chiamate dal server verranno effettuate nell'identità del server.</span><span class="sxs-lookup"><span data-stu-id="c2606-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Applicazione COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-153">Unità principale di amministrazione e protezione per i servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="c2606-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="c2606-154">Un'applicazione COM+ è un gruppo di componenti COM che, in genere, eseguono funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="c2606-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="c2606-155">Questi componenti sono ulteriormente costituiti da interfacce e metodi COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Pool di applicazioni COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-157">Funzionalità di Servizi componenti che consente la scalabilità dei processi a thread singolo e consente inoltre di eseguire il recupero dagli errori nei singoli processi fornendo altri processi in esecuzione in grado di gestire le attivazioni.</span><span class="sxs-lookup"><span data-stu-id="c2606-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Riciclo di applicazioni COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-159">Funzionalità di Servizi componenti che aumenta significativamente la stabilità complessiva delle applicazioni, consentendo di arrestare normalmente un processo associato a un'applicazione e di riavviarlo.</span><span class="sxs-lookup"><span data-stu-id="c2606-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catalogo COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="c2606-161">Archivio dati che include i dati di configurazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="c2606-162">Le prestazioni delle attività di amministrazione COM+ richiedono la lettura e la scrittura dei dati archiviati nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="c2606-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="c2606-163">È possibile accedere al catalogo solo tramite lo strumento di amministrazione Servizi componenti o tramite la libreria COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="c2606-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventi COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-165">Gli eventi COM+ corrispondono e collegano i Publisher e i sottoscrittori tramite un sistema di eventi a regime di controllo libero.</span><span class="sxs-lookup"><span data-stu-id="c2606-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="c2606-166">Un server di pubblicazione esegue la chiamata al metodo per avviare un evento e un sottoscrittore riceve queste chiamate tramite il sistema di eventi anziché direttamente dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="c2606-167">Il servizio eventi COM+ gestisce l'elenco di sottoscrittori interessati che ricevono le chiamate e indirizza tali chiamate senza richiedere la conoscenza del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Applicazione libreria COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-169">Applicazione COM+ eseguita nel processo del client che la crea.</span><span class="sxs-lookup"><span data-stu-id="c2606-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="c2606-170">Le applicazioni di libreria possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="c2606-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Pool di oggetti COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-172">Servizio automatico fornito da COM+ che consente di configurare un componente in modo che le istanze di siano mantenute attive in un pool, pronte per essere utilizzate da qualsiasi client che richiede il componente.</span><span class="sxs-lookup"><span data-stu-id="c2606-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partizioni COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-174">Servizio COM+ che consente di creare spazi di esecuzione separati per le applicazioni in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="c2606-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Set di partizioni COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-176">Gruppo di partizioni COM+ mappato a un determinato ID utente in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2606-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componenti in coda COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-178">Un servizio COM+, basato su Microsoft Message Queuing, che fornisce un modo semplice per richiamare ed eseguire i componenti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="c2606-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="c2606-179">L'elaborazione dei messaggi può essere eseguita indipendentemente dalla disponibilità o dall'accessibilità del mittente o del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2606-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Applicazione server COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-181">Applicazione COM+ che viene eseguita nel proprio processo.</span><span class="sxs-lookup"><span data-stu-id="c2606-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="c2606-182">Le applicazioni server possono supportare tutti i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**</span><span class="sxs-lookup"><span data-stu-id="c2606-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-184">Funzionalità di Servizi componenti che consente di esporre un'applicazione COM+ come un servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="c2606-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="c2606-185">Il protocollo SOAP COM+ consente inoltre di utilizzare un servizio Web XML come componente COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**</span><span class="sxs-lookup"><span data-stu-id="c2606-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-187">Unità binaria di codice che include la creazione di pacchetti e il codice di registrazione e che crea oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="c2606-188">Tutte le applicazioni COM+ sono costituite da uno o più componenti COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**albero commit**</span><span class="sxs-lookup"><span data-stu-id="c2606-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-190">In un sistema di transazioni distribuite, rappresentazione concettuale di una transazione basata sulle relazioni gerarchiche tra i singoli gestori di transazioni che partecipano a una transazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="c2606-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="c2606-191">In tale gerarchia sono inclusi i gestori delle risorse integrate associati ai gestori delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="c2606-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Oggetto COM**</span><span class="sxs-lookup"><span data-stu-id="c2606-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-193">Nel modello di programmazione COM, una struttura di programmazione che incapsula i dati e le funzionalità, che vengono definiti e allocati come una singola unità e per cui l'unico accesso pubblico è attraverso le interfacce della struttura di programmazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="c2606-194">Un oggetto COM deve supportare come minimo l'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , che mantiene l'esistenza dell'oggetto mentre viene utilizzata e fornisce l'accesso alle altre interfacce dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Gestione risorse di compensazione (CRM)**</span><span class="sxs-lookup"><span data-stu-id="c2606-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-196">Funzionalità COM+ che consente alle risorse non transazionali di partecipare a una transazione di commit in due fasi con Microsoft Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="c2606-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="c2606-197">In genere, dispongono non forniscono le funzionalità di isolamento dei gestori di risorse completi, ma forniscono atomicità transazionale e durabilità scrivendo in un log.</span><span class="sxs-lookup"><span data-stu-id="c2606-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="c2606-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-199">Uno snap-in di interfaccia utente tramite il quale gli amministratori e gli sviluppatori possono creare, configurare e gestire le applicazioni COM+, nonché amministrare le transazioni distribuite e i database residenti in memoria.</span><span class="sxs-lookup"><span data-stu-id="c2606-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="c2606-200">Lo strumento di amministrazione Servizi componenti può essere utilizzato anche per visualizzare gli eventi di sistema e gestire i servizi di sistema in locale nel computer in cui è installato lo strumento.</span><span class="sxs-lookup"><span data-stu-id="c2606-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modello concettuale**</span><span class="sxs-lookup"><span data-stu-id="c2606-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-202">Il primo passaggio della fase di progettazione dell'applicazione COM+, in cui lo sviluppatore definisce i problemi aziendali da risolvere e stabilisce quali componenti e servizi sono necessari.</span><span class="sxs-lookup"><span data-stu-id="c2606-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concorrenza**</span><span class="sxs-lookup"><span data-stu-id="c2606-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-204">Capacità di più di una transazione o di un processo di accedere contemporaneamente agli stessi dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="c2606-205">COM+ gestisce in genere la concorrenza tramite la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurato**</span><span class="sxs-lookup"><span data-stu-id="c2606-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-207">Componente COM che è stato installato in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="c2606-208">Una volta installato, il componente viene configurato nel catalogo COM+ per utilizzare i servizi COM+ disponibili.</span><span class="sxs-lookup"><span data-stu-id="c2606-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**contesto**</span><span class="sxs-lookup"><span data-stu-id="c2606-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-210">Set di proprietà della fase di esecuzione associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="c2606-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="c2606-211">Ogni oggetto COM viene eseguito in un singolo contesto dall'attivazione alla disattivazione (sempre all'interno dello stesso Apartment).</span><span class="sxs-lookup"><span data-stu-id="c2606-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="c2606-212">Inizializzata quando un oggetto viene attivato, le proprietà di contesto, ad esempio le proprietà del contesto di sicurezza, rappresentano le esigenze di runtime di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**livello dati**</span><span class="sxs-lookup"><span data-stu-id="c2606-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-214">Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello di accesso DBMS, a cui è possibile accedere tramite il livello intermedio o il livello dei servizi aziendali, a volte tramite il livello di presentazione o il livello dei servizi utente.</span><span class="sxs-lookup"><span data-stu-id="c2606-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="c2606-215">Il livello dati è costituito da componenti di accesso ai dati, anziché da connessioni DBMS non elaborate, per facilitare la condivisione delle risorse e consentire la configurazione dei client senza installare le librerie DBMS e i driver ODBC in ogni client.</span><span class="sxs-lookup"><span data-stu-id="c2606-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="c2606-216">Detto anche *livello dei servizi dati*.</span><span class="sxs-lookup"><span data-stu-id="c2606-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span><span class="sxs-lookup"><span data-stu-id="c2606-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-218">Nelle applicazioni multithread, problema di threading che si verifica quando ogni membro di un set di thread è in attesa di un altro membro del set.</span><span class="sxs-lookup"><span data-stu-id="c2606-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-220">Una forma di rappresentazione che autorizza un server a agire per conto di un cliente, offrendo al server la possibilità di rappresentare i client in rete.</span><span class="sxs-lookup"><span data-stu-id="c2606-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transazione distribuita**</span><span class="sxs-lookup"><span data-stu-id="c2606-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-222">Transazione che coinvolge più gestori di risorse, che possono trovarsi nello stesso computer o in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="c2606-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span><span class="sxs-lookup"><span data-stu-id="c2606-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-224">Servizio di sistema che gestisce le transazioni e le comunicazioni relative alle transazioni distribuite tra due o più gestori di risorse in uno o più sistemi per garantire le transazioni ACID corrette.</span><span class="sxs-lookup"><span data-stu-id="c2606-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**mascheramento dinamico**</span><span class="sxs-lookup"><span data-stu-id="c2606-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-226">Forma di mascheramento in cui l'identità client originale viene individuata come token di accesso del thread server per ogni chiamata al server downstream.</span><span class="sxs-lookup"><span data-stu-id="c2606-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="c2606-227">Sebbene l'identità presentata possa essere determinata in modo dinamico, l'overhead necessario per eseguire questa operazione può essere notevolmente più oneroso.</span><span class="sxs-lookup"><span data-stu-id="c2606-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="c2606-228">Per le applicazioni COM+, la configurazione predefinita è per la funzionalità di mascheramento dinamico, perché fornisce la flessibilità che in genere è necessaria per circostanze che richiedono l'uso della rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumeratore (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="c2606-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-230">Abilita l'enumerazione di elementi di una raccolta.</span><span class="sxs-lookup"><span data-stu-id="c2606-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**evento**</span><span class="sxs-lookup"><span data-stu-id="c2606-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-232">Azione riconosciuta da un oggetto, ad esempio il clic del mouse o la pressione di un tasto, per la quale è possibile scrivere codice per rispondere.</span><span class="sxs-lookup"><span data-stu-id="c2606-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**oggetto classe di evento**</span><span class="sxs-lookup"><span data-stu-id="c2606-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-234">Componente configurato che fornisce un record persistente nel sistema di eventi COM+ per descrivere i Publisher e le interfacce di attivazione associate a tali autori.</span><span class="sxs-lookup"><span data-stu-id="c2606-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**Metodo Event**</span><span class="sxs-lookup"><span data-stu-id="c2606-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-236">Metodo in un'interfaccia COM+ che identifica un evento COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="c2606-237">I metodi di evento devono essere denominati in modo univoco e possono contenere solo parametri di input.</span><span class="sxs-lookup"><span data-stu-id="c2606-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="c2606-238">Il valore restituito deve essere un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c2606-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**oggetto Event**</span><span class="sxs-lookup"><span data-stu-id="c2606-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-240">Oggetto COM in grado di segnalare uno o più thread in cui si è verificato un evento.</span><span class="sxs-lookup"><span data-stu-id="c2606-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="c2606-241">Qualsiasi thread all'interno di un processo può creare un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="c2606-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**eccezione**</span><span class="sxs-lookup"><span data-stu-id="c2606-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-243">Condizione o errore anomalo che si verifica durante l'esecuzione di un programma e che richiede l'esecuzione del software al di fuori del normale flusso di controllo.</span><span class="sxs-lookup"><span data-stu-id="c2606-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span><span class="sxs-lookup"><span data-stu-id="c2606-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-245">In un sistema di rete cluster, il processo di rilocazione di una risorsa di overload o di errore, ad esempio un server, un'unità disco o una rete, al relativo componente di backup.</span><span class="sxs-lookup"><span data-stu-id="c2606-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processo a thread libero**</span><span class="sxs-lookup"><span data-stu-id="c2606-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-247">Un processo con un Apartment a thread multipli e nessun Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="c2606-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Coordinatore commit globale**</span><span class="sxs-lookup"><span data-stu-id="c2606-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-249">In un sistema di transazioni distribuite basato su Microsoft Windows, la gestione transazioni radice dell'albero di commit.</span><span class="sxs-lookup"><span data-stu-id="c2606-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="c2606-250">Questo coordinatore decide di eseguire il commit o l'interruzione di una determinata transazione e non è mai in dubbio.</span><span class="sxs-lookup"><span data-stu-id="c2606-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**rappresentazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-252">Possibilità che un thread venga eseguito in un contesto di sicurezza diverso da quello del processo proprietario del thread.</span><span class="sxs-lookup"><span data-stu-id="c2606-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="c2606-253">Il thread del server utilizza un token di accesso che rappresenta le credenziali del client e, con questo, può accedere alle risorse a cui il client può accedere.</span><span class="sxs-lookup"><span data-stu-id="c2606-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**livello di rappresentazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-255">Impostazione utilizzata dal client per concedere al server un particolare livello di autorità per eseguire azioni per conto del client.</span><span class="sxs-lookup"><span data-stu-id="c2606-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="c2606-256">In COM+ è possibile impostare questa impostazione solo per le applicazioni server COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**intercettazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-258">Per un oggetto attivato in un determinato contesto, il processo di gestione delle chiamate a tale oggetto da oltre il limite del contesto.</span><span class="sxs-lookup"><span data-stu-id="c2606-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="c2606-259">Le chiamate all'interno del contesto vengono gestite con proxy di interfaccia semplici che gestiranno la mediazione necessaria per modificare l'ambiente di runtime da uno che consente di ospitare il chiamante a uno che soddisfa il chiamato.</span><span class="sxs-lookup"><span data-stu-id="c2606-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="c2606-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-261">Nella programmazione basata su COM, raccolta di funzioni pubbliche correlate che forniscono l'accesso a un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="c2606-262">Il set di interfacce in un oggetto COM compone un contratto che specifica il modo in cui i programmi e altri oggetti possono interagire con l'oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy di interfaccia**</span><span class="sxs-lookup"><span data-stu-id="c2606-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-264">Oggetto specifico dell'interfaccia che consente di creare un pacchetto di parametri (marshalling) per l'interfaccia in preparazione per una chiamata al metodo remoto e di decreare (annullare il marshalling) i valori restituiti dallo stub dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c2606-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="c2606-265">Un proxy viene eseguito nello spazio degli indirizzi del mittente e comunica con uno stub corrispondente nello spazio degli indirizzi del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2606-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**Stub interfaccia**</span><span class="sxs-lookup"><span data-stu-id="c2606-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-267">Oggetto specifico dell'interfaccia che consente di annullare il pacchetto dei parametri sottoposti a marshalling, chiamare il metodo richiesto e i pacchetti (marshalling) restituiscono valori dal metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="c2606-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="c2606-268">Lo stub viene eseguito nello spazio degli indirizzi del destinatario e comunica con un proxy di interfaccia corrispondente nello spazio degli indirizzi del mittente.</span><span class="sxs-lookup"><span data-stu-id="c2606-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**oggetto interno**</span><span class="sxs-lookup"><span data-stu-id="c2606-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-270">In una gerarchia transazionale, qualsiasi oggetto sotto l'oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="c2606-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**attivazione JIT (just-in-Time)**</span><span class="sxs-lookup"><span data-stu-id="c2606-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-272">Servizio automatico fornito da COM+ che consente l'utilizzo più produttivo delle risorse inattive del server.</span><span class="sxs-lookup"><span data-stu-id="c2606-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="c2606-273">Quando un componente viene configurato come JIT attivato, COM+ può disattivare un'istanza del componente mentre un client conserva ancora un riferimento attivo all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="c2606-274">La volta successiva che il client chiama un metodo sull'oggetto, COM+ riattiva l'oggetto in modo trasparente al client, solo nel tempo.</span><span class="sxs-lookup"><span data-stu-id="c2606-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente legacy**</span><span class="sxs-lookup"><span data-stu-id="c2606-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-276">Componente non configurato installato in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span><span class="sxs-lookup"><span data-stu-id="c2606-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-278">Elemento dell'architettura del servizio componenti in coda COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="c2606-279">Il listener è un oggetto COM che apre la coda di messaggi associata all'applicazione host e attende l'arrivo dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="c2606-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="c2606-280">Quando arrivano i messaggi, il listener invia i thread che elaborano i messaggi.</span><span class="sxs-lookup"><span data-stu-id="c2606-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modello logico**</span><span class="sxs-lookup"><span data-stu-id="c2606-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-282">Il secondo passaggio del processo di progettazione di un'applicazione COM+, in cui il modello concettuale è suddiviso nei livelli logici dell'architettura a tre livelli, come indicato di seguito: il livello di presentazione o i servizi utente; livello intermedio o servizi aziendali; e il livello dati o i servizi dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento a regime di controllo libero**</span><span class="sxs-lookup"><span data-stu-id="c2606-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-284">Un evento il cui mittente (server di pubblicazione) e il destinatario (Sottoscrittore) non sono strettamente associati.</span><span class="sxs-lookup"><span data-stu-id="c2606-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="c2606-285">In un sistema di eventi a regime di controllo libero, ad esempio gli eventi COM+, le informazioni sugli eventi di autori diversi vengono rese permanente in un archivio eventi.</span><span class="sxs-lookup"><span data-stu-id="c2606-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="c2606-286">I Sottoscrittori eseguono una query su questo archivio e selezionano gli eventi che desiderano ricevere.</span><span class="sxs-lookup"><span data-stu-id="c2606-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="c2606-287">Quando si selezionano le informazioni sull'evento dall'archivio eventi, viene creata una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c2606-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="c2606-288">Quando si verifica un evento, il sistema di eventi Cerca nel database e trova i sottoscrittori interessati, crea un nuovo oggetto di ogni classe interessata e chiama un metodo su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshalling**</span><span class="sxs-lookup"><span data-stu-id="c2606-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-290">Il processo di creazione di pacchetti e annullamento del packaging dei parametri del metodo di interfaccia attraverso i limiti del thread o del processo, in modo da poter eseguire una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="c2606-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**motore messaggi**</span><span class="sxs-lookup"><span data-stu-id="c2606-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-292">Elemento dell'architettura del servizio componenti in coda COM+ che sposta i messaggi non riusciti nella coda di input in modo che possano essere ripetuti.</span><span class="sxs-lookup"><span data-stu-id="c2606-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta evento**</span><span class="sxs-lookup"><span data-stu-id="c2606-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-294">Tipo di evento utilizzato dal sistema di eventi COM+ per notificare ai sottoscrittori interessati ogni volta che vengono creati, modificati o rimossi sottoscrizioni o oggetti della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="c2606-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**Metodo**</span><span class="sxs-lookup"><span data-stu-id="c2606-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-296">Nella programmazione basata su COM, un processo eseguito da un oggetto COM quando riceve un messaggio.</span><span class="sxs-lookup"><span data-stu-id="c2606-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**livello intermedio**</span><span class="sxs-lookup"><span data-stu-id="c2606-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-298">Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello che comprende la logica di business e le regole dei dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="c2606-299">I componenti che costituiscono il livello intermedio possono essere utilizzati per applicare le regole di business, ad esempio gli algoritmi aziendali, le normative legali o governative e le regole dei dati, progettate per garantire la coerenza delle strutture di dati all'interno di database specifici o multipli.</span><span class="sxs-lookup"><span data-stu-id="c2606-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="c2606-300">Poiché questi componenti di livello intermedio non sono collegati a un client specifico, possono essere utilizzati da tutte le applicazioni e possono essere spostati in posizioni diverse, ad esempio il tempo di risposta e le altre regole richieste.</span><span class="sxs-lookup"><span data-stu-id="c2606-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="c2606-301">Detto anche livello *Business Services* o *livello di logica di business*.</span><span class="sxs-lookup"><span data-stu-id="c2606-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processo di modello misto**</span><span class="sxs-lookup"><span data-stu-id="c2606-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-303">Processo con un Apartment a thread multipli e uno o più Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="c2606-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span><span class="sxs-lookup"><span data-stu-id="c2606-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-305">Nome che identifica in modo univoco un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="c2606-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="c2606-306">Nello stesso modo in cui un percorso identifica un file nel file system, un moniker identifica un oggetto COM nello spazio dei nomi della directory.</span><span class="sxs-lookup"><span data-stu-id="c2606-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**file con estensione msi**</span><span class="sxs-lookup"><span data-stu-id="c2606-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-308">Un file creato dallo strumento di amministrazione Servizi componenti quando si esporta un'applicazione COM+ o un proxy di applicazione per l'installazione in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="c2606-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="c2606-309">Il file con estensione msi può essere installato in qualsiasi client basato su Windows utilizzando Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c2606-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modello di Apartment a thread multipli**</span><span class="sxs-lookup"><span data-stu-id="c2606-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-311">Modello di Apartment in cui tutti i thread del processo che sono stati inizializzati come a thread libero si trovano in un unico Apartment.</span><span class="sxs-lookup"><span data-stu-id="c2606-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="c2606-312">Non è pertanto necessario effettuare il marshalling tra thread.</span><span class="sxs-lookup"><span data-stu-id="c2606-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="c2606-313">I thread non devono recuperare e inviare messaggi perché COM non usa i messaggi di finestra in questo modello.</span><span class="sxs-lookup"><span data-stu-id="c2606-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transazione nidificata**</span><span class="sxs-lookup"><span data-stu-id="c2606-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-315">Una transazione secondaria è stata avviata dall'interno di un limite di transazione primario o padre esistente.</span><span class="sxs-lookup"><span data-stu-id="c2606-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="c2606-316">Il commit della transazione primaria non viene eseguito fino a quando non viene eseguito il commit di tutte le transazioni subordinate o nidificate.</span><span class="sxs-lookup"><span data-stu-id="c2606-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="c2606-317">COM+ non supporta le transazioni nidificate.</span><span class="sxs-lookup"><span data-stu-id="c2606-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modello di Apartment neutro**</span><span class="sxs-lookup"><span data-stu-id="c2606-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-319">Modello di threading in cui gli oggetti seguono le linee guida per gli Apartment a thread multipli ma possono essere eseguiti su qualsiasi tipo di thread.</span><span class="sxs-lookup"><span data-stu-id="c2606-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="c2606-320">Il modello di Apartment neutro è il modello di threading consigliato per i componenti COM e le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**oggetto persistente**</span><span class="sxs-lookup"><span data-stu-id="c2606-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-322">Oggetto COM che può salvare lo stato interno quando viene richiesto da un client e che è conforme agli standard definiti da COM attraverso i quali i client possono richiedere l'inizializzazione, il caricamento e il salvataggio di oggetti da e verso un archivio dati (ad esempio file flat, archiviazione strutturata o memoria).</span><span class="sxs-lookup"><span data-stu-id="c2606-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="c2606-323">È responsabilità del cliente gestire la posizione in cui vengono archiviati i dati persistenti dell'oggetto, ma non il formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interfaccia oggetto permanente**</span><span class="sxs-lookup"><span data-stu-id="c2606-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-325">Interfaccia COM implementata da un oggetto persistente.</span><span class="sxs-lookup"><span data-stu-id="c2606-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="c2606-326">I client utilizzano interfacce oggetto permanenti per indicare agli oggetti permanenti quando e dove archiviare il proprio stato.</span><span class="sxs-lookup"><span data-stu-id="c2606-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interfaccia di notifica della fase zero**</span><span class="sxs-lookup"><span data-stu-id="c2606-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-328">Interfaccia COM+ che consente alle applicazioni di rilevare quando una transazione è pronta per procedere con un protocollo di commit in due fasi, in modo da poter eseguire le operazioni di notifica necessarie e comunicare con la gestione transazioni quando le operazioni sono state completate.</span><span class="sxs-lookup"><span data-stu-id="c2606-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modello fisico**</span><span class="sxs-lookup"><span data-stu-id="c2606-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-330">Il terzo e ultimo passaggio del processo di progettazione dell'applicazione COM+, in cui lo sviluppatore determina dove risiedono fisicamente i componenti e il modo in cui devono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="c2606-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Player**</span><span class="sxs-lookup"><span data-stu-id="c2606-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-332">Elemento dell'architettura del servizio COM+ Queued Components che recupera il messaggio da una coda e quindi carica l'oggetto server e gli stub di interfaccia standard per eseguire l'unmarshalling dei dati e richiamare i metodi del server.</span><span class="sxs-lookup"><span data-stu-id="c2606-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="c2606-333">Il giocatore esegue l'unmarshalling del contesto di sicurezza del client sul lato server e quindi richiama il componente server e effettua le stesse chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="c2606-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="c2606-334">Le chiamate al metodo non vengono riprodotte dal lettore finché il componente client non viene completato e la transazione che ha registrato il metodo chiama commit.</span><span class="sxs-lookup"><span data-stu-id="c2606-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**livello presentazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-336">Nel modello di architettura a tre livelli per le applicazioni aziendali, il livello che presenta i dati all'utente e, facoltativamente, consente la manipolazione e l'immissione di dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="c2606-337">I due tipi principali di interfaccia utente per il livello presentazione sono l'applicazione tradizionale e l'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="c2606-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="c2606-338">Detto anche *livello dei servizi utente*.</span><span class="sxs-lookup"><span data-stu-id="c2606-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token di accesso primario**</span><span class="sxs-lookup"><span data-stu-id="c2606-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-340">Descrive il contesto di sicurezza dell'account utente associato a un processo.</span><span class="sxs-lookup"><span data-stu-id="c2606-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**gestione proxy**</span><span class="sxs-lookup"><span data-stu-id="c2606-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-342">Nel marshalling standard, componente che gestisce tutti i proxy di interfaccia per un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-oggetto**</span><span class="sxs-lookup"><span data-stu-id="c2606-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-344">Tipo di oggetto contenuto, ad esempio la selezione di un utente in un documento, un intervallo di celle in un foglio di calcolo o un intervallo di caratteri in un documento di testo.</span><span class="sxs-lookup"><span data-stu-id="c2606-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="c2606-345">Questo tipo di oggetto viene definito pseudo-oggetto perché non viene considerato come un oggetto distinto finché un utente non contrassegna la selezione.</span><span class="sxs-lookup"><span data-stu-id="c2606-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**pubblicazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-347">Mittente di un evento.</span><span class="sxs-lookup"><span data-stu-id="c2606-347">The sender of an event.</span></span> <span data-ttu-id="c2606-348">Nell'architettura degli eventi COM+, il server di pubblicazione effettua la chiamata al metodo per avviare un evento.</span><span class="sxs-lookup"><span data-stu-id="c2606-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker della coda**</span><span class="sxs-lookup"><span data-stu-id="c2606-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-350">Moniker utilizzato per attivare un componente in coda.</span><span class="sxs-lookup"><span data-stu-id="c2606-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span><span class="sxs-lookup"><span data-stu-id="c2606-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-352">In un'applicazione multithread, condizione che si verifica quando più thread accedono a un elemento dati senza coordinamento, causando probabilmente risultati incoerenti, a seconda del thread che raggiunge prima l'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="c2606-353">COM fornisce alcune funzioni progettate appositamente per evitare race condition nei server out-of-process.</span><span class="sxs-lookup"><span data-stu-id="c2606-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**registrazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-355">Elemento dell'architettura del servizio COM+ Queued Components che effettua il marshalling del contesto di sicurezza del client in un messaggio e registra tutte le chiamate al metodo per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="c2606-356">Il registratore è una gestione proxy fornita dal sistema che seleziona le interfacce dalle interfacce accodabili nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispenser di risorse**</span><span class="sxs-lookup"><span data-stu-id="c2606-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-358">Nel modello di programmazione COM+, componente che gestisce lo stato condiviso non durevole per conto dei componenti dell'applicazione all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="c2606-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="c2606-359">I dispenser di risorse sono simili ai gestori di risorse, ma senza la garanzia di durabilità.</span><span class="sxs-lookup"><span data-stu-id="c2606-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Resource Manager**</span><span class="sxs-lookup"><span data-stu-id="c2606-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-361">Servizio che gestisce dati permanenti o durevoli nei database, nelle code di messaggi durevoli o nei file system transazionali.</span><span class="sxs-lookup"><span data-stu-id="c2606-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="c2606-362">Si tratta del Resource Manager che sa come archiviare i dati ed eseguire il ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="c2606-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="c2606-363">Le applicazioni server COM+ utilizzano i gestori di risorse per mantenere lo stato durevole di un'applicazione, ad esempio il record dell'inventario a mano, gli ordini in sospeso e gli account di credito.</span><span class="sxs-lookup"><span data-stu-id="c2606-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="c2606-364">I gestori di risorse operano in collaborazione con Microsoft Distributed Transaction Coordinator (DTC) per garantire atomicità e isolamento a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**sicurezza basata sui ruoli**</span><span class="sxs-lookup"><span data-stu-id="c2606-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-366">Servizio di sicurezza COM+ fornito per le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="c2606-367">Un ruolo rappresenta una categoria di utenti definiti per un'applicazione COM+ allo scopo di determinare le autorizzazioni di accesso alle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="c2606-368">I ruoli vengono assegnati da uno sviluppatore a componenti, interfacce e metodi.</span><span class="sxs-lookup"><span data-stu-id="c2606-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="c2606-369">Gli utenti vengono assegnati da un amministratore ai ruoli appropriati, consentendo a un utente all'interno di un determinato ruolo di accedere a tutte le risorse a cui è assegnato il ruolo.</span><span class="sxs-lookup"><span data-stu-id="c2606-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**oggetto radice**</span><span class="sxs-lookup"><span data-stu-id="c2606-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-371">Primo oggetto di una transazione, denominato radice della transazione, che viene sempre inserito in un nuovo limite transazionale.</span><span class="sxs-lookup"><span data-stu-id="c2606-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="c2606-372">In una transazione può essere presente un solo oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="c2606-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="c2606-373">Tutti gli altri oggetti nella gerarchia transazionale sotto l'oggetto radice sono detti oggetti interni.</span><span class="sxs-lookup"><span data-stu-id="c2606-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**gestione transazioni radice**</span><span class="sxs-lookup"><span data-stu-id="c2606-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-375">Gestione transazioni nel sistema che avvia una transazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="c2606-376">La transazione non viene finalizzata finché la gestione transazioni radice non determina lo stato della transazione (commit o interrotto).</span><span class="sxs-lookup"><span data-stu-id="c2606-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="c2606-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaforo**</span><span class="sxs-lookup"><span data-stu-id="c2606-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-378">Oggetto kernel utilizzato per l'accesso a una risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="c2606-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Gestione controllo servizi**</span><span class="sxs-lookup"><span data-stu-id="c2606-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-380">Un processo di Microsoft Windows Server che gestisce tutti i servizi nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="c2606-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Gestione proprietà condivise (SPM)**</span><span class="sxs-lookup"><span data-stu-id="c2606-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-382">In com+, un dispenser di risorse che è possibile utilizzare per condividere lo stato non persistente tra più oggetti all'interno di un processo server.</span><span class="sxs-lookup"><span data-stu-id="c2606-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processo a thread singolo**</span><span class="sxs-lookup"><span data-stu-id="c2606-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-384">Un processo costituito da un solo Apartment a thread singolo, che a sua volta è costituito da un solo thread.</span><span class="sxs-lookup"><span data-stu-id="c2606-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="c2606-385">Tutti gli oggetti COM che si trovano in un Apartment a thread singolo possono ricevere chiamate al metodo solo da un thread che appartiene a tale Apartment.</span><span class="sxs-lookup"><span data-stu-id="c2606-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span><span class="sxs-lookup"><span data-stu-id="c2606-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-387">Semplice protocollo basato su XML per lo scambio di informazioni strutturate e di tipo sul Web.</span><span class="sxs-lookup"><span data-stu-id="c2606-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="c2606-388">Il protocollo non contiene alcuna semantica dell'applicazione o del trasporto, che lo rende altamente modulare ed estendibile.</span><span class="sxs-lookup"><span data-stu-id="c2606-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**suddivisione registrazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-390">Per i componenti che sono già componenti COM esistenti e utilizzati nell'ambiente dei servizi COM+, la disposizione di registrazione in cui l'aspetto COM di base della registrazione viene archiviato nel registro di sistema di Windows e i nuovi servizi e attributi COM+, ad esempio i componenti in coda, vengono archiviati nel database di registrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="c2606-391">Ogni attributo Component viene archiviato nel registro di sistema di Windows o nel database di registrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="c2606-392">I nuovi componenti COM vengono registrati esclusivamente nel database di registrazione COM+, con alcune duplicazioni nel registro di sistema di Windows, in modo che gli strumenti esistenti possano usarli.</span><span class="sxs-lookup"><span data-stu-id="c2606-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**con stato**</span><span class="sxs-lookup"><span data-stu-id="c2606-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-394">O che si riferisce a un sistema o a un processo che monitora tutti i dettagli dello stato di un'attività a cui partecipa.</span><span class="sxs-lookup"><span data-stu-id="c2606-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**senza stato**</span><span class="sxs-lookup"><span data-stu-id="c2606-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-396">O che si riferisce a un sistema o a un processo che fa parte di un'attività senza monitorare tutti i dettagli dello stato.</span><span class="sxs-lookup"><span data-stu-id="c2606-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**mascheramento statico**</span><span class="sxs-lookup"><span data-stu-id="c2606-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-398">Una forma di mascheramento in cui l'identità client originale può essere presentata una volta a un server downstream, impostando l'identità del client originale una volta sul proxy.</span><span class="sxs-lookup"><span data-stu-id="c2606-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="c2606-399">Questa identità client viene presentata come token del thread del server che verrà usato nelle chiamate al metodo successive.</span><span class="sxs-lookup"><span data-stu-id="c2606-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Sottoscrittore**</span><span class="sxs-lookup"><span data-stu-id="c2606-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-401">Destinatario di un evento.</span><span class="sxs-lookup"><span data-stu-id="c2606-401">The receiver of an event.</span></span> <span data-ttu-id="c2606-402">Nell'architettura degli eventi COM+, il sottoscrittore riceve le chiamate eseguite dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**oggetto Subscription**</span><span class="sxs-lookup"><span data-stu-id="c2606-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-404">Nel sistema degli eventi COM+, oggetto creato da un Sottoscrittore per richiedere e gestire il recapito degli eventi.</span><span class="sxs-lookup"><span data-stu-id="c2606-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-406">In COM+, un servizio che passa da componente a componente e impedisce a più di un chiamante di immettere il componente in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="c2606-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="c2606-407">La sincronizzazione determina quando i thread possono inviare chiamate a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c2606-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modello architetturale a tre livelli**</span><span class="sxs-lookup"><span data-stu-id="c2606-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-409">Il Framework fondamentale per il modello di progettazione logica, segmenta i componenti di un'applicazione in tre livelli di servizi, come indicato di seguito: il livello di presentazione o i servizi utente; livello intermedio o servizi aziendali; e il livello dati o i servizi dati.</span><span class="sxs-lookup"><span data-stu-id="c2606-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="c2606-410">Questi livelli non corrispondono necessariamente a posizioni fisiche su diversi computer in una rete, ma piuttosto a livelli logici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento strettamente associato**</span><span class="sxs-lookup"><span data-stu-id="c2606-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-412">Un evento il cui mittente (server di pubblicazione) e ricevitore (Sottoscrittore) sono strettamente associati.</span><span class="sxs-lookup"><span data-stu-id="c2606-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="c2606-413">In un sistema di eventi strettamente accoppiato, il server di pubblicazione viene fornito con un'interfaccia in cui chiamare un metodo quando si verifica una modifica.</span><span class="sxs-lookup"><span data-stu-id="c2606-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="c2606-414">Il Sottoscrittore conosce l'autore da cui richiedere la notifica e le interfacce esposte.</span><span class="sxs-lookup"><span data-stu-id="c2606-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="c2606-415">Per un sistema di eventi strettamente associato è necessario che sia il server di pubblicazione che il Sottoscrittore siano sempre in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c2606-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Registro di traccia**</span><span class="sxs-lookup"><span data-stu-id="c2606-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-417">Un file di log generato automaticamente dal Distributed Transaction Coordinator Microsoft che mostra i dati relativi a una o più transazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="c2606-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="c2606-418">Esempi di dati in un log di traccia sono ID transazione, tempo transazione e messaggi che indicano il risultato della transazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transazione**</span><span class="sxs-lookup"><span data-stu-id="c2606-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-420">Unità di lavoro in cui si verifica una serie di operazioni correlate durante un processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="c2606-421">Una transazione viene eseguita una sola volta ed è atomica, ovvero tutto il lavoro viene eseguito o nessuno di essi.</span><span class="sxs-lookup"><span data-stu-id="c2606-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocollo di transazione Internet (TIP)**</span><span class="sxs-lookup"><span data-stu-id="c2606-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-423">Transaction Internet Protocol è un protocollo di commit in due fasi standard che consente ai gestori di transazioni eterogenei di coordinare le transazioni distribuite, in particolare su Internet.</span><span class="sxs-lookup"><span data-stu-id="c2606-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="c2606-424">Il protocollo di commit a due fasi è semplice da implementare ed è indipendente dal protocollo di comunicazione da applicazione ad applicazione, in modo che possa essere utilizzato con qualsiasi protocollo dell'applicazione, ma in particolare HTTP.</span><span class="sxs-lookup"><span data-stu-id="c2606-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**gestione transazioni**</span><span class="sxs-lookup"><span data-stu-id="c2606-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-426">Parte di Microsoft Distributed Transaction Coordinator (DTC) eseguita su ogni computer che partecipa a una transazione distribuita e gestisce le attività relative al commit o all'interruzione di tale parte della transazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**applicazione di elaborazione delle transazioni**</span><span class="sxs-lookup"><span data-stu-id="c2606-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-428">Raccolta di operazioni di transazione che automatizzano una determinata attività aziendale.</span><span class="sxs-lookup"><span data-stu-id="c2606-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema di elaborazione delle transazioni**</span><span class="sxs-lookup"><span data-stu-id="c2606-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-430">Sistema completo, che comprende sia l'hardware che il software del computer, che ospita un'applicazione di elaborazione delle transazioni per eseguire le transazioni di routine necessarie per condurre le attività aziendali.</span><span class="sxs-lookup"><span data-stu-id="c2606-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**protocollo di commit in due fasi**</span><span class="sxs-lookup"><span data-stu-id="c2606-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-432">Un protocollo utilizzato solo nelle transazioni distribuite garantisce che il risultato di una transazione sia coerente in tutti i gestori di transazioni che partecipano alla transazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="c2606-433">Il protocollo viene eseguito in due fasi distinte per il commit o l'interruzione di una transazione: fase 1 valuta la condizione di ogni Resource Manager e la fase due completa la transazione.</span><span class="sxs-lookup"><span data-stu-id="c2606-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente non configurato**</span><span class="sxs-lookup"><span data-stu-id="c2606-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-435">Componente COM che non è stato configurato nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="c2606-436">I componenti non configurati non possono utilizzare i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="c2606-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Whereabouts**</span><span class="sxs-lookup"><span data-stu-id="c2606-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-438">Per le transazioni DTC, struttura di dati opaca che rappresenta l'indirizzo del gestore delle transazioni di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c2606-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfacce XA**</span><span class="sxs-lookup"><span data-stu-id="c2606-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-440">Set standard di interfacce di programmazione che consentono agli sviluppatori di applicazioni COM+ di accedere ai database conformi a XA e creare gestori di risorse che operano con database relazionali, Accodamento messaggi, file transazionali e database orientati a oggetti.</span><span class="sxs-lookup"><span data-stu-id="c2606-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="c2606-441">Sebbene Microsoft non supporti direttamente il protocollo XA, Microsoft supporta le funzionalità di traduzione tra le transazioni OLE e XA.</span><span class="sxs-lookup"><span data-stu-id="c2606-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="c2606-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Servizi Web XML**</span><span class="sxs-lookup"><span data-stu-id="c2606-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="c2606-443">Unità della logica dell'applicazione che fornisce dati e servizi ad altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c2606-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="c2606-444">Le applicazioni accedono ai servizi Web XML tramite protocolli Web standard, ad esempio SOAP.</span><span class="sxs-lookup"><span data-stu-id="c2606-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
