---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf26811bc8c008fa06d647b25e48914a6e724d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999178"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="fe7e4-104">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="fe7e4-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="fe7e4-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-105">This topic is not current.</span></span> <span data-ttu-id="fe7e4-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fe7e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fe7e4-107">In combinazione con il parametro PageDeviceColorSpaceProfileURI, questo parametro definisce il comportamento di rendering per gli elementi presentati in uno spazio colori del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="fe7e4-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fe7e4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fe7e4-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="fe7e4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fe7e4-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fe7e4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fe7e4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fe7e4-111">Element Information</span></span>



| <span data-ttu-id="fe7e4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="fe7e4-112">Name</span></span> | <span data-ttu-id="fe7e4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="fe7e4-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe7e4-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="fe7e4-114">Element Type</span></span> <br/>   | <span data-ttu-id="fe7e4-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="fe7e4-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fe7e4-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="fe7e4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fe7e4-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="fe7e4-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe7e4-118">Note</span><span class="sxs-lookup"><span data-stu-id="fe7e4-118">Notes</span></span> <br/>          | <span data-ttu-id="fe7e4-119">Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="fe7e4-120">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="fe7e4-121">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="fe7e4-122">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="fe7e4-123">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="fe7e4-124">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="fe7e4-125">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="fe7e4-125">Structural Content</span></span>

<span data-ttu-id="fe7e4-126">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="fe7e4-126">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="fe7e4-127">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="fe7e4-127">Structure Variables</span></span>

<span data-ttu-id="fe7e4-128">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fe7e4-129">Nome</span><span class="sxs-lookup"><span data-stu-id="fe7e4-129">Name</span></span>                               | <span data-ttu-id="fe7e4-130">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fe7e4-130">Data type</span></span>         | <span data-ttu-id="fe7e4-131">Unità</span><span class="sxs-lookup"><span data-stu-id="fe7e4-131">Unit</span></span>                  | <span data-ttu-id="fe7e4-132">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="fe7e4-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fe7e4-133">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="fe7e4-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fe7e4-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fe7e4-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="fe7e4-135">string</span><span class="sxs-lookup"><span data-stu-id="fe7e4-135">string</span></span><br/> | <span data-ttu-id="fe7e4-136">caratteri</span><span class="sxs-lookup"><span data-stu-id="fe7e4-136">characters</span></span><br/> | <span data-ttu-id="fe7e4-137">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="fe7e4-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fe7e4-138">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fe7e4-139">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="fe7e4-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fe7e4-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="fe7e4-141">string</span><span class="sxs-lookup"><span data-stu-id="fe7e4-141">string</span></span><br/> | <span data-ttu-id="fe7e4-142">n/d</span><span class="sxs-lookup"><span data-stu-id="fe7e4-142">n/a</span></span><br/>        | <span data-ttu-id="fe7e4-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fe7e4-144">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fe7e4-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fe7e4-145">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="fe7e4-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fe7e4-146">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="fe7e4-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fe7e4-147">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="fe7e4-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fe7e4-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe7e4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe7e4-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="fe7e4-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




