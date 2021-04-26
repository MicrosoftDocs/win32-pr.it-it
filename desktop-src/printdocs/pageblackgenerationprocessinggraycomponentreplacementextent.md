---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9a790d66d1f7806a7ef86ee4a85f62225aa836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997708"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="f3fb4-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="f3fb4-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="f3fb4-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f3fb4-105">This topic is not current.</span></span> <span data-ttu-id="f3fb4-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f3fb4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f3fb4-107">Descrive l'estensione oltre i neutri (in colori cromatici) applicata da GCR.</span><span class="sxs-lookup"><span data-stu-id="f3fb4-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="f3fb4-108">0% = sostituzione uniforme del componente, 100% = sostituzione di componenti grigi.</span><span class="sxs-lookup"><span data-stu-id="f3fb4-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="f3fb4-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3fb4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f3fb4-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f3fb4-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f3fb4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3fb4-111">Element Information</span></span>



| <span data-ttu-id="f3fb4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f3fb4-112">Name</span></span> | <span data-ttu-id="f3fb4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f3fb4-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="f3fb4-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f3fb4-114">Element Type</span></span> <br/>   | <span data-ttu-id="f3fb4-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f3fb4-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="f3fb4-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f3fb4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f3fb4-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="f3fb4-117">Page</span></span><br/>                                            |
| <span data-ttu-id="f3fb4-118">Note</span><span class="sxs-lookup"><span data-stu-id="f3fb4-118">Notes</span></span> <br/>          | <span data-ttu-id="f3fb4-119">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="f3fb4-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f3fb4-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f3fb4-120">Structure Content</span></span>

<span data-ttu-id="f3fb4-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f3fb4-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f3fb4-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="f3fb4-122">Structure Properties</span></span>

<span data-ttu-id="f3fb4-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f3fb4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f3fb4-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3fb4-124">Property</span></span>                | <span data-ttu-id="f3fb4-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f3fb4-125">xsi:type</span></span>           | <span data-ttu-id="f3fb4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f3fb4-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f3fb4-127">DataType</span><span class="sxs-lookup"><span data-stu-id="f3fb4-127">DataType</span></span><br/>     | <span data-ttu-id="f3fb4-128">string</span><span class="sxs-lookup"><span data-stu-id="f3fb4-128">string</span></span><br/>  | <span data-ttu-id="f3fb4-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f3fb4-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="f3fb4-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f3fb4-130">DefaultValue</span></span><br/> | <span data-ttu-id="f3fb4-131">string</span><span class="sxs-lookup"><span data-stu-id="f3fb4-131">string</span></span><br/>  | <span data-ttu-id="f3fb4-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="f3fb4-132">undefined</span></span><br/>       |
| <span data-ttu-id="f3fb4-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f3fb4-133">MaxValue</span></span><br/>     | <span data-ttu-id="f3fb4-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3fb4-134">integer</span></span><br/> | <span data-ttu-id="f3fb4-135">100</span><span class="sxs-lookup"><span data-stu-id="f3fb4-135">100</span></span><br/>             |
| <span data-ttu-id="f3fb4-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="f3fb4-136">MinValue</span></span><br/>     | <span data-ttu-id="f3fb4-137">integer</span><span class="sxs-lookup"><span data-stu-id="f3fb4-137">integer</span></span><br/> | <span data-ttu-id="f3fb4-138">0</span><span class="sxs-lookup"><span data-stu-id="f3fb4-138">0</span></span><br/>               |
| <span data-ttu-id="f3fb4-139">Più elementi</span><span class="sxs-lookup"><span data-stu-id="f3fb4-139">Multiple</span></span><br/>     | <span data-ttu-id="f3fb4-140">integer</span><span class="sxs-lookup"><span data-stu-id="f3fb4-140">integer</span></span><br/> | <span data-ttu-id="f3fb4-141">1</span><span class="sxs-lookup"><span data-stu-id="f3fb4-141">1</span></span><br/>               |
| <span data-ttu-id="f3fb4-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f3fb4-142">Mandatory</span></span><br/>    | <span data-ttu-id="f3fb4-143">string</span><span class="sxs-lookup"><span data-stu-id="f3fb4-143">string</span></span><br/>  | <span data-ttu-id="f3fb4-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="f3fb4-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f3fb4-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="f3fb4-145">UnitType</span></span><br/>     | <span data-ttu-id="f3fb4-146">string</span><span class="sxs-lookup"><span data-stu-id="f3fb4-146">string</span></span><br/>  | <span data-ttu-id="f3fb4-147">percent</span><span class="sxs-lookup"><span data-stu-id="f3fb4-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f3fb4-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3fb4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3fb4-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f3fb4-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




