---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12002b25265a66a0aa3a5168f29e1e8e542ce31
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998078"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="86a22-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="86a22-104">PageBlendColorSpace</span></span>

<span data-ttu-id="86a22-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="86a22-105">This topic is not current.</span></span> <span data-ttu-id="86a22-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="86a22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="86a22-107">Descrive lo spazio colore da usare per le operazioni di fusione.</span><span class="sxs-lookup"><span data-stu-id="86a22-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="86a22-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="86a22-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="86a22-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="86a22-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="86a22-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="86a22-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="86a22-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="86a22-111">Element Information</span></span>



| <span data-ttu-id="86a22-112">Nome</span><span class="sxs-lookup"><span data-stu-id="86a22-112">Name</span></span> | <span data-ttu-id="86a22-113">Valore</span><span class="sxs-lookup"><span data-stu-id="86a22-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a22-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="86a22-114">Element Type</span></span> <br/>   | <span data-ttu-id="86a22-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="86a22-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="86a22-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="86a22-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="86a22-117">Processo</span><span class="sxs-lookup"><span data-stu-id="86a22-117">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="86a22-118">Note</span><span class="sxs-lookup"><span data-stu-id="86a22-118">Notes</span></span> <br/>          | <span data-ttu-id="86a22-119">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="86a22-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="86a22-120">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="86a22-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="86a22-121">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="86a22-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="86a22-122">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="86a22-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="86a22-123">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="86a22-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="86a22-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="86a22-124">Structural Content</span></span>

<span data-ttu-id="86a22-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="86a22-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="86a22-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="86a22-126">Structure Variables</span></span>

<span data-ttu-id="86a22-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="86a22-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="86a22-128">Nome</span><span class="sxs-lookup"><span data-stu-id="86a22-128">Name</span></span>                               | <span data-ttu-id="86a22-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="86a22-129">Data type</span></span>         | <span data-ttu-id="86a22-130">Unità</span><span class="sxs-lookup"><span data-stu-id="86a22-130">Unit</span></span>                  | <span data-ttu-id="86a22-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="86a22-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="86a22-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="86a22-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="86a22-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="86a22-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="86a22-134">string</span><span class="sxs-lookup"><span data-stu-id="86a22-134">string</span></span><br/> | <span data-ttu-id="86a22-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="86a22-135">characters</span></span><br/> | <span data-ttu-id="86a22-136">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="86a22-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="86a22-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="86a22-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="86a22-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="86a22-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="86a22-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="86a22-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="86a22-140">string</span><span class="sxs-lookup"><span data-stu-id="86a22-140">string</span></span><br/> | <span data-ttu-id="86a22-141">n/d</span><span class="sxs-lookup"><span data-stu-id="86a22-141">n/a</span></span><br/>        | <span data-ttu-id="86a22-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="86a22-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="86a22-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="86a22-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="86a22-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="86a22-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="86a22-145">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="86a22-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="86a22-146">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="86a22-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="86a22-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86a22-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86a22-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="86a22-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




