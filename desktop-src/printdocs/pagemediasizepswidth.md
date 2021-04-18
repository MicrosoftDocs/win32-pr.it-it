---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fef8b9e3740c5f12045e449f2a6b8100d7fc1d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320926"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="b29b7-104">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="b29b7-104">PageMediaSizePSWidth</span></span>

<span data-ttu-id="b29b7-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b29b7-105">This topic is not current.</span></span> <span data-ttu-id="b29b7-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b29b7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b29b7-107">Specifica la larghezza della pagina perpendicolare alla direzione di orientamento del feed (riferimento alla [specifica del formato di file della descrizione della stampante](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf).</span><span class="sxs-lookup"><span data-stu-id="b29b7-107">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="b29b7-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b29b7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b29b7-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b29b7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b29b7-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b29b7-110">Element Information</span></span>



| <span data-ttu-id="b29b7-111">Nome</span><span class="sxs-lookup"><span data-stu-id="b29b7-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b29b7-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b29b7-112">Element Type</span></span> <br/>   | <span data-ttu-id="b29b7-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b29b7-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="b29b7-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="b29b7-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b29b7-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="b29b7-115">Page</span></span><br/>                                             |
| <span data-ttu-id="b29b7-116">Note</span><span class="sxs-lookup"><span data-stu-id="b29b7-116">Notes</span></span> <br/>          | <span data-ttu-id="b29b7-117">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="b29b7-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b29b7-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b29b7-118">Structure Content</span></span>

<span data-ttu-id="b29b7-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b29b7-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="b29b7-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="b29b7-120">Structure Properties</span></span>

<span data-ttu-id="b29b7-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b29b7-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b29b7-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b29b7-122">Property</span></span>                | <span data-ttu-id="b29b7-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b29b7-123">xsi:type</span></span>           | <span data-ttu-id="b29b7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b29b7-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b29b7-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b29b7-125">DataType</span></span><br/>     | <span data-ttu-id="b29b7-126">string</span><span class="sxs-lookup"><span data-stu-id="b29b7-126">string</span></span><br/>  | <span data-ttu-id="b29b7-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b29b7-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b29b7-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b29b7-128">DefaultValue</span></span><br/> | <span data-ttu-id="b29b7-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="b29b7-129">integer</span></span><br/> | <span data-ttu-id="b29b7-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="b29b7-130">undefined</span></span><br/>       |
| <span data-ttu-id="b29b7-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b29b7-131">MaxValue</span></span><br/>     | <span data-ttu-id="b29b7-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="b29b7-132">integer</span></span><br/> | <span data-ttu-id="b29b7-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="b29b7-133">undefined</span></span><br/>       |
| <span data-ttu-id="b29b7-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b29b7-134">MinValue</span></span><br/>     | <span data-ttu-id="b29b7-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="b29b7-135">integer</span></span><br/> | <span data-ttu-id="b29b7-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="b29b7-136">undefined</span></span><br/>       |
| <span data-ttu-id="b29b7-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b29b7-137">Mandatory</span></span><br/>    | <span data-ttu-id="b29b7-138">string</span><span class="sxs-lookup"><span data-stu-id="b29b7-138">string</span></span><br/>  | <span data-ttu-id="b29b7-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="b29b7-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b29b7-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="b29b7-140">Multiple</span></span><br/>     | <span data-ttu-id="b29b7-141">integer</span><span class="sxs-lookup"><span data-stu-id="b29b7-141">integer</span></span><br/> | <span data-ttu-id="b29b7-142">1</span><span class="sxs-lookup"><span data-stu-id="b29b7-142">1</span></span><br/>               |
| <span data-ttu-id="b29b7-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b29b7-143">UnitType</span></span><br/>     | <span data-ttu-id="b29b7-144">string</span><span class="sxs-lookup"><span data-stu-id="b29b7-144">string</span></span><br/>  | <span data-ttu-id="b29b7-145">micron</span><span class="sxs-lookup"><span data-stu-id="b29b7-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b29b7-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b29b7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29b7-147">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="b29b7-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="b29b7-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b29b7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




