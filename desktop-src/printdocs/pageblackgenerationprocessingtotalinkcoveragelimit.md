---
description: Informazioni sull'elemento PageBlackGenerationProcessingTotalInkCoverageLimit, che specifica la somma massima consentita della copertura di quattro input penna in qualsiasi punto di un'immagine.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408444"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="69119-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="69119-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="69119-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="69119-104">This topic is not current.</span></span> <span data-ttu-id="69119-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="69119-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="69119-106">Specifica la somma massima consentita della copertura di quattro input penna in qualsiasi punto di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="69119-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="69119-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="69119-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="69119-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="69119-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="69119-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="69119-109">Element Information</span></span>



| <span data-ttu-id="69119-110">Nome</span><span class="sxs-lookup"><span data-stu-id="69119-110">Name</span></span> | <span data-ttu-id="69119-111">Valore</span><span class="sxs-lookup"><span data-stu-id="69119-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="69119-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="69119-112">Element Type</span></span> <br/>   | <span data-ttu-id="69119-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="69119-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="69119-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="69119-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="69119-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="69119-115">Page</span></span><br/>                                            |
| <span data-ttu-id="69119-116">Note</span><span class="sxs-lookup"><span data-stu-id="69119-116">Notes</span></span> <br/>          | <span data-ttu-id="69119-117">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="69119-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="69119-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="69119-118">Structure Content</span></span>

<span data-ttu-id="69119-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="69119-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="69119-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="69119-120">Structure Properties</span></span>

<span data-ttu-id="69119-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="69119-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="69119-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69119-122">Property</span></span>                | <span data-ttu-id="69119-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="69119-123">xsi:type</span></span>           | <span data-ttu-id="69119-124">Valore</span><span class="sxs-lookup"><span data-stu-id="69119-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="69119-125">DataType</span><span class="sxs-lookup"><span data-stu-id="69119-125">DataType</span></span><br/>     | <span data-ttu-id="69119-126">string</span><span class="sxs-lookup"><span data-stu-id="69119-126">string</span></span><br/>  | <span data-ttu-id="69119-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="69119-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="69119-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="69119-128">DefaultValue</span></span><br/> | <span data-ttu-id="69119-129">string</span><span class="sxs-lookup"><span data-stu-id="69119-129">string</span></span><br/>  | <span data-ttu-id="69119-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="69119-130">undefined</span></span><br/>       |
| <span data-ttu-id="69119-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="69119-131">MaxValue</span></span><br/>     | <span data-ttu-id="69119-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="69119-132">integer</span></span><br/> | <span data-ttu-id="69119-133">400</span><span class="sxs-lookup"><span data-stu-id="69119-133">400</span></span><br/>             |
| <span data-ttu-id="69119-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="69119-134">MinValue</span></span><br/>     | <span data-ttu-id="69119-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="69119-135">integer</span></span><br/> | <span data-ttu-id="69119-136">200</span><span class="sxs-lookup"><span data-stu-id="69119-136">200</span></span><br/>             |
| <span data-ttu-id="69119-137">Multipli</span><span class="sxs-lookup"><span data-stu-id="69119-137">Multiple</span></span><br/>     | <span data-ttu-id="69119-138">integer</span><span class="sxs-lookup"><span data-stu-id="69119-138">integer</span></span><br/> | <span data-ttu-id="69119-139">1</span><span class="sxs-lookup"><span data-stu-id="69119-139">1</span></span><br/>               |
| <span data-ttu-id="69119-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="69119-140">Mandatory</span></span><br/>    | <span data-ttu-id="69119-141">string</span><span class="sxs-lookup"><span data-stu-id="69119-141">string</span></span><br/>  | <span data-ttu-id="69119-142">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="69119-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="69119-143">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="69119-143">UnitType</span></span><br/>     | <span data-ttu-id="69119-144">string</span><span class="sxs-lookup"><span data-stu-id="69119-144">string</span></span><br/>  | <span data-ttu-id="69119-145">percent</span><span class="sxs-lookup"><span data-stu-id="69119-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="69119-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69119-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69119-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="69119-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




