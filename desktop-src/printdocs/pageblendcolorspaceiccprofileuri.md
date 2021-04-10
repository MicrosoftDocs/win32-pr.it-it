---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058493"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="c090d-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="c090d-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="c090d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c090d-105">This topic is not current.</span></span> <span data-ttu-id="c090d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c090d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c090d-107">Specifica un riferimento URI relativo a un profilo ICC che definisce lo spazio dei colori da utilizzare per la fusione.</span><span class="sxs-lookup"><span data-stu-id="c090d-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="c090d-108"><Uri>È un \_ nome di parte assoluto relativo alla radice del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c090d-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="c090d-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c090d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c090d-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c090d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c090d-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c090d-111">Element Information</span></span>



| <span data-ttu-id="c090d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="c090d-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c090d-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c090d-113">Element Type</span></span> <br/>   | <span data-ttu-id="c090d-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c090d-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="c090d-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="c090d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c090d-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="c090d-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="c090d-117">Note</span><span class="sxs-lookup"><span data-stu-id="c090d-117">Notes</span></span> <br/>          | <span data-ttu-id="c090d-118">Questo vale solo per i documenti XPS e non deve essere utilizzato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="c090d-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="c090d-119">Collegato all'elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="c090d-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c090d-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c090d-120">Structure Content</span></span>

<span data-ttu-id="c090d-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c090d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="c090d-122">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="c090d-122">Structure Properties</span></span>

<span data-ttu-id="c090d-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c090d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c090d-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c090d-124">Property</span></span>                | <span data-ttu-id="c090d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c090d-125">xsi:type</span></span>           | <span data-ttu-id="c090d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c090d-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c090d-127">DataType</span><span class="sxs-lookup"><span data-stu-id="c090d-127">DataType</span></span><br/>     | <span data-ttu-id="c090d-128">string</span><span class="sxs-lookup"><span data-stu-id="c090d-128">string</span></span><br/>  | <span data-ttu-id="c090d-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="c090d-129">xs:string</span></span><br/>       |
| <span data-ttu-id="c090d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c090d-130">DefaultValue</span></span><br/> | <span data-ttu-id="c090d-131">string</span><span class="sxs-lookup"><span data-stu-id="c090d-131">string</span></span><br/>  | <span data-ttu-id="c090d-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="c090d-132">undefined</span></span><br/>       |
| <span data-ttu-id="c090d-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c090d-133">MaxLength</span></span><br/>    | <span data-ttu-id="c090d-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="c090d-134">integer</span></span><br/> | <span data-ttu-id="c090d-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="c090d-135">undefined</span></span><br/>       |
| <span data-ttu-id="c090d-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="c090d-136">MinLength</span></span><br/>    | <span data-ttu-id="c090d-137">integer</span><span class="sxs-lookup"><span data-stu-id="c090d-137">integer</span></span><br/> | <span data-ttu-id="c090d-138">1</span><span class="sxs-lookup"><span data-stu-id="c090d-138">1</span></span><br/>               |
| <span data-ttu-id="c090d-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c090d-139">Mandatory</span></span><br/>    | <span data-ttu-id="c090d-140">string</span><span class="sxs-lookup"><span data-stu-id="c090d-140">string</span></span><br/>  | <span data-ttu-id="c090d-141">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="c090d-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c090d-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="c090d-142">UnitType</span></span><br/>     | <span data-ttu-id="c090d-143">string</span><span class="sxs-lookup"><span data-stu-id="c090d-143">string</span></span><br/>  | <span data-ttu-id="c090d-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="c090d-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c090d-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c090d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c090d-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c090d-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




