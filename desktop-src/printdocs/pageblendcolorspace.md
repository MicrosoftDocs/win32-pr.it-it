---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf68660929839fad79be26daebf32b9bc0f7ea5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321132"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="08d22-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="08d22-104">PageBlendColorSpace</span></span>

<span data-ttu-id="08d22-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="08d22-105">This topic is not current.</span></span> <span data-ttu-id="08d22-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="08d22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="08d22-107">Descrive lo spazio dei colori da usare per le operazioni di fusione.</span><span class="sxs-lookup"><span data-stu-id="08d22-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="08d22-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="08d22-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="08d22-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="08d22-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="08d22-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="08d22-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="08d22-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="08d22-111">Element Information</span></span>



| <span data-ttu-id="08d22-112">Nome</span><span class="sxs-lookup"><span data-stu-id="08d22-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d22-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="08d22-113">Element Type</span></span> <br/>   | <span data-ttu-id="08d22-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="08d22-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="08d22-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="08d22-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="08d22-116">Processo</span><span class="sxs-lookup"><span data-stu-id="08d22-116">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="08d22-117">Note</span><span class="sxs-lookup"><span data-stu-id="08d22-117">Notes</span></span> <br/>          | <span data-ttu-id="08d22-118">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="08d22-118">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="08d22-119">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="08d22-119">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="08d22-120">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="08d22-120">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="08d22-121">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="08d22-121">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="08d22-122">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="08d22-122">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="08d22-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="08d22-123">Structural Content</span></span>

<span data-ttu-id="08d22-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="08d22-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="08d22-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="08d22-125">Structure Variables</span></span>

<span data-ttu-id="08d22-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="08d22-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="08d22-127">Nome</span><span class="sxs-lookup"><span data-stu-id="08d22-127">Name</span></span>                               | <span data-ttu-id="08d22-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="08d22-128">Data type</span></span>         | <span data-ttu-id="08d22-129">Unità</span><span class="sxs-lookup"><span data-stu-id="08d22-129">Unit</span></span>                  | <span data-ttu-id="08d22-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="08d22-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="08d22-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="08d22-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="08d22-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="08d22-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="08d22-133">string</span><span class="sxs-lookup"><span data-stu-id="08d22-133">string</span></span><br/> | <span data-ttu-id="08d22-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="08d22-134">characters</span></span><br/> | <span data-ttu-id="08d22-135">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="08d22-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="08d22-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="08d22-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="08d22-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="08d22-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="08d22-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="08d22-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="08d22-139">string</span><span class="sxs-lookup"><span data-stu-id="08d22-139">string</span></span><br/> | <span data-ttu-id="08d22-140">n/d</span><span class="sxs-lookup"><span data-stu-id="08d22-140">n/a</span></span><br/>        | <span data-ttu-id="08d22-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="08d22-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="08d22-142">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="08d22-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="08d22-143">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="08d22-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="08d22-144">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="08d22-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="08d22-145">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="08d22-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="08d22-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08d22-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d22-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="08d22-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




