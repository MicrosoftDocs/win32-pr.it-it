---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997178"
---
# <a name="documentpageranges"></a><span data-ttu-id="9d3aa-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="9d3aa-104">DocumentPageRanges</span></span>

<span data-ttu-id="9d3aa-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-105">This topic is not current.</span></span> <span data-ttu-id="9d3aa-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9d3aa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d3aa-107">Descrive l'intervallo di output del documento nelle pagine.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="9d3aa-108">Il valore del parametro deve essere conforme alla struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="9d3aa-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="9d3aa-109">PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="9d3aa-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="9d3aa-110">PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="9d3aa-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="9d3aa-111">PageNumber: da 1 a N, dove N è il numero di pagine nel documento.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="9d3aa-112">Se *PageNumber >* N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="9d3aa-113">Gli spazi vuoti nella stringa devono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="9d3aa-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9d3aa-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9d3aa-115">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="9d3aa-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="9d3aa-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9d3aa-116">Element Information</span></span>



| <span data-ttu-id="9d3aa-117">Nome</span><span class="sxs-lookup"><span data-stu-id="9d3aa-117">Name</span></span> | <span data-ttu-id="9d3aa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9d3aa-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="9d3aa-119">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="9d3aa-119">Element Type</span></span> <br/>   | <span data-ttu-id="9d3aa-120">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9d3aa-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="9d3aa-121">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="9d3aa-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9d3aa-122">Documento</span><span class="sxs-lookup"><span data-stu-id="9d3aa-122">Document</span></span><br/>     |
| <span data-ttu-id="9d3aa-123">Note</span><span class="sxs-lookup"><span data-stu-id="9d3aa-123">Notes</span></span> <br/>          | <span data-ttu-id="9d3aa-124">nessuno</span><span class="sxs-lookup"><span data-stu-id="9d3aa-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="9d3aa-125">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="9d3aa-125">Structural Content</span></span>

<span data-ttu-id="9d3aa-126">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="9d3aa-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="9d3aa-127">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="9d3aa-127">Structure Properties</span></span>

<span data-ttu-id="9d3aa-128">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9d3aa-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d3aa-129">Property</span></span>                | <span data-ttu-id="9d3aa-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9d3aa-130">xsi:type</span></span>           | <span data-ttu-id="9d3aa-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9d3aa-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9d3aa-132">DataType</span><span class="sxs-lookup"><span data-stu-id="9d3aa-132">DataType</span></span><br/>     | <span data-ttu-id="9d3aa-133">string</span><span class="sxs-lookup"><span data-stu-id="9d3aa-133">string</span></span><br/>  | <span data-ttu-id="9d3aa-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3aa-134">xs:string</span></span><br/>       |
| <span data-ttu-id="9d3aa-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9d3aa-135">DefaultValue</span></span><br/> | <span data-ttu-id="9d3aa-136">string</span><span class="sxs-lookup"><span data-stu-id="9d3aa-136">string</span></span><br/>  | <span data-ttu-id="9d3aa-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="9d3aa-137">undefined</span></span><br/>       |
| <span data-ttu-id="9d3aa-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="9d3aa-138">MaxLength</span></span><br/>    | <span data-ttu-id="9d3aa-139">numero intero</span><span class="sxs-lookup"><span data-stu-id="9d3aa-139">integer</span></span><br/> | <span data-ttu-id="9d3aa-140">Non definito</span><span class="sxs-lookup"><span data-stu-id="9d3aa-140">undefined</span></span><br/>       |
| <span data-ttu-id="9d3aa-141">Minlength</span><span class="sxs-lookup"><span data-stu-id="9d3aa-141">MinLength</span></span><br/>    | <span data-ttu-id="9d3aa-142">integer</span><span class="sxs-lookup"><span data-stu-id="9d3aa-142">integer</span></span><br/> | <span data-ttu-id="9d3aa-143">1</span><span class="sxs-lookup"><span data-stu-id="9d3aa-143">1</span></span><br/>               |
| <span data-ttu-id="9d3aa-144">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9d3aa-144">Mandatory</span></span><br/>    | <span data-ttu-id="9d3aa-145">string</span><span class="sxs-lookup"><span data-stu-id="9d3aa-145">string</span></span><br/>  | <span data-ttu-id="9d3aa-146">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="9d3aa-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9d3aa-147">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="9d3aa-147">UnitType</span></span><br/>     | <span data-ttu-id="9d3aa-148">string</span><span class="sxs-lookup"><span data-stu-id="9d3aa-148">string</span></span><br/>  | <span data-ttu-id="9d3aa-149">caratteri</span><span class="sxs-lookup"><span data-stu-id="9d3aa-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="9d3aa-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d3aa-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d3aa-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9d3aa-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




