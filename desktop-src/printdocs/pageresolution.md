---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321158"
---
# <a name="pageresolution"></a><span data-ttu-id="e3a3f-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="e3a3f-104">PageResolution</span></span>

<span data-ttu-id="e3a3f-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-105">This topic is not current.</span></span> <span data-ttu-id="e3a3f-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3a3f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3a3f-107">Definisce la risoluzione della pagina dell'output stampato come valore qualitativo, in punti per pollice o in entrambi i modi.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="e3a3f-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e3a3f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3a3f-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e3a3f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e3a3f-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e3a3f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e3a3f-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e3a3f-111">Element Information</span></span>



| <span data-ttu-id="e3a3f-112">Nome</span><span class="sxs-lookup"><span data-stu-id="e3a3f-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="e3a3f-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e3a3f-113">Element Type</span></span> <br/>   | <span data-ttu-id="e3a3f-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e3a3f-114">Feature</span></span><br/> |
| <span data-ttu-id="e3a3f-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="e3a3f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3a3f-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="e3a3f-116">Page</span></span><br/>    |
| <span data-ttu-id="e3a3f-117">Note</span><span class="sxs-lookup"><span data-stu-id="e3a3f-117">Notes</span></span> <br/>          | <span data-ttu-id="e3a3f-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="e3a3f-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e3a3f-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e3a3f-119">Structural Content</span></span>

<span data-ttu-id="e3a3f-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e3a3f-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e3a3f-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e3a3f-121">Structure Variables</span></span>

<span data-ttu-id="e3a3f-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3a3f-123">Nome</span><span class="sxs-lookup"><span data-stu-id="e3a3f-123">Name</span></span>                                      | <span data-ttu-id="e3a3f-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e3a3f-124">Data type</span></span>          | <span data-ttu-id="e3a3f-125">Unità</span><span class="sxs-lookup"><span data-stu-id="e3a3f-125">Unit</span></span>                  | <span data-ttu-id="e3a3f-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e3a3f-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e3a3f-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e3a3f-127">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a3f-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e3a3f-128">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="e3a3f-129">string</span><span class="sxs-lookup"><span data-stu-id="e3a3f-129">string</span></span><br/>  | <span data-ttu-id="e3a3f-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="e3a3f-130">characters</span></span><br/> | <span data-ttu-id="e3a3f-131">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e3a3f-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e3a3f-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e3a3f-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-133">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="e3a3f-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e3a3f-134">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="e3a3f-135">string</span><span class="sxs-lookup"><span data-stu-id="e3a3f-135">string</span></span><br/>  | <span data-ttu-id="e3a3f-136">n/d</span><span class="sxs-lookup"><span data-stu-id="e3a3f-136">n/a</span></span><br/>        | <span data-ttu-id="e3a3f-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e3a3f-138">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="e3a3f-139">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="e3a3f-139">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="e3a3f-140">numero intero</span><span class="sxs-lookup"><span data-stu-id="e3a3f-140">integer</span></span><br/> | <span data-ttu-id="e3a3f-141">DPI</span><span class="sxs-lookup"><span data-stu-id="e3a3f-141">DPI</span></span><br/>        | <span data-ttu-id="e3a3f-142">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-142">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e3a3f-143">Specifica il componente x della risoluzione rispetto a PageImageableSize dell'oggetto in DPI (in relazione al PageMediaSize e alla direzione del feed del supporto).</span><span class="sxs-lookup"><span data-stu-id="e3a3f-143">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="e3a3f-144">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="e3a3f-144">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="e3a3f-145">numero intero</span><span class="sxs-lookup"><span data-stu-id="e3a3f-145">integer</span></span><br/> | <span data-ttu-id="e3a3f-146">DPI</span><span class="sxs-lookup"><span data-stu-id="e3a3f-146">DPI</span></span><br/>        | <span data-ttu-id="e3a3f-147">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-147">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e3a3f-148">Specifica il componente y della risoluzione rispetto a PageImageableSize dell'oggetto in DPI (in relazione al PageMediaSize e alla direzione del feed del supporto).</span><span class="sxs-lookup"><span data-stu-id="e3a3f-148">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="e3a3f-149">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="e3a3f-149">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="e3a3f-150">string</span><span class="sxs-lookup"><span data-stu-id="e3a3f-150">string</span></span><br/>  | <span data-ttu-id="e3a3f-151">n/d</span><span class="sxs-lookup"><span data-stu-id="e3a3f-151">n/a</span></span><br/>        | <span data-ttu-id="e3a3f-152">Default, Draft, High, Normal e other.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-152">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="e3a3f-153">Specifica un'etichetta di qualità per la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-153">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e3a3f-154">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="e3a3f-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e3a3f-155">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e3a3f-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e3a3f-156">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="e3a3f-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e3a3f-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3a3f-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a3f-158">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e3a3f-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




