---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Attributi XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321129"
---
# <a name="xml-attributes"></a><span data-ttu-id="faa44-104">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="faa44-104">XML Attributes</span></span>

<span data-ttu-id="faa44-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="faa44-105">This topic is not current.</span></span> <span data-ttu-id="faa44-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="faa44-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="faa44-107">Sono presenti numerosi attributi XML che vengono visualizzati in diversi tipi di elemento definiti in Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="faa44-107">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="faa44-108">Gli attributi XML con lo stesso nome in genere hanno lo stesso significato e rispettano le stesse regole indipendentemente dal tipo di elemento in cui risiedono.</span><span class="sxs-lookup"><span data-stu-id="faa44-108">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="faa44-109">Gli attributi XML sono pertanto elencati in base al nome e non al tipo di elemento host.</span><span class="sxs-lookup"><span data-stu-id="faa44-109">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="faa44-110">Gli attributi XML definiti privatamente non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="faa44-110">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="faa44-111">Solo gli attributi XML definiti in questa sezione possono essere utilizzati in un documento PrintCapabilities o in un oggetto PrintTicket, quindi solo nel contesto definito.</span><span class="sxs-lookup"><span data-stu-id="faa44-111">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="faa44-112">Sebbene le parti private non siano autorizzate a introdurre nuove definizioni nello spazio dei nomi di un'altra parte, sono consentite l'utilizzo di nomi esistenti da un altro spazio dei nomi privato, purché l'utilizzo sia coerente con l'utilizzo stabilito dall'altra parte.</span><span class="sxs-lookup"><span data-stu-id="faa44-112">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="faa44-113">Un'opzione può quindi contenere elementi ScoredProperty definiti da diverse entità, ognuno dei quali risiede in spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="faa44-113">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faa44-114">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="faa44-114">Attribute Name</span></span></th>
<th><span data-ttu-id="faa44-115">Tipi di dati e valori</span><span class="sxs-lookup"><span data-stu-id="faa44-115">Data Types and Values</span></span></th>
<th><span data-ttu-id="faa44-116">Scopo</span><span class="sxs-lookup"><span data-stu-id="faa44-116">Purpose</span></span></th>
<th><span data-ttu-id="faa44-117">Note</span><span class="sxs-lookup"><span data-stu-id="faa44-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="faa44-118">name</span><span class="sxs-lookup"><span data-stu-id="faa44-118">name</span></span> <br/></td>
<td><span data-ttu-id="faa44-119">QName XML</span><span class="sxs-lookup"><span data-stu-id="faa44-119">XML QName</span></span><br/></td>
<td><span data-ttu-id="faa44-120">Questo attributo XML identifica l'istanza dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="faa44-120">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="faa44-121">Distingue un elemento da un altro tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="faa44-121">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="faa44-122">Questo attributo XML è così ampiamente utilizzato. viene definito attributo Name.</span><span class="sxs-lookup"><span data-stu-id="faa44-122">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="faa44-123">Le restrizioni seguenti riguardano l'attributo Name.</span><span class="sxs-lookup"><span data-stu-id="faa44-123">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="faa44-124">L'attributo del nome deve essere nel formato di un QName valido definito da XML.</span><span class="sxs-lookup"><span data-stu-id="faa44-124">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="faa44-125">Ovvero deve essere qualificato da uno spazio dei nomi XML valido.</span><span class="sxs-lookup"><span data-stu-id="faa44-125">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="faa44-126">I QName visualizzati come valori degli attributi del nome devono essere qualificati in modo esplicito anche se viene definito uno spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="faa44-126">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="faa44-127">Il contenuto di tipo carattere deve essere quello di un QName valido definito da XML.</span><span class="sxs-lookup"><span data-stu-id="faa44-127">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="faa44-128">I nomi definiti privatamente devono essere qualificati con uno spazio dei nomi associato in modo univoco all'entità che ha introdotto l'attributo Name.</span><span class="sxs-lookup"><span data-stu-id="faa44-128">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="faa44-129">Requisito di univocità di pari livello: due elementi di pari livello appartenenti allo stesso tipo di elemento potrebbero avere lo stesso attributo Name.</span><span class="sxs-lookup"><span data-stu-id="faa44-129">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="faa44-130">L'unica eccezione è costituita dagli elementi option, in cui l'attributo Name può essere usato per definire un'opzione.</span><span class="sxs-lookup"><span data-stu-id="faa44-130">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="faa44-131">Di conseguenza, gli elementi di opzioni con più elementi di pari livello possono avere lo stesso attributo Name.</span><span class="sxs-lookup"><span data-stu-id="faa44-131">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="faa44-132">I tipi di elementi seguenti possono contenere attributi di nome: Property, ScoredProperty, ParameterDef, Option e feature.</span><span class="sxs-lookup"><span data-stu-id="faa44-132">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="faa44-133">gli attributi di nome devono essere visualizzati in ognuno dei tipi di elemento che li contengono, tranne nel caso di alcuni elementi di opzioni dello schema di stampa pubblico definiti in precedenza, ad esempio DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="faa44-133">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="faa44-134">Nell'esempio seguente viene illustrato come identificare un'istanza di opzione utilizzando un attributo ' name '.</span><span class="sxs-lookup"><span data-stu-id="faa44-134">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="faa44-135">Questo è il modo corretto per definire gli elementi delle opzioni.</span><span class="sxs-lookup"><span data-stu-id="faa44-135">This is the correct way to define Option elements.</span></span> <span data-ttu-id="faa44-136">Un provider non deve avere opzioni senza nome, a meno che non siano definite pubblicamente nello schema di stampa, ad esempio DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="faa44-136">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faa44-137">propagare</span><span class="sxs-lookup"><span data-stu-id="faa44-137">propagate</span></span> <br/></td>
<td><span data-ttu-id="faa44-138">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="faa44-138">Enumeration</span></span><br/> <span data-ttu-id="faa44-139">Nessun valore attualmente definito.</span><span class="sxs-lookup"><span data-stu-id="faa44-139">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="faa44-140">L'attributo propagate non viene utilizzato nella versione iniziale di Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="faa44-140">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="faa44-141">Questo argomento è documentato in modo che il codice di convalida PrintCapabilities o PrintTicket implementato per la versione iniziale di Print Schema Framework possa elaborare le versioni dello schema successive senza errori.</span><span class="sxs-lookup"><span data-stu-id="faa44-141">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="faa44-142">vincolata</span><span class="sxs-lookup"><span data-stu-id="faa44-142">constrained</span></span> <br/></td>
<td><span data-ttu-id="faa44-143">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="faa44-143">Enumeration</span></span><br/> <span data-ttu-id="faa44-144">Valori consentiti:</span><span class="sxs-lookup"><span data-stu-id="faa44-144">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="faa44-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="faa44-145">None</span></span> <br/></li>
<li><span data-ttu-id="faa44-146">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="faa44-146">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="faa44-147">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="faa44-147">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="faa44-148">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="faa44-148">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="faa44-149">Indica se l'opzione è disponibile per la selezione o per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="faa44-149">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="faa44-150">I valori consentiti dell'attributo vincolato hanno i significati seguenti.</span><span class="sxs-lookup"><span data-stu-id="faa44-150">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="faa44-151">Si noti che questi valori sono elencati nell'ordine, dal meno restrittivo (nessuno) al più restrittivo (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="faa44-151">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="faa44-152">nessuno</span><span class="sxs-lookup"><span data-stu-id="faa44-152">None</span></span> <br/>
<ul>
<li><span data-ttu-id="faa44-153">L'opzione non è vincolata.</span><span class="sxs-lookup"><span data-stu-id="faa44-153">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="faa44-154">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="faa44-154">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="faa44-155">L'opzione è vincolata dalle impostazioni PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="faa44-155">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="faa44-156">Ciò implica che la modifica della configurazione può rimuovere il vincolo.</span><span class="sxs-lookup"><span data-stu-id="faa44-156">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="faa44-157">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="faa44-157">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="faa44-158">L'opzione è vincolata dalle impostazioni dell'amministratore. l'opzione non può essere abilitata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="faa44-158">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="faa44-159">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="faa44-159">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="faa44-160">L'opzione è vincolata dalle impostazioni del dispositivo o dalle opzioni del dispositivo fisicamente installate; l'opzione non può essere abilitata dall'utente o dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="faa44-160">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="faa44-161">Quando il provider PrintCapabilities segnala i valori dell'attributo vincolato, il vincolo più restrittivo rilevato deve essere segnalato.</span><span class="sxs-lookup"><span data-stu-id="faa44-161">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="faa44-162">Se, ad esempio, un'opzione è vincolata sia da un'impostazione di amministratore che da un'impostazione del dispositivo, il provider PrintCapabilities deve segnalare DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="faa44-162">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faa44-163">xmlns</span><span class="sxs-lookup"><span data-stu-id="faa44-163">xmlns</span></span> <br/></td>
<td><span data-ttu-id="faa44-164">URI</span><span class="sxs-lookup"><span data-stu-id="faa44-164">URI</span></span><br/></td>
<td><span data-ttu-id="faa44-165">Questo attributo XML stabilisce un collegamento tra un URI (Uniform Resource Identifier) dello spazio dei nomi e il prefisso dello spazio dei nomi visualizzato nel QName XML.</span><span class="sxs-lookup"><span data-stu-id="faa44-165">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="faa44-166">È necessario stabilire un collegamento di questo tipo all'URI dello spazio dei nomi definito per il Framework dello schema di stampa prima di poter utilizzare i tag degli elementi definiti dal Framework, gli attributi, gli attributi del nome e così via.</span><span class="sxs-lookup"><span data-stu-id="faa44-166">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="faa44-167">È possibile dichiarare questo spazio dei nomi come predefinito per evitare di qualificare effettivamente i tag dell'elemento con un prefisso dello spazio dei nomi, anche se tutti gli altri QName devono essere qualificati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="faa44-167">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="faa44-168">Lo spazio dei nomi standard deve essere definito nell'elemento radice appropriato.</span><span class="sxs-lookup"><span data-stu-id="faa44-168">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="faa44-169">Osservare tutte le regole e le convenzioni XML relative all'utilizzo dell'attributo xmlns.</span><span class="sxs-lookup"><span data-stu-id="faa44-169">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="faa44-170">L'URI per il Framework di Stampa schema è http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="faa44-170">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="faa44-171">L'URI per le parole chiave di Print Schema è https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="faa44-171">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="faa44-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="faa44-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faa44-173">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="faa44-173">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




