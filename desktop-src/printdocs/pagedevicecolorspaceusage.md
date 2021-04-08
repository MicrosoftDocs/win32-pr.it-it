---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77f143457ea24d5c23aba443209ba35ce02454
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103886058"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="47110-104">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="47110-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="47110-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="47110-105">This topic is not current.</span></span> <span data-ttu-id="47110-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="47110-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47110-107">In combinazione con il parametro PageDeviceColorSpaceProfileURI, questo parametro definisce il comportamento di rendering per gli elementi presentati in uno spazio colore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47110-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="47110-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="47110-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="47110-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="47110-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="47110-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="47110-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="47110-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="47110-111">Element Information</span></span>



| <span data-ttu-id="47110-112">Nome</span><span class="sxs-lookup"><span data-stu-id="47110-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47110-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="47110-113">Element Type</span></span> <br/>   | <span data-ttu-id="47110-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="47110-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="47110-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="47110-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="47110-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="47110-116">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="47110-117">Note</span><span class="sxs-lookup"><span data-stu-id="47110-117">Notes</span></span> <br/>          | <span data-ttu-id="47110-118">Questo vale solo per i documenti XPS e non deve essere utilizzato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="47110-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="47110-119">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="47110-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="47110-120">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="47110-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="47110-121">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="47110-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="47110-122">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="47110-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="47110-123">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47110-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="47110-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="47110-124">Structural Content</span></span>

<span data-ttu-id="47110-125">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="47110-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
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

## <a name="structure-variables"></a><span data-ttu-id="47110-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="47110-126">Structure Variables</span></span>

<span data-ttu-id="47110-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="47110-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="47110-128">Nome</span><span class="sxs-lookup"><span data-stu-id="47110-128">Name</span></span>                               | <span data-ttu-id="47110-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="47110-129">Data type</span></span>         | <span data-ttu-id="47110-130">Unità</span><span class="sxs-lookup"><span data-stu-id="47110-130">Unit</span></span>                  | <span data-ttu-id="47110-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="47110-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="47110-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="47110-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="47110-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="47110-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="47110-134">string</span><span class="sxs-lookup"><span data-stu-id="47110-134">string</span></span><br/> | <span data-ttu-id="47110-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="47110-135">characters</span></span><br/> | <span data-ttu-id="47110-136">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="47110-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="47110-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="47110-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="47110-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="47110-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="47110-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="47110-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="47110-140">string</span><span class="sxs-lookup"><span data-stu-id="47110-140">string</span></span><br/> | <span data-ttu-id="47110-141">n/d</span><span class="sxs-lookup"><span data-stu-id="47110-141">n/a</span></span><br/>        | <span data-ttu-id="47110-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="47110-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="47110-143">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="47110-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="47110-144">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="47110-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="47110-145">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="47110-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="47110-146">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="47110-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="47110-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47110-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47110-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="47110-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




