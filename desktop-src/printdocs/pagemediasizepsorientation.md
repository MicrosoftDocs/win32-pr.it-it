---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997558"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="31a06-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="31a06-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="31a06-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="31a06-105">This topic is not current.</span></span> <span data-ttu-id="31a06-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="31a06-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="31a06-107">Specifica l'orientamento relativo alla direzione dell'orientamento del feed (Specifica del formato del file di descrizione della stampante [PostScript di riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="31a06-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="31a06-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="31a06-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="31a06-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="31a06-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="31a06-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="31a06-110">Element Information</span></span>



| <span data-ttu-id="31a06-111">Nome</span><span class="sxs-lookup"><span data-stu-id="31a06-111">Name</span></span> | <span data-ttu-id="31a06-112">Valore</span><span class="sxs-lookup"><span data-stu-id="31a06-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="31a06-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="31a06-113">Element Type</span></span> <br/>   | <span data-ttu-id="31a06-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="31a06-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="31a06-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="31a06-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="31a06-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="31a06-116">Page</span></span><br/>                                             |
| <span data-ttu-id="31a06-117">Note</span><span class="sxs-lookup"><span data-stu-id="31a06-117">Notes</span></span> <br/>          | <span data-ttu-id="31a06-118">Collegato all'elemento PageMediaSize, opzione CustomPS</span><span class="sxs-lookup"><span data-stu-id="31a06-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="31a06-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="31a06-119">Structure Content</span></span>

<span data-ttu-id="31a06-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="31a06-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="31a06-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="31a06-121">Structure Properties</span></span>

<span data-ttu-id="31a06-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="31a06-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="31a06-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31a06-123">Property</span></span>                | <span data-ttu-id="31a06-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="31a06-124">xsi:type</span></span>           | <span data-ttu-id="31a06-125">Valore</span><span class="sxs-lookup"><span data-stu-id="31a06-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="31a06-126">DataType</span><span class="sxs-lookup"><span data-stu-id="31a06-126">DataType</span></span><br/>     | <span data-ttu-id="31a06-127">string</span><span class="sxs-lookup"><span data-stu-id="31a06-127">string</span></span><br/>  | <span data-ttu-id="31a06-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="31a06-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="31a06-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="31a06-129">DefaultValue</span></span><br/> | <span data-ttu-id="31a06-130">integer</span><span class="sxs-lookup"><span data-stu-id="31a06-130">integer</span></span><br/> | <span data-ttu-id="31a06-131">0</span><span class="sxs-lookup"><span data-stu-id="31a06-131">0</span></span><br/>                 |
| <span data-ttu-id="31a06-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="31a06-132">MaxValue</span></span><br/>     | <span data-ttu-id="31a06-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="31a06-133">integer</span></span><br/> | <span data-ttu-id="31a06-134">3</span><span class="sxs-lookup"><span data-stu-id="31a06-134">3</span></span><br/>                 |
| <span data-ttu-id="31a06-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="31a06-135">MinValue</span></span><br/>     | <span data-ttu-id="31a06-136">integer</span><span class="sxs-lookup"><span data-stu-id="31a06-136">integer</span></span><br/> | <span data-ttu-id="31a06-137">0</span><span class="sxs-lookup"><span data-stu-id="31a06-137">0</span></span><br/>                 |
| <span data-ttu-id="31a06-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="31a06-138">Mandatory</span></span><br/>    | <span data-ttu-id="31a06-139">string</span><span class="sxs-lookup"><span data-stu-id="31a06-139">string</span></span><br/>  | <span data-ttu-id="31a06-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="31a06-140">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="31a06-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="31a06-141">Multiple</span></span><br/>     | <span data-ttu-id="31a06-142">integer</span><span class="sxs-lookup"><span data-stu-id="31a06-142">integer</span></span><br/> | <span data-ttu-id="31a06-143">1</span><span class="sxs-lookup"><span data-stu-id="31a06-143">1</span></span><br/>                 |
| <span data-ttu-id="31a06-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="31a06-144">UnitType</span></span><br/>     | <span data-ttu-id="31a06-145">string</span><span class="sxs-lookup"><span data-stu-id="31a06-145">string</span></span><br/>  | <span data-ttu-id="31a06-146">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="31a06-146">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="31a06-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31a06-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31a06-148">Specifica del formato del file di descrizione della stampante PostScript</span><span class="sxs-lookup"><span data-stu-id="31a06-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="31a06-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="31a06-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




