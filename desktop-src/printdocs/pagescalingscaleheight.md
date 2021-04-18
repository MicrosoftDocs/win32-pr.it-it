---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3f91f6b188dadbd86a18152be5228b62d21ab4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321049"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="88019-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="88019-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="88019-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="88019-105">This topic is not current.</span></span> <span data-ttu-id="88019-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="88019-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88019-107">Specifica il fattore di scala nella direzione ImageableSizeHeight per la scalabilità personalizzata.</span><span class="sxs-lookup"><span data-stu-id="88019-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="88019-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="88019-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88019-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="88019-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="88019-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="88019-110">Element Information</span></span>



| <span data-ttu-id="88019-111">Nome</span><span class="sxs-lookup"><span data-stu-id="88019-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="88019-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="88019-112">Element Type</span></span> <br/>   | <span data-ttu-id="88019-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="88019-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="88019-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="88019-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88019-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="88019-115">Page</span></span><br/>                                         |
| <span data-ttu-id="88019-116">Note</span><span class="sxs-lookup"><span data-stu-id="88019-116">Notes</span></span> <br/>          | <span data-ttu-id="88019-117">Collegato a elemento PageScaling, opzione personalizzata</span><span class="sxs-lookup"><span data-stu-id="88019-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="88019-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="88019-118">Structure Content</span></span>

<span data-ttu-id="88019-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="88019-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="88019-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="88019-120">Structure Properties</span></span>

<span data-ttu-id="88019-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="88019-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88019-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88019-122">Property</span></span>                | <span data-ttu-id="88019-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="88019-123">xsi:type</span></span>           | <span data-ttu-id="88019-124">Valore</span><span class="sxs-lookup"><span data-stu-id="88019-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="88019-125">DataType</span><span class="sxs-lookup"><span data-stu-id="88019-125">DataType</span></span><br/>     | <span data-ttu-id="88019-126">string</span><span class="sxs-lookup"><span data-stu-id="88019-126">String</span></span><br/>  | <span data-ttu-id="88019-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="88019-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="88019-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="88019-128">DefaultValue</span></span><br/> | <span data-ttu-id="88019-129">Integer</span><span class="sxs-lookup"><span data-stu-id="88019-129">Integer</span></span><br/> | <span data-ttu-id="88019-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="88019-130">undefined</span></span><br/>       |
| <span data-ttu-id="88019-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="88019-131">MaxValue</span></span><br/>     | <span data-ttu-id="88019-132">Integer</span><span class="sxs-lookup"><span data-stu-id="88019-132">Integer</span></span><br/> | <span data-ttu-id="88019-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="88019-133">undefined</span></span><br/>       |
| <span data-ttu-id="88019-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="88019-134">MinValue</span></span><br/>     | <span data-ttu-id="88019-135">Integer</span><span class="sxs-lookup"><span data-stu-id="88019-135">Integer</span></span><br/> | <span data-ttu-id="88019-136">1</span><span class="sxs-lookup"><span data-stu-id="88019-136">1</span></span><br/>               |
| <span data-ttu-id="88019-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="88019-137">Mandatory</span></span><br/>    | <span data-ttu-id="88019-138">string</span><span class="sxs-lookup"><span data-stu-id="88019-138">String</span></span><br/>  | <span data-ttu-id="88019-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="88019-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="88019-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="88019-140">Multiple</span></span><br/>     | <span data-ttu-id="88019-141">Integer</span><span class="sxs-lookup"><span data-stu-id="88019-141">Integer</span></span><br/> | <span data-ttu-id="88019-142">1</span><span class="sxs-lookup"><span data-stu-id="88019-142">1</span></span><br/>               |
| <span data-ttu-id="88019-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="88019-143">UnitType</span></span><br/>     | <span data-ttu-id="88019-144">string</span><span class="sxs-lookup"><span data-stu-id="88019-144">String</span></span><br/>  | <span data-ttu-id="88019-145">percent</span><span class="sxs-lookup"><span data-stu-id="88019-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="88019-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88019-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88019-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="88019-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




