---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6780dd5cc3b90a4f15cb6ada66ab82c4269acd82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886052"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="03368-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="03368-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="03368-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="03368-105">This topic is not current.</span></span> <span data-ttu-id="03368-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="03368-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="03368-107">Specifica l'origine di una filigrana rispetto all'origine del PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03368-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="03368-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="03368-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="03368-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="03368-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="03368-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="03368-110">Element Information</span></span>



| <span data-ttu-id="03368-111">Nome</span><span class="sxs-lookup"><span data-stu-id="03368-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="03368-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="03368-112">Element Type</span></span> <br/>   | <span data-ttu-id="03368-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="03368-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="03368-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="03368-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="03368-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="03368-115">Page</span></span><br/>                            |
| <span data-ttu-id="03368-116">Note</span><span class="sxs-lookup"><span data-stu-id="03368-116">Notes</span></span> <br/>          | <span data-ttu-id="03368-117">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="03368-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="03368-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="03368-118">Structure Content</span></span>

<span data-ttu-id="03368-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="03368-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="03368-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="03368-120">Structure Properties</span></span>

<span data-ttu-id="03368-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="03368-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="03368-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03368-122">Property</span></span>                | <span data-ttu-id="03368-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="03368-123">xsi:type</span></span>           | <span data-ttu-id="03368-124">Valore</span><span class="sxs-lookup"><span data-stu-id="03368-124">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="03368-125">DataType</span><span class="sxs-lookup"><span data-stu-id="03368-125">DataType</span></span><br/>     | <span data-ttu-id="03368-126">string</span><span class="sxs-lookup"><span data-stu-id="03368-126">string</span></span><br/>  | <span data-ttu-id="03368-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="03368-127">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="03368-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="03368-128">DefaultValue</span></span><br/> | <span data-ttu-id="03368-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="03368-129">integer</span></span><br/> | <span data-ttu-id="03368-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="03368-130">undefined</span></span><br/>                                                   |
| <span data-ttu-id="03368-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="03368-131">MaxValue</span></span><br/>     | <span data-ttu-id="03368-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="03368-132">integer</span></span><br/> | <span data-ttu-id="03368-133">Valore minore o uguale a PageImageableSize dell'oggetto-ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="03368-133">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="03368-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="03368-134">MinValue</span></span><br/>     | <span data-ttu-id="03368-135">integer</span><span class="sxs-lookup"><span data-stu-id="03368-135">integer</span></span><br/> | <span data-ttu-id="03368-136">0</span><span class="sxs-lookup"><span data-stu-id="03368-136">0</span></span><br/>                                                           |
| <span data-ttu-id="03368-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="03368-137">Multiple</span></span><br/>     | <span data-ttu-id="03368-138">integer</span><span class="sxs-lookup"><span data-stu-id="03368-138">integer</span></span><br/> | <span data-ttu-id="03368-139">1</span><span class="sxs-lookup"><span data-stu-id="03368-139">1</span></span><br/>                                                           |
| <span data-ttu-id="03368-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="03368-140">Mandatory</span></span><br/>    | <span data-ttu-id="03368-141">string</span><span class="sxs-lookup"><span data-stu-id="03368-141">string</span></span><br/>  | <span data-ttu-id="03368-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="03368-142">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="03368-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="03368-143">UnitType</span></span><br/>     | <span data-ttu-id="03368-144">string</span><span class="sxs-lookup"><span data-stu-id="03368-144">string</span></span><br/>  | <span data-ttu-id="03368-145">micron</span><span class="sxs-lookup"><span data-stu-id="03368-145">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="03368-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03368-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03368-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="03368-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




