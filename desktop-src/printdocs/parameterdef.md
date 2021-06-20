---
description: Informazioni sull'elemento ParameterDef, che definisce le caratteristiche valide dell'input del parametro. Il valore viene immesso tramite un elemento ParameterInit.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2682e3da11f471401e95e3f6515de5e18b6be895
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407294"
---
# <a name="parameterdef"></a><span data-ttu-id="834ac-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="834ac-104">ParameterDef</span></span>

<span data-ttu-id="834ac-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="834ac-105">This topic is not current.</span></span> <span data-ttu-id="834ac-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="834ac-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="834ac-107">Un elemento ParameterDef definisce le caratteristiche valide dell'input del parametro.</span><span class="sxs-lookup"><span data-stu-id="834ac-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="834ac-108">Il valore viene immesso tramite un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="834ac-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="834ac-109">Tag di elemento</span><span class="sxs-lookup"><span data-stu-id="834ac-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="834ac-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="834ac-110">XML Attributes</span></span>

<span data-ttu-id="834ac-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="834ac-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="834ac-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="834ac-112">XML Attribute</span></span>   | <span data-ttu-id="834ac-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="834ac-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="834ac-114">name</span><span class="sxs-lookup"><span data-stu-id="834ac-114">name</span></span><br/> | <span data-ttu-id="834ac-115">Definisce un nome univoco per il parametro nel contesto del documento corrente.</span><span class="sxs-lookup"><span data-stu-id="834ac-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="834ac-116">Gli attributi di nome ParameterDef duplicati rendono il documento PrintCapabilities non valido.</span><span class="sxs-lookup"><span data-stu-id="834ac-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="834ac-117">Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="834ac-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="834ac-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="834ac-118">Element Information</span></span>

<span data-ttu-id="834ac-119">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="834ac-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="834ac-120">Categoria</span><span class="sxs-lookup"><span data-stu-id="834ac-120">Category</span></span></th>
<th><span data-ttu-id="834ac-121">Dettagli</span><span class="sxs-lookup"><span data-stu-id="834ac-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="834ac-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="834ac-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="834ac-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="834ac-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="834ac-124">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="834ac-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="834ac-125">Property (uno o più elementi)</span><span class="sxs-lookup"><span data-stu-id="834ac-125">Property (one or more)</span></span><br/> <span data-ttu-id="834ac-126">Gli elementi Property standard seguenti devono essere visualizzati come contenuto di un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="834ac-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="834ac-127">DataType</span><span class="sxs-lookup"><span data-stu-id="834ac-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="834ac-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="834ac-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="834ac-129">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="834ac-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="834ac-130">MaxLength o MaxValue</span><span class="sxs-lookup"><span data-stu-id="834ac-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="834ac-131">MinLength o MinValue</span><span class="sxs-lookup"><span data-stu-id="834ac-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="834ac-132">Multiplo\*</span><span class="sxs-lookup"><span data-stu-id="834ac-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="834ac-133">UnitType</span><span class="sxs-lookup"><span data-stu-id="834ac-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="834ac-134">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="834ac-134">This element</span></span><br/></td>
<td><span data-ttu-id="834ac-135">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="834ac-135">No character data is permitted.</span></span><br/> <span data-ttu-id="834ac-136">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="834ac-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="834ac-137">\*Obbligatorio quando DataType è intero o decimale.</span><span class="sxs-lookup"><span data-stu-id="834ac-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="834ac-138">Facoltativo quando DataType è string.</span><span class="sxs-lookup"><span data-stu-id="834ac-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="834ac-139">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="834ac-139">Configuration Dependencies</span></span>

<span data-ttu-id="834ac-140">Un ParameterDef e il relativo contenuto a qualsiasi livello di annidamento potrebbero non avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="834ac-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="834ac-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="834ac-141">Example</span></span>

<span data-ttu-id="834ac-142">L'esempio seguente imposta tutti gli elementi Property necessari per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="834ac-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="834ac-143">L'esempio in [ParameterInit](parameterinit.md) illustra come inizializzare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="834ac-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="834ac-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="834ac-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="834ac-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="834ac-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




