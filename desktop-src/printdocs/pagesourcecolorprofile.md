---
description: Informazioni sull'elemento PageSourceColorProfile. Questo elemento definisce le caratteristiche del profilo colore di origine.
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709d44f8af7ea6c2709201e57bc047fe9b2d21b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118996"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="f51ab-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="f51ab-104">PageSourceColorProfile</span></span>

<span data-ttu-id="f51ab-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f51ab-105">This topic is not current.</span></span> <span data-ttu-id="f51ab-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f51ab-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f51ab-107">Definisce le caratteristiche del profilo colore di origine.</span><span class="sxs-lookup"><span data-stu-id="f51ab-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="f51ab-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f51ab-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f51ab-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f51ab-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f51ab-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f51ab-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f51ab-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f51ab-111">Element Information</span></span>



| <span data-ttu-id="f51ab-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f51ab-112">Name</span></span>                       | <span data-ttu-id="f51ab-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f51ab-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51ab-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f51ab-114">Element Type</span></span> <br/>   | <span data-ttu-id="f51ab-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="f51ab-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f51ab-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f51ab-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f51ab-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="f51ab-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f51ab-118">Note</span><span class="sxs-lookup"><span data-stu-id="f51ab-118">Notes</span></span> <br/>          | <span data-ttu-id="f51ab-119">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il printTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="f51ab-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="f51ab-120">Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="f51ab-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="f51ab-121">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="f51ab-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="f51ab-122">Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="f51ab-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="f51ab-123">Ciò non è sicuro perché potrebbero non risolversi come previsto e potrebbero creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f51ab-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f51ab-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f51ab-124">Structural Content</span></span>

<span data-ttu-id="f51ab-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f51ab-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="f51ab-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="f51ab-126">Structure Variables</span></span>

<span data-ttu-id="f51ab-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f51ab-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f51ab-128">Nome</span><span class="sxs-lookup"><span data-stu-id="f51ab-128">Name</span></span>                               | <span data-ttu-id="f51ab-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f51ab-129">Data type</span></span>         | <span data-ttu-id="f51ab-130">Unità</span><span class="sxs-lookup"><span data-stu-id="f51ab-130">Unit</span></span>                  | <span data-ttu-id="f51ab-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="f51ab-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f51ab-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f51ab-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f51ab-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f51ab-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f51ab-134">string</span><span class="sxs-lookup"><span data-stu-id="f51ab-134">string</span></span><br/> | <span data-ttu-id="f51ab-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="f51ab-135">characters</span></span><br/> | <span data-ttu-id="f51ab-136">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f51ab-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f51ab-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="f51ab-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f51ab-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="f51ab-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f51ab-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f51ab-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f51ab-140">string</span><span class="sxs-lookup"><span data-stu-id="f51ab-140">string</span></span><br/> | <span data-ttu-id="f51ab-141">n/d</span><span class="sxs-lookup"><span data-stu-id="f51ab-141">n/a</span></span><br/>        | <span data-ttu-id="f51ab-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="f51ab-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f51ab-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f51ab-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f51ab-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f51ab-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f51ab-145">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="f51ab-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f51ab-146">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="f51ab-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Option name="psk:RGB">
    <!-- Source profile used to perform color management for untagged RGB data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CMYK">
    <!-- Source profile used to perform color management for untagged CMYK data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f51ab-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f51ab-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f51ab-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f51ab-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




