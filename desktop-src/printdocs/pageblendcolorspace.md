---
description: Informazioni sull'elemento configurabile dall'utente PageBlendColorSpace. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36ce3a1def74058014fc396d9ef53aed6a32302
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549339"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="d1455-105">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="d1455-105">PageBlendColorSpace</span></span>

<span data-ttu-id="d1455-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="d1455-106">This topic is not current.</span></span> <span data-ttu-id="d1455-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d1455-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d1455-108">Descrive lo spazio colore da utilizzare per le operazioni di fusione.</span><span class="sxs-lookup"><span data-stu-id="d1455-108">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="d1455-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d1455-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d1455-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d1455-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d1455-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d1455-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d1455-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d1455-112">Element Information</span></span>



| <span data-ttu-id="d1455-113">Nome</span><span class="sxs-lookup"><span data-stu-id="d1455-113">Name</span></span> | <span data-ttu-id="d1455-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d1455-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1455-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d1455-115">Element Type</span></span> <br/>   | <span data-ttu-id="d1455-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="d1455-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d1455-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="d1455-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d1455-118">Processo</span><span class="sxs-lookup"><span data-stu-id="d1455-118">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d1455-119">Note</span><span class="sxs-lookup"><span data-stu-id="d1455-119">Notes</span></span> <br/>          | <span data-ttu-id="d1455-120">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket DEVE fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="d1455-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="d1455-121">Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="d1455-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="d1455-122">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="d1455-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="d1455-123">Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="d1455-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="d1455-124">Ciò non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d1455-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="d1455-125">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d1455-125">Structural Content</span></span>

<span data-ttu-id="d1455-126">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="d1455-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="d1455-127">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="d1455-127">Structure Variables</span></span>

<span data-ttu-id="d1455-128">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="d1455-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d1455-129">Nome</span><span class="sxs-lookup"><span data-stu-id="d1455-129">Name</span></span>                               | <span data-ttu-id="d1455-130">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d1455-130">Data type</span></span>         | <span data-ttu-id="d1455-131">Unità</span><span class="sxs-lookup"><span data-stu-id="d1455-131">Unit</span></span>                  | <span data-ttu-id="d1455-132">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="d1455-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d1455-133">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="d1455-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d1455-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d1455-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d1455-135">string</span><span class="sxs-lookup"><span data-stu-id="d1455-135">string</span></span><br/> | <span data-ttu-id="d1455-136">caratteri</span><span class="sxs-lookup"><span data-stu-id="d1455-136">characters</span></span><br/> | <span data-ttu-id="d1455-137">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d1455-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d1455-138">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="d1455-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d1455-139">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="d1455-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d1455-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d1455-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d1455-141">string</span><span class="sxs-lookup"><span data-stu-id="d1455-141">string</span></span><br/> | <span data-ttu-id="d1455-142">n/d</span><span class="sxs-lookup"><span data-stu-id="d1455-142">n/a</span></span><br/>        | <span data-ttu-id="d1455-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="d1455-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d1455-144">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d1455-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d1455-145">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d1455-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d1455-146">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="d1455-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d1455-147">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="d1455-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d1455-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1455-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1455-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="d1455-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




