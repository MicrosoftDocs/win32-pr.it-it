---
description: Ottenere informazioni sul parametro PageMediaSizePSHeight. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1e7a30935c27fadb5d6ebb8dfb8f377e05a5e3
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549100"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="06c51-105">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="06c51-105">PageMediaSizePSHeight</span></span>

<span data-ttu-id="06c51-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="06c51-106">This topic is not current.</span></span> <span data-ttu-id="06c51-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="06c51-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06c51-108">Specifica l'altezza della pagina, parallela alla direzione di orientamento del feed (riferimento PostScript [printer description file format specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="06c51-108">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="06c51-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="06c51-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06c51-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="06c51-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="06c51-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="06c51-111">Element Information</span></span>



| <span data-ttu-id="06c51-112">Nome</span><span class="sxs-lookup"><span data-stu-id="06c51-112">Name</span></span> | <span data-ttu-id="06c51-113">Valore</span><span class="sxs-lookup"><span data-stu-id="06c51-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="06c51-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="06c51-114">Element Type</span></span> <br/>   | <span data-ttu-id="06c51-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="06c51-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="06c51-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="06c51-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06c51-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="06c51-117">Page</span></span><br/>                                             |
| <span data-ttu-id="06c51-118">Note</span><span class="sxs-lookup"><span data-stu-id="06c51-118">Notes</span></span> <br/>          | <span data-ttu-id="06c51-119">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="06c51-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="06c51-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="06c51-120">Structure Content</span></span>

<span data-ttu-id="06c51-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="06c51-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="06c51-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="06c51-122">Structure Properties</span></span>

<span data-ttu-id="06c51-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="06c51-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06c51-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06c51-124">Property</span></span>                | <span data-ttu-id="06c51-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="06c51-125">xsi:type</span></span>           | <span data-ttu-id="06c51-126">Valore</span><span class="sxs-lookup"><span data-stu-id="06c51-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="06c51-127">DataType</span><span class="sxs-lookup"><span data-stu-id="06c51-127">DataType</span></span><br/>     | <span data-ttu-id="06c51-128">string</span><span class="sxs-lookup"><span data-stu-id="06c51-128">string</span></span><br/>  | <span data-ttu-id="06c51-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06c51-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="06c51-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="06c51-130">DefaultValue</span></span><br/> | <span data-ttu-id="06c51-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="06c51-131">integer</span></span><br/> | <span data-ttu-id="06c51-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="06c51-132">undefined</span></span><br/>       |
| <span data-ttu-id="06c51-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="06c51-133">MaxValue</span></span><br/>     | <span data-ttu-id="06c51-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="06c51-134">integer</span></span><br/> | <span data-ttu-id="06c51-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="06c51-135">undefined</span></span><br/>       |
| <span data-ttu-id="06c51-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="06c51-136">MinValue</span></span><br/>     | <span data-ttu-id="06c51-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="06c51-137">integer</span></span><br/> | <span data-ttu-id="06c51-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="06c51-138">undefined</span></span><br/>       |
| <span data-ttu-id="06c51-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="06c51-139">Mandatory</span></span><br/>    | <span data-ttu-id="06c51-140">string</span><span class="sxs-lookup"><span data-stu-id="06c51-140">string</span></span><br/>  | <span data-ttu-id="06c51-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="06c51-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="06c51-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="06c51-142">Multiple</span></span><br/>     | <span data-ttu-id="06c51-143">integer</span><span class="sxs-lookup"><span data-stu-id="06c51-143">integer</span></span><br/> | <span data-ttu-id="06c51-144">1</span><span class="sxs-lookup"><span data-stu-id="06c51-144">1</span></span><br/>               |
| <span data-ttu-id="06c51-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="06c51-145">UnitType</span></span><br/>     | <span data-ttu-id="06c51-146">string</span><span class="sxs-lookup"><span data-stu-id="06c51-146">string</span></span><br/>  | <span data-ttu-id="06c51-147">Micron</span><span class="sxs-lookup"><span data-stu-id="06c51-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="06c51-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06c51-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c51-149">PostScript Specifica del formato del file di descrizione della stampante</span><span class="sxs-lookup"><span data-stu-id="06c51-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="06c51-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="06c51-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




