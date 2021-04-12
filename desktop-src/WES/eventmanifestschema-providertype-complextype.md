---
title: Tipo complesso ProviderType
description: Definisce un provider e i metadati utilizzati per definire gli eventi. | Tipo complesso ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Log eventi di tipo complesso ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353371"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="ae378-105">Tipo complesso ProviderType</span><span class="sxs-lookup"><span data-stu-id="ae378-105">ProviderType Complex Type</span></span>

<span data-ttu-id="ae378-106">Definisce un provider e i metadati utilizzati per definire gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae378-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ae378-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ae378-107">Child elements</span></span>



| <span data-ttu-id="ae378-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ae378-108">Element</span></span>                                                                       | <span data-ttu-id="ae378-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae378-109">Type</span></span>                                                                         | <span data-ttu-id="ae378-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae378-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae378-111">**canali**</span><span class="sxs-lookup"><span data-stu-id="ae378-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="ae378-112">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="ae378-113">Definisce un elenco di canali a cui i provider possono registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae378-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="ae378-114">**eventi**</span><span class="sxs-lookup"><span data-stu-id="ae378-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="ae378-115">**DefinitionType**</span><span class="sxs-lookup"><span data-stu-id="ae378-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="ae378-116">Definisce un elenco di definizioni di evento degli eventi che il provider è in grado di registrare.</span><span class="sxs-lookup"><span data-stu-id="ae378-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="ae378-117">**filtri**</span><span class="sxs-lookup"><span data-stu-id="ae378-117">**filters**</span></span>                                                                   | [<span data-ttu-id="ae378-118">**FilterListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="ae378-119">Definisce un elenco di filtri supportati dal provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="ae378-120">Per determinare se si vuole scrivere un evento, è possibile usare i filtri, come per le parole chiave e per il livello.</span><span class="sxs-lookup"><span data-stu-id="ae378-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="ae378-121">**Windows Server 2008 e Windows Vista:** Non supportato fino a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae378-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="ae378-122">**Parole**</span><span class="sxs-lookup"><span data-stu-id="ae378-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="ae378-123">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="ae378-124">Definisce un elenco di parole chiave che categorizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae378-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="ae378-125">**livelli**</span><span class="sxs-lookup"><span data-stu-id="ae378-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="ae378-126">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="ae378-127">Definisce un elenco di livelli che specificano la gravità di un evento.</span><span class="sxs-lookup"><span data-stu-id="ae378-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="ae378-128">**Mappe**</span><span class="sxs-lookup"><span data-stu-id="ae378-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="ae378-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="ae378-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="ae378-130">Definisce un elenco di coppie nome/valore a cui è possibile fare riferimento nella sezione modello del manifesto.</span><span class="sxs-lookup"><span data-stu-id="ae378-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="ae378-131">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="ae378-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="ae378-132">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="ae378-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="ae378-133">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ae378-133">Not used.</span></span> <span data-ttu-id="ae378-134">Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata.</span><span class="sxs-lookup"><span data-stu-id="ae378-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="ae378-135">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="ae378-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="ae378-136">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="ae378-137">Definisce un elenco di codici operativi che è possibile usare per raggruppare gli eventi all'interno di un'attività.</span><span class="sxs-lookup"><span data-stu-id="ae378-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="ae378-138">**attività**</span><span class="sxs-lookup"><span data-stu-id="ae378-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="ae378-139">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="ae378-140">Definisce un elenco di attività che possono essere utilizzate da un provider per raggruppare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae378-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="ae378-141">In genere, è possibile utilizzare le attività per raggruppare gli eventi per una funzionalità o un componente del provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="ae378-142">**modelli**</span><span class="sxs-lookup"><span data-stu-id="ae378-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="ae378-143">**TemplateListType**</span><span class="sxs-lookup"><span data-stu-id="ae378-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="ae378-144">Definisce un elenco di modelli che specificano i dati da includere con gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae378-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="ae378-145">Attributi</span><span class="sxs-lookup"><span data-stu-id="ae378-145">Attributes</span></span>



| <span data-ttu-id="ae378-146">Nome</span><span class="sxs-lookup"><span data-stu-id="ae378-146">Name</span></span>                                | <span data-ttu-id="ae378-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae378-147">Type</span></span>                                                              | <span data-ttu-id="ae378-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae378-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae378-149">guid</span><span class="sxs-lookup"><span data-stu-id="ae378-149">guid</span></span>                                | [<span data-ttu-id="ae378-150">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="ae378-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="ae378-151">GUID che identifica in modo univoco il provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ae378-152">helpLink</span><span class="sxs-lookup"><span data-stu-id="ae378-152">helpLink</span></span>                            | <span data-ttu-id="ae378-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="ae378-153">anyURI</span></span>                                                            | <span data-ttu-id="ae378-154">Il collegamento all'URL o alla Guida MS al contenuto che fornisce informazioni sugli eventi generati dal provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ae378-155">message</span><span class="sxs-lookup"><span data-stu-id="ae378-155">message</span></span>                             | [<span data-ttu-id="ae378-156">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="ae378-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="ae378-157">Nome visualizzato localizzato per il provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-157">The localized display name for the provider.</span></span> <span data-ttu-id="ae378-158">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="ae378-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ae378-159">messageFileName</span><span class="sxs-lookup"><span data-stu-id="ae378-159">messageFileName</span></span>                     | [<span data-ttu-id="ae378-160">**filePath**</span><span class="sxs-lookup"><span data-stu-id="ae378-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="ae378-161">Percorso completo del file che contiene le risorse del messaggio localizzato del provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="ae378-162">Il file può essere un file eseguibile o un file DLL.</span><span class="sxs-lookup"><span data-stu-id="ae378-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ae378-163">name</span><span class="sxs-lookup"><span data-stu-id="ae378-163">name</span></span>                                | <span data-ttu-id="ae378-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="ae378-164">anyURI</span></span>                                                            | <span data-ttu-id="ae378-165">Nome del provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-165">The name of the provider.</span></span> <span data-ttu-id="ae378-166">Il nome deve essere nel formato, componente del prodotto *aziendale* -  - .</span><span class="sxs-lookup"><span data-stu-id="ae378-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="ae378-167">Il nome non può contenere più di 255 caratteri e non può contenere i caratteri seguenti:' >',' <',' &',' "',' \| ',' \\ ',':','','?',' \* ' o caratteri con codici minori di 31.</span><span class="sxs-lookup"><span data-stu-id="ae378-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="ae378-168">Inoltre, il nome deve seguire i vincoli generali sui nomi di file e chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae378-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="ae378-169">Questi vincoli sono disponibili nella pagina relativa alla [denominazione di un file](/windows/desktop/FileIO/naming-a-file)e ai [limiti delle dimensioni degli elementi del registro di sistema](/windows/desktop/SysInfo/registry-element-size-limits).</span><span class="sxs-lookup"><span data-stu-id="ae378-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="ae378-170">parameterFileName</span><span class="sxs-lookup"><span data-stu-id="ae378-170">parameterFileName</span></span>                   | [<span data-ttu-id="ae378-171">**filePath**</span><span class="sxs-lookup"><span data-stu-id="ae378-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="ae378-172">Percorso completo del file che contiene le risorse di stringa del parametro del provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="ae378-173">Il file può essere un file eseguibile o un file DLL.</span><span class="sxs-lookup"><span data-stu-id="ae378-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="ae378-174">È possibile specificare più di un file di parametri separati da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="ae378-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="ae378-175">Viene eseguita una ricerca nel file quando la stringa del messaggio di un evento contiene una stringa di parametro.</span><span class="sxs-lookup"><span data-stu-id="ae378-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="ae378-176">I parametri consentono di fornire stringhe di inserimento localizzabili.</span><span class="sxs-lookup"><span data-stu-id="ae378-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="ae378-177">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ae378-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="ae378-178">resourceFileName</span><span class="sxs-lookup"><span data-stu-id="ae378-178">resourceFileName</span></span>                    | [<span data-ttu-id="ae378-179">**filePath**</span><span class="sxs-lookup"><span data-stu-id="ae378-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="ae378-180">Percorso completo del file che contiene le risorse di metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="ae378-181">Il file può essere un file eseguibile o un file DLL.</span><span class="sxs-lookup"><span data-stu-id="ae378-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ae378-182">source</span><span class="sxs-lookup"><span data-stu-id="ae378-182">source</span></span>                              |                                                                   | <span data-ttu-id="ae378-183">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="ae378-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ae378-184">simbolo</span><span class="sxs-lookup"><span data-stu-id="ae378-184">symbol</span></span>                              | [<span data-ttu-id="ae378-185">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="ae378-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="ae378-186">Simbolo da utilizzare per fare riferimento al GUID del provider nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ae378-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="ae378-187">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il GUID del provider nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="ae378-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ae378-188">warnOnApplicationCompatibilityError</span><span class="sxs-lookup"><span data-stu-id="ae378-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="ae378-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="ae378-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="ae378-190">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="ae378-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="ae378-191">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae378-191">Remarks</span></span>

<span data-ttu-id="ae378-192">Il Visualizzatore eventi di Windows (Eventvwr.exe) utilizzerà la stringa di messaggio localizzata, se disponibile. in caso contrario, usa la stringa dall'attributo Name.</span><span class="sxs-lookup"><span data-stu-id="ae378-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="ae378-193">I percorsi per resourceFileName, messageFileName e parameterFileName possono contenere variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="ae378-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="ae378-194">Se si definisce una nuova variabile di ambiente da usare nel percorso, è necessario riavviare il computer in modo che il servizio Registro eventi possa selezionare la nuova variabile. in caso contrario, il servizio non sarà in grado di trovare le risorse del provider.</span><span class="sxs-lookup"><span data-stu-id="ae378-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="ae378-195">Una stringa di messaggio di un evento può contenere stringhe di inserimento e stringhe di parametri.</span><span class="sxs-lookup"><span data-stu-id="ae378-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="ae378-196">Una stringa di inserimento è nel formato%*n*, dove *n* è un indice in base uno che identifica un elemento dati dal modello di dati dell'evento che si desidera inserire nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="ae378-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="ae378-197">Una stringa di parametro (vedere l'attributo **parameterFileName** ) è nel formato%%*n*, dove n è l'identificatore di un messaggio nella tabella del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ae378-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="ae378-198">Se la stringa di messaggio dell'evento contiene "%1% %11 = %2% %12" e i valori degli elementi di dati per %1 e %2 sono rispettivamente 8 e 2 e le stringhe di parametri per% %11 e% %12 erano "quarte" e "Gallon", la stringa formattata sarebbe "8 litri = 2 litri".</span><span class="sxs-lookup"><span data-stu-id="ae378-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="ae378-199">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae378-199">Requirements</span></span>



| <span data-ttu-id="ae378-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae378-200">Requirement</span></span> | <span data-ttu-id="ae378-201">Valore</span><span class="sxs-lookup"><span data-stu-id="ae378-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae378-202">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae378-202">Minimum supported client</span></span><br/> | <span data-ttu-id="ae378-203">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae378-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae378-204">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae378-204">Minimum supported server</span></span><br/> | <span data-ttu-id="ae378-205">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae378-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

