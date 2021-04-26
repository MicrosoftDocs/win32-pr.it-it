---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78cf29952258a7c6c3489d40291ba8cd4b756c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996068"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="c4115-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="c4115-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="c4115-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c4115-105">This topic is not current.</span></span> <span data-ttu-id="c4115-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c4115-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4115-107">Specifica l'origine di una filigrana relativa all'origine di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="c4115-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="c4115-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c4115-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c4115-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c4115-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c4115-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c4115-110">Element Information</span></span>



| <span data-ttu-id="c4115-111">Nome</span><span class="sxs-lookup"><span data-stu-id="c4115-111">Name</span></span> | <span data-ttu-id="c4115-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c4115-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="c4115-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c4115-113">Element Type</span></span> <br/>   | <span data-ttu-id="c4115-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c4115-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="c4115-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="c4115-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c4115-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="c4115-116">Page</span></span><br/>                            |
| <span data-ttu-id="c4115-117">Note</span><span class="sxs-lookup"><span data-stu-id="c4115-117">Notes</span></span> <br/>          | <span data-ttu-id="c4115-118">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="c4115-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c4115-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c4115-119">Structure Content</span></span>

<span data-ttu-id="c4115-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="c4115-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c4115-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="c4115-121">Structure Properties</span></span>

<span data-ttu-id="c4115-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c4115-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c4115-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4115-123">Property</span></span>                | <span data-ttu-id="c4115-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c4115-124">xsi:type</span></span>           | <span data-ttu-id="c4115-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c4115-125">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c4115-126">DataType</span><span class="sxs-lookup"><span data-stu-id="c4115-126">DataType</span></span><br/>     | <span data-ttu-id="c4115-127">string</span><span class="sxs-lookup"><span data-stu-id="c4115-127">string</span></span><br/>  | <span data-ttu-id="c4115-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c4115-128">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="c4115-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c4115-129">DefaultValue</span></span><br/> | <span data-ttu-id="c4115-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="c4115-130">integer</span></span><br/> | <span data-ttu-id="c4115-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="c4115-131">undefined</span></span><br/>                                                   |
| <span data-ttu-id="c4115-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c4115-132">MaxValue</span></span><br/>     | <span data-ttu-id="c4115-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="c4115-133">integer</span></span><br/> | <span data-ttu-id="c4115-134">Minore o uguale al valore PageImageableSize - ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="c4115-134">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="c4115-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="c4115-135">MinValue</span></span><br/>     | <span data-ttu-id="c4115-136">integer</span><span class="sxs-lookup"><span data-stu-id="c4115-136">integer</span></span><br/> | <span data-ttu-id="c4115-137">0</span><span class="sxs-lookup"><span data-stu-id="c4115-137">0</span></span><br/>                                                           |
| <span data-ttu-id="c4115-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="c4115-138">Multiple</span></span><br/>     | <span data-ttu-id="c4115-139">integer</span><span class="sxs-lookup"><span data-stu-id="c4115-139">integer</span></span><br/> | <span data-ttu-id="c4115-140">1</span><span class="sxs-lookup"><span data-stu-id="c4115-140">1</span></span><br/>                                                           |
| <span data-ttu-id="c4115-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c4115-141">Mandatory</span></span><br/>    | <span data-ttu-id="c4115-142">string</span><span class="sxs-lookup"><span data-stu-id="c4115-142">string</span></span><br/>  | <span data-ttu-id="c4115-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="c4115-143">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="c4115-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="c4115-144">UnitType</span></span><br/>     | <span data-ttu-id="c4115-145">string</span><span class="sxs-lookup"><span data-stu-id="c4115-145">string</span></span><br/>  | <span data-ttu-id="c4115-146">Micron</span><span class="sxs-lookup"><span data-stu-id="c4115-146">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c4115-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4115-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4115-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c4115-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




