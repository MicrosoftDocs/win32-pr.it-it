---
description: Ottenere informazioni sul parametro PageMediaSizeMediaSizeHeight. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395796"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="98b0d-105">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="98b0d-105">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="98b0d-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="98b0d-106">This topic is not current.</span></span> <span data-ttu-id="98b0d-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="98b0d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98b0d-108">Specifica la direzione mediasizeheight della dimensione per l'opzione MediaSize personalizzata.</span><span class="sxs-lookup"><span data-stu-id="98b0d-108">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="98b0d-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="98b0d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="98b0d-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="98b0d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="98b0d-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="98b0d-111">Element Information</span></span>



| <span data-ttu-id="98b0d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="98b0d-112">Name</span></span> | <span data-ttu-id="98b0d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="98b0d-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="98b0d-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="98b0d-114">Element Type</span></span> <br/>   | <span data-ttu-id="98b0d-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="98b0d-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="98b0d-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="98b0d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="98b0d-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="98b0d-117">Page</span></span><br/>                                           |
| <span data-ttu-id="98b0d-118">Note</span><span class="sxs-lookup"><span data-stu-id="98b0d-118">Notes</span></span> <br/>          | <span data-ttu-id="98b0d-119">Collegato all'elemento PageMediaSize, opzione Custom</span><span class="sxs-lookup"><span data-stu-id="98b0d-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="98b0d-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="98b0d-120">Structure Content</span></span>

<span data-ttu-id="98b0d-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="98b0d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="98b0d-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="98b0d-122">Structure Properties</span></span>

<span data-ttu-id="98b0d-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="98b0d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="98b0d-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98b0d-124">Property</span></span>                | <span data-ttu-id="98b0d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="98b0d-125">xsi:type</span></span>           | <span data-ttu-id="98b0d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="98b0d-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="98b0d-127">DataType</span><span class="sxs-lookup"><span data-stu-id="98b0d-127">DataType</span></span><br/>     | <span data-ttu-id="98b0d-128">string</span><span class="sxs-lookup"><span data-stu-id="98b0d-128">string</span></span><br/>  | <span data-ttu-id="98b0d-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="98b0d-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="98b0d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="98b0d-130">DefaultValue</span></span><br/> | <span data-ttu-id="98b0d-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="98b0d-131">integer</span></span><br/> | <span data-ttu-id="98b0d-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="98b0d-132">undefined</span></span><br/>       |
| <span data-ttu-id="98b0d-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="98b0d-133">MaxValue</span></span><br/>     | <span data-ttu-id="98b0d-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="98b0d-134">integer</span></span><br/> | <span data-ttu-id="98b0d-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="98b0d-135">undefined</span></span><br/>       |
| <span data-ttu-id="98b0d-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="98b0d-136">MinValue</span></span><br/>     | <span data-ttu-id="98b0d-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="98b0d-137">integer</span></span><br/> | <span data-ttu-id="98b0d-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="98b0d-138">undefined</span></span><br/>       |
| <span data-ttu-id="98b0d-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="98b0d-139">Mandatory</span></span><br/>    | <span data-ttu-id="98b0d-140">string</span><span class="sxs-lookup"><span data-stu-id="98b0d-140">string</span></span><br/>  | <span data-ttu-id="98b0d-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="98b0d-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="98b0d-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="98b0d-142">Multiple</span></span><br/>     | <span data-ttu-id="98b0d-143">integer</span><span class="sxs-lookup"><span data-stu-id="98b0d-143">integer</span></span><br/> | <span data-ttu-id="98b0d-144">1</span><span class="sxs-lookup"><span data-stu-id="98b0d-144">1</span></span><br/>               |
| <span data-ttu-id="98b0d-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="98b0d-145">UnitType</span></span><br/>     | <span data-ttu-id="98b0d-146">string</span><span class="sxs-lookup"><span data-stu-id="98b0d-146">string</span></span><br/>  | <span data-ttu-id="98b0d-147">Micron</span><span class="sxs-lookup"><span data-stu-id="98b0d-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="98b0d-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98b0d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98b0d-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="98b0d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




