---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: Orientamento pagina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a94fb97ad1e64c7f55fd9520ed8a648a74f550
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997538"
---
# <a name="pageorientation"></a><span data-ttu-id="86c27-104">Orientamento pagina</span><span class="sxs-lookup"><span data-stu-id="86c27-104">PageOrientation</span></span>

<span data-ttu-id="86c27-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="86c27-105">This topic is not current.</span></span> <span data-ttu-id="86c27-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="86c27-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="86c27-107">Descrive l'orientamento del foglio multimediale fisico.</span><span class="sxs-lookup"><span data-stu-id="86c27-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="86c27-108">Opzione</span><span class="sxs-lookup"><span data-stu-id="86c27-108">Option</span></span>                       | <span data-ttu-id="86c27-109">Definizione</span><span class="sxs-lookup"><span data-stu-id="86c27-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c27-110">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="86c27-110">Landscape</span></span> <br/>        | <span data-ttu-id="86c27-111">Il contenuto viene ruotato a pagina 90? gradi CCW rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="86c27-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="86c27-112">Verticale</span><span class="sxs-lookup"><span data-stu-id="86c27-112">Portrait</span></span> <br/>         | <span data-ttu-id="86c27-113">Orientamento standard.</span><span class="sxs-lookup"><span data-stu-id="86c27-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="86c27-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="86c27-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="86c27-115">Il contenuto viene ruotato nella pagina 270?? gradi CCW rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="86c27-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="86c27-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="86c27-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="86c27-117">Il contenuto viene ruotato nella pagina 180?? gradi rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="86c27-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="86c27-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="86c27-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="86c27-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="86c27-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="86c27-120">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="86c27-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="86c27-121">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="86c27-121">Element Information</span></span>



| <span data-ttu-id="86c27-122">Nome</span><span class="sxs-lookup"><span data-stu-id="86c27-122">Name</span></span> | <span data-ttu-id="86c27-123">Valore</span><span class="sxs-lookup"><span data-stu-id="86c27-123">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c27-124">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="86c27-124">Element Type</span></span> <br/>   | <span data-ttu-id="86c27-125">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="86c27-125">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="86c27-126">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="86c27-126">Scoping Prefix</span></span> <br/> | <span data-ttu-id="86c27-127">Pagina</span><span class="sxs-lookup"><span data-stu-id="86c27-127">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="86c27-128">Note</span><span class="sxs-lookup"><span data-stu-id="86c27-128">Notes</span></span> <br/>          | <span data-ttu-id="86c27-129">Se un dispositivo stampante può supportare solo una direzione orizzontale e questa direzione è detta "orizzontale inverso", l'orientamento della pagina verrà comunque considerato "orizzontale".</span><span class="sxs-lookup"><span data-stu-id="86c27-129">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="86c27-130">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="86c27-130">Structural Content</span></span>

<span data-ttu-id="86c27-131">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="86c27-131">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="86c27-132">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="86c27-132">Structure Variables</span></span>

<span data-ttu-id="86c27-133">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="86c27-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="86c27-134">Nome</span><span class="sxs-lookup"><span data-stu-id="86c27-134">Name</span></span>                               | <span data-ttu-id="86c27-135">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="86c27-135">Data type</span></span>         | <span data-ttu-id="86c27-136">Unità</span><span class="sxs-lookup"><span data-stu-id="86c27-136">Unit</span></span>                  | <span data-ttu-id="86c27-137">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="86c27-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="86c27-138">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="86c27-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="86c27-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="86c27-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="86c27-140">string</span><span class="sxs-lookup"><span data-stu-id="86c27-140">string</span></span><br/> | <span data-ttu-id="86c27-141">caratteri</span><span class="sxs-lookup"><span data-stu-id="86c27-141">characters</span></span><br/> | <span data-ttu-id="86c27-142">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="86c27-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="86c27-143">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="86c27-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="86c27-144">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="86c27-144">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="86c27-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="86c27-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="86c27-146">string</span><span class="sxs-lookup"><span data-stu-id="86c27-146">string</span></span><br/> | <span data-ttu-id="86c27-147">n/d</span><span class="sxs-lookup"><span data-stu-id="86c27-147">n/a</span></span><br/>        | <span data-ttu-id="86c27-148">True, False.</span><span class="sxs-lookup"><span data-stu-id="86c27-148">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="86c27-149">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="86c27-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="86c27-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="86c27-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="86c27-151">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="86c27-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="86c27-152">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="86c27-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="86c27-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86c27-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86c27-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="86c27-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




