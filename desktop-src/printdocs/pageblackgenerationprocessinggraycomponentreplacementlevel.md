---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c0d55c2150f5a2299672ebf95d6656b238acc1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351886"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="1b69c-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="1b69c-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="1b69c-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1b69c-105">This topic is not current.</span></span> <span data-ttu-id="1b69c-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1b69c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1b69c-107">Specifica la percentuale di sostituzione del componente grigio da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1b69c-107">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="1b69c-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1b69c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1b69c-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1b69c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1b69c-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1b69c-110">Element Information</span></span>



| <span data-ttu-id="1b69c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="1b69c-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b69c-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1b69c-112">Element Type</span></span> <br/>   | <span data-ttu-id="1b69c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1b69c-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1b69c-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="1b69c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1b69c-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="1b69c-115">Page</span></span><br/>                                            |
| <span data-ttu-id="1b69c-116">Note</span><span class="sxs-lookup"><span data-stu-id="1b69c-116">Notes</span></span> <br/>          | <span data-ttu-id="1b69c-117">Collegato a elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="1b69c-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1b69c-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1b69c-118">Structure Content</span></span>

<span data-ttu-id="1b69c-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="1b69c-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1b69c-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="1b69c-120">Structure Properties</span></span>

<span data-ttu-id="1b69c-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1b69c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1b69c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1b69c-122">Property</span></span>                | <span data-ttu-id="1b69c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1b69c-123">xsi:type</span></span>           | <span data-ttu-id="1b69c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1b69c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1b69c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="1b69c-125">DataType</span></span><br/>     | <span data-ttu-id="1b69c-126">string</span><span class="sxs-lookup"><span data-stu-id="1b69c-126">string</span></span><br/>  | <span data-ttu-id="1b69c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1b69c-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="1b69c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1b69c-128">DefaultValue</span></span><br/> | <span data-ttu-id="1b69c-129">string</span><span class="sxs-lookup"><span data-stu-id="1b69c-129">string</span></span><br/>  | <span data-ttu-id="1b69c-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="1b69c-130">undefined</span></span><br/>       |
| <span data-ttu-id="1b69c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1b69c-131">MaxValue</span></span><br/>     | <span data-ttu-id="1b69c-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="1b69c-132">integer</span></span><br/> | <span data-ttu-id="1b69c-133">100</span><span class="sxs-lookup"><span data-stu-id="1b69c-133">100</span></span><br/>             |
| <span data-ttu-id="1b69c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="1b69c-134">MinValue</span></span><br/>     | <span data-ttu-id="1b69c-135">integer</span><span class="sxs-lookup"><span data-stu-id="1b69c-135">integer</span></span><br/> | <span data-ttu-id="1b69c-136">0</span><span class="sxs-lookup"><span data-stu-id="1b69c-136">0</span></span><br/>               |
| <span data-ttu-id="1b69c-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="1b69c-137">Multiple</span></span><br/>     | <span data-ttu-id="1b69c-138">integer</span><span class="sxs-lookup"><span data-stu-id="1b69c-138">integer</span></span><br/> | <span data-ttu-id="1b69c-139">1</span><span class="sxs-lookup"><span data-stu-id="1b69c-139">1</span></span><br/>               |
| <span data-ttu-id="1b69c-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="1b69c-140">Mandatory</span></span><br/>    | <span data-ttu-id="1b69c-141">string</span><span class="sxs-lookup"><span data-stu-id="1b69c-141">string</span></span><br/>  | <span data-ttu-id="1b69c-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="1b69c-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1b69c-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="1b69c-143">UnitType</span></span><br/>     | <span data-ttu-id="1b69c-144">string</span><span class="sxs-lookup"><span data-stu-id="1b69c-144">string</span></span><br/>  | <span data-ttu-id="1b69c-145">percent</span><span class="sxs-lookup"><span data-stu-id="1b69c-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1b69c-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b69c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b69c-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1b69c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




