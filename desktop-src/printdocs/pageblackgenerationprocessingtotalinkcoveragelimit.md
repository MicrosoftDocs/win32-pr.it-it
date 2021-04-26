---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993878"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="0d787-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="0d787-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="0d787-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0d787-105">This topic is not current.</span></span> <span data-ttu-id="0d787-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0d787-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0d787-107">Specifica la somma massima consentita della copertura dei quattro input penna in qualsiasi punto di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="0d787-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="0d787-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0d787-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0d787-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0d787-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0d787-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0d787-110">Element Information</span></span>



| <span data-ttu-id="0d787-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0d787-111">Name</span></span> | <span data-ttu-id="0d787-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0d787-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="0d787-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0d787-113">Element Type</span></span> <br/>   | <span data-ttu-id="0d787-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0d787-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="0d787-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0d787-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0d787-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="0d787-116">Page</span></span><br/>                                            |
| <span data-ttu-id="0d787-117">Note</span><span class="sxs-lookup"><span data-stu-id="0d787-117">Notes</span></span> <br/>          | <span data-ttu-id="0d787-118">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="0d787-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0d787-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0d787-119">Structure Content</span></span>

<span data-ttu-id="0d787-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0d787-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0d787-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="0d787-121">Structure Properties</span></span>

<span data-ttu-id="0d787-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0d787-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0d787-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d787-123">Property</span></span>                | <span data-ttu-id="0d787-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0d787-124">xsi:type</span></span>           | <span data-ttu-id="0d787-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0d787-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0d787-126">DataType</span><span class="sxs-lookup"><span data-stu-id="0d787-126">DataType</span></span><br/>     | <span data-ttu-id="0d787-127">string</span><span class="sxs-lookup"><span data-stu-id="0d787-127">string</span></span><br/>  | <span data-ttu-id="0d787-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0d787-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="0d787-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0d787-129">DefaultValue</span></span><br/> | <span data-ttu-id="0d787-130">string</span><span class="sxs-lookup"><span data-stu-id="0d787-130">string</span></span><br/>  | <span data-ttu-id="0d787-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="0d787-131">undefined</span></span><br/>       |
| <span data-ttu-id="0d787-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0d787-132">MaxValue</span></span><br/>     | <span data-ttu-id="0d787-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="0d787-133">integer</span></span><br/> | <span data-ttu-id="0d787-134">400</span><span class="sxs-lookup"><span data-stu-id="0d787-134">400</span></span><br/>             |
| <span data-ttu-id="0d787-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="0d787-135">MinValue</span></span><br/>     | <span data-ttu-id="0d787-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="0d787-136">integer</span></span><br/> | <span data-ttu-id="0d787-137">200</span><span class="sxs-lookup"><span data-stu-id="0d787-137">200</span></span><br/>             |
| <span data-ttu-id="0d787-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="0d787-138">Multiple</span></span><br/>     | <span data-ttu-id="0d787-139">integer</span><span class="sxs-lookup"><span data-stu-id="0d787-139">integer</span></span><br/> | <span data-ttu-id="0d787-140">1</span><span class="sxs-lookup"><span data-stu-id="0d787-140">1</span></span><br/>               |
| <span data-ttu-id="0d787-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0d787-141">Mandatory</span></span><br/>    | <span data-ttu-id="0d787-142">string</span><span class="sxs-lookup"><span data-stu-id="0d787-142">string</span></span><br/>  | <span data-ttu-id="0d787-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0d787-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0d787-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="0d787-144">UnitType</span></span><br/>     | <span data-ttu-id="0d787-145">string</span><span class="sxs-lookup"><span data-stu-id="0d787-145">string</span></span><br/>  | <span data-ttu-id="0d787-146">percent</span><span class="sxs-lookup"><span data-stu-id="0d787-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0d787-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d787-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d787-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0d787-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




