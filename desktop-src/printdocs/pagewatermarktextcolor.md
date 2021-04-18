---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104530577"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="707a4-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="707a4-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="707a4-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="707a4-105">This topic is not current.</span></span> <span data-ttu-id="707a4-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="707a4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="707a4-107">Definisce il colore sRGB per il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="707a4-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="707a4-108">Il formato è ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="707a4-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="707a4-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="707a4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="707a4-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="707a4-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="707a4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="707a4-111">Element Information</span></span>



| <span data-ttu-id="707a4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="707a4-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="707a4-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="707a4-113">Element Type</span></span> <br/>   | <span data-ttu-id="707a4-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="707a4-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="707a4-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="707a4-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="707a4-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="707a4-116">Page</span></span><br/>                            |
| <span data-ttu-id="707a4-117">Note</span><span class="sxs-lookup"><span data-stu-id="707a4-117">Notes</span></span> <br/>          | <span data-ttu-id="707a4-118">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="707a4-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="707a4-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="707a4-119">Structure Content</span></span>

<span data-ttu-id="707a4-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="707a4-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="707a4-121">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="707a4-121">Structure Properties</span></span>

<span data-ttu-id="707a4-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="707a4-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="707a4-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="707a4-123">Property</span></span>                | <span data-ttu-id="707a4-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="707a4-124">xsi:type</span></span>           | <span data-ttu-id="707a4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="707a4-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="707a4-126">DataType</span><span class="sxs-lookup"><span data-stu-id="707a4-126">DataType</span></span><br/>     | <span data-ttu-id="707a4-127">string</span><span class="sxs-lookup"><span data-stu-id="707a4-127">string</span></span><br/>  | <span data-ttu-id="707a4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="707a4-128">xs:string</span></span><br/>       |
| <span data-ttu-id="707a4-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="707a4-129">DefaultValue</span></span><br/> | <span data-ttu-id="707a4-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="707a4-130">integer</span></span><br/> | <span data-ttu-id="707a4-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="707a4-131">undefined</span></span><br/>       |
| <span data-ttu-id="707a4-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="707a4-132">MaxValue</span></span><br/>     | <span data-ttu-id="707a4-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="707a4-133">integer</span></span><br/> | <span data-ttu-id="707a4-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="707a4-134">undefined</span></span><br/>       |
| <span data-ttu-id="707a4-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="707a4-135">MinValue</span></span><br/>     | <span data-ttu-id="707a4-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="707a4-136">integer</span></span><br/> | <span data-ttu-id="707a4-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="707a4-137">undefined</span></span><br/>       |
| <span data-ttu-id="707a4-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="707a4-138">Mandatory</span></span><br/>    | <span data-ttu-id="707a4-139">string</span><span class="sxs-lookup"><span data-stu-id="707a4-139">string</span></span><br/>  | <span data-ttu-id="707a4-140">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="707a4-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="707a4-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="707a4-141">UnitType</span></span><br/>     | <span data-ttu-id="707a4-142">string</span><span class="sxs-lookup"><span data-stu-id="707a4-142">string</span></span><br/>  | <span data-ttu-id="707a4-143">sRGB</span><span class="sxs-lookup"><span data-stu-id="707a4-143">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="707a4-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="707a4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="707a4-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="707a4-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




