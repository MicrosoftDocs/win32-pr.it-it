---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401834"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="14e14-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="14e14-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="14e14-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="14e14-105">This topic is not current.</span></span> <span data-ttu-id="14e14-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="14e14-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="14e14-107">Specifica l'offset di ridimensionamento nella direzione ImageableSizeHeight per la scalabilità personalizzata.</span><span class="sxs-lookup"><span data-stu-id="14e14-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="14e14-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="14e14-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="14e14-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="14e14-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="14e14-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="14e14-110">Element Information</span></span>



| <span data-ttu-id="14e14-111">Nome</span><span class="sxs-lookup"><span data-stu-id="14e14-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="14e14-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="14e14-112">Element Type</span></span> <br/>   | <span data-ttu-id="14e14-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="14e14-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="14e14-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="14e14-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="14e14-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="14e14-115">Page</span></span><br/>                                         |
| <span data-ttu-id="14e14-116">Note</span><span class="sxs-lookup"><span data-stu-id="14e14-116">Notes</span></span> <br/>          | <span data-ttu-id="14e14-117">Collegato a elemento PageScaling, opzione personalizzata</span><span class="sxs-lookup"><span data-stu-id="14e14-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="14e14-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="14e14-118">Structure Content</span></span>

<span data-ttu-id="14e14-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="14e14-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="14e14-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="14e14-120">Structure Properties</span></span>

<span data-ttu-id="14e14-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="14e14-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="14e14-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14e14-122">Property</span></span>                | <span data-ttu-id="14e14-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="14e14-123">xsi:type</span></span>           | <span data-ttu-id="14e14-124">Valore</span><span class="sxs-lookup"><span data-stu-id="14e14-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="14e14-125">DataType</span><span class="sxs-lookup"><span data-stu-id="14e14-125">DataType</span></span><br/>     | <span data-ttu-id="14e14-126">string</span><span class="sxs-lookup"><span data-stu-id="14e14-126">string</span></span><br/>  | <span data-ttu-id="14e14-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="14e14-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="14e14-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="14e14-128">DefaultValue</span></span><br/> | <span data-ttu-id="14e14-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="14e14-129">integer</span></span><br/> | <span data-ttu-id="14e14-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="14e14-130">undefined</span></span><br/>       |
| <span data-ttu-id="14e14-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="14e14-131">MaxValue</span></span><br/>     | <span data-ttu-id="14e14-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="14e14-132">integer</span></span><br/> | <span data-ttu-id="14e14-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="14e14-133">undefined</span></span><br/>       |
| <span data-ttu-id="14e14-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="14e14-134">MinValue</span></span><br/>     | <span data-ttu-id="14e14-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="14e14-135">integer</span></span><br/> | <span data-ttu-id="14e14-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="14e14-136">undefined</span></span><br/>       |
| <span data-ttu-id="14e14-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="14e14-137">Mandatory</span></span><br/>    | <span data-ttu-id="14e14-138">string</span><span class="sxs-lookup"><span data-stu-id="14e14-138">string</span></span><br/>  | <span data-ttu-id="14e14-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="14e14-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="14e14-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="14e14-140">Multiple</span></span><br/>     | <span data-ttu-id="14e14-141">integer</span><span class="sxs-lookup"><span data-stu-id="14e14-141">integer</span></span><br/> | <span data-ttu-id="14e14-142">1</span><span class="sxs-lookup"><span data-stu-id="14e14-142">1</span></span><br/>               |
| <span data-ttu-id="14e14-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="14e14-143">UnitType</span></span><br/>     | <span data-ttu-id="14e14-144">string</span><span class="sxs-lookup"><span data-stu-id="14e14-144">string</span></span><br/>  | <span data-ttu-id="14e14-145">micron</span><span class="sxs-lookup"><span data-stu-id="14e14-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="14e14-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14e14-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e14-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="14e14-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




