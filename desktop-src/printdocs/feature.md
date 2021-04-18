---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321000"
---
# <a name="feature"></a><span data-ttu-id="be175-104">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="be175-104">Feature</span></span>

<span data-ttu-id="be175-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="be175-105">This topic is not current.</span></span> <span data-ttu-id="be175-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="be175-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="be175-107">Un elemento Feature contiene un elenco completo degli elementi option e Property che descrivono completamente un attributo del dispositivo, l'impostazione della formattazione dei processi o altre caratteristiche rilevanti.</span><span class="sxs-lookup"><span data-stu-id="be175-107">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="be175-108">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="be175-108">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="be175-109">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="be175-109">XML Attributes</span></span>

<span data-ttu-id="be175-110">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="be175-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="be175-111">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="be175-111">XML Attribute</span></span>   | <span data-ttu-id="be175-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="be175-112">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be175-113">name</span><span class="sxs-lookup"><span data-stu-id="be175-113">name</span></span><br/> | <span data-ttu-id="be175-114">Include il nome della funzionalità, ovvero una funzionalità standard o una funzionalità definita privatamente.</span><span class="sxs-lookup"><span data-stu-id="be175-114">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="be175-115">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="be175-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="be175-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="be175-116">Element Information</span></span>

<span data-ttu-id="be175-117">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="be175-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be175-118">Category</span><span class="sxs-lookup"><span data-stu-id="be175-118">Category</span></span></th>
<th><span data-ttu-id="be175-119">Dettagli</span><span class="sxs-lookup"><span data-stu-id="be175-119">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be175-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="be175-120">Parent elements</span></span><br/></td>
<td><span data-ttu-id="be175-121">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="be175-121">PrintCapabilities</span></span> <br/> <span data-ttu-id="be175-122">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="be175-122">PrintTicket</span></span> <br/> <span data-ttu-id="be175-123">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="be175-123">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be175-124">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="be175-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="be175-125">Uno dei seguenti gruppi:</span><span class="sxs-lookup"><span data-stu-id="be175-125">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="be175-126"><em>Funzionalità</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="be175-126"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="be175-127"><em>Opzione</em> (uno o più)</span><span class="sxs-lookup"><span data-stu-id="be175-127"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="be175-128"><em>Property</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="be175-128"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="be175-129">oppure</span><span class="sxs-lookup"><span data-stu-id="be175-129">or</span></span> <br/>
<ul>
<li><span data-ttu-id="be175-130"><em>Funzionalità</em> (uno o più)</span><span class="sxs-lookup"><span data-stu-id="be175-130"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="be175-131"><em>Opzione</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="be175-131"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="be175-132"><em>Property</em> (zero o più)</span><span class="sxs-lookup"><span data-stu-id="be175-132"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be175-133">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="be175-133">This element</span></span><br/></td>
<td><span data-ttu-id="be175-134">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="be175-134">No character data is permitted.</span></span><br/> <span data-ttu-id="be175-135">Sono consentiti elementi di opzioni figlio duplicati di pari livello.</span><span class="sxs-lookup"><span data-stu-id="be175-135">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="be175-136">Sono consentiti collegamenti a attributi nome duplicati.</span><span class="sxs-lookup"><span data-stu-id="be175-136">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="be175-137">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="be175-137">Configuration Dependencies</span></span>

<span data-ttu-id="be175-138">Gli elementi Feature non possono avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be175-138">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="be175-139">Utilizzo elementi</span><span class="sxs-lookup"><span data-stu-id="be175-139">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="be175-140">Relazione con attributi XML</span><span class="sxs-lookup"><span data-stu-id="be175-140">Relationship to XML Attributes</span></span>

<span data-ttu-id="be175-141">Nella rappresentazione di funzionalità/opzioni, un attributo del dispositivo è rappresentato da un elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="be175-141">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="be175-142">L'attributo Device viene identificato in modo univoco dall'attributo Name nell'elemento Feature dell'attributo Device, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="be175-142">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="be175-143">In questo esempio, l'attributo del dispositivo è Resolution.</span><span class="sxs-lookup"><span data-stu-id="be175-143">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="be175-144">Lo schema di stampa definisce un set di attributi di nome per determinate istanze di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="be175-144">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="be175-145">Questi attributi del nome servono per identificare un set di istanze di funzionalità predefinite associate a specifici attributi di dispositivo configurabili.</span><span class="sxs-lookup"><span data-stu-id="be175-145">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="be175-146">Questi nomi di istanze di funzionalità devono essere usati quando applicabile, perché aumentano la portabilità del documento PrintCapabilities e gli PrintTicket che derivano da essi.</span><span class="sxs-lookup"><span data-stu-id="be175-146">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="be175-147">È possibile che vengano introdotte istanze di funzionalità definite privatamente se alcuni attributi del dispositivo non corrispondono a nessuna delle istanze di funzionalità definite dallo schema.</span><span class="sxs-lookup"><span data-stu-id="be175-147">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="be175-148">Per informazioni sulla sintassi per gli attributi Name e sulle convenzioni applicabili ai nomi definiti dallo schema e privati, vedere [attributi XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="be175-148">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="be175-149">Relazione con elemento option</span><span class="sxs-lookup"><span data-stu-id="be175-149">Relationship to Option Element</span></span>

<span data-ttu-id="be175-150">Ognuno degli stati possibili è rappresentato da un elemento option.</span><span class="sxs-lookup"><span data-stu-id="be175-150">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="be175-151">Ogni definizione di opzione contiene uno o più elementi ScoredProperty, che sono stati raggruppati in modo univoco o caratterizzano lo stato rappresentato.</span><span class="sxs-lookup"><span data-stu-id="be175-151">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="be175-152">La tecnica utilizzata per creare le definizioni delle opzioni è descritta in [definizioni di opzioni](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="be175-152">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="be175-153">Tutti gli elementi option associati a un particolare elemento Feature si trovano come elementi figlio dell'elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="be175-153">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="be175-154">Sottocaratteristiche</span><span class="sxs-lookup"><span data-stu-id="be175-154">Subfeatures</span></span>

<span data-ttu-id="be175-155">Il Framework dello schema di stampa consente inoltre di raggruppare gli elementi della funzionalità in modo gerarchico.</span><span class="sxs-lookup"><span data-stu-id="be175-155">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="be175-156">Ovvero un elemento feature può contenere uno o più elementi Feature figlio (sottocaratteristiche).</span><span class="sxs-lookup"><span data-stu-id="be175-156">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="be175-157">Questo può essere utile per organizzare elementi di funzionalità correlati o per elementi di funzionalità che controllano gli aspetti di una funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be175-157">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="be175-158">Un esempio è un dispositivo che supporta la graffettatura.</span><span class="sxs-lookup"><span data-stu-id="be175-158">One example is a device that supports stapling.</span></span> <span data-ttu-id="be175-159">Un dispositivo di questo tipo potrebbe offrire all'utente la possibilità di scegliere dove posizionare la graffetta, ad esempio nell'angolo superiore sinistro o nell'angolo superiore destro oppure lungo il bordo superiore oppure lungo il bordo sinistro.</span><span class="sxs-lookup"><span data-stu-id="be175-159">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="be175-160">L'interfaccia utente per questo dispositivo deve essere in grado di presentare prima l'utente con le scelte di livello più alto, che in questo caso è se usare la graffettatura.</span><span class="sxs-lookup"><span data-stu-id="be175-160">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="be175-161">Solo dopo che l'utente ha deciso di usare la pinzatura, deve essere presentato con un secondo livello di scelta, la posizione di base.</span><span class="sxs-lookup"><span data-stu-id="be175-161">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="be175-162">Una gerarchia di funzionalità aggiunge la struttura aggiuntiva che rende possibile un'interfaccia utente di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="be175-162">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="be175-163">Il Framework dello schema di stampa consente alle funzionalità secondarie di avere le proprie funzionalità secondarie figlio, consentendo così un livello illimitato di annidamento.</span><span class="sxs-lookup"><span data-stu-id="be175-163">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="be175-164">Il Framework dello schema di stampa consente inoltre di visualizzare gli elementi delle opzioni allo stesso livello delle sottocaratteristiche; ovvero come elementi di pari livello all'interno dello stesso elemento della funzionalità padre.</span><span class="sxs-lookup"><span data-stu-id="be175-164">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="be175-165">In questo modo l'utente può prendere la decisione di alto livello (se usare la graffettatura) prima di effettuare le selezioni delle sottofunzionalità.</span><span class="sxs-lookup"><span data-stu-id="be175-165">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="be175-166">Per questo esempio l'elemento della funzionalità radice, "Staples", può contenere due elementi option, "on" e "off", nonché una sottofunzionalità denominata "StapleLocation".</span><span class="sxs-lookup"><span data-stu-id="be175-166">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="be175-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="be175-167">Example</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="be175-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be175-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be175-169">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="be175-169">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




