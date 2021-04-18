---
title: Tipo complesso EventDefinitionType
description: Definisce un evento che il provider è in grado di scrivere.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- Log eventi di tipo complesso EventDefinitionType
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302664"
---
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="fb091-104">Tipo complesso EventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="fb091-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="fb091-105">Definisce un evento che il provider è in grado di scrivere.</span><span class="sxs-lookup"><span data-stu-id="fb091-105">Defines an event that your provider can write.</span></span>

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="fb091-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="fb091-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb091-107">Nome</span><span class="sxs-lookup"><span data-stu-id="fb091-107">Name</span></span></th>
<th><span data-ttu-id="fb091-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb091-108">Type</span></span></th>
<th><span data-ttu-id="fb091-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb091-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb091-110">channel</span><span class="sxs-lookup"><span data-stu-id="fb091-110">channel</span></span></td>
<td><span data-ttu-id="fb091-111">token</span><span class="sxs-lookup"><span data-stu-id="fb091-111">token</span></span></td>
<td><span data-ttu-id="fb091-112">Identificatore che identifica il canale in cui viene scritto l'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="fb091-113">Specificare un identificatore di canale di uno dei canali definiti o importati.</span><span class="sxs-lookup"><span data-stu-id="fb091-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="fb091-114">Se il canale non specifica un identificatore del canale, utilizzare il nome del canale.</span><span class="sxs-lookup"><span data-stu-id="fb091-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="fb091-115">Per informazioni dettagliate sulla definizione o sull'importazione di un canale, vedere il tipo complesso <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb091-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="fb091-116">Se non si specifica un canale, l'evento non viene scritto in un canale.</span><span class="sxs-lookup"><span data-stu-id="fb091-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="fb091-117">In genere, l'unico motivo per non specificare un canale è se si scrivono eventi solo in una sessione ETW.</span><span class="sxs-lookup"><span data-stu-id="fb091-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="fb091-118">Per informazioni dettagliate, vedere Creazione di una sessione ETW, vedere <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">controllo delle sessioni di traccia eventi</a>.</span><span class="sxs-lookup"><span data-stu-id="fb091-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb091-119">keywords</span><span class="sxs-lookup"><span data-stu-id="fb091-119">keywords</span></span></td>
<td><span data-ttu-id="fb091-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb091-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="fb091-121">Elenco separato da spazi di nomi di parole chiave che identificano la categoria di eventi a cui appartiene l'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="fb091-122">Specificare il nome di una parola chiave nell'elenco di parole chiave definite.</span><span class="sxs-lookup"><span data-stu-id="fb091-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="fb091-123">Per informazioni dettagliate sulla definizione di parole chiave, vedere il tipo complesso <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb091-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="fb091-124">Se non si specificano le parole chiave, il descrittore dell'evento conterrà zero per le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="fb091-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb091-125">livello</span><span class="sxs-lookup"><span data-stu-id="fb091-125">level</span></span></td>
<td><span data-ttu-id="fb091-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="fb091-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="fb091-127">Livello di dettaglio da utilizzare durante la scrittura dell'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="fb091-128">Specificare il nome di un livello definito nel manifesto o uno dei livelli definiti nel file \Include\Winmeta.xml incluso nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fb091-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="fb091-129">Per informazioni dettagliate sulla definizione di un livello, vedere il tipo complesso <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb091-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="fb091-130">Se non si specifica un livello, il descrittore dell'evento conterrà uno zero per il livello.</span><span class="sxs-lookup"><span data-stu-id="fb091-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="fb091-131">È necessario specificare un livello se il tipo di canale in cui viene scritto l'evento è admin; il livello deve essere uno dei livelli seguenti definiti in Winmeata.xml:</span><span class="sxs-lookup"><span data-stu-id="fb091-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="fb091-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="fb091-132">win:Critical</span></span></li>
<li><span data-ttu-id="fb091-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="fb091-133">win:Error</span></span></li>
<li><span data-ttu-id="fb091-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="fb091-134">win:Warning</span></span></li>
<li><span data-ttu-id="fb091-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="fb091-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb091-136">message</span><span class="sxs-lookup"><span data-stu-id="fb091-136">message</span></span></td>
<td><span data-ttu-id="fb091-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb091-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="fb091-138">Messaggio localizzato per l'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-138">The localized message for the event.</span></span> <span data-ttu-id="fb091-139">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione <a href="eventmanifestschema-stringtable-resources-element.md"><strong>un'STRINGTABLE</strong></a> del manifesto.</span><span class="sxs-lookup"><span data-stu-id="fb091-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="fb091-140">È necessario specificare un messaggio se il tipo di canale in cui viene scritto l'evento è admin.</span><span class="sxs-lookup"><span data-stu-id="fb091-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb091-141">notLogged</span><span class="sxs-lookup"><span data-stu-id="fb091-141">notLogged</span></span></td>
<td><span data-ttu-id="fb091-142">boolean</span><span class="sxs-lookup"><span data-stu-id="fb091-142">boolean</span></span></td>
<td><span data-ttu-id="fb091-143">Determina se il provider registra questo evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="fb091-144">Specificare true se il provider registra questo evento. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="fb091-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="fb091-145">Utilizzare questo attributo per indicare che il provider non registra più questo evento anziché rimuovere l'evento dal manifesto.</span><span class="sxs-lookup"><span data-stu-id="fb091-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="fb091-146">Mantenendo l'evento nel manifesto si consente ai consumer di decodificare i file ETL precedenti che includono l'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="fb091-147"><strong>Windows Server 2008 e Windows Vista:</strong> Questo attributo non è supportato nelle versioni del compilatore di messaggi fornite prima della versione di Windows 7 del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fb091-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb091-148">codice operativo</span><span class="sxs-lookup"><span data-stu-id="fb091-148">opcode</span></span></td>
<td><span data-ttu-id="fb091-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="fb091-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="fb091-150">Nome di un codice operativo che identifica un'operazione all'interno dell'attività.</span><span class="sxs-lookup"><span data-stu-id="fb091-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="fb091-151">Specificare il nome di un codice operativo definito nel manifesto o uno dei codici operativi definiti in Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="fb091-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="fb091-152">Per informazioni dettagliate sulla definizione di un codice operativo, vedere il tipo complesso <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb091-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="fb091-153">Se l'attività a cui si fa riferimento contiene opcode specifici dell'attività (locale), è possibile specificare uno dei codici operativi specifici delle attività o un codice operativo definito a livello del provider (codice operativo globale).</span><span class="sxs-lookup"><span data-stu-id="fb091-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="fb091-154">Se si specifica un codice operativo globale, il valore del codice operativo globale non può corrispondere a uno dei codici operativi locali per l'attività.</span><span class="sxs-lookup"><span data-stu-id="fb091-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="fb091-155">Se si fa riferimento a un opcode locale, l'attributo dell'attività deve fare riferimento all'attività a cui appartiene il codice operativo locale.</span><span class="sxs-lookup"><span data-stu-id="fb091-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="fb091-156">Se non si specifica un codice operativo, il descrittore dell'evento conterrà un valore zero per OpCode.</span><span class="sxs-lookup"><span data-stu-id="fb091-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb091-157">simbolo</span><span class="sxs-lookup"><span data-stu-id="fb091-157">symbol</span></span></td>
<td><span data-ttu-id="fb091-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb091-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="fb091-159">Simbolo da utilizzare per fare riferimento al descrittore dell'evento per questo evento nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb091-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="fb091-160">Il <a href="message-compiler--mc-exe-.md"><strong>compilatore di messaggi (MC.exe)</strong></a> usa il simbolo per creare una costante per il descrittore dell'evento nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="fb091-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="fb091-161">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fb091-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="fb091-162">Usare il descrittore quando si chiama la funzione <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> per scrivere l'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb091-163">attività</span><span class="sxs-lookup"><span data-stu-id="fb091-163">task</span></span></td>
<td><span data-ttu-id="fb091-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="fb091-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="fb091-165">Nome di un'attività che identifica il componente o il sottocomponente che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="fb091-166">Consente di specificare il nome di un'attività definita nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="fb091-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="fb091-167">Per informazioni dettagliate sulla definizione di un'attività, vedere il tipo complesso <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb091-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="fb091-168">Se non si specifica un'attività, il descrittore dell'evento conterrà uno zero per l'attività.</span><span class="sxs-lookup"><span data-stu-id="fb091-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb091-169">template</span><span class="sxs-lookup"><span data-stu-id="fb091-169">template</span></span></td>
<td><span data-ttu-id="fb091-170">token</span><span class="sxs-lookup"><span data-stu-id="fb091-170">token</span></span></td>
<td><span data-ttu-id="fb091-171">Identificatore del modello che definisce gli elementi di dati inclusi in questo evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="fb091-172">Specificare l'identificatore di un modello definito nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="fb091-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="fb091-173">Per informazioni dettagliate sulla definizione di un modello, vedere il tipo complesso <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb091-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb091-174">Valore</span><span class="sxs-lookup"><span data-stu-id="fb091-174">value</span></span></td>
<td><span data-ttu-id="fb091-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb091-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="fb091-176">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-176">The event identifier.</span></span> <span data-ttu-id="fb091-177">L'identificatore deve essere univoco all'interno dell'elenco di eventi definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fb091-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb091-178">version</span><span class="sxs-lookup"><span data-stu-id="fb091-178">version</span></span></td>
<td><span data-ttu-id="fb091-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fb091-179">unsignedByte</span></span></td>
<td><span data-ttu-id="fb091-180">Numero di versione a un byte della definizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="fb091-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb091-181">Remarks</span></span>

<span data-ttu-id="fb091-182">Se si utilizza [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) per formattare la stringa di messaggio per l'evento (oppure utilizzare il Visualizzatore eventi per visualizzare la stringa di messaggio), la stringa di messaggio può contenere stringhe di inserimento e una qualsiasi delle stringhe di formato supportate dalla funzione **FormatMessage** Win32.</span><span class="sxs-lookup"><span data-stu-id="fb091-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="fb091-183">Le stringhe di inserimento sono limitate a%*n* o%*n*! s!</span><span class="sxs-lookup"><span data-stu-id="fb091-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="fb091-184">(ad esempio, %1), dove *n* è il riferimento basato su uno degli elementi di dati definiti nel modello dell'evento.</span><span class="sxs-lookup"><span data-stu-id="fb091-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="fb091-185">La stringa di messaggio può inoltre contenere stringhe di inserimento di parametri nel formato%%*n* , ad esempio% %4.</span><span class="sxs-lookup"><span data-stu-id="fb091-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="fb091-186">Il numero massimo di stringhe di inserimento che il messaggio può contenere è 100.</span><span class="sxs-lookup"><span data-stu-id="fb091-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb091-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb091-187">Requirements</span></span>



| <span data-ttu-id="fb091-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb091-188">Requirement</span></span> | <span data-ttu-id="fb091-189">Valore</span><span class="sxs-lookup"><span data-stu-id="fb091-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb091-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb091-190">Minimum supported client</span></span><br/> | <span data-ttu-id="fb091-191">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb091-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb091-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb091-192">Minimum supported server</span></span><br/> | <span data-ttu-id="fb091-193">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb091-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

