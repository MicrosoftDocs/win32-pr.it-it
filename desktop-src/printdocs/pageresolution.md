---
description: Informazioni sull'elemento PageResolution configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: Pageresolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394821"
---
# <a name="pageresolution"></a><span data-ttu-id="e73a6-105">Pageresolution</span><span class="sxs-lookup"><span data-stu-id="e73a6-105">PageResolution</span></span>

<span data-ttu-id="e73a6-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e73a6-106">This topic is not current.</span></span> <span data-ttu-id="e73a6-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e73a6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e73a6-108">Definisce la risoluzione della pagina dell'output stampato come valore qualitativo, in punti per pollice o in entrambi i modi.</span><span class="sxs-lookup"><span data-stu-id="e73a6-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="e73a6-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e73a6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e73a6-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e73a6-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e73a6-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e73a6-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e73a6-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e73a6-112">Element Information</span></span>



| <span data-ttu-id="e73a6-113">Nome</span><span class="sxs-lookup"><span data-stu-id="e73a6-113">Name</span></span> | <span data-ttu-id="e73a6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e73a6-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e73a6-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e73a6-115">Element Type</span></span> <br/>   | <span data-ttu-id="e73a6-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e73a6-116">Feature</span></span><br/> |
| <span data-ttu-id="e73a6-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e73a6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e73a6-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="e73a6-118">Page</span></span><br/>    |
| <span data-ttu-id="e73a6-119">Note</span><span class="sxs-lookup"><span data-stu-id="e73a6-119">Notes</span></span> <br/>          | <span data-ttu-id="e73a6-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="e73a6-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e73a6-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e73a6-121">Structural Content</span></span>

<span data-ttu-id="e73a6-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e73a6-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e73a6-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e73a6-123">Structure Variables</span></span>

<span data-ttu-id="e73a6-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e73a6-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e73a6-125">Nome</span><span class="sxs-lookup"><span data-stu-id="e73a6-125">Name</span></span>                                      | <span data-ttu-id="e73a6-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e73a6-126">Data type</span></span>          | <span data-ttu-id="e73a6-127">Unità</span><span class="sxs-lookup"><span data-stu-id="e73a6-127">Unit</span></span>                  | <span data-ttu-id="e73a6-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e73a6-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e73a6-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e73a6-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e73a6-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e73a6-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="e73a6-131">string</span><span class="sxs-lookup"><span data-stu-id="e73a6-131">string</span></span><br/>  | <span data-ttu-id="e73a6-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="e73a6-132">characters</span></span><br/> | <span data-ttu-id="e73a6-133">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e73a6-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e73a6-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e73a6-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e73a6-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="e73a6-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="e73a6-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e73a6-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="e73a6-137">string</span><span class="sxs-lookup"><span data-stu-id="e73a6-137">string</span></span><br/>  | <span data-ttu-id="e73a6-138">n/d</span><span class="sxs-lookup"><span data-stu-id="e73a6-138">n/a</span></span><br/>        | <span data-ttu-id="e73a6-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="e73a6-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e73a6-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e73a6-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="e73a6-141">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="e73a6-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="e73a6-142">numero intero</span><span class="sxs-lookup"><span data-stu-id="e73a6-142">integer</span></span><br/> | <span data-ttu-id="e73a6-143">DPI</span><span class="sxs-lookup"><span data-stu-id="e73a6-143">DPI</span></span><br/>        | <span data-ttu-id="e73a6-144">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e73a6-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e73a6-145">Specifica il componente x della risoluzione rispetto a PageImageableSize in DPI (relativo a PageMediaSize e alla direzione del feed dei supporti).</span><span class="sxs-lookup"><span data-stu-id="e73a6-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="e73a6-146">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="e73a6-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="e73a6-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="e73a6-147">integer</span></span><br/> | <span data-ttu-id="e73a6-148">DPI</span><span class="sxs-lookup"><span data-stu-id="e73a6-148">DPI</span></span><br/>        | <span data-ttu-id="e73a6-149">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e73a6-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e73a6-150">Specifica il componente y della risoluzione rispetto a PageImageableSize in DPI (relativo a PageMediaSize e alla direzione del feed dei supporti).</span><span class="sxs-lookup"><span data-stu-id="e73a6-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="e73a6-151">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="e73a6-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="e73a6-152">string</span><span class="sxs-lookup"><span data-stu-id="e73a6-152">string</span></span><br/>  | <span data-ttu-id="e73a6-153">n/d</span><span class="sxs-lookup"><span data-stu-id="e73a6-153">n/a</span></span><br/>        | <span data-ttu-id="e73a6-154">Default, Draft, High, Normal, Other.</span><span class="sxs-lookup"><span data-stu-id="e73a6-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="e73a6-155">Specifica un'etichetta di qualità per la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="e73a6-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e73a6-156">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e73a6-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e73a6-157">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="e73a6-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e73a6-158">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="e73a6-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e73a6-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73a6-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e73a6-160">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e73a6-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




