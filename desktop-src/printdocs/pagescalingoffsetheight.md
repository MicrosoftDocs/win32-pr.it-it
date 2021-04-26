---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a91178f1506196ab505a90de8bf3a3163fa8a3c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993739"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="1bd74-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="1bd74-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="1bd74-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1bd74-105">This topic is not current.</span></span> <span data-ttu-id="1bd74-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1bd74-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1bd74-107">Specifica l'offset di ridimensionamento nella direzione ImageableSizeHeight per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1bd74-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="1bd74-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1bd74-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bd74-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1bd74-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1bd74-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1bd74-110">Element Information</span></span>



| <span data-ttu-id="1bd74-111">Nome</span><span class="sxs-lookup"><span data-stu-id="1bd74-111">Name</span></span> | <span data-ttu-id="1bd74-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1bd74-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="1bd74-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1bd74-113">Element Type</span></span> <br/>   | <span data-ttu-id="1bd74-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1bd74-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="1bd74-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1bd74-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1bd74-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="1bd74-116">Page</span></span><br/>                                         |
| <span data-ttu-id="1bd74-117">Note</span><span class="sxs-lookup"><span data-stu-id="1bd74-117">Notes</span></span> <br/>          | <span data-ttu-id="1bd74-118">Collegato all'elemento PageScaling, opzione Custom</span><span class="sxs-lookup"><span data-stu-id="1bd74-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1bd74-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1bd74-119">Structure Content</span></span>

<span data-ttu-id="1bd74-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="1bd74-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1bd74-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="1bd74-121">Structure Properties</span></span>

<span data-ttu-id="1bd74-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1bd74-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1bd74-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1bd74-123">Property</span></span>                | <span data-ttu-id="1bd74-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1bd74-124">xsi:type</span></span>           | <span data-ttu-id="1bd74-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1bd74-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1bd74-126">DataType</span><span class="sxs-lookup"><span data-stu-id="1bd74-126">DataType</span></span><br/>     | <span data-ttu-id="1bd74-127">string</span><span class="sxs-lookup"><span data-stu-id="1bd74-127">string</span></span><br/>  | <span data-ttu-id="1bd74-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1bd74-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="1bd74-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1bd74-129">DefaultValue</span></span><br/> | <span data-ttu-id="1bd74-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="1bd74-130">integer</span></span><br/> | <span data-ttu-id="1bd74-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="1bd74-131">undefined</span></span><br/>       |
| <span data-ttu-id="1bd74-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1bd74-132">MaxValue</span></span><br/>     | <span data-ttu-id="1bd74-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="1bd74-133">integer</span></span><br/> | <span data-ttu-id="1bd74-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="1bd74-134">undefined</span></span><br/>       |
| <span data-ttu-id="1bd74-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="1bd74-135">MinValue</span></span><br/>     | <span data-ttu-id="1bd74-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="1bd74-136">integer</span></span><br/> | <span data-ttu-id="1bd74-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="1bd74-137">undefined</span></span><br/>       |
| <span data-ttu-id="1bd74-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="1bd74-138">Mandatory</span></span><br/>    | <span data-ttu-id="1bd74-139">string</span><span class="sxs-lookup"><span data-stu-id="1bd74-139">string</span></span><br/>  | <span data-ttu-id="1bd74-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="1bd74-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1bd74-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="1bd74-141">Multiple</span></span><br/>     | <span data-ttu-id="1bd74-142">integer</span><span class="sxs-lookup"><span data-stu-id="1bd74-142">integer</span></span><br/> | <span data-ttu-id="1bd74-143">1</span><span class="sxs-lookup"><span data-stu-id="1bd74-143">1</span></span><br/>               |
| <span data-ttu-id="1bd74-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="1bd74-144">UnitType</span></span><br/>     | <span data-ttu-id="1bd74-145">string</span><span class="sxs-lookup"><span data-stu-id="1bd74-145">string</span></span><br/>  | <span data-ttu-id="1bd74-146">Micron</span><span class="sxs-lookup"><span data-stu-id="1bd74-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1bd74-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bd74-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd74-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1bd74-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




