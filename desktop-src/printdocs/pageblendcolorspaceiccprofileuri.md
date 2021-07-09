---
description: Informazioni sul parametro PageBlendColorSpaceICCProfileURI. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549319"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="b33a6-105">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="b33a6-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="b33a6-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b33a6-106">This topic is not current.</span></span> <span data-ttu-id="b33a6-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b33a6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b33a6-108">Specifica un riferimento URI relativo a un profilo ICC che definisce lo spazio colore da usare per la fusione.</span><span class="sxs-lookup"><span data-stu-id="b33a6-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="b33a6-109">è <Uri> un nome di parte assoluto relativo alla radice del \_ pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b33a6-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="b33a6-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b33a6-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b33a6-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b33a6-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b33a6-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b33a6-112">Element Information</span></span>



| <span data-ttu-id="b33a6-113">Nome</span><span class="sxs-lookup"><span data-stu-id="b33a6-113">Name</span></span> | <span data-ttu-id="b33a6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b33a6-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33a6-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b33a6-115">Element Type</span></span> <br/>   | <span data-ttu-id="b33a6-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b33a6-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="b33a6-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b33a6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b33a6-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="b33a6-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="b33a6-119">Note</span><span class="sxs-lookup"><span data-stu-id="b33a6-119">Notes</span></span> <br/>          | <span data-ttu-id="b33a6-120">Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="b33a6-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="b33a6-121">Collegato all'elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="b33a6-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b33a6-122">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b33a6-122">Structure Content</span></span>

<span data-ttu-id="b33a6-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b33a6-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b33a6-124">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="b33a6-124">Structure Properties</span></span>

<span data-ttu-id="b33a6-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b33a6-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b33a6-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b33a6-126">Property</span></span>                | <span data-ttu-id="b33a6-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b33a6-127">xsi:type</span></span>           | <span data-ttu-id="b33a6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b33a6-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b33a6-129">DataType</span><span class="sxs-lookup"><span data-stu-id="b33a6-129">DataType</span></span><br/>     | <span data-ttu-id="b33a6-130">string</span><span class="sxs-lookup"><span data-stu-id="b33a6-130">string</span></span><br/>  | <span data-ttu-id="b33a6-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="b33a6-131">xs:string</span></span><br/>       |
| <span data-ttu-id="b33a6-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b33a6-132">DefaultValue</span></span><br/> | <span data-ttu-id="b33a6-133">string</span><span class="sxs-lookup"><span data-stu-id="b33a6-133">string</span></span><br/>  | <span data-ttu-id="b33a6-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="b33a6-134">undefined</span></span><br/>       |
| <span data-ttu-id="b33a6-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b33a6-135">MaxLength</span></span><br/>    | <span data-ttu-id="b33a6-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="b33a6-136">integer</span></span><br/> | <span data-ttu-id="b33a6-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="b33a6-137">undefined</span></span><br/>       |
| <span data-ttu-id="b33a6-138">Minlength</span><span class="sxs-lookup"><span data-stu-id="b33a6-138">MinLength</span></span><br/>    | <span data-ttu-id="b33a6-139">integer</span><span class="sxs-lookup"><span data-stu-id="b33a6-139">integer</span></span><br/> | <span data-ttu-id="b33a6-140">1</span><span class="sxs-lookup"><span data-stu-id="b33a6-140">1</span></span><br/>               |
| <span data-ttu-id="b33a6-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b33a6-141">Mandatory</span></span><br/>    | <span data-ttu-id="b33a6-142">string</span><span class="sxs-lookup"><span data-stu-id="b33a6-142">string</span></span><br/>  | <span data-ttu-id="b33a6-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b33a6-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b33a6-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="b33a6-144">UnitType</span></span><br/>     | <span data-ttu-id="b33a6-145">string</span><span class="sxs-lookup"><span data-stu-id="b33a6-145">string</span></span><br/>  | <span data-ttu-id="b33a6-146">caratteri</span><span class="sxs-lookup"><span data-stu-id="b33a6-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b33a6-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b33a6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b33a6-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b33a6-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




