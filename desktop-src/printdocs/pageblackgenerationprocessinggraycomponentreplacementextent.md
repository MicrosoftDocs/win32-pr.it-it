---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886056"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="82627-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="82627-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="82627-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="82627-105">This topic is not current.</span></span> <span data-ttu-id="82627-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="82627-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="82627-107">Descrive la portata oltre i neutri (in colori cromatici) a cui si applica GCR.</span><span class="sxs-lookup"><span data-stu-id="82627-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="82627-108">0% = sostituzione componente uniforme, 100% = sostituzione componente grigio.</span><span class="sxs-lookup"><span data-stu-id="82627-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="82627-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="82627-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="82627-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="82627-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="82627-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="82627-111">Element Information</span></span>



| <span data-ttu-id="82627-112">Nome</span><span class="sxs-lookup"><span data-stu-id="82627-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="82627-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="82627-113">Element Type</span></span> <br/>   | <span data-ttu-id="82627-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="82627-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="82627-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="82627-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="82627-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="82627-116">Page</span></span><br/>                                            |
| <span data-ttu-id="82627-117">Note</span><span class="sxs-lookup"><span data-stu-id="82627-117">Notes</span></span> <br/>          | <span data-ttu-id="82627-118">Collegato a elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="82627-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="82627-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="82627-119">Structure Content</span></span>

<span data-ttu-id="82627-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="82627-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="82627-121">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="82627-121">Structure Properties</span></span>

<span data-ttu-id="82627-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="82627-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="82627-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82627-123">Property</span></span>                | <span data-ttu-id="82627-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="82627-124">xsi:type</span></span>           | <span data-ttu-id="82627-125">Valore</span><span class="sxs-lookup"><span data-stu-id="82627-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="82627-126">DataType</span><span class="sxs-lookup"><span data-stu-id="82627-126">DataType</span></span><br/>     | <span data-ttu-id="82627-127">string</span><span class="sxs-lookup"><span data-stu-id="82627-127">string</span></span><br/>  | <span data-ttu-id="82627-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="82627-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="82627-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="82627-129">DefaultValue</span></span><br/> | <span data-ttu-id="82627-130">string</span><span class="sxs-lookup"><span data-stu-id="82627-130">string</span></span><br/>  | <span data-ttu-id="82627-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="82627-131">undefined</span></span><br/>       |
| <span data-ttu-id="82627-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="82627-132">MaxValue</span></span><br/>     | <span data-ttu-id="82627-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="82627-133">integer</span></span><br/> | <span data-ttu-id="82627-134">100</span><span class="sxs-lookup"><span data-stu-id="82627-134">100</span></span><br/>             |
| <span data-ttu-id="82627-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="82627-135">MinValue</span></span><br/>     | <span data-ttu-id="82627-136">integer</span><span class="sxs-lookup"><span data-stu-id="82627-136">integer</span></span><br/> | <span data-ttu-id="82627-137">0</span><span class="sxs-lookup"><span data-stu-id="82627-137">0</span></span><br/>               |
| <span data-ttu-id="82627-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="82627-138">Multiple</span></span><br/>     | <span data-ttu-id="82627-139">integer</span><span class="sxs-lookup"><span data-stu-id="82627-139">integer</span></span><br/> | <span data-ttu-id="82627-140">1</span><span class="sxs-lookup"><span data-stu-id="82627-140">1</span></span><br/>               |
| <span data-ttu-id="82627-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="82627-141">Mandatory</span></span><br/>    | <span data-ttu-id="82627-142">string</span><span class="sxs-lookup"><span data-stu-id="82627-142">string</span></span><br/>  | <span data-ttu-id="82627-143">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="82627-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="82627-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="82627-144">UnitType</span></span><br/>     | <span data-ttu-id="82627-145">string</span><span class="sxs-lookup"><span data-stu-id="82627-145">string</span></span><br/>  | <span data-ttu-id="82627-146">percent</span><span class="sxs-lookup"><span data-stu-id="82627-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="82627-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82627-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82627-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="82627-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




