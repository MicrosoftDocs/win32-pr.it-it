---
description: Ottenere informazioni sul parametro PageScalingOffsetHeight. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f02370d28716dd3a8840001959bb7d963307d2f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548959"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="9b6e0-105">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="9b6e0-105">PageScalingOffsetHeight</span></span>

<span data-ttu-id="9b6e0-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-106">This topic is not current.</span></span> <span data-ttu-id="9b6e0-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b6e0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b6e0-108">Specifica l'offset di ridimensionamento nella direzione ImageableSizeHeight per il ridimensionamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-108">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="9b6e0-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9b6e0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9b6e0-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="9b6e0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9b6e0-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9b6e0-111">Element Information</span></span>



| <span data-ttu-id="9b6e0-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9b6e0-112">Name</span></span> | <span data-ttu-id="9b6e0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9b6e0-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="9b6e0-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="9b6e0-114">Element Type</span></span> <br/>   | <span data-ttu-id="9b6e0-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9b6e0-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="9b6e0-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="9b6e0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9b6e0-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="9b6e0-117">Page</span></span><br/>                                         |
| <span data-ttu-id="9b6e0-118">Note</span><span class="sxs-lookup"><span data-stu-id="9b6e0-118">Notes</span></span> <br/>          | <span data-ttu-id="9b6e0-119">Collegato all'elemento PageScaling, opzione Custom</span><span class="sxs-lookup"><span data-stu-id="9b6e0-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9b6e0-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="9b6e0-120">Structure Content</span></span>

<span data-ttu-id="9b6e0-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9b6e0-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="9b6e0-122">Structure Properties</span></span>

<span data-ttu-id="9b6e0-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9b6e0-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b6e0-124">Property</span></span>                | <span data-ttu-id="9b6e0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9b6e0-125">xsi:type</span></span>           | <span data-ttu-id="9b6e0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9b6e0-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9b6e0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="9b6e0-127">DataType</span></span><br/>     | <span data-ttu-id="9b6e0-128">string</span><span class="sxs-lookup"><span data-stu-id="9b6e0-128">string</span></span><br/>  | <span data-ttu-id="9b6e0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9b6e0-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="9b6e0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9b6e0-130">DefaultValue</span></span><br/> | <span data-ttu-id="9b6e0-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="9b6e0-131">integer</span></span><br/> | <span data-ttu-id="9b6e0-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="9b6e0-132">undefined</span></span><br/>       |
| <span data-ttu-id="9b6e0-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9b6e0-133">MaxValue</span></span><br/>     | <span data-ttu-id="9b6e0-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="9b6e0-134">integer</span></span><br/> | <span data-ttu-id="9b6e0-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="9b6e0-135">undefined</span></span><br/>       |
| <span data-ttu-id="9b6e0-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="9b6e0-136">MinValue</span></span><br/>     | <span data-ttu-id="9b6e0-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="9b6e0-137">integer</span></span><br/> | <span data-ttu-id="9b6e0-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="9b6e0-138">undefined</span></span><br/>       |
| <span data-ttu-id="9b6e0-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9b6e0-139">Mandatory</span></span><br/>    | <span data-ttu-id="9b6e0-140">string</span><span class="sxs-lookup"><span data-stu-id="9b6e0-140">string</span></span><br/>  | <span data-ttu-id="9b6e0-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="9b6e0-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9b6e0-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="9b6e0-142">Multiple</span></span><br/>     | <span data-ttu-id="9b6e0-143">integer</span><span class="sxs-lookup"><span data-stu-id="9b6e0-143">integer</span></span><br/> | <span data-ttu-id="9b6e0-144">1</span><span class="sxs-lookup"><span data-stu-id="9b6e0-144">1</span></span><br/>               |
| <span data-ttu-id="9b6e0-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="9b6e0-145">UnitType</span></span><br/>     | <span data-ttu-id="9b6e0-146">string</span><span class="sxs-lookup"><span data-stu-id="9b6e0-146">string</span></span><br/>  | <span data-ttu-id="9b6e0-147">Micron</span><span class="sxs-lookup"><span data-stu-id="9b6e0-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="9b6e0-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b6e0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b6e0-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9b6e0-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




