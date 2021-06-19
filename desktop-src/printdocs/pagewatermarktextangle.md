---
description: Ottenere altre informazioni sul parametro PageWatermarkTextAngle. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395976"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="93e09-105">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="93e09-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="93e09-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="93e09-106">This topic is not current.</span></span> <span data-ttu-id="93e09-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="93e09-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="93e09-108">Specifica l'angolo del testo della filigrana rispetto alla direzione PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="93e09-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="93e09-109">L'angolo viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="93e09-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="93e09-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="93e09-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="93e09-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="93e09-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="93e09-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="93e09-112">Element Information</span></span>



| <span data-ttu-id="93e09-113">Nome</span><span class="sxs-lookup"><span data-stu-id="93e09-113">Name</span></span> | <span data-ttu-id="93e09-114">Valore</span><span class="sxs-lookup"><span data-stu-id="93e09-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="93e09-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="93e09-115">Element Type</span></span> <br/>   | <span data-ttu-id="93e09-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="93e09-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="93e09-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="93e09-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="93e09-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="93e09-118">Page</span></span><br/>                            |
| <span data-ttu-id="93e09-119">Note</span><span class="sxs-lookup"><span data-stu-id="93e09-119">Notes</span></span> <br/>          | <span data-ttu-id="93e09-120">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="93e09-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="93e09-121">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="93e09-121">Structure Content</span></span>

<span data-ttu-id="93e09-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="93e09-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="93e09-123">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="93e09-123">Structure Properties</span></span>

<span data-ttu-id="93e09-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="93e09-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="93e09-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="93e09-125">Property</span></span>                | <span data-ttu-id="93e09-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="93e09-126">xsi:type</span></span>           | <span data-ttu-id="93e09-127">Valore</span><span class="sxs-lookup"><span data-stu-id="93e09-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="93e09-128">DataType</span><span class="sxs-lookup"><span data-stu-id="93e09-128">DataType</span></span><br/>     | <span data-ttu-id="93e09-129">string</span><span class="sxs-lookup"><span data-stu-id="93e09-129">string</span></span><br/>  | <span data-ttu-id="93e09-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="93e09-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="93e09-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="93e09-131">DefaultValue</span></span><br/> | <span data-ttu-id="93e09-132">integer</span><span class="sxs-lookup"><span data-stu-id="93e09-132">integer</span></span><br/> | <span data-ttu-id="93e09-133">0</span><span class="sxs-lookup"><span data-stu-id="93e09-133">0</span></span><br/>               |
| <span data-ttu-id="93e09-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="93e09-134">MaxValue</span></span><br/>     | <span data-ttu-id="93e09-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="93e09-135">integer</span></span><br/> | <span data-ttu-id="93e09-136">359</span><span class="sxs-lookup"><span data-stu-id="93e09-136">359</span></span><br/>             |
| <span data-ttu-id="93e09-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="93e09-137">MinValue</span></span><br/>     | <span data-ttu-id="93e09-138">integer</span><span class="sxs-lookup"><span data-stu-id="93e09-138">integer</span></span><br/> | <span data-ttu-id="93e09-139">0</span><span class="sxs-lookup"><span data-stu-id="93e09-139">0</span></span><br/>               |
| <span data-ttu-id="93e09-140">Multipli</span><span class="sxs-lookup"><span data-stu-id="93e09-140">Multiple</span></span><br/>     | <span data-ttu-id="93e09-141">integer</span><span class="sxs-lookup"><span data-stu-id="93e09-141">integer</span></span><br/> | <span data-ttu-id="93e09-142">1</span><span class="sxs-lookup"><span data-stu-id="93e09-142">1</span></span><br/>               |
| <span data-ttu-id="93e09-143">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="93e09-143">Mandatory</span></span><br/>    | <span data-ttu-id="93e09-144">string</span><span class="sxs-lookup"><span data-stu-id="93e09-144">string</span></span><br/>  | <span data-ttu-id="93e09-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="93e09-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="93e09-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="93e09-146">UnitType</span></span><br/>     | <span data-ttu-id="93e09-147">string</span><span class="sxs-lookup"><span data-stu-id="93e09-147">string</span></span><br/>  | <span data-ttu-id="93e09-148">gradi</span><span class="sxs-lookup"><span data-stu-id="93e09-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="93e09-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93e09-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93e09-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="93e09-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




