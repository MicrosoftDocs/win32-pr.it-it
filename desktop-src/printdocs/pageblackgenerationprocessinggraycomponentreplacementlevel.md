---
description: Informazioni sull'elemento PageBlackGenerationProcessingGrayComponentReplacementLevel, che specifica la percentuale di sostituzione del componente grigio.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8499c8521b974d01657c171a99e86e738c82b4e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408484"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="4cca9-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="4cca9-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="4cca9-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="4cca9-104">This topic is not current.</span></span> <span data-ttu-id="4cca9-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4cca9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4cca9-106">Specifica la percentuale di sostituzione del componente grigio da eseguire.</span><span class="sxs-lookup"><span data-stu-id="4cca9-106">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="4cca9-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4cca9-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4cca9-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="4cca9-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4cca9-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4cca9-109">Element Information</span></span>



| <span data-ttu-id="4cca9-110">Nome</span><span class="sxs-lookup"><span data-stu-id="4cca9-110">Name</span></span> | <span data-ttu-id="4cca9-111">Valore</span><span class="sxs-lookup"><span data-stu-id="4cca9-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="4cca9-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="4cca9-112">Element Type</span></span> <br/>   | <span data-ttu-id="4cca9-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4cca9-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="4cca9-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="4cca9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4cca9-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="4cca9-115">Page</span></span><br/>                                            |
| <span data-ttu-id="4cca9-116">Note</span><span class="sxs-lookup"><span data-stu-id="4cca9-116">Notes</span></span> <br/>          | <span data-ttu-id="4cca9-117">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="4cca9-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4cca9-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="4cca9-118">Structure Content</span></span>

<span data-ttu-id="4cca9-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="4cca9-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="4cca9-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="4cca9-120">Structure Properties</span></span>

<span data-ttu-id="4cca9-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="4cca9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4cca9-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4cca9-122">Property</span></span>                | <span data-ttu-id="4cca9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4cca9-123">xsi:type</span></span>           | <span data-ttu-id="4cca9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4cca9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4cca9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4cca9-125">DataType</span></span><br/>     | <span data-ttu-id="4cca9-126">string</span><span class="sxs-lookup"><span data-stu-id="4cca9-126">string</span></span><br/>  | <span data-ttu-id="4cca9-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4cca9-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="4cca9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4cca9-128">DefaultValue</span></span><br/> | <span data-ttu-id="4cca9-129">string</span><span class="sxs-lookup"><span data-stu-id="4cca9-129">string</span></span><br/>  | <span data-ttu-id="4cca9-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="4cca9-130">undefined</span></span><br/>       |
| <span data-ttu-id="4cca9-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4cca9-131">MaxValue</span></span><br/>     | <span data-ttu-id="4cca9-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="4cca9-132">integer</span></span><br/> | <span data-ttu-id="4cca9-133">100</span><span class="sxs-lookup"><span data-stu-id="4cca9-133">100</span></span><br/>             |
| <span data-ttu-id="4cca9-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="4cca9-134">MinValue</span></span><br/>     | <span data-ttu-id="4cca9-135">integer</span><span class="sxs-lookup"><span data-stu-id="4cca9-135">integer</span></span><br/> | <span data-ttu-id="4cca9-136">0</span><span class="sxs-lookup"><span data-stu-id="4cca9-136">0</span></span><br/>               |
| <span data-ttu-id="4cca9-137">Multipli</span><span class="sxs-lookup"><span data-stu-id="4cca9-137">Multiple</span></span><br/>     | <span data-ttu-id="4cca9-138">integer</span><span class="sxs-lookup"><span data-stu-id="4cca9-138">integer</span></span><br/> | <span data-ttu-id="4cca9-139">1</span><span class="sxs-lookup"><span data-stu-id="4cca9-139">1</span></span><br/>               |
| <span data-ttu-id="4cca9-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="4cca9-140">Mandatory</span></span><br/>    | <span data-ttu-id="4cca9-141">string</span><span class="sxs-lookup"><span data-stu-id="4cca9-141">string</span></span><br/>  | <span data-ttu-id="4cca9-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4cca9-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4cca9-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="4cca9-143">UnitType</span></span><br/>     | <span data-ttu-id="4cca9-144">string</span><span class="sxs-lookup"><span data-stu-id="4cca9-144">string</span></span><br/>  | <span data-ttu-id="4cca9-145">percent</span><span class="sxs-lookup"><span data-stu-id="4cca9-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4cca9-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cca9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cca9-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4cca9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




