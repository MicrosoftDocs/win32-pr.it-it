---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f004329c217d4aab6ddc3c1d166037e7c7b5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104401850"
---
# <a name="pageorientation"></a><span data-ttu-id="41091-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="41091-104">PageOrientation</span></span>

<span data-ttu-id="41091-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="41091-105">This topic is not current.</span></span> <span data-ttu-id="41091-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="41091-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="41091-107">Descrive l'orientamento del foglio multimediale fisico.</span><span class="sxs-lookup"><span data-stu-id="41091-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="41091-108">Opzione</span><span class="sxs-lookup"><span data-stu-id="41091-108">Option</span></span>                       | <span data-ttu-id="41091-109">Definizione</span><span class="sxs-lookup"><span data-stu-id="41091-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41091-110">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="41091-110">Landscape</span></span> <br/>        | <span data-ttu-id="41091-111">Il contenuto viene ruotato nella pagina 90? gradi in senso antiorario rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="41091-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="41091-112">Verticale</span><span class="sxs-lookup"><span data-stu-id="41091-112">Portrait</span></span> <br/>         | <span data-ttu-id="41091-113">Orientamento standard.</span><span class="sxs-lookup"><span data-stu-id="41091-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="41091-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="41091-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="41091-115">Il contenuto viene ruotato nella pagina 270? gradi in senso antiorario rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="41091-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="41091-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="41091-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="41091-117">Il contenuto viene ruotato nella pagina 180? gradi rispetto all'orientamento standard (verticale).</span><span class="sxs-lookup"><span data-stu-id="41091-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="41091-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="41091-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="41091-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="41091-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="41091-120">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="41091-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="41091-121">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="41091-121">Element Information</span></span>



| <span data-ttu-id="41091-122">Nome</span><span class="sxs-lookup"><span data-stu-id="41091-122">Name</span></span>                       |                                                                                                                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41091-123">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="41091-123">Element Type</span></span> <br/>   | <span data-ttu-id="41091-124">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="41091-124">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="41091-125">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="41091-125">Scoping Prefix</span></span> <br/> | <span data-ttu-id="41091-126">Pagina</span><span class="sxs-lookup"><span data-stu-id="41091-126">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="41091-127">Note</span><span class="sxs-lookup"><span data-stu-id="41091-127">Notes</span></span> <br/>          | <span data-ttu-id="41091-128">Se un dispositivo stampante può supportare solo una direzione orizzontale e questa direzione è detta "orizzontale inverso", l'orientamento della pagina verrà comunque considerato "orizzontale".</span><span class="sxs-lookup"><span data-stu-id="41091-128">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="41091-129">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="41091-129">Structural Content</span></span>

<span data-ttu-id="41091-130">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="41091-130">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="41091-131">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="41091-131">Structure Variables</span></span>

<span data-ttu-id="41091-132">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="41091-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="41091-133">Nome</span><span class="sxs-lookup"><span data-stu-id="41091-133">Name</span></span>                               | <span data-ttu-id="41091-134">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="41091-134">Data type</span></span>         | <span data-ttu-id="41091-135">Unità</span><span class="sxs-lookup"><span data-stu-id="41091-135">Unit</span></span>                  | <span data-ttu-id="41091-136">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="41091-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="41091-137">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="41091-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="41091-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="41091-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="41091-139">string</span><span class="sxs-lookup"><span data-stu-id="41091-139">string</span></span><br/> | <span data-ttu-id="41091-140">caratteri</span><span class="sxs-lookup"><span data-stu-id="41091-140">characters</span></span><br/> | <span data-ttu-id="41091-141">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="41091-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="41091-142">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="41091-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="41091-143">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="41091-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="41091-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="41091-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="41091-145">string</span><span class="sxs-lookup"><span data-stu-id="41091-145">string</span></span><br/> | <span data-ttu-id="41091-146">n/d</span><span class="sxs-lookup"><span data-stu-id="41091-146">n/a</span></span><br/>        | <span data-ttu-id="41091-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="41091-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="41091-148">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="41091-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="41091-149">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="41091-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="41091-150">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="41091-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="41091-151">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="41091-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="41091-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41091-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41091-153">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="41091-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




