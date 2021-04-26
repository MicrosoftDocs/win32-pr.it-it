---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b82c2b0c0f2c86a792706ec7e00819ccda1038c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997958"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="a5595-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="a5595-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="a5595-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a5595-105">This topic is not current.</span></span> <span data-ttu-id="a5595-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a5595-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a5595-107">Specifica l'offset di ridimensionamento nella direzione ImageableSizeWidth per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a5595-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="a5595-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a5595-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a5595-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="a5595-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a5595-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a5595-110">Element Information</span></span>



| <span data-ttu-id="a5595-111">Nome</span><span class="sxs-lookup"><span data-stu-id="a5595-111">Name</span></span> | <span data-ttu-id="a5595-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a5595-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="a5595-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a5595-113">Element Type</span></span> <br/>   | <span data-ttu-id="a5595-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a5595-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="a5595-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a5595-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a5595-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="a5595-116">Page</span></span><br/>                                         |
| <span data-ttu-id="a5595-117">Note</span><span class="sxs-lookup"><span data-stu-id="a5595-117">Notes</span></span> <br/>          | <span data-ttu-id="a5595-118">Collegato all'elemento PageScaling, opzione Personalizzata</span><span class="sxs-lookup"><span data-stu-id="a5595-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a5595-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="a5595-119">Structure Content</span></span>

<span data-ttu-id="a5595-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="a5595-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a5595-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="a5595-121">Structure Properties</span></span>

<span data-ttu-id="a5595-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a5595-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a5595-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5595-123">Property</span></span>                | <span data-ttu-id="a5595-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a5595-124">xsi:type</span></span>           | <span data-ttu-id="a5595-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a5595-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a5595-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a5595-126">DataType</span></span><br/>     | <span data-ttu-id="a5595-127">string</span><span class="sxs-lookup"><span data-stu-id="a5595-127">string</span></span><br/>  | <span data-ttu-id="a5595-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a5595-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="a5595-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a5595-129">DefaultValue</span></span><br/> | <span data-ttu-id="a5595-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="a5595-130">integer</span></span><br/> | <span data-ttu-id="a5595-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="a5595-131">undefined</span></span><br/>       |
| <span data-ttu-id="a5595-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a5595-132">MaxValue</span></span><br/>     | <span data-ttu-id="a5595-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="a5595-133">integer</span></span><br/> | <span data-ttu-id="a5595-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="a5595-134">undefined</span></span><br/>       |
| <span data-ttu-id="a5595-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="a5595-135">MinValue</span></span><br/>     | <span data-ttu-id="a5595-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="a5595-136">integer</span></span><br/> | <span data-ttu-id="a5595-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="a5595-137">undefined</span></span><br/>       |
| <span data-ttu-id="a5595-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="a5595-138">Mandatory</span></span><br/>    | <span data-ttu-id="a5595-139">string</span><span class="sxs-lookup"><span data-stu-id="a5595-139">string</span></span><br/>  | <span data-ttu-id="a5595-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a5595-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a5595-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="a5595-141">Multiple</span></span><br/>     | <span data-ttu-id="a5595-142">integer</span><span class="sxs-lookup"><span data-stu-id="a5595-142">integer</span></span><br/> | <span data-ttu-id="a5595-143">1</span><span class="sxs-lookup"><span data-stu-id="a5595-143">1</span></span><br/>               |
| <span data-ttu-id="a5595-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="a5595-144">UnitType</span></span><br/>     | <span data-ttu-id="a5595-145">string</span><span class="sxs-lookup"><span data-stu-id="a5595-145">string</span></span><br/>  | <span data-ttu-id="a5595-146">Micron</span><span class="sxs-lookup"><span data-stu-id="a5595-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a5595-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5595-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5595-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a5595-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




