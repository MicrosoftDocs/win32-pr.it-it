---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07566926c2115855ea7321af90e7d1caebcd0a82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321073"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="eebfd-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="eebfd-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="eebfd-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eebfd-105">This topic is not current.</span></span> <span data-ttu-id="eebfd-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eebfd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eebfd-107">Specifica la somma massima consentita della copertura a quattro input penna in un punto qualsiasi di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="eebfd-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="eebfd-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eebfd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eebfd-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="eebfd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="eebfd-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eebfd-110">Element Information</span></span>



| <span data-ttu-id="eebfd-111">Nome</span><span class="sxs-lookup"><span data-stu-id="eebfd-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="eebfd-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="eebfd-112">Element Type</span></span> <br/>   | <span data-ttu-id="eebfd-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="eebfd-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="eebfd-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="eebfd-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eebfd-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="eebfd-115">Page</span></span><br/>                                            |
| <span data-ttu-id="eebfd-116">Note</span><span class="sxs-lookup"><span data-stu-id="eebfd-116">Notes</span></span> <br/>          | <span data-ttu-id="eebfd-117">Collegato a elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="eebfd-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="eebfd-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="eebfd-118">Structure Content</span></span>

<span data-ttu-id="eebfd-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eebfd-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="eebfd-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="eebfd-120">Structure Properties</span></span>

<span data-ttu-id="eebfd-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="eebfd-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eebfd-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eebfd-122">Property</span></span>                | <span data-ttu-id="eebfd-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="eebfd-123">xsi:type</span></span>           | <span data-ttu-id="eebfd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="eebfd-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="eebfd-125">DataType</span><span class="sxs-lookup"><span data-stu-id="eebfd-125">DataType</span></span><br/>     | <span data-ttu-id="eebfd-126">string</span><span class="sxs-lookup"><span data-stu-id="eebfd-126">string</span></span><br/>  | <span data-ttu-id="eebfd-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="eebfd-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="eebfd-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="eebfd-128">DefaultValue</span></span><br/> | <span data-ttu-id="eebfd-129">string</span><span class="sxs-lookup"><span data-stu-id="eebfd-129">string</span></span><br/>  | <span data-ttu-id="eebfd-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="eebfd-130">undefined</span></span><br/>       |
| <span data-ttu-id="eebfd-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="eebfd-131">MaxValue</span></span><br/>     | <span data-ttu-id="eebfd-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="eebfd-132">integer</span></span><br/> | <span data-ttu-id="eebfd-133">400</span><span class="sxs-lookup"><span data-stu-id="eebfd-133">400</span></span><br/>             |
| <span data-ttu-id="eebfd-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="eebfd-134">MinValue</span></span><br/>     | <span data-ttu-id="eebfd-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="eebfd-135">integer</span></span><br/> | <span data-ttu-id="eebfd-136">200</span><span class="sxs-lookup"><span data-stu-id="eebfd-136">200</span></span><br/>             |
| <span data-ttu-id="eebfd-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="eebfd-137">Multiple</span></span><br/>     | <span data-ttu-id="eebfd-138">integer</span><span class="sxs-lookup"><span data-stu-id="eebfd-138">integer</span></span><br/> | <span data-ttu-id="eebfd-139">1</span><span class="sxs-lookup"><span data-stu-id="eebfd-139">1</span></span><br/>               |
| <span data-ttu-id="eebfd-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="eebfd-140">Mandatory</span></span><br/>    | <span data-ttu-id="eebfd-141">string</span><span class="sxs-lookup"><span data-stu-id="eebfd-141">string</span></span><br/>  | <span data-ttu-id="eebfd-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="eebfd-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="eebfd-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="eebfd-143">UnitType</span></span><br/>     | <span data-ttu-id="eebfd-144">string</span><span class="sxs-lookup"><span data-stu-id="eebfd-144">string</span></span><br/>  | <span data-ttu-id="eebfd-145">percent</span><span class="sxs-lookup"><span data-stu-id="eebfd-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="eebfd-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eebfd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eebfd-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="eebfd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




