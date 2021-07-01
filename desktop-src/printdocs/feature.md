---
description: Esaminare gli elementi Feature, che contengono un elenco di elementi Option e Property che descrivono un attributo del dispositivo, un'impostazione di formattazione del processo o altre caratteristiche rilevanti.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120636"
---
# <a name="feature"></a><span data-ttu-id="5ab73-103">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5ab73-103">Feature</span></span>

<span data-ttu-id="5ab73-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5ab73-104">This topic is not current.</span></span> <span data-ttu-id="5ab73-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5ab73-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ab73-106">Un elemento Feature contiene un elenco completo degli elementi Option e Property che descrivono completamente un attributo del dispositivo, un'impostazione di formattazione del processo o altre caratteristiche rilevanti.</span><span class="sxs-lookup"><span data-stu-id="5ab73-106">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5ab73-107">Tag di elemento</span><span class="sxs-lookup"><span data-stu-id="5ab73-107">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="5ab73-108">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="5ab73-108">XML Attributes</span></span>

<span data-ttu-id="5ab73-109">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="5ab73-109">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5ab73-110">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="5ab73-110">XML Attribute</span></span>   | <span data-ttu-id="5ab73-111">Dettagli</span><span class="sxs-lookup"><span data-stu-id="5ab73-111">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab73-112">name</span><span class="sxs-lookup"><span data-stu-id="5ab73-112">name</span></span><br/> | <span data-ttu-id="5ab73-113">Contiene il nome della funzionalità, una funzionalità standard o una funzionalità definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="5ab73-113">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="5ab73-114">Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="5ab73-114">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5ab73-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5ab73-115">Element Information</span></span>

<span data-ttu-id="5ab73-116">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="5ab73-116">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ab73-117">Categoria</span><span class="sxs-lookup"><span data-stu-id="5ab73-117">Category</span></span></th>
<th><span data-ttu-id="5ab73-118">Dettagli</span><span class="sxs-lookup"><span data-stu-id="5ab73-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ab73-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5ab73-119">Parent elements</span></span><br/></td>
<td><span data-ttu-id="5ab73-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="5ab73-120">PrintCapabilities</span></span> <br/> <span data-ttu-id="5ab73-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="5ab73-121">PrintTicket</span></span> <br/> <span data-ttu-id="5ab73-122">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5ab73-122">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab73-123">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5ab73-123">Child elements</span></span><br/></td>
<td><span data-ttu-id="5ab73-124">Uno dei gruppi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ab73-124">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="5ab73-125"><em>Funzionalità</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="5ab73-125"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="5ab73-126"><em>Opzione</em> (una o più)</span><span class="sxs-lookup"><span data-stu-id="5ab73-126"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="5ab73-127"><em>Proprietà</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="5ab73-127"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="5ab73-128">oppure</span><span class="sxs-lookup"><span data-stu-id="5ab73-128">or</span></span> <br/>
<ul>
<li><span data-ttu-id="5ab73-129"><em>Funzionalità</em> (una o più)</span><span class="sxs-lookup"><span data-stu-id="5ab73-129"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="5ab73-130"><em>Opzione</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="5ab73-130"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="5ab73-131"><em>Proprietà</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="5ab73-131"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab73-132">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="5ab73-132">This element</span></span><br/></td>
<td><span data-ttu-id="5ab73-133">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="5ab73-133">No character data is permitted.</span></span><br/> <span data-ttu-id="5ab73-134">Sono consentiti elementi Option figlio duplicati di pari livello.</span><span class="sxs-lookup"><span data-stu-id="5ab73-134">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="5ab73-135">Tasti di scelta rapida degli attributi nome duplicati consentiti.</span><span class="sxs-lookup"><span data-stu-id="5ab73-135">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5ab73-136">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="5ab73-136">Configuration Dependencies</span></span>

<span data-ttu-id="5ab73-137">Gli elementi di funzionalità potrebbero non avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5ab73-137">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="5ab73-138">Utilizzo degli elementi</span><span class="sxs-lookup"><span data-stu-id="5ab73-138">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="5ab73-139">Relazione con gli attributi XML</span><span class="sxs-lookup"><span data-stu-id="5ab73-139">Relationship to XML Attributes</span></span>

<span data-ttu-id="5ab73-140">Nella rappresentazione di funzionalità/opzione un attributo del dispositivo è rappresentato da un elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="5ab73-140">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="5ab73-141">L'attributo device è identificato in modo univoco dall'attributo name nell'elemento Feature dell'attributo device, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="5ab73-141">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="5ab73-142">In questo esempio l'attributo del dispositivo è Resolution.</span><span class="sxs-lookup"><span data-stu-id="5ab73-142">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="5ab73-143">Lo schema di stampa definisce un set di attributi del nome per determinate istanze di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5ab73-143">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="5ab73-144">Questi attributi di nome consentono di identificare un set di istanze di funzionalità predefinite associate a specifici attributi di dispositivo configurabili.</span><span class="sxs-lookup"><span data-stu-id="5ab73-144">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="5ab73-145">Questi nomi di istanza di funzionalità devono essere usati quando applicabile, perché aumentano la portabilità del documento PrintCapabilities e degli oggetti PrintTicket derivati da essi.</span><span class="sxs-lookup"><span data-stu-id="5ab73-145">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="5ab73-146">Le istanze di funzionalità definite privatamente possono essere introdotte se alcuni attributi del dispositivo non corrispondono a nessuna delle istanze di funzionalità definite nello schema.</span><span class="sxs-lookup"><span data-stu-id="5ab73-146">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="5ab73-147">Per informazioni sulla sintassi per gli attributi del nome e sulle convenzioni applicabili ai nomi definiti da schema e definiti privatamente, vedere [Attributi XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="5ab73-147">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="5ab73-148">Relazione con l'elemento Option</span><span class="sxs-lookup"><span data-stu-id="5ab73-148">Relationship to Option Element</span></span>

<span data-ttu-id="5ab73-149">Ognuno degli stati possibili è rappresentato da un elemento Option.</span><span class="sxs-lookup"><span data-stu-id="5ab73-149">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="5ab73-150">Ogni definizione di opzione contiene uno o più elementi ScoredProperty, che insieme descrivono o caratterizzano in modo univoco lo stato rappresentato.</span><span class="sxs-lookup"><span data-stu-id="5ab73-150">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="5ab73-151">La tecnica usata per creare le definizioni delle opzioni è descritta in [Definizioni di opzioni](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="5ab73-151">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="5ab73-152">Tutti gli elementi Option associati a un particolare elemento Feature risiedono come elementi figlio dell'elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="5ab73-152">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="5ab73-153">Funzionalità secondarie</span><span class="sxs-lookup"><span data-stu-id="5ab73-153">Subfeatures</span></span>

<span data-ttu-id="5ab73-154">Print Schema Framework consente anche di raggruppare gli elementi feature in modo gerarchico.</span><span class="sxs-lookup"><span data-stu-id="5ab73-154">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="5ab73-155">Ovvero, un elemento Feature può contenere uno o più elementi Feature figlio (sottofeature).</span><span class="sxs-lookup"><span data-stu-id="5ab73-155">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="5ab73-156">Ciò può essere utile per organizzare gli elementi feature correlati o per gli elementi Feature che controllano gli aspetti di una funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ab73-156">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="5ab73-157">Un esempio è un dispositivo che supporta la graffatura.</span><span class="sxs-lookup"><span data-stu-id="5ab73-157">One example is a device that supports stapling.</span></span> <span data-ttu-id="5ab73-158">Un dispositivo di questo tipo potrebbe offrire all'utente la possibilità di scegliere dove trovare la graffatura, ad esempio nell'angolo superiore sinistro o nell'angolo superiore destro, lungo il bordo superiore o lungo il bordo sinistro.</span><span class="sxs-lookup"><span data-stu-id="5ab73-158">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="5ab73-159">L'interfaccia utente per questo dispositivo deve essere in grado di presentare prima all'utente le scelte di livello più alto, che in questo caso è se usare la graffatura.</span><span class="sxs-lookup"><span data-stu-id="5ab73-159">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="5ab73-160">Solo dopo che l'utente ha deciso di usare la graffatura, deve presentarsi con un secondo livello di scelta, la posizione di graffatura.</span><span class="sxs-lookup"><span data-stu-id="5ab73-160">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="5ab73-161">Una gerarchia di funzionalità aggiunge la struttura aggiuntiva che rende possibile un'interfaccia utente di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="5ab73-161">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="5ab73-162">Print Schema Framework consente alle sottofeature di avere sottofeature figlio, consentendo un livello illimitato di annidamento.</span><span class="sxs-lookup"><span data-stu-id="5ab73-162">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="5ab73-163">Print Schema Framework consente anche di visualizzare gli elementi Option allo stesso livello delle sottofeature. cio, come elementi di pari livello all'interno dello stesso elemento Feature padre.</span><span class="sxs-lookup"><span data-stu-id="5ab73-163">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="5ab73-164">In questo modo l'utente può prendere la decisione di alto livello (se usare la graffatura) prima di effettuare le selezioni delle sottofeature.</span><span class="sxs-lookup"><span data-stu-id="5ab73-164">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="5ab73-165">Per questo esempio l'elemento Feature radice, "Staple", può contenere due elementi Option, "On" e "Off", nonché una sottofeature denominata "StapleLocation".</span><span class="sxs-lookup"><span data-stu-id="5ab73-165">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="5ab73-166">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ab73-166">Example</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5ab73-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ab73-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab73-168">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5ab73-168">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




