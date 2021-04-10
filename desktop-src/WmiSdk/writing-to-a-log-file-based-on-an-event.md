---
description: La classe LogFileEventConsumer può scrivere testo predefinito in un file di log quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Scrittura in un file di log in base a un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226931"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="20edb-104">Scrittura in un file di log in base a un evento</span><span class="sxs-lookup"><span data-stu-id="20edb-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="20edb-105">La classe [**LogFileEventConsumer**](logfileeventconsumer.md) può scrivere testo predefinito in un file di log quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="20edb-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="20edb-106">Questa classe è un consumer di eventi standard fornito da WMI.</span><span class="sxs-lookup"><span data-stu-id="20edb-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="20edb-107">La procedura di base per l'utilizzo di consumer standard è sempre la stessa ed è disponibile per il [monitoraggio e la risposta a eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="20edb-108">La procedura seguente aggiunge alla procedura di base, è specifica della classe [**LogFileEventConsumer**](logfileeventconsumer.md) e descrive come creare un consumer di eventi che esegue un programma.</span><span class="sxs-lookup"><span data-stu-id="20edb-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="20edb-109">**Per creare un consumer di eventi che scrive in un file di log**</span><span class="sxs-lookup"><span data-stu-id="20edb-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="20edb-110">Nel file Managed Object Format (MOF) creare un'istanza di [**LogFileEventConsumer**](logfileeventconsumer.md) per ricevere gli eventi richiesti nella query, assegnare un nome all'istanza nella proprietà **Name** e quindi inserire il percorso del file di log nella proprietà **filename** .</span><span class="sxs-lookup"><span data-stu-id="20edb-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="20edb-111">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="20edb-112">Consente di specificare il modello di testo da scrivere nel file di log nella proprietà Text.</span><span class="sxs-lookup"><span data-stu-id="20edb-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="20edb-113">Per ulteriori informazioni, vedere [utilizzo di modelli di stringa standard](using-standard-string-templates.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="20edb-114">Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e definire una query per specificare gli eventi che attiveranno il consumer.</span><span class="sxs-lookup"><span data-stu-id="20edb-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="20edb-115">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="20edb-116">Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**LogFileEventConsumer**](logfileeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="20edb-117">Per controllare chi legge o scrive nel file di log, impostare la sicurezza per la directory in cui si trova il registro al livello richiesto.</span><span class="sxs-lookup"><span data-stu-id="20edb-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="20edb-118">Compilare il file MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="20edb-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="20edb-119">Example</span></span>

<span data-ttu-id="20edb-120">L'esempio in questa sezione è codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="20edb-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="20edb-121">Nell'esempio viene usato il LogFileEventConsumer standard per creare una classe consumer denominata LogFileEvent che scrive una riga nel file c: \\ logfile. log quando viene creata un'istanza della classe LogFileEvent.</span><span class="sxs-lookup"><span data-stu-id="20edb-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="20edb-122">Nella procedura riportata di seguito viene descritto come utilizzare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="20edb-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="20edb-123">**Per usare l'esempio**</span><span class="sxs-lookup"><span data-stu-id="20edb-123">**To use the example**</span></span>

1.  <span data-ttu-id="20edb-124">Copiare il file MOF riportato di seguito in un file di testo e salvarlo con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="20edb-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="20edb-125">In una finestra di comando compilare il file MOF usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="20edb-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="20edb-126">**Mofcomp** *nomefile \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="20edb-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="20edb-127">Aprire logfile. log per visualizzare la riga specificata da LogFileEvent.Name: "evento del consumer di eventi di logfile".</span><span class="sxs-lookup"><span data-stu-id="20edb-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a><span data-ttu-id="20edb-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20edb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20edb-129">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="20edb-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



