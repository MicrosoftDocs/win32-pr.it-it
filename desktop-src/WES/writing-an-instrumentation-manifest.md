---
title: Scrittura di un manifesto di strumentazione
description: Le applicazioni e le dll usano un manifesto di strumentazione per identificare i provider di strumentazione e gli eventi scritti dai provider.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399062"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="045e9-103">Scrittura di un manifesto di strumentazione</span><span class="sxs-lookup"><span data-stu-id="045e9-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="045e9-104">Le applicazioni e le dll usano un manifesto di strumentazione per identificare i provider di strumentazione e gli eventi scritti dai provider.</span><span class="sxs-lookup"><span data-stu-id="045e9-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="045e9-105">Un manifesto è un file XML che contiene gli elementi che identificano il provider.</span><span class="sxs-lookup"><span data-stu-id="045e9-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="045e9-106">La convenzione prevede l'uso di. Man come estensione per il manifesto.</span><span class="sxs-lookup"><span data-stu-id="045e9-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="045e9-107">Il manifesto deve essere conforme all'XSD del manifesto dell'evento.</span><span class="sxs-lookup"><span data-stu-id="045e9-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="045e9-108">Per informazioni dettagliate sullo schema, vedere [schema EventManifest](eventmanifestschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="045e9-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="045e9-109">Un provider di strumentazione è qualsiasi applicazione o DLL che chiama le funzioni [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)o [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) per scrivere eventi in una sessione di traccia di [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) o in un canale del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="045e9-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="045e9-110">Un'applicazione può definire un singolo provider di strumentazione che copre tutti gli eventi che scrive oppure può definire un provider per l'applicazione e un provider per ogni dll.</span><span class="sxs-lookup"><span data-stu-id="045e9-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="045e9-111">Il numero di provider definiti dall'applicazione nel manifesto dipende esclusivamente dal modo in cui l'applicazione desidera organizzare gli eventi che scrive.</span><span class="sxs-lookup"><span data-stu-id="045e9-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="045e9-112">Il vantaggio di specificare un provider per ogni DLL è che è quindi possibile abilitare e disabilitare i singoli provider e quindi gli eventi che generano.</span><span class="sxs-lookup"><span data-stu-id="045e9-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="045e9-113">Questo vantaggio si applica solo se il provider è abilitato da una sessione di traccia ETW.</span><span class="sxs-lookup"><span data-stu-id="045e9-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="045e9-114">Tutti gli eventi che specificano un canale del registro eventi vengono sempre scritti su tale canale.</span><span class="sxs-lookup"><span data-stu-id="045e9-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="045e9-115">Il manifesto deve identificare il provider e gli eventi che scrive, ma gli altri metadati, ad esempio canali, livelli e parole chiave, sono facoltativi. la definizione dei metadati facoltativi dipende da chi utilizzerà gli eventi.</span><span class="sxs-lookup"><span data-stu-id="045e9-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="045e9-116">Se, ad esempio, gli amministratori o il personale di supporto utilizzano gli eventi utilizzando uno strumento come il Visualizzatore eventi Windows che legge gli eventi dai canali del registro eventi, è necessario definire i canali in cui vengono scritti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="045e9-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="045e9-117">Tuttavia, se il provider viene abilitato solo da una sessione di traccia ETW, non è necessario definire i canali.</span><span class="sxs-lookup"><span data-stu-id="045e9-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="045e9-118">Sebbene i metadati di livello, attività, OpCode e parole chiave siano facoltativi, è consigliabile usarli per raggruppare o raggruppare in modo logico gli eventi.</span><span class="sxs-lookup"><span data-stu-id="045e9-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="045e9-119">Il raggruppamento degli eventi consente ai consumer di utilizzare solo gli eventi di interesse.</span><span class="sxs-lookup"><span data-stu-id="045e9-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="045e9-120">Ad esempio, il consumer può eseguire una query per tutti gli eventi in cui Level è "Critical" e la parola chiave è "Write" oppure eseguire una query per tutti gli eventi scritti da un'attività specifica.</span><span class="sxs-lookup"><span data-stu-id="045e9-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="045e9-121">Oltre ai consumer che utilizzano il livello e le parole chiave per utilizzare tipi di eventi specifici, una sessione di traccia ETW può utilizzare i metadati di livello e parola chiave per indicare a ETW di limitare gli eventi scritti nel log di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="045e9-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="045e9-122">Ad esempio, la sessione può limitare gli eventi solo agli eventi in cui il livello è "Error" o "Critical" e la parola chiave è "Read".</span><span class="sxs-lookup"><span data-stu-id="045e9-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="045e9-123">Un provider può definire i filtri utilizzati da una sessione per filtrare gli eventi in base ai dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="045e9-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="045e9-124">Con il livello e le parole chiave, ETW determina se l'evento viene scritto nel log ma con i filtri, il provider usa i criteri dei dati del filtro per determinare se scrive l'evento nella sessione.</span><span class="sxs-lookup"><span data-stu-id="045e9-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="045e9-125">I filtri sono applicabili solo quando una sessione di traccia ETW Abilita il provider.</span><span class="sxs-lookup"><span data-stu-id="045e9-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="045e9-126">Le sezioni seguenti illustrano come definire i componenti del manifesto:</span><span class="sxs-lookup"><span data-stu-id="045e9-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="045e9-127">Identificazione del provider</span><span class="sxs-lookup"><span data-stu-id="045e9-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="045e9-128">Definizione dei canali in cui vengono scritti gli eventi</span><span class="sxs-lookup"><span data-stu-id="045e9-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="045e9-129">Definizione dei livelli di gravità degli eventi scritti dal provider</span><span class="sxs-lookup"><span data-stu-id="045e9-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="045e9-130">Definizione delle attività e delle operazioni eseguite dal provider</span><span class="sxs-lookup"><span data-stu-id="045e9-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="045e9-131">Definizione delle parole chiave che classificano gli eventi scritti dal provider</span><span class="sxs-lookup"><span data-stu-id="045e9-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="045e9-132">Definizione dei filtri utilizzati dal provider per filtrare gli eventi scritti</span><span class="sxs-lookup"><span data-stu-id="045e9-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="045e9-133">Definizione delle mappe nome/valore a cui fa riferimento i dati del modello</span><span class="sxs-lookup"><span data-stu-id="045e9-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="045e9-134">Definizione dei modelli che definiscono i dati specifici dell'evento</span><span class="sxs-lookup"><span data-stu-id="045e9-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="045e9-135">Definizione degli eventi scritti dal provider</span><span class="sxs-lookup"><span data-stu-id="045e9-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="045e9-136">Sebbene sia possibile creare manualmente un manifesto di strumentazione, è consigliabile utilizzare lo strumento ECManGen.exe incluso nella \\ cartella bin del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="045e9-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="045e9-137">Lo strumento ECManGen.exe usa un'interfaccia utente grafica che guida la creazione di un manifesto da zero senza dover usare tag XML.</span><span class="sxs-lookup"><span data-stu-id="045e9-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="045e9-138">Conoscere le informazioni contenute in questa sezione e nella sezione [dello schema EventManifest](eventmanifestschema-schema.md) è utile quando si usa lo strumento.</span><span class="sxs-lookup"><span data-stu-id="045e9-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="045e9-139">Se si usa Visual Studio come editor XML, è possibile aggiungere lo schema [EventManifest](eventmanifestschema-schema.md) al progetto (vedere il menu XML) per sfruttare i vantaggi di IntelliSense, della convalida dello schema inline e di altre funzionalità per rendere la scrittura del manifesto semplice e accurata.</span><span class="sxs-lookup"><span data-stu-id="045e9-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="045e9-140">Dopo aver scritto il manifesto, usare il compilatore di messaggi per convalidare il manifesto e generare i file di risorse e di intestazione inclusi nel provider.</span><span class="sxs-lookup"><span data-stu-id="045e9-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="045e9-141">Per altre informazioni, vedere [compilazione di un manifesto di strumentazione](compiling-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="045e9-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="045e9-142">Nell'esempio seguente viene illustrata la struttura di un manifesto dell'evento completamente definito.</span><span class="sxs-lookup"><span data-stu-id="045e9-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 