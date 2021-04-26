---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ef53d9fe2906ae04cd1e7e3ea1513a631bc162
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997458"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="0b29b-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="0b29b-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="0b29b-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0b29b-105">This topic is not current.</span></span> <span data-ttu-id="0b29b-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0b29b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0b29b-107">Specifica il fattore di scala nella direzione ImageableSizeWidth per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0b29b-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="0b29b-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0b29b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0b29b-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0b29b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0b29b-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0b29b-110">Element Information</span></span>



| <span data-ttu-id="0b29b-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0b29b-111">Name</span></span> | <span data-ttu-id="0b29b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0b29b-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="0b29b-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0b29b-113">Element Type</span></span> <br/>   | <span data-ttu-id="0b29b-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0b29b-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="0b29b-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0b29b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0b29b-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="0b29b-116">Page</span></span><br/>                                         |
| <span data-ttu-id="0b29b-117">Note</span><span class="sxs-lookup"><span data-stu-id="0b29b-117">Notes</span></span> <br/>          | <span data-ttu-id="0b29b-118">Collegato all'elemento PageScaling, opzione Personalizzata</span><span class="sxs-lookup"><span data-stu-id="0b29b-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0b29b-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0b29b-119">Structure Content</span></span>

<span data-ttu-id="0b29b-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0b29b-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0b29b-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="0b29b-121">Structure Properties</span></span>

<span data-ttu-id="0b29b-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0b29b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0b29b-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b29b-123">Property</span></span>                | <span data-ttu-id="0b29b-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0b29b-124">xsi:type</span></span>           | <span data-ttu-id="0b29b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0b29b-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0b29b-126">DataType</span><span class="sxs-lookup"><span data-stu-id="0b29b-126">DataType</span></span><br/>     | <span data-ttu-id="0b29b-127">Stringa</span><span class="sxs-lookup"><span data-stu-id="0b29b-127">String</span></span><br/>  | <span data-ttu-id="0b29b-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0b29b-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="0b29b-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0b29b-129">DefaultValue</span></span><br/> | <span data-ttu-id="0b29b-130">Intero</span><span class="sxs-lookup"><span data-stu-id="0b29b-130">Integer</span></span><br/> | <span data-ttu-id="0b29b-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="0b29b-131">undefined</span></span><br/>       |
| <span data-ttu-id="0b29b-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0b29b-132">MaxValue</span></span><br/>     | <span data-ttu-id="0b29b-133">Intero</span><span class="sxs-lookup"><span data-stu-id="0b29b-133">Integer</span></span><br/> | <span data-ttu-id="0b29b-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="0b29b-134">undefined</span></span><br/>       |
| <span data-ttu-id="0b29b-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="0b29b-135">MinValue</span></span><br/>     | <span data-ttu-id="0b29b-136">Integer</span><span class="sxs-lookup"><span data-stu-id="0b29b-136">Integer</span></span><br/> | <span data-ttu-id="0b29b-137">1</span><span class="sxs-lookup"><span data-stu-id="0b29b-137">1</span></span><br/>               |
| <span data-ttu-id="0b29b-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0b29b-138">Mandatory</span></span><br/>    | <span data-ttu-id="0b29b-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="0b29b-139">String</span></span><br/>  | <span data-ttu-id="0b29b-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0b29b-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0b29b-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="0b29b-141">Multiple</span></span><br/>     | <span data-ttu-id="0b29b-142">Integer</span><span class="sxs-lookup"><span data-stu-id="0b29b-142">Integer</span></span><br/> | <span data-ttu-id="0b29b-143">1</span><span class="sxs-lookup"><span data-stu-id="0b29b-143">1</span></span><br/>               |
| <span data-ttu-id="0b29b-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="0b29b-144">UnitType</span></span><br/>     | <span data-ttu-id="0b29b-145">Stringa</span><span class="sxs-lookup"><span data-stu-id="0b29b-145">String</span></span><br/>  | <span data-ttu-id="0b29b-146">Micron</span><span class="sxs-lookup"><span data-stu-id="0b29b-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0b29b-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b29b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b29b-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0b29b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




