---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996878"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="5570c-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="5570c-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="5570c-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5570c-105">This topic is not current.</span></span> <span data-ttu-id="5570c-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5570c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5570c-107">Specifica la trasparenza per la filigrana.</span><span class="sxs-lookup"><span data-stu-id="5570c-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="5570c-108">Completamente opaco avrebbe un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="5570c-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="5570c-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5570c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5570c-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5570c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5570c-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5570c-111">Element Information</span></span>



| <span data-ttu-id="5570c-112">Nome</span><span class="sxs-lookup"><span data-stu-id="5570c-112">Name</span></span> | <span data-ttu-id="5570c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5570c-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="5570c-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5570c-114">Element Type</span></span> <br/>   | <span data-ttu-id="5570c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5570c-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="5570c-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5570c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5570c-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="5570c-117">Page</span></span><br/>                            |
| <span data-ttu-id="5570c-118">Note</span><span class="sxs-lookup"><span data-stu-id="5570c-118">Notes</span></span> <br/>          | <span data-ttu-id="5570c-119">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="5570c-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5570c-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5570c-120">Structure Content</span></span>

<span data-ttu-id="5570c-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="5570c-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5570c-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="5570c-122">Structure Properties</span></span>

<span data-ttu-id="5570c-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5570c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5570c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5570c-124">Property</span></span>                | <span data-ttu-id="5570c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5570c-125">xsi:type</span></span>           | <span data-ttu-id="5570c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5570c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5570c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5570c-127">DataType</span></span><br/>     | <span data-ttu-id="5570c-128">string</span><span class="sxs-lookup"><span data-stu-id="5570c-128">string</span></span><br/>  | <span data-ttu-id="5570c-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5570c-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="5570c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5570c-130">DefaultValue</span></span><br/> | <span data-ttu-id="5570c-131">integer</span><span class="sxs-lookup"><span data-stu-id="5570c-131">integer</span></span><br/> | <span data-ttu-id="5570c-132">0</span><span class="sxs-lookup"><span data-stu-id="5570c-132">0</span></span><br/>               |
| <span data-ttu-id="5570c-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5570c-133">MaxValue</span></span><br/>     | <span data-ttu-id="5570c-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="5570c-134">integer</span></span><br/> | <span data-ttu-id="5570c-135">100</span><span class="sxs-lookup"><span data-stu-id="5570c-135">100</span></span><br/>             |
| <span data-ttu-id="5570c-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="5570c-136">MinValue</span></span><br/>     | <span data-ttu-id="5570c-137">integer</span><span class="sxs-lookup"><span data-stu-id="5570c-137">integer</span></span><br/> | <span data-ttu-id="5570c-138">0</span><span class="sxs-lookup"><span data-stu-id="5570c-138">0</span></span><br/>               |
| <span data-ttu-id="5570c-139">Più elementi</span><span class="sxs-lookup"><span data-stu-id="5570c-139">Multiple</span></span><br/>     | <span data-ttu-id="5570c-140">integer</span><span class="sxs-lookup"><span data-stu-id="5570c-140">integer</span></span><br/> | <span data-ttu-id="5570c-141">1</span><span class="sxs-lookup"><span data-stu-id="5570c-141">1</span></span><br/>               |
| <span data-ttu-id="5570c-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="5570c-142">Mandatory</span></span><br/>    | <span data-ttu-id="5570c-143">string</span><span class="sxs-lookup"><span data-stu-id="5570c-143">string</span></span><br/>  | <span data-ttu-id="5570c-144">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="5570c-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5570c-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="5570c-145">UnitType</span></span><br/>     | <span data-ttu-id="5570c-146">string</span><span class="sxs-lookup"><span data-stu-id="5570c-146">string</span></span><br/>  | <span data-ttu-id="5570c-147">percent</span><span class="sxs-lookup"><span data-stu-id="5570c-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5570c-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5570c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5570c-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5570c-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




