---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320923"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="a2070-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="a2070-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="a2070-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a2070-105">This topic is not current.</span></span> <span data-ttu-id="a2070-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a2070-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a2070-107">Specifica la trasparenza per la filigrana.</span><span class="sxs-lookup"><span data-stu-id="a2070-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="a2070-108">Il valore di completamente opaco avrà un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="a2070-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="a2070-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a2070-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a2070-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="a2070-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a2070-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a2070-111">Element Information</span></span>



| <span data-ttu-id="a2070-112">Nome</span><span class="sxs-lookup"><span data-stu-id="a2070-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="a2070-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a2070-113">Element Type</span></span> <br/>   | <span data-ttu-id="a2070-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a2070-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="a2070-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="a2070-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a2070-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="a2070-116">Page</span></span><br/>                            |
| <span data-ttu-id="a2070-117">Note</span><span class="sxs-lookup"><span data-stu-id="a2070-117">Notes</span></span> <br/>          | <span data-ttu-id="a2070-118">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="a2070-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a2070-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="a2070-119">Structure Content</span></span>

<span data-ttu-id="a2070-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="a2070-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="a2070-121">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="a2070-121">Structure Properties</span></span>

<span data-ttu-id="a2070-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a2070-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a2070-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2070-123">Property</span></span>                | <span data-ttu-id="a2070-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a2070-124">xsi:type</span></span>           | <span data-ttu-id="a2070-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a2070-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a2070-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a2070-126">DataType</span></span><br/>     | <span data-ttu-id="a2070-127">string</span><span class="sxs-lookup"><span data-stu-id="a2070-127">string</span></span><br/>  | <span data-ttu-id="a2070-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a2070-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="a2070-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a2070-129">DefaultValue</span></span><br/> | <span data-ttu-id="a2070-130">integer</span><span class="sxs-lookup"><span data-stu-id="a2070-130">integer</span></span><br/> | <span data-ttu-id="a2070-131">0</span><span class="sxs-lookup"><span data-stu-id="a2070-131">0</span></span><br/>               |
| <span data-ttu-id="a2070-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a2070-132">MaxValue</span></span><br/>     | <span data-ttu-id="a2070-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="a2070-133">integer</span></span><br/> | <span data-ttu-id="a2070-134">100</span><span class="sxs-lookup"><span data-stu-id="a2070-134">100</span></span><br/>             |
| <span data-ttu-id="a2070-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="a2070-135">MinValue</span></span><br/>     | <span data-ttu-id="a2070-136">integer</span><span class="sxs-lookup"><span data-stu-id="a2070-136">integer</span></span><br/> | <span data-ttu-id="a2070-137">0</span><span class="sxs-lookup"><span data-stu-id="a2070-137">0</span></span><br/>               |
| <span data-ttu-id="a2070-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="a2070-138">Multiple</span></span><br/>     | <span data-ttu-id="a2070-139">integer</span><span class="sxs-lookup"><span data-stu-id="a2070-139">integer</span></span><br/> | <span data-ttu-id="a2070-140">1</span><span class="sxs-lookup"><span data-stu-id="a2070-140">1</span></span><br/>               |
| <span data-ttu-id="a2070-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="a2070-141">Mandatory</span></span><br/>    | <span data-ttu-id="a2070-142">string</span><span class="sxs-lookup"><span data-stu-id="a2070-142">string</span></span><br/>  | <span data-ttu-id="a2070-143">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="a2070-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a2070-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="a2070-144">UnitType</span></span><br/>     | <span data-ttu-id="a2070-145">string</span><span class="sxs-lookup"><span data-stu-id="a2070-145">string</span></span><br/>  | <span data-ttu-id="a2070-146">percent</span><span class="sxs-lookup"><span data-stu-id="a2070-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a2070-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2070-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2070-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a2070-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




