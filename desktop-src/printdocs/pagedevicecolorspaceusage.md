---
description: Esaminare l'elemento PageDeviceColorSpaceUsage configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b81a37d103d3ce5f1cbb1fb8c032a18d495c2c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396666"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="e5bfc-105">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="e5bfc-105">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="e5bfc-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-106">This topic is not current.</span></span> <span data-ttu-id="e5bfc-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e5bfc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e5bfc-108">Insieme al parametro PageDeviceColorSpaceProfileURI, questo parametro definisce il comportamento di rendering per gli elementi presentati in uno spazio colori del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-108">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="e5bfc-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e5bfc-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e5bfc-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e5bfc-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e5bfc-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e5bfc-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e5bfc-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e5bfc-112">Element Information</span></span>



| <span data-ttu-id="e5bfc-113">Nome</span><span class="sxs-lookup"><span data-stu-id="e5bfc-113">Name</span></span> | <span data-ttu-id="e5bfc-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e5bfc-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5bfc-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e5bfc-115">Element Type</span></span> <br/>   | <span data-ttu-id="e5bfc-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e5bfc-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e5bfc-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e5bfc-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e5bfc-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="e5bfc-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e5bfc-119">Note</span><span class="sxs-lookup"><span data-stu-id="e5bfc-119">Notes</span></span> <br/>          | <span data-ttu-id="e5bfc-120">Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="e5bfc-121">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="e5bfc-122">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="e5bfc-123">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="e5bfc-124">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="e5bfc-125">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e5bfc-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e5bfc-126">Structural Content</span></span>

<span data-ttu-id="e5bfc-127">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e5bfc-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e5bfc-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e5bfc-128">Structure Variables</span></span>

<span data-ttu-id="e5bfc-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e5bfc-130">Nome</span><span class="sxs-lookup"><span data-stu-id="e5bfc-130">Name</span></span>                               | <span data-ttu-id="e5bfc-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e5bfc-131">Data type</span></span>         | <span data-ttu-id="e5bfc-132">Unità</span><span class="sxs-lookup"><span data-stu-id="e5bfc-132">Unit</span></span>                  | <span data-ttu-id="e5bfc-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e5bfc-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e5bfc-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e5bfc-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e5bfc-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e5bfc-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e5bfc-136">string</span><span class="sxs-lookup"><span data-stu-id="e5bfc-136">string</span></span><br/> | <span data-ttu-id="e5bfc-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="e5bfc-137">characters</span></span><br/> | <span data-ttu-id="e5bfc-138">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e5bfc-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e5bfc-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e5bfc-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e5bfc-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e5bfc-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e5bfc-142">string</span><span class="sxs-lookup"><span data-stu-id="e5bfc-142">string</span></span><br/> | <span data-ttu-id="e5bfc-143">n/d</span><span class="sxs-lookup"><span data-stu-id="e5bfc-143">n/a</span></span><br/>        | <span data-ttu-id="e5bfc-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e5bfc-145">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e5bfc-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e5bfc-146">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e5bfc-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e5bfc-147">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="e5bfc-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e5bfc-148">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="e5bfc-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e5bfc-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5bfc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5bfc-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e5bfc-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




