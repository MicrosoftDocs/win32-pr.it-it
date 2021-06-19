---
description: Ottenere informazioni sul parametro PageWatermarkOriginWidth. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe6457496972231877af2a51e03bc5109083d0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396006"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="cadf7-105">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="cadf7-105">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="cadf7-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="cadf7-106">This topic is not current.</span></span> <span data-ttu-id="cadf7-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cadf7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cadf7-108">Specifica l'origine di una filigrana relativa all'origine di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="cadf7-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="cadf7-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cadf7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cadf7-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="cadf7-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cadf7-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cadf7-111">Element Information</span></span>



| <span data-ttu-id="cadf7-112">Nome</span><span class="sxs-lookup"><span data-stu-id="cadf7-112">Name</span></span> | <span data-ttu-id="cadf7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cadf7-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="cadf7-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="cadf7-114">Element Type</span></span> <br/>   | <span data-ttu-id="cadf7-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cadf7-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="cadf7-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="cadf7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cadf7-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="cadf7-117">Page</span></span><br/>                            |
| <span data-ttu-id="cadf7-118">Note</span><span class="sxs-lookup"><span data-stu-id="cadf7-118">Notes</span></span> <br/>          | <span data-ttu-id="cadf7-119">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="cadf7-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cadf7-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="cadf7-120">Structure Content</span></span>

<span data-ttu-id="cadf7-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="cadf7-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cadf7-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="cadf7-122">Structure Properties</span></span>

<span data-ttu-id="cadf7-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="cadf7-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cadf7-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cadf7-124">Property</span></span>                | <span data-ttu-id="cadf7-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cadf7-125">xsi:type</span></span>           | <span data-ttu-id="cadf7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cadf7-126">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="cadf7-127">DataType</span><span class="sxs-lookup"><span data-stu-id="cadf7-127">DataType</span></span><br/>     | <span data-ttu-id="cadf7-128">string</span><span class="sxs-lookup"><span data-stu-id="cadf7-128">string</span></span><br/>  | <span data-ttu-id="cadf7-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cadf7-129">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="cadf7-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cadf7-130">DefaultValue</span></span><br/> | <span data-ttu-id="cadf7-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="cadf7-131">integer</span></span><br/> | <span data-ttu-id="cadf7-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="cadf7-132">undefined</span></span><br/>                                                   |
| <span data-ttu-id="cadf7-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="cadf7-133">MaxValue</span></span><br/>     | <span data-ttu-id="cadf7-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="cadf7-134">integer</span></span><br/> | <span data-ttu-id="cadf7-135">Minore o uguale al valore PageImageableSize - ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="cadf7-135">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="cadf7-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="cadf7-136">MinValue</span></span><br/>     | <span data-ttu-id="cadf7-137">integer</span><span class="sxs-lookup"><span data-stu-id="cadf7-137">integer</span></span><br/> | <span data-ttu-id="cadf7-138">0</span><span class="sxs-lookup"><span data-stu-id="cadf7-138">0</span></span><br/>                                                           |
| <span data-ttu-id="cadf7-139">Multipli</span><span class="sxs-lookup"><span data-stu-id="cadf7-139">Multiple</span></span><br/>     | <span data-ttu-id="cadf7-140">integer</span><span class="sxs-lookup"><span data-stu-id="cadf7-140">integer</span></span><br/> | <span data-ttu-id="cadf7-141">1</span><span class="sxs-lookup"><span data-stu-id="cadf7-141">1</span></span><br/>                                                           |
| <span data-ttu-id="cadf7-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="cadf7-142">Mandatory</span></span><br/>    | <span data-ttu-id="cadf7-143">string</span><span class="sxs-lookup"><span data-stu-id="cadf7-143">string</span></span><br/>  | <span data-ttu-id="cadf7-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="cadf7-144">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="cadf7-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="cadf7-145">UnitType</span></span><br/>     | <span data-ttu-id="cadf7-146">string</span><span class="sxs-lookup"><span data-stu-id="cadf7-146">string</span></span><br/>  | <span data-ttu-id="cadf7-147">Micron</span><span class="sxs-lookup"><span data-stu-id="cadf7-147">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="cadf7-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cadf7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cadf7-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="cadf7-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




