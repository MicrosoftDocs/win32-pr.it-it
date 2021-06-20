---
description: Informazioni sull'elemento PageBlackGenerationProcessingUnderColorAdditionLevel, che descrive la quantità di input penna cromatico da aggiungere alle aree con BlackInkLimit.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b496fbe890f53d1da8d1054cc5a19fe6318811
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408414"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="6c093-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="6c093-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="6c093-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6c093-104">This topic is not current.</span></span> <span data-ttu-id="6c093-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6c093-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6c093-106">Descrive la quantità di input penna cromatico (in proporzioni di componenti grigi) da aggiungere alle aree in cui GCR/UCR ha generato "BlackInkLimit" (o UCAStart, se specificato) nelle aree neutre o quasi neutre.</span><span class="sxs-lookup"><span data-stu-id="6c093-106">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="6c093-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6c093-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6c093-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="6c093-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6c093-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6c093-109">Element Information</span></span>



| <span data-ttu-id="6c093-110">Nome</span><span class="sxs-lookup"><span data-stu-id="6c093-110">Name</span></span> | <span data-ttu-id="6c093-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6c093-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="6c093-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6c093-112">Element Type</span></span> <br/>   | <span data-ttu-id="6c093-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6c093-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="6c093-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6c093-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6c093-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="6c093-115">Page</span></span><br/>                                            |
| <span data-ttu-id="6c093-116">Note</span><span class="sxs-lookup"><span data-stu-id="6c093-116">Notes</span></span> <br/>          | <span data-ttu-id="6c093-117">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="6c093-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6c093-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="6c093-118">Structure Content</span></span>

<span data-ttu-id="6c093-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6c093-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="6c093-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="6c093-120">Structure Properties</span></span>

<span data-ttu-id="6c093-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6c093-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6c093-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c093-122">Property</span></span>                | <span data-ttu-id="6c093-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6c093-123">xsi:type</span></span>           | <span data-ttu-id="6c093-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6c093-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6c093-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6c093-125">DataType</span></span><br/>     | <span data-ttu-id="6c093-126">string</span><span class="sxs-lookup"><span data-stu-id="6c093-126">string</span></span><br/>  | <span data-ttu-id="6c093-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6c093-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="6c093-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6c093-128">DefaultValue</span></span><br/> | <span data-ttu-id="6c093-129">string</span><span class="sxs-lookup"><span data-stu-id="6c093-129">string</span></span><br/>  | <span data-ttu-id="6c093-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="6c093-130">undefined</span></span><br/>       |
| <span data-ttu-id="6c093-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6c093-131">MaxValue</span></span><br/>     | <span data-ttu-id="6c093-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="6c093-132">integer</span></span><br/> | <span data-ttu-id="6c093-133">100</span><span class="sxs-lookup"><span data-stu-id="6c093-133">100</span></span><br/>             |
| <span data-ttu-id="6c093-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="6c093-134">MinValue</span></span><br/>     | <span data-ttu-id="6c093-135">integer</span><span class="sxs-lookup"><span data-stu-id="6c093-135">integer</span></span><br/> | <span data-ttu-id="6c093-136">0</span><span class="sxs-lookup"><span data-stu-id="6c093-136">0</span></span><br/>               |
| <span data-ttu-id="6c093-137">Multipli</span><span class="sxs-lookup"><span data-stu-id="6c093-137">Multiple</span></span><br/>     | <span data-ttu-id="6c093-138">integer</span><span class="sxs-lookup"><span data-stu-id="6c093-138">integer</span></span><br/> | <span data-ttu-id="6c093-139">1</span><span class="sxs-lookup"><span data-stu-id="6c093-139">1</span></span><br/>               |
| <span data-ttu-id="6c093-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6c093-140">Mandatory</span></span><br/>    | <span data-ttu-id="6c093-141">string</span><span class="sxs-lookup"><span data-stu-id="6c093-141">string</span></span><br/>  | <span data-ttu-id="6c093-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="6c093-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6c093-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="6c093-143">UnitType</span></span><br/>     | <span data-ttu-id="6c093-144">string</span><span class="sxs-lookup"><span data-stu-id="6c093-144">string</span></span><br/>  | <span data-ttu-id="6c093-145">percent</span><span class="sxs-lookup"><span data-stu-id="6c093-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6c093-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c093-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c093-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6c093-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




