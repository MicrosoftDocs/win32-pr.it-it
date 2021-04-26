---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b43d8d9ee366fc742dc3d7b1617f6297fc96e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995668"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="05df2-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="05df2-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="05df2-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="05df2-105">This topic is not current.</span></span> <span data-ttu-id="05df2-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="05df2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="05df2-107">Descrive la quantità di input penna cromatico (in proporzioni di componenti grigi) da aggiungere alle aree in cui GCR/UCR ha generato "BlackInkLimit" (o UCAStart, se specificato) nelle aree neutre o quasi neutre.</span><span class="sxs-lookup"><span data-stu-id="05df2-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="05df2-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="05df2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="05df2-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="05df2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="05df2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="05df2-110">Element Information</span></span>



| <span data-ttu-id="05df2-111">Nome</span><span class="sxs-lookup"><span data-stu-id="05df2-111">Name</span></span> | <span data-ttu-id="05df2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="05df2-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="05df2-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="05df2-113">Element Type</span></span> <br/>   | <span data-ttu-id="05df2-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="05df2-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="05df2-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="05df2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="05df2-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="05df2-116">Page</span></span><br/>                                            |
| <span data-ttu-id="05df2-117">Note</span><span class="sxs-lookup"><span data-stu-id="05df2-117">Notes</span></span> <br/>          | <span data-ttu-id="05df2-118">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="05df2-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="05df2-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="05df2-119">Structure Content</span></span>

<span data-ttu-id="05df2-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="05df2-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="05df2-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="05df2-121">Structure Properties</span></span>

<span data-ttu-id="05df2-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="05df2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="05df2-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="05df2-123">Property</span></span>                | <span data-ttu-id="05df2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="05df2-124">xsi:type</span></span>           | <span data-ttu-id="05df2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="05df2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="05df2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="05df2-126">DataType</span></span><br/>     | <span data-ttu-id="05df2-127">string</span><span class="sxs-lookup"><span data-stu-id="05df2-127">string</span></span><br/>  | <span data-ttu-id="05df2-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="05df2-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="05df2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="05df2-129">DefaultValue</span></span><br/> | <span data-ttu-id="05df2-130">string</span><span class="sxs-lookup"><span data-stu-id="05df2-130">string</span></span><br/>  | <span data-ttu-id="05df2-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="05df2-131">undefined</span></span><br/>       |
| <span data-ttu-id="05df2-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="05df2-132">MaxValue</span></span><br/>     | <span data-ttu-id="05df2-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="05df2-133">integer</span></span><br/> | <span data-ttu-id="05df2-134">100</span><span class="sxs-lookup"><span data-stu-id="05df2-134">100</span></span><br/>             |
| <span data-ttu-id="05df2-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="05df2-135">MinValue</span></span><br/>     | <span data-ttu-id="05df2-136">integer</span><span class="sxs-lookup"><span data-stu-id="05df2-136">integer</span></span><br/> | <span data-ttu-id="05df2-137">0</span><span class="sxs-lookup"><span data-stu-id="05df2-137">0</span></span><br/>               |
| <span data-ttu-id="05df2-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="05df2-138">Multiple</span></span><br/>     | <span data-ttu-id="05df2-139">integer</span><span class="sxs-lookup"><span data-stu-id="05df2-139">integer</span></span><br/> | <span data-ttu-id="05df2-140">1</span><span class="sxs-lookup"><span data-stu-id="05df2-140">1</span></span><br/>               |
| <span data-ttu-id="05df2-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="05df2-141">Mandatory</span></span><br/>    | <span data-ttu-id="05df2-142">string</span><span class="sxs-lookup"><span data-stu-id="05df2-142">string</span></span><br/>  | <span data-ttu-id="05df2-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="05df2-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="05df2-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="05df2-144">UnitType</span></span><br/>     | <span data-ttu-id="05df2-145">string</span><span class="sxs-lookup"><span data-stu-id="05df2-145">string</span></span><br/>  | <span data-ttu-id="05df2-146">percent</span><span class="sxs-lookup"><span data-stu-id="05df2-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="05df2-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05df2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05df2-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="05df2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




