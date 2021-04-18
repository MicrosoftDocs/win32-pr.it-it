---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a9cd5532bf4d109b94c579ef2ad21d242aca9a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321016"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="b4146-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="b4146-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="b4146-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b4146-105">This topic is not current.</span></span> <span data-ttu-id="b4146-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b4146-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b4146-107">Specifica l'offset di ridimensionamento nella direzione ImageableSizeWidth per la scalabilità personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b4146-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="b4146-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b4146-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b4146-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b4146-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b4146-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b4146-110">Element Information</span></span>



| <span data-ttu-id="b4146-111">Nome</span><span class="sxs-lookup"><span data-stu-id="b4146-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="b4146-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b4146-112">Element Type</span></span> <br/>   | <span data-ttu-id="b4146-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b4146-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="b4146-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="b4146-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b4146-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="b4146-115">Page</span></span><br/>                                         |
| <span data-ttu-id="b4146-116">Note</span><span class="sxs-lookup"><span data-stu-id="b4146-116">Notes</span></span> <br/>          | <span data-ttu-id="b4146-117">Collegato a elemento PageScaling, opzione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b4146-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b4146-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b4146-118">Structure Content</span></span>

<span data-ttu-id="b4146-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b4146-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="b4146-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="b4146-120">Structure Properties</span></span>

<span data-ttu-id="b4146-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b4146-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b4146-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4146-122">Property</span></span>                | <span data-ttu-id="b4146-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b4146-123">xsi:type</span></span>           | <span data-ttu-id="b4146-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b4146-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b4146-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b4146-125">DataType</span></span><br/>     | <span data-ttu-id="b4146-126">string</span><span class="sxs-lookup"><span data-stu-id="b4146-126">string</span></span><br/>  | <span data-ttu-id="b4146-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b4146-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b4146-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b4146-128">DefaultValue</span></span><br/> | <span data-ttu-id="b4146-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="b4146-129">integer</span></span><br/> | <span data-ttu-id="b4146-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="b4146-130">undefined</span></span><br/>       |
| <span data-ttu-id="b4146-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b4146-131">MaxValue</span></span><br/>     | <span data-ttu-id="b4146-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="b4146-132">integer</span></span><br/> | <span data-ttu-id="b4146-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="b4146-133">undefined</span></span><br/>       |
| <span data-ttu-id="b4146-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b4146-134">MinValue</span></span><br/>     | <span data-ttu-id="b4146-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="b4146-135">integer</span></span><br/> | <span data-ttu-id="b4146-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="b4146-136">undefined</span></span><br/>       |
| <span data-ttu-id="b4146-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b4146-137">Mandatory</span></span><br/>    | <span data-ttu-id="b4146-138">string</span><span class="sxs-lookup"><span data-stu-id="b4146-138">string</span></span><br/>  | <span data-ttu-id="b4146-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="b4146-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b4146-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="b4146-140">Multiple</span></span><br/>     | <span data-ttu-id="b4146-141">integer</span><span class="sxs-lookup"><span data-stu-id="b4146-141">integer</span></span><br/> | <span data-ttu-id="b4146-142">1</span><span class="sxs-lookup"><span data-stu-id="b4146-142">1</span></span><br/>               |
| <span data-ttu-id="b4146-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b4146-143">UnitType</span></span><br/>     | <span data-ttu-id="b4146-144">string</span><span class="sxs-lookup"><span data-stu-id="b4146-144">string</span></span><br/>  | <span data-ttu-id="b4146-145">micron</span><span class="sxs-lookup"><span data-stu-id="b4146-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b4146-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4146-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4146-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b4146-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




