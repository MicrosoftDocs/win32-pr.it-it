---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2e1e0a75c5bb6ec95a611d304d575fcf91a13e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998058"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="5cbb2-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="5cbb2-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="5cbb2-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5cbb2-105">This topic is not current.</span></span> <span data-ttu-id="5cbb2-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5cbb2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5cbb2-107">Specifica l'offset, parallelo alla direzione di orientamento del feed (Specifica del formato del file di descrizione della stampante [PostScript di riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="5cbb2-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="5cbb2-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5cbb2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5cbb2-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5cbb2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5cbb2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5cbb2-110">Element Information</span></span>



| <span data-ttu-id="5cbb2-111">Nome</span><span class="sxs-lookup"><span data-stu-id="5cbb2-111">Name</span></span> | <span data-ttu-id="5cbb2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5cbb2-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5cbb2-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5cbb2-113">Element Type</span></span> <br/>   | <span data-ttu-id="5cbb2-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5cbb2-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="5cbb2-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5cbb2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5cbb2-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="5cbb2-116">Page</span></span><br/>                                             |
| <span data-ttu-id="5cbb2-117">Note</span><span class="sxs-lookup"><span data-stu-id="5cbb2-117">Notes</span></span> <br/>          | <span data-ttu-id="5cbb2-118">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="5cbb2-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5cbb2-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5cbb2-119">Structure Content</span></span>

<span data-ttu-id="5cbb2-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5cbb2-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="5cbb2-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="5cbb2-121">Structure Properties</span></span>

<span data-ttu-id="5cbb2-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5cbb2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5cbb2-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5cbb2-123">Property</span></span>                | <span data-ttu-id="5cbb2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5cbb2-124">xsi:type</span></span>           | <span data-ttu-id="5cbb2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5cbb2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5cbb2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5cbb2-126">DataType</span></span><br/>     | <span data-ttu-id="5cbb2-127">string</span><span class="sxs-lookup"><span data-stu-id="5cbb2-127">string</span></span><br/>  | <span data-ttu-id="5cbb2-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5cbb2-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5cbb2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5cbb2-129">DefaultValue</span></span><br/> | <span data-ttu-id="5cbb2-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="5cbb2-130">integer</span></span><br/> | <span data-ttu-id="5cbb2-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="5cbb2-131">undefined</span></span><br/>       |
| <span data-ttu-id="5cbb2-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5cbb2-132">MaxValue</span></span><br/>     | <span data-ttu-id="5cbb2-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="5cbb2-133">integer</span></span><br/> | <span data-ttu-id="5cbb2-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="5cbb2-134">undefined</span></span><br/>       |
| <span data-ttu-id="5cbb2-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="5cbb2-135">MinValue</span></span><br/>     | <span data-ttu-id="5cbb2-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="5cbb2-136">integer</span></span><br/> | <span data-ttu-id="5cbb2-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="5cbb2-137">undefined</span></span><br/>       |
| <span data-ttu-id="5cbb2-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="5cbb2-138">Mandatory</span></span><br/>    | <span data-ttu-id="5cbb2-139">string</span><span class="sxs-lookup"><span data-stu-id="5cbb2-139">string</span></span><br/>  | <span data-ttu-id="5cbb2-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5cbb2-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5cbb2-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="5cbb2-141">Multiple</span></span><br/>     | <span data-ttu-id="5cbb2-142">integer</span><span class="sxs-lookup"><span data-stu-id="5cbb2-142">integer</span></span><br/> | <span data-ttu-id="5cbb2-143">1</span><span class="sxs-lookup"><span data-stu-id="5cbb2-143">1</span></span><br/>               |
| <span data-ttu-id="5cbb2-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="5cbb2-144">UnitType</span></span><br/>     | <span data-ttu-id="5cbb2-145">string</span><span class="sxs-lookup"><span data-stu-id="5cbb2-145">string</span></span><br/>  | <span data-ttu-id="5cbb2-146">Micron</span><span class="sxs-lookup"><span data-stu-id="5cbb2-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5cbb2-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cbb2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cbb2-148">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="5cbb2-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="5cbb2-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5cbb2-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




