---
description: Ottenere informazioni sul parametro PageMediaSizePSOrientation. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1b3aff1099199a98d6c8be899824dd1a1f17c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395726"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="b80b4-105">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="b80b4-105">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="b80b4-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b80b4-106">This topic is not current.</span></span> <span data-ttu-id="b80b4-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b80b4-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b80b4-108">Specifica l'orientamento relativo alla direzione di orientamento del feed (Specifica del formato file di descrizione della stampante [PostScript di riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="b80b4-108">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="b80b4-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b80b4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b80b4-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b80b4-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b80b4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b80b4-111">Element Information</span></span>



| <span data-ttu-id="b80b4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b80b4-112">Name</span></span> | <span data-ttu-id="b80b4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b80b4-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b80b4-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b80b4-114">Element Type</span></span> <br/>   | <span data-ttu-id="b80b4-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b80b4-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="b80b4-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b80b4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b80b4-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="b80b4-117">Page</span></span><br/>                                             |
| <span data-ttu-id="b80b4-118">Note</span><span class="sxs-lookup"><span data-stu-id="b80b4-118">Notes</span></span> <br/>          | <span data-ttu-id="b80b4-119">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="b80b4-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b80b4-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b80b4-120">Structure Content</span></span>

<span data-ttu-id="b80b4-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b80b4-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="b80b4-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="b80b4-122">Structure Properties</span></span>

<span data-ttu-id="b80b4-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b80b4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b80b4-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b80b4-124">Property</span></span>                | <span data-ttu-id="b80b4-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b80b4-125">xsi:type</span></span>           | <span data-ttu-id="b80b4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b80b4-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="b80b4-127">DataType</span><span class="sxs-lookup"><span data-stu-id="b80b4-127">DataType</span></span><br/>     | <span data-ttu-id="b80b4-128">string</span><span class="sxs-lookup"><span data-stu-id="b80b4-128">string</span></span><br/>  | <span data-ttu-id="b80b4-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b80b4-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="b80b4-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b80b4-130">DefaultValue</span></span><br/> | <span data-ttu-id="b80b4-131">integer</span><span class="sxs-lookup"><span data-stu-id="b80b4-131">integer</span></span><br/> | <span data-ttu-id="b80b4-132">0</span><span class="sxs-lookup"><span data-stu-id="b80b4-132">0</span></span><br/>                 |
| <span data-ttu-id="b80b4-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b80b4-133">MaxValue</span></span><br/>     | <span data-ttu-id="b80b4-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="b80b4-134">integer</span></span><br/> | <span data-ttu-id="b80b4-135">3</span><span class="sxs-lookup"><span data-stu-id="b80b4-135">3</span></span><br/>                 |
| <span data-ttu-id="b80b4-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="b80b4-136">MinValue</span></span><br/>     | <span data-ttu-id="b80b4-137">integer</span><span class="sxs-lookup"><span data-stu-id="b80b4-137">integer</span></span><br/> | <span data-ttu-id="b80b4-138">0</span><span class="sxs-lookup"><span data-stu-id="b80b4-138">0</span></span><br/>                 |
| <span data-ttu-id="b80b4-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b80b4-139">Mandatory</span></span><br/>    | <span data-ttu-id="b80b4-140">string</span><span class="sxs-lookup"><span data-stu-id="b80b4-140">string</span></span><br/>  | <span data-ttu-id="b80b4-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="b80b4-141">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="b80b4-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="b80b4-142">Multiple</span></span><br/>     | <span data-ttu-id="b80b4-143">integer</span><span class="sxs-lookup"><span data-stu-id="b80b4-143">integer</span></span><br/> | <span data-ttu-id="b80b4-144">1</span><span class="sxs-lookup"><span data-stu-id="b80b4-144">1</span></span><br/>                 |
| <span data-ttu-id="b80b4-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="b80b4-145">UnitType</span></span><br/>     | <span data-ttu-id="b80b4-146">string</span><span class="sxs-lookup"><span data-stu-id="b80b4-146">string</span></span><br/>  | <span data-ttu-id="b80b4-147">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="b80b4-147">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b80b4-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b80b4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b80b4-149">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="b80b4-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="b80b4-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b80b4-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




