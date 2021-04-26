---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca8051fc265e107bff0be53c409eb103df2a8326
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995509"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="0cfd5-104">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="0cfd5-104">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="0cfd5-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-105">This topic is not current.</span></span> <span data-ttu-id="0cfd5-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0cfd5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0cfd5-107">Specifica l'offset perpendicolare alla direzione di orientamento del feed (Specifica del formato del file di descrizione della stampante [PostScript di riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="0cfd5-107">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="0cfd5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0cfd5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0cfd5-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0cfd5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0cfd5-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0cfd5-110">Element Information</span></span>



| <span data-ttu-id="0cfd5-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0cfd5-111">Name</span></span> | <span data-ttu-id="0cfd5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0cfd5-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0cfd5-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0cfd5-113">Element Type</span></span> <br/>   | <span data-ttu-id="0cfd5-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0cfd5-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="0cfd5-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0cfd5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0cfd5-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="0cfd5-116">Page</span></span><br/>                                             |
| <span data-ttu-id="0cfd5-117">Note</span><span class="sxs-lookup"><span data-stu-id="0cfd5-117">Notes</span></span> <br/>          | <span data-ttu-id="0cfd5-118">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="0cfd5-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0cfd5-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0cfd5-119">Structure Content</span></span>

<span data-ttu-id="0cfd5-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0cfd5-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="0cfd5-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="0cfd5-121">Structure Properties</span></span>

<span data-ttu-id="0cfd5-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0cfd5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0cfd5-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0cfd5-123">Property</span></span>                | <span data-ttu-id="0cfd5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0cfd5-124">xsi:type</span></span>           | <span data-ttu-id="0cfd5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0cfd5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0cfd5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="0cfd5-126">DataType</span></span><br/>     | <span data-ttu-id="0cfd5-127">string</span><span class="sxs-lookup"><span data-stu-id="0cfd5-127">string</span></span><br/>  | <span data-ttu-id="0cfd5-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0cfd5-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="0cfd5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0cfd5-129">DefaultValue</span></span><br/> | <span data-ttu-id="0cfd5-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="0cfd5-130">integer</span></span><br/> | <span data-ttu-id="0cfd5-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="0cfd5-131">undefined</span></span><br/>       |
| <span data-ttu-id="0cfd5-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0cfd5-132">MaxValue</span></span><br/>     | <span data-ttu-id="0cfd5-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="0cfd5-133">integer</span></span><br/> | <span data-ttu-id="0cfd5-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="0cfd5-134">undefined</span></span><br/>       |
| <span data-ttu-id="0cfd5-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="0cfd5-135">MinValue</span></span><br/>     | <span data-ttu-id="0cfd5-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="0cfd5-136">integer</span></span><br/> | <span data-ttu-id="0cfd5-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="0cfd5-137">undefined</span></span><br/>       |
| <span data-ttu-id="0cfd5-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0cfd5-138">Mandatory</span></span><br/>    | <span data-ttu-id="0cfd5-139">string</span><span class="sxs-lookup"><span data-stu-id="0cfd5-139">string</span></span><br/>  | <span data-ttu-id="0cfd5-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0cfd5-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0cfd5-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="0cfd5-141">Multiple</span></span><br/>     | <span data-ttu-id="0cfd5-142">integer</span><span class="sxs-lookup"><span data-stu-id="0cfd5-142">integer</span></span><br/> | <span data-ttu-id="0cfd5-143">1</span><span class="sxs-lookup"><span data-stu-id="0cfd5-143">1</span></span><br/>               |
| <span data-ttu-id="0cfd5-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="0cfd5-144">UnitType</span></span><br/>     | <span data-ttu-id="0cfd5-145">string</span><span class="sxs-lookup"><span data-stu-id="0cfd5-145">string</span></span><br/>  | <span data-ttu-id="0cfd5-146">Micron</span><span class="sxs-lookup"><span data-stu-id="0cfd5-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0cfd5-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cfd5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cfd5-148">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="0cfd5-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="0cfd5-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0cfd5-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




