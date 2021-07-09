---
description: Esaminare l'elemento configurabile dall'utente PageDestinationColorProfile. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c12e8b6e322f024c3603abc97b0e4e0413d5b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549219"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="ad9f6-105">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="ad9f6-105">PageDestinationColorProfile</span></span>

<span data-ttu-id="ad9f6-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-106">This topic is not current.</span></span> <span data-ttu-id="ad9f6-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ad9f6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad9f6-108">Definisce le caratteristiche del profilo colori di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-108">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="ad9f6-109">Descrive se l'applicazione o il driver seleziona il profilo colori di destinazione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-109">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="ad9f6-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ad9f6-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad9f6-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ad9f6-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ad9f6-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ad9f6-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ad9f6-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ad9f6-113">Element Information</span></span>



| <span data-ttu-id="ad9f6-114">Nome</span><span class="sxs-lookup"><span data-stu-id="ad9f6-114">Name</span></span> | <span data-ttu-id="ad9f6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ad9f6-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9f6-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ad9f6-116">Element Type</span></span> <br/>   | <span data-ttu-id="ad9f6-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="ad9f6-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ad9f6-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="ad9f6-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad9f6-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="ad9f6-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ad9f6-120">Note</span><span class="sxs-lookup"><span data-stu-id="ad9f6-120">Notes</span></span> <br/>          | <span data-ttu-id="ad9f6-121">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket DEVE fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="ad9f6-122">Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="ad9f6-123">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="ad9f6-124">Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="ad9f6-125">Ciò non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ad9f6-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ad9f6-126">Structural Content</span></span>

<span data-ttu-id="ad9f6-127">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="ad9f6-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ad9f6-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ad9f6-128">Structure Variables</span></span>

<span data-ttu-id="ad9f6-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad9f6-130">Nome</span><span class="sxs-lookup"><span data-stu-id="ad9f6-130">Name</span></span>                               | <span data-ttu-id="ad9f6-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad9f6-131">Data type</span></span>         | <span data-ttu-id="ad9f6-132">Unità</span><span class="sxs-lookup"><span data-stu-id="ad9f6-132">Unit</span></span>                  | <span data-ttu-id="ad9f6-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ad9f6-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ad9f6-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ad9f6-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ad9f6-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ad9f6-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ad9f6-136">string</span><span class="sxs-lookup"><span data-stu-id="ad9f6-136">string</span></span><br/> | <span data-ttu-id="ad9f6-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="ad9f6-137">characters</span></span><br/> | <span data-ttu-id="ad9f6-138">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ad9f6-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ad9f6-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ad9f6-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ad9f6-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ad9f6-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ad9f6-142">string</span><span class="sxs-lookup"><span data-stu-id="ad9f6-142">string</span></span><br/> | <span data-ttu-id="ad9f6-143">n/d</span><span class="sxs-lookup"><span data-stu-id="ad9f6-143">n/a</span></span><br/>        | <span data-ttu-id="ad9f6-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ad9f6-145">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ad9f6-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ad9f6-146">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ad9f6-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ad9f6-147">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="ad9f6-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ad9f6-148">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="ad9f6-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ad9f6-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad9f6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad9f6-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ad9f6-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




