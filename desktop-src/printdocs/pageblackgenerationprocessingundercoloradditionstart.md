---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Esaminare il parametro PageBlackGenerationProcessingUnderColorAdditionStart. Questo argomento non è corrente. Per informazioni aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549349"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="27187-105">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="27187-105">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="27187-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="27187-106">This topic is not current.</span></span> <span data-ttu-id="27187-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="27187-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27187-108">Descrive il livello di ombreggiatura al di sotto del quale verrà applicato l'uca.</span><span class="sxs-lookup"><span data-stu-id="27187-108">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="27187-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="27187-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27187-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="27187-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="27187-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="27187-111">Element Information</span></span>



| <span data-ttu-id="27187-112">Nome</span><span class="sxs-lookup"><span data-stu-id="27187-112">Name</span></span> | <span data-ttu-id="27187-113">Valore</span><span class="sxs-lookup"><span data-stu-id="27187-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="27187-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="27187-114">Element Type</span></span> <br/>   | <span data-ttu-id="27187-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="27187-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="27187-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="27187-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27187-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="27187-117">Page</span></span><br/>                                            |
| <span data-ttu-id="27187-118">Note</span><span class="sxs-lookup"><span data-stu-id="27187-118">Notes</span></span> <br/>          | <span data-ttu-id="27187-119">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="27187-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="27187-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="27187-120">Structure Content</span></span>

<span data-ttu-id="27187-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="27187-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
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

## <a name="structure-properties"></a><span data-ttu-id="27187-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="27187-122">Structure Properties</span></span>

<span data-ttu-id="27187-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="27187-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27187-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="27187-124">Property</span></span>                | <span data-ttu-id="27187-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="27187-125">xsi:type</span></span>           | <span data-ttu-id="27187-126">Valore</span><span class="sxs-lookup"><span data-stu-id="27187-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="27187-127">DataType</span><span class="sxs-lookup"><span data-stu-id="27187-127">DataType</span></span><br/>     | <span data-ttu-id="27187-128">string</span><span class="sxs-lookup"><span data-stu-id="27187-128">string</span></span><br/>  | <span data-ttu-id="27187-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="27187-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="27187-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="27187-130">DefaultValue</span></span><br/> | <span data-ttu-id="27187-131">string</span><span class="sxs-lookup"><span data-stu-id="27187-131">string</span></span><br/>  | <span data-ttu-id="27187-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="27187-132">undefined</span></span><br/>       |
| <span data-ttu-id="27187-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="27187-133">MaxValue</span></span><br/>     | <span data-ttu-id="27187-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="27187-134">integer</span></span><br/> | <span data-ttu-id="27187-135">100</span><span class="sxs-lookup"><span data-stu-id="27187-135">100</span></span><br/>             |
| <span data-ttu-id="27187-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="27187-136">MinValue</span></span><br/>     | <span data-ttu-id="27187-137">integer</span><span class="sxs-lookup"><span data-stu-id="27187-137">integer</span></span><br/> | <span data-ttu-id="27187-138">0</span><span class="sxs-lookup"><span data-stu-id="27187-138">0</span></span><br/>               |
| <span data-ttu-id="27187-139">Multipli</span><span class="sxs-lookup"><span data-stu-id="27187-139">Multiple</span></span><br/>     | <span data-ttu-id="27187-140">integer</span><span class="sxs-lookup"><span data-stu-id="27187-140">integer</span></span><br/> | <span data-ttu-id="27187-141">1</span><span class="sxs-lookup"><span data-stu-id="27187-141">1</span></span><br/>               |
| <span data-ttu-id="27187-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="27187-142">Mandatory</span></span><br/>    | <span data-ttu-id="27187-143">string</span><span class="sxs-lookup"><span data-stu-id="27187-143">string</span></span><br/>  | <span data-ttu-id="27187-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="27187-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="27187-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="27187-145">UnitType</span></span><br/>     | <span data-ttu-id="27187-146">string</span><span class="sxs-lookup"><span data-stu-id="27187-146">string</span></span><br/>  | <span data-ttu-id="27187-147">percent</span><span class="sxs-lookup"><span data-stu-id="27187-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="27187-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27187-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27187-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="27187-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




