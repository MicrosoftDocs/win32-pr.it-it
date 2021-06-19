---
description: Ottenere informazioni sul parametro PageWatermarkTextFontSize. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395996"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="3af8f-105">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="3af8f-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="3af8f-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="3af8f-106">This topic is not current.</span></span> <span data-ttu-id="3af8f-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3af8f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3af8f-108">Definisce le dimensioni dei caratteri disponibili per il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="3af8f-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="3af8f-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3af8f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3af8f-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="3af8f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3af8f-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3af8f-111">Element Information</span></span>



| <span data-ttu-id="3af8f-112">Nome</span><span class="sxs-lookup"><span data-stu-id="3af8f-112">Name</span></span> | <span data-ttu-id="3af8f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3af8f-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="3af8f-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="3af8f-114">Element Type</span></span> <br/>   | <span data-ttu-id="3af8f-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3af8f-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="3af8f-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="3af8f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3af8f-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="3af8f-117">Page</span></span><br/>                            |
| <span data-ttu-id="3af8f-118">Note</span><span class="sxs-lookup"><span data-stu-id="3af8f-118">Notes</span></span> <br/>          | <span data-ttu-id="3af8f-119">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="3af8f-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3af8f-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="3af8f-120">Structure Content</span></span>

<span data-ttu-id="3af8f-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="3af8f-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="3af8f-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="3af8f-122">Structure Properties</span></span>

<span data-ttu-id="3af8f-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="3af8f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3af8f-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3af8f-124">Property</span></span>                | <span data-ttu-id="3af8f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3af8f-125">xsi:type</span></span>           | <span data-ttu-id="3af8f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3af8f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3af8f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="3af8f-127">DataType</span></span><br/>     | <span data-ttu-id="3af8f-128">string</span><span class="sxs-lookup"><span data-stu-id="3af8f-128">string</span></span><br/>  | <span data-ttu-id="3af8f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3af8f-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="3af8f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3af8f-130">DefaultValue</span></span><br/> | <span data-ttu-id="3af8f-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="3af8f-131">integer</span></span><br/> | <span data-ttu-id="3af8f-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="3af8f-132">undefined</span></span><br/>       |
| <span data-ttu-id="3af8f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3af8f-133">MaxValue</span></span><br/>     | <span data-ttu-id="3af8f-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="3af8f-134">integer</span></span><br/> | <span data-ttu-id="3af8f-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="3af8f-135">undefined</span></span><br/>       |
| <span data-ttu-id="3af8f-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="3af8f-136">MinValue</span></span><br/>     | <span data-ttu-id="3af8f-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="3af8f-137">integer</span></span><br/> | <span data-ttu-id="3af8f-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="3af8f-138">undefined</span></span><br/>       |
| <span data-ttu-id="3af8f-139">Multipli</span><span class="sxs-lookup"><span data-stu-id="3af8f-139">Multiple</span></span><br/>     | <span data-ttu-id="3af8f-140">numero intero</span><span class="sxs-lookup"><span data-stu-id="3af8f-140">integer</span></span><br/> | <span data-ttu-id="3af8f-141">Non definito</span><span class="sxs-lookup"><span data-stu-id="3af8f-141">undefined</span></span><br/>       |
| <span data-ttu-id="3af8f-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="3af8f-142">Mandatory</span></span><br/>    | <span data-ttu-id="3af8f-143">string</span><span class="sxs-lookup"><span data-stu-id="3af8f-143">string</span></span><br/>  | <span data-ttu-id="3af8f-144">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="3af8f-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3af8f-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="3af8f-145">UnitType</span></span><br/>     | <span data-ttu-id="3af8f-146">string</span><span class="sxs-lookup"><span data-stu-id="3af8f-146">string</span></span><br/>  | <span data-ttu-id="3af8f-147">punti</span><span class="sxs-lookup"><span data-stu-id="3af8f-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="3af8f-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3af8f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3af8f-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3af8f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




