---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351806"
---
# <a name="documentpageranges"></a><span data-ttu-id="0c0b0-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="0c0b0-104">DocumentPageRanges</span></span>

<span data-ttu-id="0c0b0-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0c0b0-105">This topic is not current.</span></span> <span data-ttu-id="0c0b0-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0c0b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c0b0-107">Descrive l'intervallo di output del documento in pagine.</span><span class="sxs-lookup"><span data-stu-id="0c0b0-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="0c0b0-108">Il valore del parametro deve essere conforme alla struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="0c0b0-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="0c0b0-109">PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="0c0b0-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="0c0b0-110">PageRange: "*pageNumber*" o "*pageNumber* - *pageNumber*"</span><span class="sxs-lookup"><span data-stu-id="0c0b0-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="0c0b0-111">PageNumber: da 1 a N, dove N è il numero di pagine nel documento.</span><span class="sxs-lookup"><span data-stu-id="0c0b0-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="0c0b0-112">Se *pagenumber* > n, *pageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="0c0b0-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="0c0b0-113">Gli spazi vuoti nella stringa devono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="0c0b0-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="0c0b0-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0c0b0-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c0b0-115">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0c0b0-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="0c0b0-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0c0b0-116">Element Information</span></span>



| <span data-ttu-id="0c0b0-117">Nome</span><span class="sxs-lookup"><span data-stu-id="0c0b0-117">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="0c0b0-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0c0b0-118">Element Type</span></span> <br/>   | <span data-ttu-id="0c0b0-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0c0b0-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="0c0b0-120">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="0c0b0-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c0b0-121">Documento</span><span class="sxs-lookup"><span data-stu-id="0c0b0-121">Document</span></span><br/>     |
| <span data-ttu-id="0c0b0-122">Note</span><span class="sxs-lookup"><span data-stu-id="0c0b0-122">Notes</span></span> <br/>          | <span data-ttu-id="0c0b0-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="0c0b0-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="0c0b0-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0c0b0-124">Structural Content</span></span>

<span data-ttu-id="0c0b0-125">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="0c0b0-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0c0b0-126">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="0c0b0-126">Structure Properties</span></span>

<span data-ttu-id="0c0b0-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0c0b0-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c0b0-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c0b0-128">Property</span></span>                | <span data-ttu-id="0c0b0-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0c0b0-129">xsi:type</span></span>           | <span data-ttu-id="0c0b0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="0c0b0-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0c0b0-131">DataType</span><span class="sxs-lookup"><span data-stu-id="0c0b0-131">DataType</span></span><br/>     | <span data-ttu-id="0c0b0-132">string</span><span class="sxs-lookup"><span data-stu-id="0c0b0-132">string</span></span><br/>  | <span data-ttu-id="0c0b0-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c0b0-133">xs:string</span></span><br/>       |
| <span data-ttu-id="0c0b0-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0c0b0-134">DefaultValue</span></span><br/> | <span data-ttu-id="0c0b0-135">string</span><span class="sxs-lookup"><span data-stu-id="0c0b0-135">string</span></span><br/>  | <span data-ttu-id="0c0b0-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="0c0b0-136">undefined</span></span><br/>       |
| <span data-ttu-id="0c0b0-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0c0b0-137">MaxLength</span></span><br/>    | <span data-ttu-id="0c0b0-138">numero intero</span><span class="sxs-lookup"><span data-stu-id="0c0b0-138">integer</span></span><br/> | <span data-ttu-id="0c0b0-139">Non definito</span><span class="sxs-lookup"><span data-stu-id="0c0b0-139">undefined</span></span><br/>       |
| <span data-ttu-id="0c0b0-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="0c0b0-140">MinLength</span></span><br/>    | <span data-ttu-id="0c0b0-141">integer</span><span class="sxs-lookup"><span data-stu-id="0c0b0-141">integer</span></span><br/> | <span data-ttu-id="0c0b0-142">1</span><span class="sxs-lookup"><span data-stu-id="0c0b0-142">1</span></span><br/>               |
| <span data-ttu-id="0c0b0-143">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0c0b0-143">Mandatory</span></span><br/>    | <span data-ttu-id="0c0b0-144">string</span><span class="sxs-lookup"><span data-stu-id="0c0b0-144">string</span></span><br/>  | <span data-ttu-id="0c0b0-145">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="0c0b0-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0c0b0-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="0c0b0-146">UnitType</span></span><br/>     | <span data-ttu-id="0c0b0-147">string</span><span class="sxs-lookup"><span data-stu-id="0c0b0-147">string</span></span><br/>  | <span data-ttu-id="0c0b0-148">caratteri</span><span class="sxs-lookup"><span data-stu-id="0c0b0-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0c0b0-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c0b0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c0b0-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0c0b0-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




