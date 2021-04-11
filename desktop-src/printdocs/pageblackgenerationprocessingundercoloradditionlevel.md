---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fb6866dae4eb4a39de5c2b3b5d678a7388d703
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234583"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="f80d9-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="f80d9-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="f80d9-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f80d9-105">This topic is not current.</span></span> <span data-ttu-id="f80d9-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f80d9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f80d9-107">Descrive l'input penna cromatico (in proporzioni di componenti grigio) da aggiungere alle aree in cui GCR/UCR ha generato "BlackInkLimit" (o UCAStart, se specificato) nelle aree neutre scure e quasi neutre.</span><span class="sxs-lookup"><span data-stu-id="f80d9-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="f80d9-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f80d9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f80d9-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f80d9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f80d9-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f80d9-110">Element Information</span></span>



| <span data-ttu-id="f80d9-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f80d9-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="f80d9-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f80d9-112">Element Type</span></span> <br/>   | <span data-ttu-id="f80d9-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f80d9-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="f80d9-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="f80d9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f80d9-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="f80d9-115">Page</span></span><br/>                                            |
| <span data-ttu-id="f80d9-116">Note</span><span class="sxs-lookup"><span data-stu-id="f80d9-116">Notes</span></span> <br/>          | <span data-ttu-id="f80d9-117">Collegato a elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="f80d9-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f80d9-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f80d9-118">Structure Content</span></span>

<span data-ttu-id="f80d9-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f80d9-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f80d9-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="f80d9-120">Structure Properties</span></span>

<span data-ttu-id="f80d9-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f80d9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f80d9-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f80d9-122">Property</span></span>                | <span data-ttu-id="f80d9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f80d9-123">xsi:type</span></span>           | <span data-ttu-id="f80d9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f80d9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f80d9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f80d9-125">DataType</span></span><br/>     | <span data-ttu-id="f80d9-126">string</span><span class="sxs-lookup"><span data-stu-id="f80d9-126">string</span></span><br/>  | <span data-ttu-id="f80d9-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f80d9-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f80d9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f80d9-128">DefaultValue</span></span><br/> | <span data-ttu-id="f80d9-129">string</span><span class="sxs-lookup"><span data-stu-id="f80d9-129">string</span></span><br/>  | <span data-ttu-id="f80d9-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="f80d9-130">undefined</span></span><br/>       |
| <span data-ttu-id="f80d9-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f80d9-131">MaxValue</span></span><br/>     | <span data-ttu-id="f80d9-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="f80d9-132">integer</span></span><br/> | <span data-ttu-id="f80d9-133">100</span><span class="sxs-lookup"><span data-stu-id="f80d9-133">100</span></span><br/>             |
| <span data-ttu-id="f80d9-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f80d9-134">MinValue</span></span><br/>     | <span data-ttu-id="f80d9-135">integer</span><span class="sxs-lookup"><span data-stu-id="f80d9-135">integer</span></span><br/> | <span data-ttu-id="f80d9-136">0</span><span class="sxs-lookup"><span data-stu-id="f80d9-136">0</span></span><br/>               |
| <span data-ttu-id="f80d9-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="f80d9-137">Multiple</span></span><br/>     | <span data-ttu-id="f80d9-138">integer</span><span class="sxs-lookup"><span data-stu-id="f80d9-138">integer</span></span><br/> | <span data-ttu-id="f80d9-139">1</span><span class="sxs-lookup"><span data-stu-id="f80d9-139">1</span></span><br/>               |
| <span data-ttu-id="f80d9-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f80d9-140">Mandatory</span></span><br/>    | <span data-ttu-id="f80d9-141">string</span><span class="sxs-lookup"><span data-stu-id="f80d9-141">string</span></span><br/>  | <span data-ttu-id="f80d9-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="f80d9-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f80d9-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="f80d9-143">UnitType</span></span><br/>     | <span data-ttu-id="f80d9-144">string</span><span class="sxs-lookup"><span data-stu-id="f80d9-144">string</span></span><br/>  | <span data-ttu-id="f80d9-145">percent</span><span class="sxs-lookup"><span data-stu-id="f80d9-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f80d9-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f80d9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f80d9-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f80d9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




