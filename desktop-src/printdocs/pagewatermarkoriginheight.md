---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90736f8cac9c919f9d640ffc01311024ef79bc3a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994490"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="f5ce1-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="f5ce1-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="f5ce1-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-105">This topic is not current.</span></span> <span data-ttu-id="f5ce1-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f5ce1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f5ce1-107">Specifica l'origine di una filigrana rispetto all'origine di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="f5ce1-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5ce1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f5ce1-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f5ce1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f5ce1-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5ce1-110">Element Information</span></span>



| <span data-ttu-id="f5ce1-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f5ce1-111">Name</span></span> | <span data-ttu-id="f5ce1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ce1-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="f5ce1-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f5ce1-113">Element Type</span></span> <br/>   | <span data-ttu-id="f5ce1-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f5ce1-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="f5ce1-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f5ce1-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f5ce1-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="f5ce1-116">Page</span></span><br/>                            |
| <span data-ttu-id="f5ce1-117">Note</span><span class="sxs-lookup"><span data-stu-id="f5ce1-117">Notes</span></span> <br/>          | <span data-ttu-id="f5ce1-118">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="f5ce1-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f5ce1-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f5ce1-119">Structure Content</span></span>

<span data-ttu-id="f5ce1-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f5ce1-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f5ce1-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="f5ce1-121">Structure Properties</span></span>

<span data-ttu-id="f5ce1-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f5ce1-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5ce1-123">Property</span></span>                | <span data-ttu-id="f5ce1-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f5ce1-124">xsi:type</span></span>           | <span data-ttu-id="f5ce1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ce1-125">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f5ce1-126">DataType</span><span class="sxs-lookup"><span data-stu-id="f5ce1-126">DataType</span></span><br/>     | <span data-ttu-id="f5ce1-127">string</span><span class="sxs-lookup"><span data-stu-id="f5ce1-127">string</span></span><br/>  | <span data-ttu-id="f5ce1-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f5ce1-128">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="f5ce1-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f5ce1-129">DefaultValue</span></span><br/> | <span data-ttu-id="f5ce1-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="f5ce1-130">integer</span></span><br/> | <span data-ttu-id="f5ce1-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="f5ce1-131">undefined</span></span><br/>                                                    |
| <span data-ttu-id="f5ce1-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f5ce1-132">MaxValue</span></span><br/>     | <span data-ttu-id="f5ce1-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="f5ce1-133">integer</span></span><br/> | <span data-ttu-id="f5ce1-134">Minore o uguale a PageImageableSize - Valore ExtentHeight</span><span class="sxs-lookup"><span data-stu-id="f5ce1-134">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="f5ce1-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="f5ce1-135">MinValue</span></span><br/>     | <span data-ttu-id="f5ce1-136">integer</span><span class="sxs-lookup"><span data-stu-id="f5ce1-136">integer</span></span><br/> | <span data-ttu-id="f5ce1-137">0</span><span class="sxs-lookup"><span data-stu-id="f5ce1-137">0</span></span><br/>                                                            |
| <span data-ttu-id="f5ce1-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="f5ce1-138">Multiple</span></span><br/>     | <span data-ttu-id="f5ce1-139">integer</span><span class="sxs-lookup"><span data-stu-id="f5ce1-139">integer</span></span><br/> | <span data-ttu-id="f5ce1-140">1</span><span class="sxs-lookup"><span data-stu-id="f5ce1-140">1</span></span><br/>                                                            |
| <span data-ttu-id="f5ce1-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f5ce1-141">Mandatory</span></span><br/>    | <span data-ttu-id="f5ce1-142">string</span><span class="sxs-lookup"><span data-stu-id="f5ce1-142">string</span></span><br/>  | <span data-ttu-id="f5ce1-143">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="f5ce1-143">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="f5ce1-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="f5ce1-144">UnitType</span></span><br/>     | <span data-ttu-id="f5ce1-145">string</span><span class="sxs-lookup"><span data-stu-id="f5ce1-145">string</span></span><br/>  | <span data-ttu-id="f5ce1-146">Micron</span><span class="sxs-lookup"><span data-stu-id="f5ce1-146">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="f5ce1-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5ce1-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5ce1-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f5ce1-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




