---
description: Ottenere informazioni sul parametro PageScalingScaleHeight. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51bdb5577b5e3863cfadab1fa9eb74ff40d54da
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548839"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="16f9e-105">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="16f9e-105">PageScalingScaleHeight</span></span>

<span data-ttu-id="16f9e-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="16f9e-106">This topic is not current.</span></span> <span data-ttu-id="16f9e-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16f9e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16f9e-108">Specifica il fattore di scala nella direzione ImageableSizeHeight per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="16f9e-108">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="16f9e-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16f9e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="16f9e-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="16f9e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="16f9e-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16f9e-111">Element Information</span></span>



| <span data-ttu-id="16f9e-112">Nome</span><span class="sxs-lookup"><span data-stu-id="16f9e-112">Name</span></span> | <span data-ttu-id="16f9e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="16f9e-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="16f9e-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="16f9e-114">Element Type</span></span> <br/>   | <span data-ttu-id="16f9e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="16f9e-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="16f9e-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="16f9e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="16f9e-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="16f9e-117">Page</span></span><br/>                                         |
| <span data-ttu-id="16f9e-118">Note</span><span class="sxs-lookup"><span data-stu-id="16f9e-118">Notes</span></span> <br/>          | <span data-ttu-id="16f9e-119">Collegato all'elemento PageScaling, opzione Personalizzata</span><span class="sxs-lookup"><span data-stu-id="16f9e-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="16f9e-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="16f9e-120">Structure Content</span></span>

<span data-ttu-id="16f9e-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="16f9e-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="16f9e-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="16f9e-122">Structure Properties</span></span>

<span data-ttu-id="16f9e-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="16f9e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="16f9e-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16f9e-124">Property</span></span>                | <span data-ttu-id="16f9e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="16f9e-125">xsi:type</span></span>           | <span data-ttu-id="16f9e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="16f9e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="16f9e-127">DataType</span><span class="sxs-lookup"><span data-stu-id="16f9e-127">DataType</span></span><br/>     | <span data-ttu-id="16f9e-128">Stringa</span><span class="sxs-lookup"><span data-stu-id="16f9e-128">String</span></span><br/>  | <span data-ttu-id="16f9e-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="16f9e-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="16f9e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="16f9e-130">DefaultValue</span></span><br/> | <span data-ttu-id="16f9e-131">Intero</span><span class="sxs-lookup"><span data-stu-id="16f9e-131">Integer</span></span><br/> | <span data-ttu-id="16f9e-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="16f9e-132">undefined</span></span><br/>       |
| <span data-ttu-id="16f9e-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="16f9e-133">MaxValue</span></span><br/>     | <span data-ttu-id="16f9e-134">Intero</span><span class="sxs-lookup"><span data-stu-id="16f9e-134">Integer</span></span><br/> | <span data-ttu-id="16f9e-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="16f9e-135">undefined</span></span><br/>       |
| <span data-ttu-id="16f9e-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="16f9e-136">MinValue</span></span><br/>     | <span data-ttu-id="16f9e-137">Integer</span><span class="sxs-lookup"><span data-stu-id="16f9e-137">Integer</span></span><br/> | <span data-ttu-id="16f9e-138">1</span><span class="sxs-lookup"><span data-stu-id="16f9e-138">1</span></span><br/>               |
| <span data-ttu-id="16f9e-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="16f9e-139">Mandatory</span></span><br/>    | <span data-ttu-id="16f9e-140">Stringa</span><span class="sxs-lookup"><span data-stu-id="16f9e-140">String</span></span><br/>  | <span data-ttu-id="16f9e-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="16f9e-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="16f9e-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="16f9e-142">Multiple</span></span><br/>     | <span data-ttu-id="16f9e-143">Integer</span><span class="sxs-lookup"><span data-stu-id="16f9e-143">Integer</span></span><br/> | <span data-ttu-id="16f9e-144">1</span><span class="sxs-lookup"><span data-stu-id="16f9e-144">1</span></span><br/>               |
| <span data-ttu-id="16f9e-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="16f9e-145">UnitType</span></span><br/>     | <span data-ttu-id="16f9e-146">Stringa</span><span class="sxs-lookup"><span data-stu-id="16f9e-146">String</span></span><br/>  | <span data-ttu-id="16f9e-147">percent</span><span class="sxs-lookup"><span data-stu-id="16f9e-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="16f9e-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16f9e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16f9e-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="16f9e-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




