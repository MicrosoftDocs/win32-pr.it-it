---
description: Ottenere informazioni sul parametro PageWatermarkTransparency. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394786"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="c5b85-105">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="c5b85-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="c5b85-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c5b85-106">This topic is not current.</span></span> <span data-ttu-id="c5b85-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c5b85-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5b85-108">Specifica la trasparenza per la filigrana.</span><span class="sxs-lookup"><span data-stu-id="c5b85-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="c5b85-109">Completamente opaco avrebbe un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="c5b85-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="c5b85-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c5b85-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c5b85-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c5b85-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c5b85-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c5b85-112">Element Information</span></span>



| <span data-ttu-id="c5b85-113">Nome</span><span class="sxs-lookup"><span data-stu-id="c5b85-113">Name</span></span> | <span data-ttu-id="c5b85-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c5b85-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="c5b85-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c5b85-115">Element Type</span></span> <br/>   | <span data-ttu-id="c5b85-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c5b85-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="c5b85-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="c5b85-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c5b85-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="c5b85-118">Page</span></span><br/>                            |
| <span data-ttu-id="c5b85-119">Note</span><span class="sxs-lookup"><span data-stu-id="c5b85-119">Notes</span></span> <br/>          | <span data-ttu-id="c5b85-120">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="c5b85-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c5b85-121">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c5b85-121">Structure Content</span></span>

<span data-ttu-id="c5b85-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c5b85-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="c5b85-123">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="c5b85-123">Structure Properties</span></span>

<span data-ttu-id="c5b85-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c5b85-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c5b85-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5b85-125">Property</span></span>                | <span data-ttu-id="c5b85-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c5b85-126">xsi:type</span></span>           | <span data-ttu-id="c5b85-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c5b85-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c5b85-128">DataType</span><span class="sxs-lookup"><span data-stu-id="c5b85-128">DataType</span></span><br/>     | <span data-ttu-id="c5b85-129">string</span><span class="sxs-lookup"><span data-stu-id="c5b85-129">string</span></span><br/>  | <span data-ttu-id="c5b85-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c5b85-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="c5b85-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c5b85-131">DefaultValue</span></span><br/> | <span data-ttu-id="c5b85-132">integer</span><span class="sxs-lookup"><span data-stu-id="c5b85-132">integer</span></span><br/> | <span data-ttu-id="c5b85-133">0</span><span class="sxs-lookup"><span data-stu-id="c5b85-133">0</span></span><br/>               |
| <span data-ttu-id="c5b85-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c5b85-134">MaxValue</span></span><br/>     | <span data-ttu-id="c5b85-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="c5b85-135">integer</span></span><br/> | <span data-ttu-id="c5b85-136">100</span><span class="sxs-lookup"><span data-stu-id="c5b85-136">100</span></span><br/>             |
| <span data-ttu-id="c5b85-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="c5b85-137">MinValue</span></span><br/>     | <span data-ttu-id="c5b85-138">integer</span><span class="sxs-lookup"><span data-stu-id="c5b85-138">integer</span></span><br/> | <span data-ttu-id="c5b85-139">0</span><span class="sxs-lookup"><span data-stu-id="c5b85-139">0</span></span><br/>               |
| <span data-ttu-id="c5b85-140">Multipli</span><span class="sxs-lookup"><span data-stu-id="c5b85-140">Multiple</span></span><br/>     | <span data-ttu-id="c5b85-141">integer</span><span class="sxs-lookup"><span data-stu-id="c5b85-141">integer</span></span><br/> | <span data-ttu-id="c5b85-142">1</span><span class="sxs-lookup"><span data-stu-id="c5b85-142">1</span></span><br/>               |
| <span data-ttu-id="c5b85-143">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c5b85-143">Mandatory</span></span><br/>    | <span data-ttu-id="c5b85-144">string</span><span class="sxs-lookup"><span data-stu-id="c5b85-144">string</span></span><br/>  | <span data-ttu-id="c5b85-145">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="c5b85-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c5b85-146">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="c5b85-146">UnitType</span></span><br/>     | <span data-ttu-id="c5b85-147">string</span><span class="sxs-lookup"><span data-stu-id="c5b85-147">string</span></span><br/>  | <span data-ttu-id="c5b85-148">percent</span><span class="sxs-lookup"><span data-stu-id="c5b85-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c5b85-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5b85-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5b85-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c5b85-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




