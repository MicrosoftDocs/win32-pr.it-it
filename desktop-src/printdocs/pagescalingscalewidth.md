---
description: Ottenere informazioni sul parametro PageScalingScaleWidth. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6180395eb656ee40d8558f7208fec2ad2fce8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548799"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="7d995-105">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="7d995-105">PageScalingScaleWidth</span></span>

<span data-ttu-id="7d995-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7d995-106">This topic is not current.</span></span> <span data-ttu-id="7d995-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7d995-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7d995-108">Specifica il fattore di scala nella direzione ImageableSizeWidth per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7d995-108">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="7d995-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7d995-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7d995-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7d995-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7d995-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7d995-111">Element Information</span></span>



| <span data-ttu-id="7d995-112">Nome</span><span class="sxs-lookup"><span data-stu-id="7d995-112">Name</span></span> | <span data-ttu-id="7d995-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7d995-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="7d995-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7d995-114">Element Type</span></span> <br/>   | <span data-ttu-id="7d995-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7d995-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="7d995-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7d995-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7d995-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="7d995-117">Page</span></span><br/>                                         |
| <span data-ttu-id="7d995-118">Note</span><span class="sxs-lookup"><span data-stu-id="7d995-118">Notes</span></span> <br/>          | <span data-ttu-id="7d995-119">Collegato all'elemento PageScaling, opzione Personalizzata</span><span class="sxs-lookup"><span data-stu-id="7d995-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7d995-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7d995-120">Structure Content</span></span>

<span data-ttu-id="7d995-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7d995-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="7d995-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="7d995-122">Structure Properties</span></span>

<span data-ttu-id="7d995-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7d995-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7d995-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d995-124">Property</span></span>                | <span data-ttu-id="7d995-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7d995-125">xsi:type</span></span>           | <span data-ttu-id="7d995-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7d995-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7d995-127">DataType</span><span class="sxs-lookup"><span data-stu-id="7d995-127">DataType</span></span><br/>     | <span data-ttu-id="7d995-128">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d995-128">String</span></span><br/>  | <span data-ttu-id="7d995-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7d995-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="7d995-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7d995-130">DefaultValue</span></span><br/> | <span data-ttu-id="7d995-131">Intero</span><span class="sxs-lookup"><span data-stu-id="7d995-131">Integer</span></span><br/> | <span data-ttu-id="7d995-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="7d995-132">undefined</span></span><br/>       |
| <span data-ttu-id="7d995-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7d995-133">MaxValue</span></span><br/>     | <span data-ttu-id="7d995-134">Intero</span><span class="sxs-lookup"><span data-stu-id="7d995-134">Integer</span></span><br/> | <span data-ttu-id="7d995-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="7d995-135">undefined</span></span><br/>       |
| <span data-ttu-id="7d995-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="7d995-136">MinValue</span></span><br/>     | <span data-ttu-id="7d995-137">Integer</span><span class="sxs-lookup"><span data-stu-id="7d995-137">Integer</span></span><br/> | <span data-ttu-id="7d995-138">1</span><span class="sxs-lookup"><span data-stu-id="7d995-138">1</span></span><br/>               |
| <span data-ttu-id="7d995-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7d995-139">Mandatory</span></span><br/>    | <span data-ttu-id="7d995-140">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d995-140">String</span></span><br/>  | <span data-ttu-id="7d995-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7d995-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7d995-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="7d995-142">Multiple</span></span><br/>     | <span data-ttu-id="7d995-143">Integer</span><span class="sxs-lookup"><span data-stu-id="7d995-143">Integer</span></span><br/> | <span data-ttu-id="7d995-144">1</span><span class="sxs-lookup"><span data-stu-id="7d995-144">1</span></span><br/>               |
| <span data-ttu-id="7d995-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="7d995-145">UnitType</span></span><br/>     | <span data-ttu-id="7d995-146">Stringa</span><span class="sxs-lookup"><span data-stu-id="7d995-146">String</span></span><br/>  | <span data-ttu-id="7d995-147">Micron</span><span class="sxs-lookup"><span data-stu-id="7d995-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7d995-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d995-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d995-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7d995-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




