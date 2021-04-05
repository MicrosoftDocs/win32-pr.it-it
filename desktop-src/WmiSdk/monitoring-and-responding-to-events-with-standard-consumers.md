---
description: È possibile utilizzare le classi consumer standard installate per eseguire azioni in base agli eventi in un sistema operativo.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Monitoraggio e risposta agli eventi con consumer standard
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103886338"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="04c60-103">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="04c60-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="04c60-104">È possibile utilizzare le [classi consumer standard](standard-consumer-classes.md) installate per eseguire azioni in base agli eventi in un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="04c60-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="04c60-105">I consumer standard sono classi semplici già registrate e definiscono classi consumer permanenti.</span><span class="sxs-lookup"><span data-stu-id="04c60-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="04c60-106">Ogni consumer standard esegue un'azione specifica dopo la ricezione di una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="04c60-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="04c60-107">Ad esempio, è possibile definire un'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per eseguire uno script quando lo spazio libero su disco in un computer è diverso da una dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="04c60-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="04c60-108">WMI compila gli utenti standard in spazi dei nomi predefiniti che dipendono dal sistema operativo, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="04c60-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="04c60-109">In Windows Server 2003, tutti gli utenti standard vengono compilati per impostazione predefinita nello \\ spazio dei nomi "sottoscrizione radice".</span><span class="sxs-lookup"><span data-stu-id="04c60-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="04c60-110">Per gli spazi dei nomi e i sistemi operativi predefiniti specifici per ogni classe WMI, vedere le sezioni osservazioni e requisiti di ogni argomento della classe.</span><span class="sxs-lookup"><span data-stu-id="04c60-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="04c60-111">Nella tabella seguente sono elencati e descritti i consumer standard WMI.</span><span class="sxs-lookup"><span data-stu-id="04c60-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="04c60-112">Consumer standard</span><span class="sxs-lookup"><span data-stu-id="04c60-112">Standard consumer</span></span>                                              | <span data-ttu-id="04c60-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04c60-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04c60-114">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="04c60-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="04c60-115">Esegue uno script quando riceve una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="04c60-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="04c60-116">Per ulteriori informazioni, vedere [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="04c60-117">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="04c60-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="04c60-118">Scrive stringhe personalizzate in un file di log di testo quando riceve una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="04c60-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="04c60-119">Per ulteriori informazioni, vedere [scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="04c60-120">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="04c60-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="04c60-121">Registra un messaggio specifico nel registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="04c60-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="04c60-122">Per ulteriori informazioni, vedere [registrazione nel registro eventi NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="04c60-123">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="04c60-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="04c60-124">Invia un messaggio di posta elettronica tramite SMTP ogni volta che viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="04c60-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="04c60-125">Per ulteriori informazioni, vedere [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="04c60-126">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="04c60-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="04c60-127">Avvia un processo quando un evento viene recapitato a un sistema locale.</span><span class="sxs-lookup"><span data-stu-id="04c60-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="04c60-128">Il file eseguibile deve trovarsi in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro per impedire a un utente non autorizzato di sostituire l'eseguibile con un altro eseguibile.</span><span class="sxs-lookup"><span data-stu-id="04c60-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="04c60-129">Per ulteriori informazioni, vedere [esecuzione di un programma dalla riga di comando in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="04c60-130">Nella procedura seguente viene descritto come monitorare e rispondere agli eventi utilizzando un consumer standard.</span><span class="sxs-lookup"><span data-stu-id="04c60-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="04c60-131">Si noti che la procedura è identica per un file, uno script o un'applicazione di Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="04c60-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="04c60-132">**Per monitorare e rispondere agli eventi con un consumer standard**</span><span class="sxs-lookup"><span data-stu-id="04c60-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="04c60-133">Specificare lo spazio dei nomi in un file MOF utilizzando lo [ \# spazio dei nomi pragma](pragma-namespace.md)del comando per il preprocessore MOF.</span><span class="sxs-lookup"><span data-stu-id="04c60-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="04c60-134">In uno script o un'applicazione specificare lo spazio dei nomi nel codice che si connette a WMI.</span><span class="sxs-lookup"><span data-stu-id="04c60-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="04c60-135">Nell'esempio di codice MOF seguente viene illustrato come specificare lo \\ spazio dei nomi della sottoscrizione radice.</span><span class="sxs-lookup"><span data-stu-id="04c60-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="04c60-136">La maggior parte [*degli eventi intrinseci*](gloss-i.md) è associata a modifiche alle istanze di classe nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="04c60-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="04c60-137">Tuttavia, gli eventi del registro di sistema, ad esempio [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) , vengono generati nello \\ spazio dei nomi predefinito radice dal [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).</span><span class="sxs-lookup"><span data-stu-id="04c60-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="04c60-138">Un consumer può includere classi di evento situate in altri spazi dei nomi specificando lo spazio dei nomi nella proprietà **EventNamespace** nella query [**\_ \_ EventFilter**](--eventfilter.md) per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="04c60-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="04c60-139">Le classi [*degli eventi intrinseci*](gloss-i.md) , ad esempio [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sono disponibili in ogni spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="04c60-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="04c60-140">Creare e popolare un'istanza di una classe consumer standard.</span><span class="sxs-lookup"><span data-stu-id="04c60-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="04c60-141">Questa istanza può avere un valore univoco nella proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="04c60-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="04c60-142">È possibile aggiornare un consumer esistente riutilizzando lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="04c60-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="04c60-143">**InsertionStringTemplates** contiene il testo da inserire in un evento specificato in **eventType**.</span><span class="sxs-lookup"><span data-stu-id="04c60-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="04c60-144">È possibile usare stringhe letterali o fare riferimento direttamente a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="04c60-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="04c60-145">Per ulteriori informazioni, vedere [utilizzo di modelli di stringa standard](using-standard-string-templates.md) e [istruzione SELECT per le query di eventi](select-statement-for-event-queries.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="04c60-146">Utilizzare un'origine esistente per il registro eventi che supporti una stringa di inserimento senza testo associato.</span><span class="sxs-lookup"><span data-stu-id="04c60-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="04c60-147">Nell'esempio di codice MOF seguente viene illustrato come utilizzare un'origine esistente di WSH e un valore **eventId** pari a 8.</span><span class="sxs-lookup"><span data-stu-id="04c60-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  <span data-ttu-id="04c60-148">Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e definire una query per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="04c60-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="04c60-149">Nell'esempio seguente il filtro monitora la chiave del registro di sistema in cui sono registrati i programmi di avvio.</span><span class="sxs-lookup"><span data-stu-id="04c60-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="04c60-150">Il monitoraggio di questa chiave del registro di sistema può essere importante perché un programma non autorizzato è in grado di registrarsi nella chiave, che ne determina l'avvio all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="04c60-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  <span data-ttu-id="04c60-151">Identificazione di un evento per il monitoraggio e la creazione di una query di eventi.</span><span class="sxs-lookup"><span data-stu-id="04c60-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="04c60-152">È possibile verificare se esiste un evento intrinseco o estrinseco che usa.</span><span class="sxs-lookup"><span data-stu-id="04c60-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="04c60-153">Utilizzare, ad esempio, la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del provider del registro di sistema per monitorare le modifiche apportate al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="04c60-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="04c60-154">Se non esiste una classe che descrive un evento che è necessario monitorare, è necessario creare un provider di eventi personalizzato e definire nuove classi di evento estrinseche.</span><span class="sxs-lookup"><span data-stu-id="04c60-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="04c60-155">Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="04c60-156">In un file MOF è possibile definire un [*alias*](gloss-a.md) per il filtro e il consumer, che fornisce un modo semplice per descrivere i percorsi dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="04c60-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="04c60-157">Nell'esempio seguente viene illustrato come definire un [*alias*](gloss-a.md) per il filtro e il consumer.</span><span class="sxs-lookup"><span data-stu-id="04c60-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="04c60-158">Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro e le classi consumer.</span><span class="sxs-lookup"><span data-stu-id="04c60-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="04c60-159">Questa istanza determina che quando si verifica un evento che corrisponde al filtro specificato, è necessario che venga eseguita l'azione specificata dal consumer.</span><span class="sxs-lookup"><span data-stu-id="04c60-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="04c60-160">[**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e **\_ \_ FilterToConsumerBinding** devono avere lo stesso ID di sicurezza (SID) singolo nella proprietà **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="04c60-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="04c60-161">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="04c60-162">Nell'esempio seguente viene illustrato come identificare un'istanza tramite il percorso dell'oggetto o come utilizzare un alias come espressione a sintassi abbreviata per il percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="04c60-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="04c60-163">Nell'esempio seguente il filtro viene associato al consumer tramite alias.</span><span class="sxs-lookup"><span data-stu-id="04c60-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="04c60-164">È possibile associare un filtro a diversi consumer, a indicare che quando si verificano eventi corrispondenti, è necessario eseguire diverse azioni. in alternativa, è possibile associare un consumer a diversi filtri, a indicare che l'azione deve essere eseguita quando si verificano eventi che corrispondono a uno dei filtri.</span><span class="sxs-lookup"><span data-stu-id="04c60-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="04c60-165">Le azioni seguenti vengono eseguite in base alla condizione di consumer ed eventi:</span><span class="sxs-lookup"><span data-stu-id="04c60-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="04c60-166">Se uno dei consumer permanenti ha esito negativo, altri utenti che richiedono l'evento ricevono la notifica.</span><span class="sxs-lookup"><span data-stu-id="04c60-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="04c60-167">Se viene eliminato un evento, WMI genera [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="04c60-168">Se si sottoscrive questo evento, viene restituito l'evento che viene eliminato e un riferimento a [**\_ \_ EventConsumer**](--eventconsumer.md) rappresenta l'utente che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="04c60-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="04c60-169">Se un consumer ha esito negativo, WMI genera [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), che può contenere altre informazioni nelle proprietà **ErrorCode**, **ErrorDescription** e **ErrorObject** .</span><span class="sxs-lookup"><span data-stu-id="04c60-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="04c60-170">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="04c60-171">Esempio</span><span class="sxs-lookup"><span data-stu-id="04c60-171">Example</span></span>

<span data-ttu-id="04c60-172">Nell'esempio seguente viene illustrato il file MOF per un'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="04c60-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="04c60-173">Dopo la compilazione di questo MOF, qualsiasi tentativo di creare, eliminare o modificare un valore nel percorso del registro di sistema **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** registra una voce nel log eventi dell'applicazione, sotto l'origine "WSH".</span><span class="sxs-lookup"><span data-stu-id="04c60-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a><span data-ttu-id="04c60-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04c60-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c60-175">Ricezione di eventi in modo sicuro</span><span class="sxs-lookup"><span data-stu-id="04c60-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
