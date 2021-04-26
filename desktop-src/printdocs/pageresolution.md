---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: Pageresolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e44a7ff73c03929d3dfc8bc9f7c31c878ad039c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993718"
---
# <a name="pageresolution"></a><span data-ttu-id="87746-104">Pageresolution</span><span class="sxs-lookup"><span data-stu-id="87746-104">PageResolution</span></span>

<span data-ttu-id="87746-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="87746-105">This topic is not current.</span></span> <span data-ttu-id="87746-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87746-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87746-107">Definisce la risoluzione della pagina dell'output stampato come valore qualitativo, in punti per pollice o in entrambi i modi.</span><span class="sxs-lookup"><span data-stu-id="87746-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="87746-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="87746-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87746-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="87746-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="87746-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="87746-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="87746-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="87746-111">Element Information</span></span>



| <span data-ttu-id="87746-112">Nome</span><span class="sxs-lookup"><span data-stu-id="87746-112">Name</span></span> | <span data-ttu-id="87746-113">Valore</span><span class="sxs-lookup"><span data-stu-id="87746-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="87746-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="87746-114">Element Type</span></span> <br/>   | <span data-ttu-id="87746-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="87746-115">Feature</span></span><br/> |
| <span data-ttu-id="87746-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="87746-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87746-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="87746-117">Page</span></span><br/>    |
| <span data-ttu-id="87746-118">Note</span><span class="sxs-lookup"><span data-stu-id="87746-118">Notes</span></span> <br/>          | <span data-ttu-id="87746-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="87746-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="87746-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="87746-120">Structural Content</span></span>

<span data-ttu-id="87746-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="87746-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="87746-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="87746-122">Structure Variables</span></span>

<span data-ttu-id="87746-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="87746-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87746-124">Nome</span><span class="sxs-lookup"><span data-stu-id="87746-124">Name</span></span>                                      | <span data-ttu-id="87746-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="87746-125">Data type</span></span>          | <span data-ttu-id="87746-126">Unità</span><span class="sxs-lookup"><span data-stu-id="87746-126">Unit</span></span>                  | <span data-ttu-id="87746-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="87746-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="87746-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="87746-128">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87746-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="87746-129">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="87746-130">string</span><span class="sxs-lookup"><span data-stu-id="87746-130">string</span></span><br/>  | <span data-ttu-id="87746-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="87746-131">characters</span></span><br/> | <span data-ttu-id="87746-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="87746-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="87746-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="87746-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="87746-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="87746-134">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="87746-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="87746-135">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="87746-136">string</span><span class="sxs-lookup"><span data-stu-id="87746-136">string</span></span><br/>  | <span data-ttu-id="87746-137">n/d</span><span class="sxs-lookup"><span data-stu-id="87746-137">n/a</span></span><br/>        | <span data-ttu-id="87746-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="87746-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="87746-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="87746-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="87746-140">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="87746-140">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="87746-141">numero intero</span><span class="sxs-lookup"><span data-stu-id="87746-141">integer</span></span><br/> | <span data-ttu-id="87746-142">DPI</span><span class="sxs-lookup"><span data-stu-id="87746-142">DPI</span></span><br/>        | <span data-ttu-id="87746-143">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="87746-143">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="87746-144">Specifica il componente x della risoluzione relativo a PageImageableSize in DPI (rispetto alla direzione PageMediaSize e feed del supporto).</span><span class="sxs-lookup"><span data-stu-id="87746-144">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="87746-145">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="87746-145">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="87746-146">numero intero</span><span class="sxs-lookup"><span data-stu-id="87746-146">integer</span></span><br/> | <span data-ttu-id="87746-147">DPI</span><span class="sxs-lookup"><span data-stu-id="87746-147">DPI</span></span><br/>        | <span data-ttu-id="87746-148">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="87746-148">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="87746-149">Specifica il componente y della risoluzione rispetto a PageImageableSize in DPI (relativo a PageMediaSize e alla direzione del feed dei supporti).</span><span class="sxs-lookup"><span data-stu-id="87746-149">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="87746-150">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="87746-150">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="87746-151">string</span><span class="sxs-lookup"><span data-stu-id="87746-151">string</span></span><br/>  | <span data-ttu-id="87746-152">n/d</span><span class="sxs-lookup"><span data-stu-id="87746-152">n/a</span></span><br/>        | <span data-ttu-id="87746-153">Default, Draft, High, Normal, Other.</span><span class="sxs-lookup"><span data-stu-id="87746-153">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="87746-154">Specifica un'etichetta di qualità per la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="87746-154">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="87746-155">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="87746-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="87746-156">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="87746-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="87746-157">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="87746-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="87746-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87746-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87746-159">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="87746-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




