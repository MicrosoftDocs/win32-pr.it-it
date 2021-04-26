---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 29d7ae65-9dd3-4a29-8e5e-79708638a3bb
title: PageMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d41ed2af931068e340e9a9d0828db109594de8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994518"
---
# <a name="pagemediatype"></a><span data-ttu-id="e3225-104">PageMediaType</span><span class="sxs-lookup"><span data-stu-id="e3225-104">PageMediaType</span></span>

<span data-ttu-id="e3225-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e3225-105">This topic is not current.</span></span> <span data-ttu-id="e3225-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3225-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3225-107">Descrive le opzioni MediaType e le caratteristiche di ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="e3225-107">Describes the MediaType options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="e3225-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e3225-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3225-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e3225-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e3225-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e3225-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e3225-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e3225-111">Element Information</span></span>



| <span data-ttu-id="e3225-112">Nome</span><span class="sxs-lookup"><span data-stu-id="e3225-112">Name</span></span> | <span data-ttu-id="e3225-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e3225-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e3225-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e3225-114">Element Type</span></span> <br/>   | <span data-ttu-id="e3225-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="e3225-115">Feature</span></span><br/> |
| <span data-ttu-id="e3225-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e3225-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3225-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="e3225-117">Page</span></span><br/>    |
| <span data-ttu-id="e3225-118">Note</span><span class="sxs-lookup"><span data-stu-id="e3225-118">Notes</span></span> <br/>          | <span data-ttu-id="e3225-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="e3225-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e3225-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e3225-120">Structural Content</span></span>

<span data-ttu-id="e3225-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e3225-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">_BackCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">_FrontCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_MaterialValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">_PrePrintedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">_PrePunchedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">_RecycledValue_</psf:Value>
    </psf:ScoredProperty>     
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_WeightValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="e3225-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e3225-122">Structure Variables</span></span>

<span data-ttu-id="e3225-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e3225-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3225-124">Nome</span><span class="sxs-lookup"><span data-stu-id="e3225-124">Name</span></span>                               | <span data-ttu-id="e3225-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e3225-125">Data type</span></span>          | <span data-ttu-id="e3225-126">Unità</span><span class="sxs-lookup"><span data-stu-id="e3225-126">Unit</span></span>                              | <span data-ttu-id="e3225-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e3225-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e3225-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e3225-128">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e3225-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e3225-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e3225-130">string</span><span class="sxs-lookup"><span data-stu-id="e3225-130">string</span></span><br/>  | <span data-ttu-id="e3225-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="e3225-131">characters</span></span><br/>             | <span data-ttu-id="e3225-132">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e3225-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e3225-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3225-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e3225-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="e3225-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e3225-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e3225-136">string</span><span class="sxs-lookup"><span data-stu-id="e3225-136">string</span></span><br/>  | <span data-ttu-id="e3225-137">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-137">n/a</span></span><br/>                    | <span data-ttu-id="e3225-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="e3225-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e3225-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e3225-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="e3225-140">\_BackCoatingValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-140">\_BackCoatingValue\_</span></span><br/>    | <span data-ttu-id="e3225-141">string</span><span class="sxs-lookup"><span data-stu-id="e3225-141">string</span></span><br/>  | <span data-ttu-id="e3225-142">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-142">n/a</span></span><br/>                    | <span data-ttu-id="e3225-143">Glossario, HighGloss, Matte, None, Satin, SemiGloss.</span><span class="sxs-lookup"><span data-stu-id="e3225-143">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span></span><br/>                                                                                                                          | <span data-ttu-id="e3225-144">Specifica l'iratura del lato posteriore del supporto.</span><span class="sxs-lookup"><span data-stu-id="e3225-144">Specifies the coating of the back side of the media.</span></span><br/>              |
| <span data-ttu-id="e3225-145">\_FrontCoatingValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-145">\_FrontCoatingValue\_</span></span><br/>   | <span data-ttu-id="e3225-146">string</span><span class="sxs-lookup"><span data-stu-id="e3225-146">string</span></span><br/>  | <span data-ttu-id="e3225-147">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-147">n/a</span></span><br/>                    | <span data-ttu-id="e3225-148">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span><span class="sxs-lookup"><span data-stu-id="e3225-148">Glossy, HighGloss, Matte, None, Satin, SemiGloss.</span></span><br/>                                                                                                                          | <span data-ttu-id="e3225-149">Specifica l'utilizzo del lato anteriore del supporto.</span><span class="sxs-lookup"><span data-stu-id="e3225-149">Specifies the coating of the front side of the media.</span></span><br/>             |
| <span data-ttu-id="e3225-150">\_MaterialValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-150">\_MaterialValue\_</span></span><br/>       | <span data-ttu-id="e3225-151">string</span><span class="sxs-lookup"><span data-stu-id="e3225-151">string</span></span><br/>  | <span data-ttu-id="e3225-152">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-152">n/a</span></span><br/>                    | <span data-ttu-id="e3225-153">Aluminum, Display, DryFilm, Paper, Polyester, Transparency, WetFilm.</span><span class="sxs-lookup"><span data-stu-id="e3225-153">Aluminum, Display, DryFilm, Paper, Polyester, Transparency, WetFilm.</span></span><br/>                                                                                                       | <span data-ttu-id="e3225-154">Specifica il materiale di cui è costituito il supporto.</span><span class="sxs-lookup"><span data-stu-id="e3225-154">Specifies the material the media is made out of.</span></span><br/>                  |
| <span data-ttu-id="e3225-155">\_PrePrintedValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-155">\_PrePrintedValue\_</span></span><br/>     | <span data-ttu-id="e3225-156">string</span><span class="sxs-lookup"><span data-stu-id="e3225-156">string</span></span><br/>  | <span data-ttu-id="e3225-157">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-157">n/a</span></span><br/>                    | <span data-ttu-id="e3225-158">None, PrePrinted, Letterhead.</span><span class="sxs-lookup"><span data-stu-id="e3225-158">None, PrePrinted, Letterhead.</span></span><br/>                                                                                                                                              | <span data-ttu-id="e3225-159">Specifica le caratteristiche prestampate dei supporti.</span><span class="sxs-lookup"><span data-stu-id="e3225-159">Specifies media preprinted characteristics.</span></span><br/>                       |
| <span data-ttu-id="e3225-160">\_PrePunchedValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-160">\_PrePunchedValue\_</span></span><br/>     | <span data-ttu-id="e3225-161">string</span><span class="sxs-lookup"><span data-stu-id="e3225-161">string</span></span><br/>  | <span data-ttu-id="e3225-162">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-162">n/a</span></span><br/>                    | <span data-ttu-id="e3225-163">Nessuno, PrePunched.</span><span class="sxs-lookup"><span data-stu-id="e3225-163">None, PrePunched.</span></span><br/>                                                                                                                                                          | <span data-ttu-id="e3225-164">Specifica le caratteristiche prepunched dei supporti.</span><span class="sxs-lookup"><span data-stu-id="e3225-164">Specifies media prepunched characteristics.</span></span><br/>                       |
| <span data-ttu-id="e3225-165">\_RecycledValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-165">\_RecycledValue\_</span></span><br/>       | <span data-ttu-id="e3225-166">string</span><span class="sxs-lookup"><span data-stu-id="e3225-166">string</span></span><br/>  | <span data-ttu-id="e3225-167">n/d</span><span class="sxs-lookup"><span data-stu-id="e3225-167">n/a</span></span><br/>                    | <span data-ttu-id="e3225-168">Nessuno, Standard.</span><span class="sxs-lookup"><span data-stu-id="e3225-168">None, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e3225-169">Specifica le caratteristiche di riciclo dei supporti.</span><span class="sxs-lookup"><span data-stu-id="e3225-169">Specifies media recycled characteristics.</span></span><br/>                         |
| <span data-ttu-id="e3225-170">\_WeightValue\_</span><span class="sxs-lookup"><span data-stu-id="e3225-170">\_WeightValue\_</span></span><br/>         | <span data-ttu-id="e3225-171">numero intero</span><span class="sxs-lookup"><span data-stu-id="e3225-171">integer</span></span><br/> | <span data-ttu-id="e3225-172">grammi per metro quadrato</span><span class="sxs-lookup"><span data-stu-id="e3225-172">grams per square meter</span></span><br/> | <span data-ttu-id="e3225-173">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e3225-173">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e3225-174">Specifica le caratteristiche del peso dei supporti.</span><span class="sxs-lookup"><span data-stu-id="e3225-174">Specifies media weight characteristics.</span></span><br/>                           |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e3225-175">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e3225-175">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e3225-176">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` nomi .</span><span class="sxs-lookup"><span data-stu-id="e3225-176">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="e3225-177">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="e3225-177">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies Media would be Automatically selected. -->
  <psf:Option name="psk:AutoSelect"/>
  <!-- Specifies archival quality media. -->
  <psf:Option name="psk:Archival">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty back printing film media. -->
  <psf:Option name="psk:BackPrintFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard bond media. -->
  <psf:Option name="psk:Bond">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard card stock media. -->
  <psf:Option name="psk:CardStock">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies continuous feed media. -->
  <psf:Option name="psk:Continous">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard envelope media. -->
  <psf:Option name="psk:EnvelopePlain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies windowed envelope media. -->
  <psf:Option name="psk:EnvelopeWindow">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies fabric media. -->
  <psf:Option name="psk:Fabric">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Polyester</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty high resolution media. -->
  <psf:Option name="psk:HighResolution">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies label media. -->
  <psf:Option name="psk:Label">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies attached multi-part forms media. -->
  <psf:Option name="psk:MultiLayerForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies separate multi-part forms media. -->
  <psf:Option name="psk:MultiPartForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard photographic media. -->
  <psf:Option name="psk:Photographic">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies film photographic media. -->
  <psf:Option name="psk:PhotographicFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies glossy photographic media. -->
  <psf:Option name="psk:PhotographicGlossy">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Glossy</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies high gloss photographic media. -->
  <psf:Option name="psk:PhotographicHighGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">HighGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies matte photographic media. -->
  <psf:Option name="psk:PhotographicMatte">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Matte</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies satin photographic media. -->
  <psf:Option name="psk:PhotographicSatin">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Satin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies semi-gloss photographic media. -->
  <psf:Option name="psk:PhotographicSemiGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">SemiGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard paper media. -->
  <psf:Option name="psk:Plain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in continuous form. -->
  <psf:Option name="psk:Screen">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in paged form. -->
  <psf:Option name="psk:ScreenPaged">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty stationery media. -->
  <psf:Option name="psk:Stationery">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">Letterhead</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is not pre-cut (single tabs). -->
  <psf:Option name="psk:TabStockFull">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is pre-cut (multiple tabs). -->
  <psf:Option name="psk:TabStockPreCut">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies transparency media. -->
  <psf:Option name="psk:Transparency">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Transparency</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty T-shirt transfer media. -->
  <psf:Option name="psk:TShirtTransfer">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies unknown or unlisted media. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="e3225-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3225-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3225-179">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e3225-179">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
