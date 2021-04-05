---
description: La classe NTEventLogEventConsumer scrive un messaggio nel registro eventi di Windows quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Registrazione nel registro eventi NT in base a un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883517"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="0f419-104">Registrazione nel registro eventi NT in base a un evento</span><span class="sxs-lookup"><span data-stu-id="0f419-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="0f419-105">La classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) scrive un messaggio nel registro eventi di Windows quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="0f419-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="0f419-106">Questa classe è un consumer di eventi standard fornito da WMI.</span><span class="sxs-lookup"><span data-stu-id="0f419-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="0f419-107">Per impostazione predefinita, gli utenti autenticati non possono registrare gli eventi nel registro applicazioni in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="0f419-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="0f419-108">Di conseguenza, l'esempio descritto in questo argomento avrà esito negativo se si usa la proprietà **UNCServerName** della classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) e si specifica un computer remoto come valore.</span><span class="sxs-lookup"><span data-stu-id="0f419-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="0f419-109">Per informazioni su come modificare la sicurezza del registro eventi, vedere l' [articolo della Knowledge Knowledge](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="0f419-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="0f419-110">La procedura di base per l'uso di un consumer standard è descritta in [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="0f419-111">Di seguito sono riportati passaggi aggiuntivi oltre alla procedura di base, necessari quando si usa la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="0f419-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="0f419-112">Nei passaggi viene descritto come creare un consumer di eventi che scrive nel registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f419-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="0f419-113">Nella procedura seguente viene descritto come creare un consumer di eventi che scrive nel registro eventi NT.</span><span class="sxs-lookup"><span data-stu-id="0f419-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="0f419-114">**Per creare un consumer di eventi che scrive nel registro eventi di Windows**</span><span class="sxs-lookup"><span data-stu-id="0f419-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="0f419-115">In un file di Managed Object Format (MOF) creare un'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) per ricevere gli eventi richiesti nella query.</span><span class="sxs-lookup"><span data-stu-id="0f419-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="0f419-116">Per ulteriori informazioni sulla scrittura di codice MOF, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="0f419-117">Creare, e Name, un'istanza di [**\_ \_ EventFilter**](--eventfilter.md)e quindi creare una query per specificare il tipo di evento che attiva la scrittura nel registro eventi NT.</span><span class="sxs-lookup"><span data-stu-id="0f419-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="0f419-118">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="0f419-119">Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="0f419-120">Compilare il file MOF utilizzando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="0f419-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f419-121">Example</span></span>

<span data-ttu-id="0f419-122">L'esempio in questa sezione è codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="0f419-123">Nell'esempio viene illustrato come creare un consumer per scrivere nel registro eventi dell'applicazione utilizzando [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0f419-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="0f419-124">Il file MOF crea una nuova classe denominata "NTLogCons \_ example", un filtro eventi per eseguire una query per le operazioni, ad esempio la creazione, in un'istanza di questa nuova classe e un'associazione tra filtro e consumer.</span><span class="sxs-lookup"><span data-stu-id="0f419-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="0f419-125">Poiché l'ultima azione nel file MOF consiste nel creare un'istanza dell' \_ esempio NTLogCons, è possibile visualizzare immediatamente l'evento nel registro eventi dell'applicazione eseguendo Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="0f419-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="0f419-126">`EventID=0x0A for SourceName="WinMgmt"`Identifica un messaggio con il testo seguente.</span><span class="sxs-lookup"><span data-stu-id="0f419-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="0f419-127">"%1", "%2", "%3" sono segnaposto per le stringhe corrispondenti specificate nella matrice InsertionStringTemplates.</span><span class="sxs-lookup"><span data-stu-id="0f419-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="0f419-128">Nella procedura riportata di seguito viene descritto come utilizzare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="0f419-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="0f419-129">**Per usare l'esempio**</span><span class="sxs-lookup"><span data-stu-id="0f419-129">**To use the example**</span></span>

1.  <span data-ttu-id="0f419-130">Copiare il file MOF riportato di seguito in un file di testo e salvarlo con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="0f419-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="0f419-131">In una finestra di comando compilare il file MOF usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="0f419-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="0f419-132">**Mofcomp** *nomefile \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="0f419-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="0f419-133">Eseguire Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="0f419-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="0f419-134">Esaminare il registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f419-134">Look at the Application event log.</span></span> <span data-ttu-id="0f419-135">Verrà visualizzato un evento con ID = 10 ( **eventId**), Source = "WMI" e Type = Error.</span><span class="sxs-lookup"><span data-stu-id="0f419-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="0f419-136">Fare doppio clic sul messaggio del **tipo di informazioni** da WMI con 10 nella colonna **evento** .</span><span class="sxs-lookup"><span data-stu-id="0f419-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="0f419-137">Verrà visualizzata la seguente descrizione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="0f419-137">The following description will be displayed for the event.</span></span>

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a><span data-ttu-id="0f419-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f419-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f419-139">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="0f419-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



