---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba727cfa1c11850b62a883b95ab78a6dfae50
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996258"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="76372-104">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="76372-104">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="76372-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="76372-105">This topic is not current.</span></span> <span data-ttu-id="76372-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="76372-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="76372-107">Specifica il comportamento di generazione nero per le separazioni CMYK.</span><span class="sxs-lookup"><span data-stu-id="76372-107">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="76372-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="76372-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="76372-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="76372-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="76372-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="76372-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="76372-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="76372-111">Element Information</span></span>



| <span data-ttu-id="76372-112">Nome</span><span class="sxs-lookup"><span data-stu-id="76372-112">Name</span></span> | <span data-ttu-id="76372-113">Valore</span><span class="sxs-lookup"><span data-stu-id="76372-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="76372-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="76372-114">Element Type</span></span> <br/>   | <span data-ttu-id="76372-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="76372-115">Feature</span></span><br/> |
| <span data-ttu-id="76372-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="76372-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="76372-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="76372-117">Page</span></span><br/>    |
| <span data-ttu-id="76372-118">Note</span><span class="sxs-lookup"><span data-stu-id="76372-118">Notes</span></span> <br/>          | <span data-ttu-id="76372-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="76372-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="76372-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="76372-120">Structural Content</span></span>

<span data-ttu-id="76372-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="76372-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="76372-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="76372-122">Structure Variables</span></span>

<span data-ttu-id="76372-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="76372-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="76372-124">Nome</span><span class="sxs-lookup"><span data-stu-id="76372-124">Name</span></span>                               | <span data-ttu-id="76372-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="76372-125">Data type</span></span>         | <span data-ttu-id="76372-126">Unità</span><span class="sxs-lookup"><span data-stu-id="76372-126">Unit</span></span>                  | <span data-ttu-id="76372-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="76372-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="76372-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="76372-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="76372-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="76372-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="76372-130">string</span><span class="sxs-lookup"><span data-stu-id="76372-130">string</span></span><br/> | <span data-ttu-id="76372-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="76372-131">characters</span></span><br/> | <span data-ttu-id="76372-132">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="76372-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="76372-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="76372-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="76372-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="76372-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="76372-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="76372-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="76372-136">string</span><span class="sxs-lookup"><span data-stu-id="76372-136">string</span></span><br/> | <span data-ttu-id="76372-137">n/d</span><span class="sxs-lookup"><span data-stu-id="76372-137">n/a</span></span><br/>        | <span data-ttu-id="76372-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="76372-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="76372-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="76372-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="76372-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="76372-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="76372-141">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="76372-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="76372-142">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="76372-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="76372-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76372-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76372-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="76372-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




