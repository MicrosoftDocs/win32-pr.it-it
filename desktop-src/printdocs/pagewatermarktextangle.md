---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916e409040f0c7163f1168d48581270f077aaa3a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234580"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="39e61-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="39e61-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="39e61-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="39e61-105">This topic is not current.</span></span> <span data-ttu-id="39e61-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="39e61-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="39e61-107">Specifica l'angolo del testo della filigrana relativo alla direzione del PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="39e61-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="39e61-108">L'angolo viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="39e61-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="39e61-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="39e61-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="39e61-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="39e61-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="39e61-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="39e61-111">Element Information</span></span>



| <span data-ttu-id="39e61-112">Nome</span><span class="sxs-lookup"><span data-stu-id="39e61-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="39e61-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="39e61-113">Element Type</span></span> <br/>   | <span data-ttu-id="39e61-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="39e61-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="39e61-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="39e61-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="39e61-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="39e61-116">Page</span></span><br/>                            |
| <span data-ttu-id="39e61-117">Note</span><span class="sxs-lookup"><span data-stu-id="39e61-117">Notes</span></span> <br/>          | <span data-ttu-id="39e61-118">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="39e61-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="39e61-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="39e61-119">Structure Content</span></span>

<span data-ttu-id="39e61-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="39e61-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="39e61-121">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="39e61-121">Structure Properties</span></span>

<span data-ttu-id="39e61-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="39e61-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="39e61-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39e61-123">Property</span></span>                | <span data-ttu-id="39e61-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="39e61-124">xsi:type</span></span>           | <span data-ttu-id="39e61-125">Valore</span><span class="sxs-lookup"><span data-stu-id="39e61-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="39e61-126">DataType</span><span class="sxs-lookup"><span data-stu-id="39e61-126">DataType</span></span><br/>     | <span data-ttu-id="39e61-127">string</span><span class="sxs-lookup"><span data-stu-id="39e61-127">string</span></span><br/>  | <span data-ttu-id="39e61-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="39e61-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="39e61-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="39e61-129">DefaultValue</span></span><br/> | <span data-ttu-id="39e61-130">integer</span><span class="sxs-lookup"><span data-stu-id="39e61-130">integer</span></span><br/> | <span data-ttu-id="39e61-131">0</span><span class="sxs-lookup"><span data-stu-id="39e61-131">0</span></span><br/>               |
| <span data-ttu-id="39e61-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="39e61-132">MaxValue</span></span><br/>     | <span data-ttu-id="39e61-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="39e61-133">integer</span></span><br/> | <span data-ttu-id="39e61-134">359</span><span class="sxs-lookup"><span data-stu-id="39e61-134">359</span></span><br/>             |
| <span data-ttu-id="39e61-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="39e61-135">MinValue</span></span><br/>     | <span data-ttu-id="39e61-136">integer</span><span class="sxs-lookup"><span data-stu-id="39e61-136">integer</span></span><br/> | <span data-ttu-id="39e61-137">0</span><span class="sxs-lookup"><span data-stu-id="39e61-137">0</span></span><br/>               |
| <span data-ttu-id="39e61-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="39e61-138">Multiple</span></span><br/>     | <span data-ttu-id="39e61-139">integer</span><span class="sxs-lookup"><span data-stu-id="39e61-139">integer</span></span><br/> | <span data-ttu-id="39e61-140">1</span><span class="sxs-lookup"><span data-stu-id="39e61-140">1</span></span><br/>               |
| <span data-ttu-id="39e61-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="39e61-141">Mandatory</span></span><br/>    | <span data-ttu-id="39e61-142">string</span><span class="sxs-lookup"><span data-stu-id="39e61-142">string</span></span><br/>  | <span data-ttu-id="39e61-143">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="39e61-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="39e61-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="39e61-144">UnitType</span></span><br/>     | <span data-ttu-id="39e61-145">string</span><span class="sxs-lookup"><span data-stu-id="39e61-145">string</span></span><br/>  | <span data-ttu-id="39e61-146">gradi</span><span class="sxs-lookup"><span data-stu-id="39e61-146">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="39e61-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39e61-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39e61-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="39e61-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




