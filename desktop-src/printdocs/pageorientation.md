---
description: Informazioni sull'elemento configurabile dall'utente PageOrientation. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: Orientamento pagina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f0af08fcd29f34bb55bd16b1eac50487e96ffb
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549119"
---
# <a name="pageorientation"></a><span data-ttu-id="7a7b9-105">Orientamento pagina</span><span class="sxs-lookup"><span data-stu-id="7a7b9-105">PageOrientation</span></span>

<span data-ttu-id="7a7b9-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-106">This topic is not current.</span></span> <span data-ttu-id="7a7b9-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a7b9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a7b9-108">Descrive l'orientamento del foglio multimediale fisico.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-108">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="7a7b9-109">Opzione</span><span class="sxs-lookup"><span data-stu-id="7a7b9-109">Option</span></span>                       | <span data-ttu-id="7a7b9-110">Definizione</span><span class="sxs-lookup"><span data-stu-id="7a7b9-110">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7b9-111">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="7a7b9-111">Landscape</span></span> <br/>        | <span data-ttu-id="7a7b9-112">Il contenuto viene ruotato a pagina 90? gradi CCW rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="7a7b9-112">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="7a7b9-113">Verticale</span><span class="sxs-lookup"><span data-stu-id="7a7b9-113">Portrait</span></span> <br/>         | <span data-ttu-id="7a7b9-114">Orientamento standard.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-114">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="7a7b9-115">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="7a7b9-115">ReverseLandscape</span></span> <br/> | <span data-ttu-id="7a7b9-116">Il contenuto viene ruotato nella pagina 270?? gradi CCW rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="7a7b9-116">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="7a7b9-117">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="7a7b9-117">ReversePortrait</span></span> <br/>  | <span data-ttu-id="7a7b9-118">Il contenuto viene ruotato nella pagina 180?? gradi rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="7a7b9-118">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="7a7b9-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7a7b9-119">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7a7b9-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7a7b9-120">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7a7b9-121">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7a7b9-121">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7a7b9-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7a7b9-122">Element Information</span></span>



| <span data-ttu-id="7a7b9-123">Nome</span><span class="sxs-lookup"><span data-stu-id="7a7b9-123">Name</span></span> | <span data-ttu-id="7a7b9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7a7b9-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7b9-125">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7a7b9-125">Element Type</span></span> <br/>   | <span data-ttu-id="7a7b9-126">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="7a7b9-126">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="7a7b9-127">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7a7b9-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a7b9-128">Pagina</span><span class="sxs-lookup"><span data-stu-id="7a7b9-128">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="7a7b9-129">Note</span><span class="sxs-lookup"><span data-stu-id="7a7b9-129">Notes</span></span> <br/>          | <span data-ttu-id="7a7b9-130">Se un dispositivo stampante può supportare solo una direzione orizzontale e questa direzione è detta "orizzontale inverso", l'orientamento della pagina verrà comunque considerato "orizzontale".</span><span class="sxs-lookup"><span data-stu-id="7a7b9-130">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7a7b9-131">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7a7b9-131">Structural Content</span></span>

<span data-ttu-id="7a7b9-132">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7a7b9-132">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="7a7b9-133">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="7a7b9-133">Structure Variables</span></span>

<span data-ttu-id="7a7b9-134">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-134">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a7b9-135">Nome</span><span class="sxs-lookup"><span data-stu-id="7a7b9-135">Name</span></span>                               | <span data-ttu-id="7a7b9-136">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7a7b9-136">Data type</span></span>         | <span data-ttu-id="7a7b9-137">Unità</span><span class="sxs-lookup"><span data-stu-id="7a7b9-137">Unit</span></span>                  | <span data-ttu-id="7a7b9-138">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="7a7b9-138">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7a7b9-139">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7a7b9-139">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7a7b9-140">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7a7b9-140">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7a7b9-141">string</span><span class="sxs-lookup"><span data-stu-id="7a7b9-141">string</span></span><br/> | <span data-ttu-id="7a7b9-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="7a7b9-142">characters</span></span><br/> | <span data-ttu-id="7a7b9-143">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7a7b9-143">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7a7b9-144">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-144">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7a7b9-145">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-145">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7a7b9-146">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7a7b9-146">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7a7b9-147">string</span><span class="sxs-lookup"><span data-stu-id="7a7b9-147">string</span></span><br/> | <span data-ttu-id="7a7b9-148">n/d</span><span class="sxs-lookup"><span data-stu-id="7a7b9-148">n/a</span></span><br/>        | <span data-ttu-id="7a7b9-149">True, False.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-149">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7a7b9-150">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7a7b9-150">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7a7b9-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7a7b9-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7a7b9-152">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="7a7b9-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7a7b9-153">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="7a7b9-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="7a7b9-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a7b9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a7b9-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7a7b9-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




