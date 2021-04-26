---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2608535c65cbde04005334ed970c0d27cb1feffb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996178"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="66619-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="66619-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="66619-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="66619-105">This topic is not current.</span></span> <span data-ttu-id="66619-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="66619-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="66619-107">Descrive il punto nell'intervallo "evidenziazione da ombreggiatura" in cui deve iniziare GCR (ombreggiatura più scura al 100%.)</span><span class="sxs-lookup"><span data-stu-id="66619-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="66619-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="66619-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="66619-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="66619-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="66619-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="66619-110">Element Information</span></span>



| <span data-ttu-id="66619-111">Nome</span><span class="sxs-lookup"><span data-stu-id="66619-111">Name</span></span> | <span data-ttu-id="66619-112">Valore</span><span class="sxs-lookup"><span data-stu-id="66619-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="66619-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="66619-113">Element Type</span></span> <br/>   | <span data-ttu-id="66619-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="66619-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="66619-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="66619-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="66619-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="66619-116">Page</span></span><br/>                                            |
| <span data-ttu-id="66619-117">Note</span><span class="sxs-lookup"><span data-stu-id="66619-117">Notes</span></span> <br/>          | <span data-ttu-id="66619-118">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="66619-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="66619-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="66619-119">Structure Content</span></span>

<span data-ttu-id="66619-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="66619-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="66619-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="66619-121">Structure Properties</span></span>

<span data-ttu-id="66619-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="66619-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="66619-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66619-123">Property</span></span>                | <span data-ttu-id="66619-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="66619-124">xsi:type</span></span>           | <span data-ttu-id="66619-125">Valore</span><span class="sxs-lookup"><span data-stu-id="66619-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="66619-126">DataType</span><span class="sxs-lookup"><span data-stu-id="66619-126">DataType</span></span><br/>     | <span data-ttu-id="66619-127">string</span><span class="sxs-lookup"><span data-stu-id="66619-127">string</span></span><br/>  | <span data-ttu-id="66619-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="66619-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="66619-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="66619-129">DefaultValue</span></span><br/> | <span data-ttu-id="66619-130">string</span><span class="sxs-lookup"><span data-stu-id="66619-130">string</span></span><br/>  | <span data-ttu-id="66619-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="66619-131">undefined</span></span><br/>       |
| <span data-ttu-id="66619-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="66619-132">MaxValue</span></span><br/>     | <span data-ttu-id="66619-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="66619-133">integer</span></span><br/> | <span data-ttu-id="66619-134">100</span><span class="sxs-lookup"><span data-stu-id="66619-134">100</span></span><br/>             |
| <span data-ttu-id="66619-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="66619-135">MinValue</span></span><br/>     | <span data-ttu-id="66619-136">integer</span><span class="sxs-lookup"><span data-stu-id="66619-136">integer</span></span><br/> | <span data-ttu-id="66619-137">0</span><span class="sxs-lookup"><span data-stu-id="66619-137">0</span></span><br/>               |
| <span data-ttu-id="66619-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="66619-138">Multiple</span></span><br/>     | <span data-ttu-id="66619-139">integer</span><span class="sxs-lookup"><span data-stu-id="66619-139">integer</span></span><br/> | <span data-ttu-id="66619-140">1</span><span class="sxs-lookup"><span data-stu-id="66619-140">1</span></span><br/>               |
| <span data-ttu-id="66619-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="66619-141">Mandatory</span></span><br/>    | <span data-ttu-id="66619-142">string</span><span class="sxs-lookup"><span data-stu-id="66619-142">string</span></span><br/>  | <span data-ttu-id="66619-143">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="66619-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="66619-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="66619-144">UnitType</span></span><br/>     | <span data-ttu-id="66619-145">string</span><span class="sxs-lookup"><span data-stu-id="66619-145">string</span></span><br/>  | <span data-ttu-id="66619-146">percent</span><span class="sxs-lookup"><span data-stu-id="66619-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="66619-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66619-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66619-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="66619-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




