---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d44dbc63632479c66686cea50b781abf715c76
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401842"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="5cdc1-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="5cdc1-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="5cdc1-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-105">This topic is not current.</span></span> <span data-ttu-id="5cdc1-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5cdc1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5cdc1-107">Descrive il livello di ombreggiatura al di sotto del quale verrà applicata l'UCA.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="5cdc1-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5cdc1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5cdc1-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5cdc1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5cdc1-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5cdc1-110">Element Information</span></span>



| <span data-ttu-id="5cdc1-111">Nome</span><span class="sxs-lookup"><span data-stu-id="5cdc1-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5cdc1-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5cdc1-112">Element Type</span></span> <br/>   | <span data-ttu-id="5cdc1-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5cdc1-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5cdc1-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="5cdc1-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5cdc1-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="5cdc1-115">Page</span></span><br/>                                            |
| <span data-ttu-id="5cdc1-116">Note</span><span class="sxs-lookup"><span data-stu-id="5cdc1-116">Notes</span></span> <br/>          | <span data-ttu-id="5cdc1-117">Collegato a elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="5cdc1-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5cdc1-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5cdc1-118">Structure Content</span></span>

<span data-ttu-id="5cdc1-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="5cdc1-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5cdc1-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="5cdc1-120">Structure Properties</span></span>

<span data-ttu-id="5cdc1-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5cdc1-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5cdc1-122">Property</span></span>                | <span data-ttu-id="5cdc1-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5cdc1-123">xsi:type</span></span>           | <span data-ttu-id="5cdc1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5cdc1-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5cdc1-125">DataType</span><span class="sxs-lookup"><span data-stu-id="5cdc1-125">DataType</span></span><br/>     | <span data-ttu-id="5cdc1-126">string</span><span class="sxs-lookup"><span data-stu-id="5cdc1-126">string</span></span><br/>  | <span data-ttu-id="5cdc1-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5cdc1-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="5cdc1-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5cdc1-128">DefaultValue</span></span><br/> | <span data-ttu-id="5cdc1-129">string</span><span class="sxs-lookup"><span data-stu-id="5cdc1-129">string</span></span><br/>  | <span data-ttu-id="5cdc1-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="5cdc1-130">undefined</span></span><br/>       |
| <span data-ttu-id="5cdc1-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5cdc1-131">MaxValue</span></span><br/>     | <span data-ttu-id="5cdc1-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="5cdc1-132">integer</span></span><br/> | <span data-ttu-id="5cdc1-133">100</span><span class="sxs-lookup"><span data-stu-id="5cdc1-133">100</span></span><br/>             |
| <span data-ttu-id="5cdc1-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="5cdc1-134">MinValue</span></span><br/>     | <span data-ttu-id="5cdc1-135">integer</span><span class="sxs-lookup"><span data-stu-id="5cdc1-135">integer</span></span><br/> | <span data-ttu-id="5cdc1-136">0</span><span class="sxs-lookup"><span data-stu-id="5cdc1-136">0</span></span><br/>               |
| <span data-ttu-id="5cdc1-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="5cdc1-137">Multiple</span></span><br/>     | <span data-ttu-id="5cdc1-138">integer</span><span class="sxs-lookup"><span data-stu-id="5cdc1-138">integer</span></span><br/> | <span data-ttu-id="5cdc1-139">1</span><span class="sxs-lookup"><span data-stu-id="5cdc1-139">1</span></span><br/>               |
| <span data-ttu-id="5cdc1-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="5cdc1-140">Mandatory</span></span><br/>    | <span data-ttu-id="5cdc1-141">string</span><span class="sxs-lookup"><span data-stu-id="5cdc1-141">string</span></span><br/>  | <span data-ttu-id="5cdc1-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="5cdc1-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5cdc1-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="5cdc1-143">UnitType</span></span><br/>     | <span data-ttu-id="5cdc1-144">string</span><span class="sxs-lookup"><span data-stu-id="5cdc1-144">string</span></span><br/>  | <span data-ttu-id="5cdc1-145">percent</span><span class="sxs-lookup"><span data-stu-id="5cdc1-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5cdc1-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cdc1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cdc1-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5cdc1-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




