---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb576ce7d623f4d036db1332b0339e6cef518d3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320863"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="74c7c-104">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="74c7c-104">PageMediaSizePSHeight</span></span>

<span data-ttu-id="74c7c-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="74c7c-105">This topic is not current.</span></span> <span data-ttu-id="74c7c-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74c7c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74c7c-107">Specifica l'altezza della pagina, in parallelo alla direzione di orientamento del feed (riferimento al [formato del file di descrizione della stampante di PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="74c7c-107">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="74c7c-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="74c7c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="74c7c-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="74c7c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="74c7c-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="74c7c-110">Element Information</span></span>



| <span data-ttu-id="74c7c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="74c7c-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="74c7c-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="74c7c-112">Element Type</span></span> <br/>   | <span data-ttu-id="74c7c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="74c7c-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="74c7c-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="74c7c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="74c7c-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="74c7c-115">Page</span></span><br/>                                             |
| <span data-ttu-id="74c7c-116">Note</span><span class="sxs-lookup"><span data-stu-id="74c7c-116">Notes</span></span> <br/>          | <span data-ttu-id="74c7c-117">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="74c7c-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="74c7c-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="74c7c-118">Structure Content</span></span>

<span data-ttu-id="74c7c-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="74c7c-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="74c7c-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="74c7c-120">Structure Properties</span></span>

<span data-ttu-id="74c7c-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="74c7c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="74c7c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74c7c-122">Property</span></span>                | <span data-ttu-id="74c7c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="74c7c-123">xsi:type</span></span>           | <span data-ttu-id="74c7c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="74c7c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="74c7c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="74c7c-125">DataType</span></span><br/>     | <span data-ttu-id="74c7c-126">string</span><span class="sxs-lookup"><span data-stu-id="74c7c-126">string</span></span><br/>  | <span data-ttu-id="74c7c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="74c7c-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="74c7c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="74c7c-128">DefaultValue</span></span><br/> | <span data-ttu-id="74c7c-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="74c7c-129">integer</span></span><br/> | <span data-ttu-id="74c7c-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="74c7c-130">undefined</span></span><br/>       |
| <span data-ttu-id="74c7c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="74c7c-131">MaxValue</span></span><br/>     | <span data-ttu-id="74c7c-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="74c7c-132">integer</span></span><br/> | <span data-ttu-id="74c7c-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="74c7c-133">undefined</span></span><br/>       |
| <span data-ttu-id="74c7c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="74c7c-134">MinValue</span></span><br/>     | <span data-ttu-id="74c7c-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="74c7c-135">integer</span></span><br/> | <span data-ttu-id="74c7c-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="74c7c-136">undefined</span></span><br/>       |
| <span data-ttu-id="74c7c-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="74c7c-137">Mandatory</span></span><br/>    | <span data-ttu-id="74c7c-138">string</span><span class="sxs-lookup"><span data-stu-id="74c7c-138">string</span></span><br/>  | <span data-ttu-id="74c7c-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="74c7c-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="74c7c-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="74c7c-140">Multiple</span></span><br/>     | <span data-ttu-id="74c7c-141">integer</span><span class="sxs-lookup"><span data-stu-id="74c7c-141">integer</span></span><br/> | <span data-ttu-id="74c7c-142">1</span><span class="sxs-lookup"><span data-stu-id="74c7c-142">1</span></span><br/>               |
| <span data-ttu-id="74c7c-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="74c7c-143">UnitType</span></span><br/>     | <span data-ttu-id="74c7c-144">string</span><span class="sxs-lookup"><span data-stu-id="74c7c-144">string</span></span><br/>  | <span data-ttu-id="74c7c-145">micron</span><span class="sxs-lookup"><span data-stu-id="74c7c-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="74c7c-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74c7c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c7c-147">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="74c7c-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="74c7c-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="74c7c-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




