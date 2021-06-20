---
description: Il parametro PageBlackGenerationProcessingGrayComponentReplacementExtent descrive l'extent oltre i neutri in colori cromatici a cui viene applicato GCR.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3bd5e4fdbafba97884a7aed608b23e4c26ce1c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408504"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="b5cf5-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="b5cf5-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="b5cf5-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-104">This topic is not current.</span></span> <span data-ttu-id="b5cf5-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b5cf5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b5cf5-106">Descrive l'estensione oltre i neutri (in colori cromatici) applicata da GCR.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-106">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="b5cf5-107">0% = Sostituzione uniforme dei componenti, 100% = Sostituzione componente grigio.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-107">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="b5cf5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b5cf5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b5cf5-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b5cf5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b5cf5-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b5cf5-110">Element Information</span></span>



| <span data-ttu-id="b5cf5-111">Nome</span><span class="sxs-lookup"><span data-stu-id="b5cf5-111">Name</span></span> | <span data-ttu-id="b5cf5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b5cf5-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="b5cf5-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b5cf5-113">Element Type</span></span> <br/>   | <span data-ttu-id="b5cf5-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b5cf5-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="b5cf5-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b5cf5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b5cf5-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="b5cf5-116">Page</span></span><br/>                                            |
| <span data-ttu-id="b5cf5-117">Note</span><span class="sxs-lookup"><span data-stu-id="b5cf5-117">Notes</span></span> <br/>          | <span data-ttu-id="b5cf5-118">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="b5cf5-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b5cf5-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b5cf5-119">Structure Content</span></span>

<span data-ttu-id="b5cf5-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b5cf5-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="b5cf5-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="b5cf5-121">Structure Properties</span></span>

<span data-ttu-id="b5cf5-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b5cf5-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5cf5-123">Property</span></span>                | <span data-ttu-id="b5cf5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b5cf5-124">xsi:type</span></span>           | <span data-ttu-id="b5cf5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b5cf5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b5cf5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b5cf5-126">DataType</span></span><br/>     | <span data-ttu-id="b5cf5-127">string</span><span class="sxs-lookup"><span data-stu-id="b5cf5-127">string</span></span><br/>  | <span data-ttu-id="b5cf5-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b5cf5-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="b5cf5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b5cf5-129">DefaultValue</span></span><br/> | <span data-ttu-id="b5cf5-130">string</span><span class="sxs-lookup"><span data-stu-id="b5cf5-130">string</span></span><br/>  | <span data-ttu-id="b5cf5-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="b5cf5-131">undefined</span></span><br/>       |
| <span data-ttu-id="b5cf5-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b5cf5-132">MaxValue</span></span><br/>     | <span data-ttu-id="b5cf5-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="b5cf5-133">integer</span></span><br/> | <span data-ttu-id="b5cf5-134">100</span><span class="sxs-lookup"><span data-stu-id="b5cf5-134">100</span></span><br/>             |
| <span data-ttu-id="b5cf5-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="b5cf5-135">MinValue</span></span><br/>     | <span data-ttu-id="b5cf5-136">integer</span><span class="sxs-lookup"><span data-stu-id="b5cf5-136">integer</span></span><br/> | <span data-ttu-id="b5cf5-137">0</span><span class="sxs-lookup"><span data-stu-id="b5cf5-137">0</span></span><br/>               |
| <span data-ttu-id="b5cf5-138">Multipli</span><span class="sxs-lookup"><span data-stu-id="b5cf5-138">Multiple</span></span><br/>     | <span data-ttu-id="b5cf5-139">integer</span><span class="sxs-lookup"><span data-stu-id="b5cf5-139">integer</span></span><br/> | <span data-ttu-id="b5cf5-140">1</span><span class="sxs-lookup"><span data-stu-id="b5cf5-140">1</span></span><br/>               |
| <span data-ttu-id="b5cf5-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b5cf5-141">Mandatory</span></span><br/>    | <span data-ttu-id="b5cf5-142">string</span><span class="sxs-lookup"><span data-stu-id="b5cf5-142">string</span></span><br/>  | <span data-ttu-id="b5cf5-143">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="b5cf5-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b5cf5-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="b5cf5-144">UnitType</span></span><br/>     | <span data-ttu-id="b5cf5-145">string</span><span class="sxs-lookup"><span data-stu-id="b5cf5-145">string</span></span><br/>  | <span data-ttu-id="b5cf5-146">percent</span><span class="sxs-lookup"><span data-stu-id="b5cf5-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b5cf5-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5cf5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5cf5-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b5cf5-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




