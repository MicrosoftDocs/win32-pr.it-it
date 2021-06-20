---
description: Informazioni sull'elemento PageBlackGenerationProcessingGrayComponentReplacementStart, che descrive il punto in cui deve iniziare GCR.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e7e5a7e22c20b15dc373a2cce2bfe19e3417d4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408464"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="d0d95-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="d0d95-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="d0d95-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="d0d95-104">This topic is not current.</span></span> <span data-ttu-id="d0d95-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d0d95-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d0d95-106">Descrive il punto nell'intervallo "evidenziazione da ombreggiatura" in cui deve iniziare GCR (ombreggiatura più scura al 100%.)</span><span class="sxs-lookup"><span data-stu-id="d0d95-106">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="d0d95-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d0d95-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d0d95-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="d0d95-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d0d95-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d0d95-109">Element Information</span></span>



| <span data-ttu-id="d0d95-110">Nome</span><span class="sxs-lookup"><span data-stu-id="d0d95-110">Name</span></span> | <span data-ttu-id="d0d95-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d0d95-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="d0d95-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d0d95-112">Element Type</span></span> <br/>   | <span data-ttu-id="d0d95-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d0d95-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="d0d95-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="d0d95-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d0d95-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="d0d95-115">Page</span></span><br/>                                            |
| <span data-ttu-id="d0d95-116">Note</span><span class="sxs-lookup"><span data-stu-id="d0d95-116">Notes</span></span> <br/>          | <span data-ttu-id="d0d95-117">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="d0d95-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d0d95-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="d0d95-118">Structure Content</span></span>

<span data-ttu-id="d0d95-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="d0d95-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="d0d95-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="d0d95-120">Structure Properties</span></span>

<span data-ttu-id="d0d95-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="d0d95-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d0d95-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d0d95-122">Property</span></span>                | <span data-ttu-id="d0d95-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d0d95-123">xsi:type</span></span>           | <span data-ttu-id="d0d95-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d0d95-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d0d95-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d0d95-125">DataType</span></span><br/>     | <span data-ttu-id="d0d95-126">string</span><span class="sxs-lookup"><span data-stu-id="d0d95-126">string</span></span><br/>  | <span data-ttu-id="d0d95-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d0d95-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d0d95-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d0d95-128">DefaultValue</span></span><br/> | <span data-ttu-id="d0d95-129">string</span><span class="sxs-lookup"><span data-stu-id="d0d95-129">string</span></span><br/>  | <span data-ttu-id="d0d95-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="d0d95-130">undefined</span></span><br/>       |
| <span data-ttu-id="d0d95-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d0d95-131">MaxValue</span></span><br/>     | <span data-ttu-id="d0d95-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="d0d95-132">integer</span></span><br/> | <span data-ttu-id="d0d95-133">100</span><span class="sxs-lookup"><span data-stu-id="d0d95-133">100</span></span><br/>             |
| <span data-ttu-id="d0d95-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="d0d95-134">MinValue</span></span><br/>     | <span data-ttu-id="d0d95-135">integer</span><span class="sxs-lookup"><span data-stu-id="d0d95-135">integer</span></span><br/> | <span data-ttu-id="d0d95-136">0</span><span class="sxs-lookup"><span data-stu-id="d0d95-136">0</span></span><br/>               |
| <span data-ttu-id="d0d95-137">Multipli</span><span class="sxs-lookup"><span data-stu-id="d0d95-137">Multiple</span></span><br/>     | <span data-ttu-id="d0d95-138">integer</span><span class="sxs-lookup"><span data-stu-id="d0d95-138">integer</span></span><br/> | <span data-ttu-id="d0d95-139">1</span><span class="sxs-lookup"><span data-stu-id="d0d95-139">1</span></span><br/>               |
| <span data-ttu-id="d0d95-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="d0d95-140">Mandatory</span></span><br/>    | <span data-ttu-id="d0d95-141">string</span><span class="sxs-lookup"><span data-stu-id="d0d95-141">string</span></span><br/>  | <span data-ttu-id="d0d95-142">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="d0d95-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d0d95-143">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="d0d95-143">UnitType</span></span><br/>     | <span data-ttu-id="d0d95-144">string</span><span class="sxs-lookup"><span data-stu-id="d0d95-144">string</span></span><br/>  | <span data-ttu-id="d0d95-145">percent</span><span class="sxs-lookup"><span data-stu-id="d0d95-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d0d95-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0d95-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0d95-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="d0d95-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




