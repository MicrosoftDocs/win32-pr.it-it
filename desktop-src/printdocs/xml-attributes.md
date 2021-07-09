---
description: Informazioni sugli attributi XML in Print Schema Framework. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Attributi XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548819"
---
# <a name="xml-attributes"></a><span data-ttu-id="a9956-105">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="a9956-105">XML Attributes</span></span>

<span data-ttu-id="a9956-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a9956-106">This topic is not current.</span></span> <span data-ttu-id="a9956-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a9956-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a9956-108">Esistono diversi attributi XML presenti in diversi tipi di elemento definiti in Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="a9956-108">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="a9956-109">Gli attributi XML con lo stesso nome hanno in genere lo stesso significato e rispettano le stesse regole indipendentemente dal tipo di elemento in cui si trovano.</span><span class="sxs-lookup"><span data-stu-id="a9956-109">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="a9956-110">Di conseguenza, gli attributi XML sono elencati qui in base al nome e non in base al tipo di elemento host.</span><span class="sxs-lookup"><span data-stu-id="a9956-110">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="a9956-111">Gli attributi XML definiti privatamente non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="a9956-111">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="a9956-112">Solo gli attributi XML definiti qui possono essere usati in un documento PrintCapabilities o printTicket e quindi solo nel contesto definito.</span><span class="sxs-lookup"><span data-stu-id="a9956-112">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="a9956-113">Sebbene le parti private non siano autorizzate a introdurre nuove definizioni nello spazio dei nomi di un'altra parte, possono usare nomi esistenti di un altro spazio dei nomi privato, purché l'uso sia coerente con l'utilizzo stabilito dall'altra parte.</span><span class="sxs-lookup"><span data-stu-id="a9956-113">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="a9956-114">Un'opzione può quindi contenere elementi ScoredProperty definiti da diverse parti, ognuna delle quali risiede in spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="a9956-114">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9956-115">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="a9956-115">Attribute Name</span></span></th>
<th><span data-ttu-id="a9956-116">Tipi di dati e valori</span><span class="sxs-lookup"><span data-stu-id="a9956-116">Data Types and Values</span></span></th>
<th><span data-ttu-id="a9956-117">Scopo</span><span class="sxs-lookup"><span data-stu-id="a9956-117">Purpose</span></span></th>
<th><span data-ttu-id="a9956-118">Note</span><span class="sxs-lookup"><span data-stu-id="a9956-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9956-119">name</span><span class="sxs-lookup"><span data-stu-id="a9956-119">name</span></span> <br/></td>
<td><span data-ttu-id="a9956-120">XML QName</span><span class="sxs-lookup"><span data-stu-id="a9956-120">XML QName</span></span><br/></td>
<td><span data-ttu-id="a9956-121">Questo attributo XML identifica l'istanza dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a9956-121">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="a9956-122">Distingue un elemento da un altro dello stesso tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="a9956-122">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="a9956-123">Questo attributo XML è così ampiamente usato che viene definito attributo name.</span><span class="sxs-lookup"><span data-stu-id="a9956-123">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="a9956-124">Le restrizioni seguenti riguardano l'attributo name.</span><span class="sxs-lookup"><span data-stu-id="a9956-124">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="a9956-125">L'attributo name deve essere nel formato di un QName definito da XML valido.</span><span class="sxs-lookup"><span data-stu-id="a9956-125">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="a9956-126">Ciò significa che deve essere qualificato da uno spazio dei nomi XML valido.</span><span class="sxs-lookup"><span data-stu-id="a9956-126">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="a9956-127">I nomi QName visualizzati come valori degli attributi del nome devono essere qualificati in modo esplicito con lo spazio dei nomi anche se è definito uno spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9956-127">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="a9956-128">Il contenuto dei caratteri deve corrispondere a quello di un QName definito da XML valido.</span><span class="sxs-lookup"><span data-stu-id="a9956-128">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="a9956-129">I nomi definiti privatamente devono essere qualificati con uno spazio dei nomi associato in modo univoco all'entità che ha introdotto l'attributo name.</span><span class="sxs-lookup"><span data-stu-id="a9956-129">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="a9956-130">Requisito di univocità di pari livello: due elementi di pari livello appartenenti allo stesso tipo di elemento non possono avere lo stesso attributo name.</span><span class="sxs-lookup"><span data-stu-id="a9956-130">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="a9956-131">L'unica eccezione sono gli elementi Option, in cui l'attributo name può essere usato per definire un'opzione.</span><span class="sxs-lookup"><span data-stu-id="a9956-131">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="a9956-132">Di conseguenza, gli elementi Option con più elementi di pari livello possono avere lo stesso attributo name.</span><span class="sxs-lookup"><span data-stu-id="a9956-132">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="a9956-133">I tipi di elemento seguenti possono contenere attributi di nome: Property, ScoredProperty, ParameterDef, Option e Feature.</span><span class="sxs-lookup"><span data-stu-id="a9956-133">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="a9956-134">Gli attributi name devono essere visualizzati in ognuno dei tipi di elemento che li contengono, tranne nel caso di alcuni elementi Print Schema Option pubblici definiti in precedenza, ad esempio DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="a9956-134">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="a9956-135">Nell'esempio seguente viene illustrato come identificare un'istanza Option usando un attributo 'name'.</span><span class="sxs-lookup"><span data-stu-id="a9956-135">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="a9956-136">Questo è il modo corretto per definire gli elementi Option.</span><span class="sxs-lookup"><span data-stu-id="a9956-136">This is the correct way to define Option elements.</span></span> <span data-ttu-id="a9956-137">Un provider non deve avere opzioni senza nome, a meno che non siano definite pubblicamente nello schema di stampa, ad esempio DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="a9956-137">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
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
<td><span data-ttu-id="a9956-138">Propagare</span><span class="sxs-lookup"><span data-stu-id="a9956-138">propagate</span></span> <br/></td>
<td><span data-ttu-id="a9956-139">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="a9956-139">Enumeration</span></span><br/> <span data-ttu-id="a9956-140">Nessun valore è attualmente definito.</span><span class="sxs-lookup"><span data-stu-id="a9956-140">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="a9956-141">L'attributo propagate non viene usato nella versione iniziale di Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="a9956-141">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="a9956-142">Questo documento è documentato in modo che il codice di convalida PrintCapabilities o PrintTicket implementato per la versione iniziale di Print Schema Framework possa elaborare qualsiasi versione successiva dello schema senza errori.</span><span class="sxs-lookup"><span data-stu-id="a9956-142">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a9956-143">Vincolata</span><span class="sxs-lookup"><span data-stu-id="a9956-143">constrained</span></span> <br/></td>
<td><span data-ttu-id="a9956-144">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="a9956-144">Enumeration</span></span><br/> <span data-ttu-id="a9956-145">Valori consentiti:</span><span class="sxs-lookup"><span data-stu-id="a9956-145">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="a9956-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a9956-146">None</span></span> <br/></li>
<li><span data-ttu-id="a9956-147">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="a9956-147">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="a9956-148">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="a9956-148">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="a9956-149">Impostazioni dispositivo</span><span class="sxs-lookup"><span data-stu-id="a9956-149">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="a9956-150">Indica se l'opzione è disponibile per la selezione o per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a9956-150">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="a9956-151">I valori consentiti dell'attributo vincolato hanno i significati seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9956-151">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="a9956-152">Si noti che questi valori sono elencati in ordine, dal meno restrittivo (Nessuno) al più restrittivo (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="a9956-152">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="a9956-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a9956-153">None</span></span> <br/>
<ul>
<li><span data-ttu-id="a9956-154">L'opzione non è vincolata.</span><span class="sxs-lookup"><span data-stu-id="a9956-154">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="a9956-155">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="a9956-155">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="a9956-156">L'opzione è vincolata dalle impostazioni di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="a9956-156">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="a9956-157">Ciò implica che la modifica della configurazione può rimuovere il vincolo.</span><span class="sxs-lookup"><span data-stu-id="a9956-157">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="a9956-158">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="a9956-158">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="a9956-159">L'opzione è vincolata dalle impostazioni dell'amministratore. L'opzione non può essere abilitata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a9956-159">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="a9956-160">Impostazioni dispositivo</span><span class="sxs-lookup"><span data-stu-id="a9956-160">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="a9956-161">L'opzione è vincolata dalle impostazioni del dispositivo o dalle opzioni del dispositivo installato fisicamente. L'opzione non può essere abilitata dall'utente o dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="a9956-161">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="a9956-162">Quando il provider PrintCapabilities segnala i valori dell'attributo vincolato, deve essere segnalato il vincolo più restrittivo trovato.</span><span class="sxs-lookup"><span data-stu-id="a9956-162">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="a9956-163">Ad esempio, se un'opzione è vincolata sia da un'impostazione dell'amministratore che da un'impostazione del dispositivo, il provider PrintCapabilities deve segnalare DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="a9956-163">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9956-164">xmlns</span><span class="sxs-lookup"><span data-stu-id="a9956-164">xmlns</span></span> <br/></td>
<td><span data-ttu-id="a9956-165">URI</span><span class="sxs-lookup"><span data-stu-id="a9956-165">URI</span></span><br/></td>
<td><span data-ttu-id="a9956-166">Questo attributo XML stabilisce un collegamento tra un URI (Uniform Resource Identifier) dello spazio dei nomi e il prefisso dello spazio dei nomi visualizzato nel QName XML.</span><span class="sxs-lookup"><span data-stu-id="a9956-166">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="a9956-167">È necessario stabilire un collegamento di questo tipo all'URI dello spazio dei nomi definito per Print Schema Framework prima di poter usare qualsiasi tag di elemento definito dal framework, attributi, attributi del nome e così via.</span><span class="sxs-lookup"><span data-stu-id="a9956-167">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="a9956-168">È possibile dichiarare questo spazio dei nomi come predefinito per evitare di qualificare effettivamente i tag degli elementi con un prefisso dello spazio dei nomi, anche se tutti gli altri QName devono essere qualificati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="a9956-168">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="a9956-169">Lo spazio dei nomi standard deve essere definito nell'elemento radice appropriato.</span><span class="sxs-lookup"><span data-stu-id="a9956-169">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="a9956-170">Osservare tutte le regole e le convenzioni XML relative all'uso dell'attributo xmlns.</span><span class="sxs-lookup"><span data-stu-id="a9956-170">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="a9956-171">L'URI per Print Schema Framework è http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="a9956-171">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="a9956-172">L'URI per le parole chiave dello schema di stampa è https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="a9956-172">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a9956-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9956-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9956-174">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a9956-174">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




