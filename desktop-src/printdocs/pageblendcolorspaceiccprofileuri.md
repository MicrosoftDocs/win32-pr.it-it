---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997698"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="1471e-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="1471e-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="1471e-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1471e-105">This topic is not current.</span></span> <span data-ttu-id="1471e-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1471e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1471e-107">Specifica un riferimento URI relativo a un profilo ICC che definisce lo spazio colore da utilizzare per la fusione.</span><span class="sxs-lookup"><span data-stu-id="1471e-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="1471e-108">è <Uri> un nome di parte assoluto relativo alla radice del \_ pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1471e-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="1471e-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1471e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1471e-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1471e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1471e-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1471e-111">Element Information</span></span>



| <span data-ttu-id="1471e-112">Nome</span><span class="sxs-lookup"><span data-stu-id="1471e-112">Name</span></span> | <span data-ttu-id="1471e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1471e-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1471e-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1471e-114">Element Type</span></span> <br/>   | <span data-ttu-id="1471e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1471e-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="1471e-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1471e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1471e-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="1471e-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="1471e-118">Note</span><span class="sxs-lookup"><span data-stu-id="1471e-118">Notes</span></span> <br/>          | <span data-ttu-id="1471e-119">Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="1471e-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="1471e-120">Collegato all'elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="1471e-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1471e-121">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1471e-121">Structure Content</span></span>

<span data-ttu-id="1471e-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="1471e-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1471e-123">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="1471e-123">Structure Properties</span></span>

<span data-ttu-id="1471e-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1471e-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1471e-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1471e-125">Property</span></span>                | <span data-ttu-id="1471e-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1471e-126">xsi:type</span></span>           | <span data-ttu-id="1471e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1471e-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1471e-128">DataType</span><span class="sxs-lookup"><span data-stu-id="1471e-128">DataType</span></span><br/>     | <span data-ttu-id="1471e-129">string</span><span class="sxs-lookup"><span data-stu-id="1471e-129">string</span></span><br/>  | <span data-ttu-id="1471e-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="1471e-130">xs:string</span></span><br/>       |
| <span data-ttu-id="1471e-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1471e-131">DefaultValue</span></span><br/> | <span data-ttu-id="1471e-132">string</span><span class="sxs-lookup"><span data-stu-id="1471e-132">string</span></span><br/>  | <span data-ttu-id="1471e-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="1471e-133">undefined</span></span><br/>       |
| <span data-ttu-id="1471e-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1471e-134">MaxLength</span></span><br/>    | <span data-ttu-id="1471e-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="1471e-135">integer</span></span><br/> | <span data-ttu-id="1471e-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="1471e-136">undefined</span></span><br/>       |
| <span data-ttu-id="1471e-137">Minlength</span><span class="sxs-lookup"><span data-stu-id="1471e-137">MinLength</span></span><br/>    | <span data-ttu-id="1471e-138">integer</span><span class="sxs-lookup"><span data-stu-id="1471e-138">integer</span></span><br/> | <span data-ttu-id="1471e-139">1</span><span class="sxs-lookup"><span data-stu-id="1471e-139">1</span></span><br/>               |
| <span data-ttu-id="1471e-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="1471e-140">Mandatory</span></span><br/>    | <span data-ttu-id="1471e-141">string</span><span class="sxs-lookup"><span data-stu-id="1471e-141">string</span></span><br/>  | <span data-ttu-id="1471e-142">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="1471e-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1471e-143">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="1471e-143">UnitType</span></span><br/>     | <span data-ttu-id="1471e-144">string</span><span class="sxs-lookup"><span data-stu-id="1471e-144">string</span></span><br/>  | <span data-ttu-id="1471e-145">caratteri</span><span class="sxs-lookup"><span data-stu-id="1471e-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1471e-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1471e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1471e-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1471e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




