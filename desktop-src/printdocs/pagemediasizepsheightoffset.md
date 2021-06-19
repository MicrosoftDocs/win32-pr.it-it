---
description: Ottenere informazioni sul parametro PageMediaSizePSHeightOffset. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395736"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="b53b6-105">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="b53b6-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="b53b6-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b53b6-106">This topic is not current.</span></span> <span data-ttu-id="b53b6-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b53b6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b53b6-108">Specifica l'offset, parallelo alla direzione di orientamento del feed (Specifica del formato del file di descrizione della stampante [PostScript di riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="b53b6-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="b53b6-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b53b6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b53b6-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b53b6-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b53b6-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b53b6-111">Element Information</span></span>



| <span data-ttu-id="b53b6-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b53b6-112">Name</span></span> | <span data-ttu-id="b53b6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b53b6-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b53b6-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b53b6-114">Element Type</span></span> <br/>   | <span data-ttu-id="b53b6-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b53b6-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="b53b6-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b53b6-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b53b6-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="b53b6-117">Page</span></span><br/>                                             |
| <span data-ttu-id="b53b6-118">Note</span><span class="sxs-lookup"><span data-stu-id="b53b6-118">Notes</span></span> <br/>          | <span data-ttu-id="b53b6-119">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="b53b6-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b53b6-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b53b6-120">Structure Content</span></span>

<span data-ttu-id="b53b6-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b53b6-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b53b6-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="b53b6-122">Structure Properties</span></span>

<span data-ttu-id="b53b6-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b53b6-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b53b6-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b53b6-124">Property</span></span>                | <span data-ttu-id="b53b6-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b53b6-125">xsi:type</span></span>           | <span data-ttu-id="b53b6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b53b6-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b53b6-127">DataType</span><span class="sxs-lookup"><span data-stu-id="b53b6-127">DataType</span></span><br/>     | <span data-ttu-id="b53b6-128">string</span><span class="sxs-lookup"><span data-stu-id="b53b6-128">string</span></span><br/>  | <span data-ttu-id="b53b6-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b53b6-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="b53b6-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b53b6-130">DefaultValue</span></span><br/> | <span data-ttu-id="b53b6-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="b53b6-131">integer</span></span><br/> | <span data-ttu-id="b53b6-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="b53b6-132">undefined</span></span><br/>       |
| <span data-ttu-id="b53b6-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b53b6-133">MaxValue</span></span><br/>     | <span data-ttu-id="b53b6-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="b53b6-134">integer</span></span><br/> | <span data-ttu-id="b53b6-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="b53b6-135">undefined</span></span><br/>       |
| <span data-ttu-id="b53b6-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="b53b6-136">MinValue</span></span><br/>     | <span data-ttu-id="b53b6-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="b53b6-137">integer</span></span><br/> | <span data-ttu-id="b53b6-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="b53b6-138">undefined</span></span><br/>       |
| <span data-ttu-id="b53b6-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b53b6-139">Mandatory</span></span><br/>    | <span data-ttu-id="b53b6-140">string</span><span class="sxs-lookup"><span data-stu-id="b53b6-140">string</span></span><br/>  | <span data-ttu-id="b53b6-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="b53b6-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b53b6-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="b53b6-142">Multiple</span></span><br/>     | <span data-ttu-id="b53b6-143">integer</span><span class="sxs-lookup"><span data-stu-id="b53b6-143">integer</span></span><br/> | <span data-ttu-id="b53b6-144">1</span><span class="sxs-lookup"><span data-stu-id="b53b6-144">1</span></span><br/>               |
| <span data-ttu-id="b53b6-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="b53b6-145">UnitType</span></span><br/>     | <span data-ttu-id="b53b6-146">string</span><span class="sxs-lookup"><span data-stu-id="b53b6-146">string</span></span><br/>  | <span data-ttu-id="b53b6-147">Micron</span><span class="sxs-lookup"><span data-stu-id="b53b6-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b53b6-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b53b6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53b6-149">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="b53b6-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="b53b6-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b53b6-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




