---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d718d80f6b3cc369ddcb5c088a1299d639634b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997478"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="85173-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="85173-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="85173-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="85173-105">This topic is not current.</span></span> <span data-ttu-id="85173-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="85173-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85173-107">Specifica il fattore di scala nella direzione ImageableSizeHeight per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="85173-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="85173-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="85173-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="85173-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="85173-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="85173-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="85173-110">Element Information</span></span>



| <span data-ttu-id="85173-111">Nome</span><span class="sxs-lookup"><span data-stu-id="85173-111">Name</span></span> | <span data-ttu-id="85173-112">Valore</span><span class="sxs-lookup"><span data-stu-id="85173-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="85173-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="85173-113">Element Type</span></span> <br/>   | <span data-ttu-id="85173-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="85173-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="85173-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="85173-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="85173-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="85173-116">Page</span></span><br/>                                         |
| <span data-ttu-id="85173-117">Note</span><span class="sxs-lookup"><span data-stu-id="85173-117">Notes</span></span> <br/>          | <span data-ttu-id="85173-118">Collegato all'elemento PageScaling, opzione Personalizzata</span><span class="sxs-lookup"><span data-stu-id="85173-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="85173-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="85173-119">Structure Content</span></span>

<span data-ttu-id="85173-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="85173-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="85173-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="85173-121">Structure Properties</span></span>

<span data-ttu-id="85173-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="85173-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="85173-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="85173-123">Property</span></span>                | <span data-ttu-id="85173-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="85173-124">xsi:type</span></span>           | <span data-ttu-id="85173-125">Valore</span><span class="sxs-lookup"><span data-stu-id="85173-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="85173-126">DataType</span><span class="sxs-lookup"><span data-stu-id="85173-126">DataType</span></span><br/>     | <span data-ttu-id="85173-127">Stringa</span><span class="sxs-lookup"><span data-stu-id="85173-127">String</span></span><br/>  | <span data-ttu-id="85173-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="85173-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="85173-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="85173-129">DefaultValue</span></span><br/> | <span data-ttu-id="85173-130">Intero</span><span class="sxs-lookup"><span data-stu-id="85173-130">Integer</span></span><br/> | <span data-ttu-id="85173-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="85173-131">undefined</span></span><br/>       |
| <span data-ttu-id="85173-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="85173-132">MaxValue</span></span><br/>     | <span data-ttu-id="85173-133">Intero</span><span class="sxs-lookup"><span data-stu-id="85173-133">Integer</span></span><br/> | <span data-ttu-id="85173-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="85173-134">undefined</span></span><br/>       |
| <span data-ttu-id="85173-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="85173-135">MinValue</span></span><br/>     | <span data-ttu-id="85173-136">Integer</span><span class="sxs-lookup"><span data-stu-id="85173-136">Integer</span></span><br/> | <span data-ttu-id="85173-137">1</span><span class="sxs-lookup"><span data-stu-id="85173-137">1</span></span><br/>               |
| <span data-ttu-id="85173-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="85173-138">Mandatory</span></span><br/>    | <span data-ttu-id="85173-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="85173-139">String</span></span><br/>  | <span data-ttu-id="85173-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="85173-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="85173-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="85173-141">Multiple</span></span><br/>     | <span data-ttu-id="85173-142">Integer</span><span class="sxs-lookup"><span data-stu-id="85173-142">Integer</span></span><br/> | <span data-ttu-id="85173-143">1</span><span class="sxs-lookup"><span data-stu-id="85173-143">1</span></span><br/>               |
| <span data-ttu-id="85173-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="85173-144">UnitType</span></span><br/>     | <span data-ttu-id="85173-145">Stringa</span><span class="sxs-lookup"><span data-stu-id="85173-145">String</span></span><br/>  | <span data-ttu-id="85173-146">percent</span><span class="sxs-lookup"><span data-stu-id="85173-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="85173-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85173-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85173-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="85173-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




