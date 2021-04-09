---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d3e12591f6c648e6e636e1bb72f4df694d0d13
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103969015"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="7ad0d-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="7ad0d-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="7ad0d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-105">This topic is not current.</span></span> <span data-ttu-id="7ad0d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7ad0d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7ad0d-107">Specifica l'origine di una filigrana rispetto all'origine del PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="7ad0d-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7ad0d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7ad0d-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7ad0d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7ad0d-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7ad0d-110">Element Information</span></span>



| <span data-ttu-id="7ad0d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7ad0d-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="7ad0d-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7ad0d-112">Element Type</span></span> <br/>   | <span data-ttu-id="7ad0d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7ad0d-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="7ad0d-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="7ad0d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7ad0d-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="7ad0d-115">Page</span></span><br/>                            |
| <span data-ttu-id="7ad0d-116">Note</span><span class="sxs-lookup"><span data-stu-id="7ad0d-116">Notes</span></span> <br/>          | <span data-ttu-id="7ad0d-117">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="7ad0d-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7ad0d-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7ad0d-118">Structure Content</span></span>

<span data-ttu-id="7ad0d-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="7ad0d-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="7ad0d-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="7ad0d-120">Structure Properties</span></span>

<span data-ttu-id="7ad0d-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7ad0d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7ad0d-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ad0d-122">Property</span></span>                | <span data-ttu-id="7ad0d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7ad0d-123">xsi:type</span></span>           | <span data-ttu-id="7ad0d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7ad0d-124">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7ad0d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7ad0d-125">DataType</span></span><br/>     | <span data-ttu-id="7ad0d-126">string</span><span class="sxs-lookup"><span data-stu-id="7ad0d-126">string</span></span><br/>  | <span data-ttu-id="7ad0d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ad0d-127">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="7ad0d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7ad0d-128">DefaultValue</span></span><br/> | <span data-ttu-id="7ad0d-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="7ad0d-129">integer</span></span><br/> | <span data-ttu-id="7ad0d-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="7ad0d-130">undefined</span></span><br/>                                                    |
| <span data-ttu-id="7ad0d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7ad0d-131">MaxValue</span></span><br/>     | <span data-ttu-id="7ad0d-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="7ad0d-132">integer</span></span><br/> | <span data-ttu-id="7ad0d-133">Valore minore o uguale a PageImageableSize dell'oggetto-ExtentHeight</span><span class="sxs-lookup"><span data-stu-id="7ad0d-133">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="7ad0d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7ad0d-134">MinValue</span></span><br/>     | <span data-ttu-id="7ad0d-135">integer</span><span class="sxs-lookup"><span data-stu-id="7ad0d-135">integer</span></span><br/> | <span data-ttu-id="7ad0d-136">0</span><span class="sxs-lookup"><span data-stu-id="7ad0d-136">0</span></span><br/>                                                            |
| <span data-ttu-id="7ad0d-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="7ad0d-137">Multiple</span></span><br/>     | <span data-ttu-id="7ad0d-138">integer</span><span class="sxs-lookup"><span data-stu-id="7ad0d-138">integer</span></span><br/> | <span data-ttu-id="7ad0d-139">1</span><span class="sxs-lookup"><span data-stu-id="7ad0d-139">1</span></span><br/>                                                            |
| <span data-ttu-id="7ad0d-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7ad0d-140">Mandatory</span></span><br/>    | <span data-ttu-id="7ad0d-141">string</span><span class="sxs-lookup"><span data-stu-id="7ad0d-141">string</span></span><br/>  | <span data-ttu-id="7ad0d-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="7ad0d-142">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="7ad0d-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="7ad0d-143">UnitType</span></span><br/>     | <span data-ttu-id="7ad0d-144">string</span><span class="sxs-lookup"><span data-stu-id="7ad0d-144">string</span></span><br/>  | <span data-ttu-id="7ad0d-145">micron</span><span class="sxs-lookup"><span data-stu-id="7ad0d-145">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="7ad0d-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ad0d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ad0d-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7ad0d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




