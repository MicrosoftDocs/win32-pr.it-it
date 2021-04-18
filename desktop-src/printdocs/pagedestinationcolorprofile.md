---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde6077bc2bae611c2a791ecf041cb52588c2ebb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321121"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="c29ab-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="c29ab-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="c29ab-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c29ab-105">This topic is not current.</span></span> <span data-ttu-id="c29ab-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c29ab-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c29ab-107">Definisce le caratteristiche del profilo colori di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c29ab-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="c29ab-108">Descrive se l'applicazione o il driver seleziona il profilo colori di destinazione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c29ab-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="c29ab-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c29ab-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c29ab-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="c29ab-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c29ab-111">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c29ab-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c29ab-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c29ab-112">Element Information</span></span>



| <span data-ttu-id="c29ab-113">Nome</span><span class="sxs-lookup"><span data-stu-id="c29ab-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29ab-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c29ab-114">Element Type</span></span> <br/>   | <span data-ttu-id="c29ab-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="c29ab-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c29ab-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="c29ab-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c29ab-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="c29ab-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c29ab-118">Note</span><span class="sxs-lookup"><span data-stu-id="c29ab-118">Notes</span></span> <br/>          | <span data-ttu-id="c29ab-119">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="c29ab-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="c29ab-120">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="c29ab-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="c29ab-121">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="c29ab-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="c29ab-122">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="c29ab-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="c29ab-123">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c29ab-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c29ab-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="c29ab-124">Structural Content</span></span>

<span data-ttu-id="c29ab-125">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c29ab-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="c29ab-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="c29ab-126">Structure Variables</span></span>

<span data-ttu-id="c29ab-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c29ab-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c29ab-128">Nome</span><span class="sxs-lookup"><span data-stu-id="c29ab-128">Name</span></span>                               | <span data-ttu-id="c29ab-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c29ab-129">Data type</span></span>         | <span data-ttu-id="c29ab-130">Unità</span><span class="sxs-lookup"><span data-stu-id="c29ab-130">Unit</span></span>                  | <span data-ttu-id="c29ab-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="c29ab-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c29ab-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="c29ab-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c29ab-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c29ab-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c29ab-134">string</span><span class="sxs-lookup"><span data-stu-id="c29ab-134">string</span></span><br/> | <span data-ttu-id="c29ab-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="c29ab-135">characters</span></span><br/> | <span data-ttu-id="c29ab-136">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c29ab-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c29ab-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="c29ab-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c29ab-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="c29ab-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c29ab-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c29ab-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c29ab-140">string</span><span class="sxs-lookup"><span data-stu-id="c29ab-140">string</span></span><br/> | <span data-ttu-id="c29ab-141">n/d</span><span class="sxs-lookup"><span data-stu-id="c29ab-141">n/a</span></span><br/>        | <span data-ttu-id="c29ab-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="c29ab-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c29ab-143">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c29ab-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c29ab-144">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="c29ab-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c29ab-145">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c29ab-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c29ab-146">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="c29ab-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c29ab-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c29ab-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c29ab-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c29ab-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




