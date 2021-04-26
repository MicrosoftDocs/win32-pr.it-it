---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cc8c7f3c9a692ffbe180c253d448d7c4e320d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999128"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="0a5e5-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="0a5e5-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="0a5e5-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-105">This topic is not current.</span></span> <span data-ttu-id="0a5e5-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a5e5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a5e5-107">Definisce le dimensioni dei caratteri disponibili per il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="0a5e5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a5e5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0a5e5-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0a5e5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0a5e5-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a5e5-110">Element Information</span></span>



| <span data-ttu-id="0a5e5-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0a5e5-111">Name</span></span> | <span data-ttu-id="0a5e5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5e5-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="0a5e5-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0a5e5-113">Element Type</span></span> <br/>   | <span data-ttu-id="0a5e5-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0a5e5-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="0a5e5-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0a5e5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a5e5-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="0a5e5-116">Page</span></span><br/>                            |
| <span data-ttu-id="0a5e5-117">Note</span><span class="sxs-lookup"><span data-stu-id="0a5e5-117">Notes</span></span> <br/>          | <span data-ttu-id="0a5e5-118">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="0a5e5-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0a5e5-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0a5e5-119">Structure Content</span></span>

<span data-ttu-id="0a5e5-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="0a5e5-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0a5e5-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="0a5e5-121">Structure Properties</span></span>

<span data-ttu-id="0a5e5-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a5e5-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a5e5-123">Property</span></span>                | <span data-ttu-id="0a5e5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0a5e5-124">xsi:type</span></span>           | <span data-ttu-id="0a5e5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5e5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0a5e5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="0a5e5-126">DataType</span></span><br/>     | <span data-ttu-id="0a5e5-127">string</span><span class="sxs-lookup"><span data-stu-id="0a5e5-127">string</span></span><br/>  | <span data-ttu-id="0a5e5-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0a5e5-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="0a5e5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0a5e5-129">DefaultValue</span></span><br/> | <span data-ttu-id="0a5e5-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="0a5e5-130">integer</span></span><br/> | <span data-ttu-id="0a5e5-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="0a5e5-131">undefined</span></span><br/>       |
| <span data-ttu-id="0a5e5-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0a5e5-132">MaxValue</span></span><br/>     | <span data-ttu-id="0a5e5-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="0a5e5-133">integer</span></span><br/> | <span data-ttu-id="0a5e5-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="0a5e5-134">undefined</span></span><br/>       |
| <span data-ttu-id="0a5e5-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="0a5e5-135">MinValue</span></span><br/>     | <span data-ttu-id="0a5e5-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="0a5e5-136">integer</span></span><br/> | <span data-ttu-id="0a5e5-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="0a5e5-137">undefined</span></span><br/>       |
| <span data-ttu-id="0a5e5-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="0a5e5-138">Multiple</span></span><br/>     | <span data-ttu-id="0a5e5-139">numero intero</span><span class="sxs-lookup"><span data-stu-id="0a5e5-139">integer</span></span><br/> | <span data-ttu-id="0a5e5-140">Non definito</span><span class="sxs-lookup"><span data-stu-id="0a5e5-140">undefined</span></span><br/>       |
| <span data-ttu-id="0a5e5-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0a5e5-141">Mandatory</span></span><br/>    | <span data-ttu-id="0a5e5-142">string</span><span class="sxs-lookup"><span data-stu-id="0a5e5-142">string</span></span><br/>  | <span data-ttu-id="0a5e5-143">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="0a5e5-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0a5e5-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="0a5e5-144">UnitType</span></span><br/>     | <span data-ttu-id="0a5e5-145">string</span><span class="sxs-lookup"><span data-stu-id="0a5e5-145">string</span></span><br/>  | <span data-ttu-id="0a5e5-146">punti</span><span class="sxs-lookup"><span data-stu-id="0a5e5-146">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="0a5e5-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a5e5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a5e5-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0a5e5-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




