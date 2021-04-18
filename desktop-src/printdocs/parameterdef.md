---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320962"
---
# <a name="parameterdef"></a><span data-ttu-id="f6c3b-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f6c3b-104">ParameterDef</span></span>

<span data-ttu-id="f6c3b-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-105">This topic is not current.</span></span> <span data-ttu-id="f6c3b-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f6c3b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f6c3b-107">Un elemento ParameterDef definisce le caratteristiche valide dell'input dei parametri.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="f6c3b-108">Il valore viene immesso per mezzo di un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="f6c3b-109">Tag elemento</span><span class="sxs-lookup"><span data-stu-id="f6c3b-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="f6c3b-110">Attributi XML</span><span class="sxs-lookup"><span data-stu-id="f6c3b-110">XML Attributes</span></span>

<span data-ttu-id="f6c3b-111">Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="f6c3b-112">Attributo XML</span><span class="sxs-lookup"><span data-stu-id="f6c3b-112">XML Attribute</span></span>   | <span data-ttu-id="f6c3b-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="f6c3b-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c3b-114">name</span><span class="sxs-lookup"><span data-stu-id="f6c3b-114">name</span></span><br/> | <span data-ttu-id="f6c3b-115">Definisce un nome univoco per il parametro nel contesto del documento corrente.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="f6c3b-116">Gli attributi del nome ParameterDef duplicato eseguono il rendering del documento PrintCapabilities non valido.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="f6c3b-117">Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c3b-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="f6c3b-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f6c3b-118">Element Information</span></span>

<span data-ttu-id="f6c3b-119">Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6c3b-120">Category</span><span class="sxs-lookup"><span data-stu-id="f6c3b-120">Category</span></span></th>
<th><span data-ttu-id="f6c3b-121">Dettagli</span><span class="sxs-lookup"><span data-stu-id="f6c3b-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6c3b-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f6c3b-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="f6c3b-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="f6c3b-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6c3b-124">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f6c3b-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="f6c3b-125">Property (uno o più elementi)</span><span class="sxs-lookup"><span data-stu-id="f6c3b-125">Property (one or more)</span></span><br/> <span data-ttu-id="f6c3b-126">Gli elementi di proprietà standard seguenti devono apparire come contenuto di un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="f6c3b-127">DataType</span><span class="sxs-lookup"><span data-stu-id="f6c3b-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="f6c3b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f6c3b-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="f6c3b-129">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f6c3b-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="f6c3b-130">MaxLength o MaxValue</span><span class="sxs-lookup"><span data-stu-id="f6c3b-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="f6c3b-131">MinLength o MinValue</span><span class="sxs-lookup"><span data-stu-id="f6c3b-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="f6c3b-132">Più</span><span class="sxs-lookup"><span data-stu-id="f6c3b-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="f6c3b-133">UnitType</span><span class="sxs-lookup"><span data-stu-id="f6c3b-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6c3b-134">Questo elemento</span><span class="sxs-lookup"><span data-stu-id="f6c3b-134">This element</span></span><br/></td>
<td><span data-ttu-id="f6c3b-135">Non sono consentiti dati di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-135">No character data is permitted.</span></span><br/> <span data-ttu-id="f6c3b-136">Gli elementi di pari livello figlio duplicati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f6c3b-137">\*Obbligatorio quando DataType è Integer o Decimal.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="f6c3b-138">Facoltativo quando DataType è una stringa.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="f6c3b-139">Dipendenze di configurazione</span><span class="sxs-lookup"><span data-stu-id="f6c3b-139">Configuration Dependencies</span></span>

<span data-ttu-id="f6c3b-140">Un ParameterDef e il relativo contenuto a qualsiasi livello di annidamento non possono avere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="f6c3b-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="f6c3b-141">Example</span></span>

<span data-ttu-id="f6c3b-142">Nell'esempio seguente vengono impostati tutti gli elementi Property necessari per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="f6c3b-143">Nell'esempio in [ParameterInit](parameterinit.md) viene illustrato come inizializzare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f6c3b-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f6c3b-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6c3b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6c3b-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f6c3b-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




