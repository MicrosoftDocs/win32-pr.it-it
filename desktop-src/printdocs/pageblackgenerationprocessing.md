---
description: Informazioni sull'elemento PageBlackGenerationProcessing, che specifica il comportamento di generazione del nero per le separazioni CMYK.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21861595917b67390857b380a416e441d454081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408514"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="34da2-103">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="34da2-103">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="34da2-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="34da2-104">This topic is not current.</span></span> <span data-ttu-id="34da2-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="34da2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="34da2-106">Specifica il comportamento di generazione del nero per le separazioni CMYK.</span><span class="sxs-lookup"><span data-stu-id="34da2-106">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="34da2-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="34da2-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="34da2-108">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="34da2-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="34da2-109">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="34da2-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="34da2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="34da2-110">Element Information</span></span>



| <span data-ttu-id="34da2-111">Nome</span><span class="sxs-lookup"><span data-stu-id="34da2-111">Name</span></span> | <span data-ttu-id="34da2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="34da2-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="34da2-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="34da2-113">Element Type</span></span> <br/>   | <span data-ttu-id="34da2-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="34da2-114">Feature</span></span><br/> |
| <span data-ttu-id="34da2-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="34da2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="34da2-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="34da2-116">Page</span></span><br/>    |
| <span data-ttu-id="34da2-117">Note</span><span class="sxs-lookup"><span data-stu-id="34da2-117">Notes</span></span> <br/>          | <span data-ttu-id="34da2-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="34da2-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="34da2-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="34da2-119">Structural Content</span></span>

<span data-ttu-id="34da2-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="34da2-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="34da2-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="34da2-121">Structure Variables</span></span>

<span data-ttu-id="34da2-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="34da2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="34da2-123">Nome</span><span class="sxs-lookup"><span data-stu-id="34da2-123">Name</span></span>                               | <span data-ttu-id="34da2-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="34da2-124">Data type</span></span>         | <span data-ttu-id="34da2-125">Unità</span><span class="sxs-lookup"><span data-stu-id="34da2-125">Unit</span></span>                  | <span data-ttu-id="34da2-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="34da2-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="34da2-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="34da2-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="34da2-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="34da2-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="34da2-129">string</span><span class="sxs-lookup"><span data-stu-id="34da2-129">string</span></span><br/> | <span data-ttu-id="34da2-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="34da2-130">characters</span></span><br/> | <span data-ttu-id="34da2-131">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="34da2-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="34da2-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="34da2-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="34da2-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="34da2-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="34da2-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="34da2-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="34da2-135">string</span><span class="sxs-lookup"><span data-stu-id="34da2-135">string</span></span><br/> | <span data-ttu-id="34da2-136">n/d</span><span class="sxs-lookup"><span data-stu-id="34da2-136">n/a</span></span><br/>        | <span data-ttu-id="34da2-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="34da2-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="34da2-138">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="34da2-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="34da2-139">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="34da2-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="34da2-140">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="34da2-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="34da2-141">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="34da2-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="34da2-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34da2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34da2-143">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="34da2-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




