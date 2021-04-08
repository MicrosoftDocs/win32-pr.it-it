---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058488"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="c5723-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="c5723-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="c5723-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c5723-105">This topic is not current.</span></span> <span data-ttu-id="c5723-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c5723-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5723-107">Definisce le dimensioni dei caratteri disponibili per il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="c5723-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="c5723-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c5723-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c5723-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c5723-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c5723-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c5723-110">Element Information</span></span>



| <span data-ttu-id="c5723-111">Nome</span><span class="sxs-lookup"><span data-stu-id="c5723-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="c5723-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c5723-112">Element Type</span></span> <br/>   | <span data-ttu-id="c5723-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c5723-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="c5723-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="c5723-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c5723-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="c5723-115">Page</span></span><br/>                            |
| <span data-ttu-id="c5723-116">Note</span><span class="sxs-lookup"><span data-stu-id="c5723-116">Notes</span></span> <br/>          | <span data-ttu-id="c5723-117">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="c5723-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c5723-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c5723-118">Structure Content</span></span>

<span data-ttu-id="c5723-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c5723-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c5723-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="c5723-120">Structure Properties</span></span>

<span data-ttu-id="c5723-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c5723-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c5723-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5723-122">Property</span></span>                | <span data-ttu-id="c5723-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c5723-123">xsi:type</span></span>           | <span data-ttu-id="c5723-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c5723-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c5723-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c5723-125">DataType</span></span><br/>     | <span data-ttu-id="c5723-126">string</span><span class="sxs-lookup"><span data-stu-id="c5723-126">string</span></span><br/>  | <span data-ttu-id="c5723-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c5723-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="c5723-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c5723-128">DefaultValue</span></span><br/> | <span data-ttu-id="c5723-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="c5723-129">integer</span></span><br/> | <span data-ttu-id="c5723-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="c5723-130">undefined</span></span><br/>       |
| <span data-ttu-id="c5723-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c5723-131">MaxValue</span></span><br/>     | <span data-ttu-id="c5723-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="c5723-132">integer</span></span><br/> | <span data-ttu-id="c5723-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="c5723-133">undefined</span></span><br/>       |
| <span data-ttu-id="c5723-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="c5723-134">MinValue</span></span><br/>     | <span data-ttu-id="c5723-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="c5723-135">integer</span></span><br/> | <span data-ttu-id="c5723-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="c5723-136">undefined</span></span><br/>       |
| <span data-ttu-id="c5723-137">Più elementi</span><span class="sxs-lookup"><span data-stu-id="c5723-137">Multiple</span></span><br/>     | <span data-ttu-id="c5723-138">numero intero</span><span class="sxs-lookup"><span data-stu-id="c5723-138">integer</span></span><br/> | <span data-ttu-id="c5723-139">Non definito</span><span class="sxs-lookup"><span data-stu-id="c5723-139">undefined</span></span><br/>       |
| <span data-ttu-id="c5723-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c5723-140">Mandatory</span></span><br/>    | <span data-ttu-id="c5723-141">string</span><span class="sxs-lookup"><span data-stu-id="c5723-141">string</span></span><br/>  | <span data-ttu-id="c5723-142">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="c5723-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c5723-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="c5723-143">UnitType</span></span><br/>     | <span data-ttu-id="c5723-144">string</span><span class="sxs-lookup"><span data-stu-id="c5723-144">string</span></span><br/>  | <span data-ttu-id="c5723-145">punti</span><span class="sxs-lookup"><span data-stu-id="c5723-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="c5723-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5723-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5723-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c5723-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




