---
description: Informazioni sull'elemento DocumentPageRanges, che descrive l'intervallo di output del documento nelle pagine.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: Controlli DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409254"
---
# <a name="documentpageranges"></a><span data-ttu-id="fab8a-103">Controlli DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="fab8a-103">DocumentPageRanges</span></span>

<span data-ttu-id="fab8a-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="fab8a-104">This topic is not current.</span></span> <span data-ttu-id="fab8a-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fab8a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fab8a-106">Descrive l'intervallo di output del documento nelle pagine.</span><span class="sxs-lookup"><span data-stu-id="fab8a-106">Describes the output range of the document in pages.</span></span> <span data-ttu-id="fab8a-107">Il valore del parametro deve essere conforme alla struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="fab8a-107">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="fab8a-108">PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="fab8a-108">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="fab8a-109">PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="fab8a-109">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="fab8a-110">PageNumber: da 1 a N, dove N è il numero di pagine nel documento.</span><span class="sxs-lookup"><span data-stu-id="fab8a-110">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="fab8a-111">Se *PageNumber* > N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="fab8a-111">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="fab8a-112">Gli spazi vuoti nella stringa devono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="fab8a-112">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="fab8a-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fab8a-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fab8a-114">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="fab8a-114">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="fab8a-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fab8a-115">Element Information</span></span>



| <span data-ttu-id="fab8a-116">Nome</span><span class="sxs-lookup"><span data-stu-id="fab8a-116">Name</span></span> | <span data-ttu-id="fab8a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fab8a-117">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="fab8a-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="fab8a-118">Element Type</span></span> <br/>   | <span data-ttu-id="fab8a-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fab8a-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="fab8a-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="fab8a-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fab8a-121">Documento</span><span class="sxs-lookup"><span data-stu-id="fab8a-121">Document</span></span><br/>     |
| <span data-ttu-id="fab8a-122">Note</span><span class="sxs-lookup"><span data-stu-id="fab8a-122">Notes</span></span> <br/>          | <span data-ttu-id="fab8a-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="fab8a-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="fab8a-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="fab8a-124">Structural Content</span></span>

<span data-ttu-id="fab8a-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="fab8a-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fab8a-126">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="fab8a-126">Structure Properties</span></span>

<span data-ttu-id="fab8a-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="fab8a-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fab8a-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fab8a-128">Property</span></span>                | <span data-ttu-id="fab8a-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fab8a-129">xsi:type</span></span>           | <span data-ttu-id="fab8a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="fab8a-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fab8a-131">DataType</span><span class="sxs-lookup"><span data-stu-id="fab8a-131">DataType</span></span><br/>     | <span data-ttu-id="fab8a-132">string</span><span class="sxs-lookup"><span data-stu-id="fab8a-132">string</span></span><br/>  | <span data-ttu-id="fab8a-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="fab8a-133">xs:string</span></span><br/>       |
| <span data-ttu-id="fab8a-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fab8a-134">DefaultValue</span></span><br/> | <span data-ttu-id="fab8a-135">string</span><span class="sxs-lookup"><span data-stu-id="fab8a-135">string</span></span><br/>  | <span data-ttu-id="fab8a-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="fab8a-136">undefined</span></span><br/>       |
| <span data-ttu-id="fab8a-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fab8a-137">MaxLength</span></span><br/>    | <span data-ttu-id="fab8a-138">numero intero</span><span class="sxs-lookup"><span data-stu-id="fab8a-138">integer</span></span><br/> | <span data-ttu-id="fab8a-139">Non definito</span><span class="sxs-lookup"><span data-stu-id="fab8a-139">undefined</span></span><br/>       |
| <span data-ttu-id="fab8a-140">Minlength</span><span class="sxs-lookup"><span data-stu-id="fab8a-140">MinLength</span></span><br/>    | <span data-ttu-id="fab8a-141">integer</span><span class="sxs-lookup"><span data-stu-id="fab8a-141">integer</span></span><br/> | <span data-ttu-id="fab8a-142">1</span><span class="sxs-lookup"><span data-stu-id="fab8a-142">1</span></span><br/>               |
| <span data-ttu-id="fab8a-143">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="fab8a-143">Mandatory</span></span><br/>    | <span data-ttu-id="fab8a-144">string</span><span class="sxs-lookup"><span data-stu-id="fab8a-144">string</span></span><br/>  | <span data-ttu-id="fab8a-145">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="fab8a-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fab8a-146">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="fab8a-146">UnitType</span></span><br/>     | <span data-ttu-id="fab8a-147">string</span><span class="sxs-lookup"><span data-stu-id="fab8a-147">string</span></span><br/>  | <span data-ttu-id="fab8a-148">caratteri</span><span class="sxs-lookup"><span data-stu-id="fab8a-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fab8a-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fab8a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab8a-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="fab8a-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




