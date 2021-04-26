---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92845b635aa7db1f44394cb6ef76b32292ea0dd4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996138"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="b404b-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="b404b-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="b404b-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b404b-105">This topic is not current.</span></span> <span data-ttu-id="b404b-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b404b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b404b-107">Definisce le caratteristiche del profilo colori di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b404b-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="b404b-108">Descrive se l'applicazione o il driver seleziona il profilo colori di destinazione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b404b-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="b404b-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b404b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b404b-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b404b-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b404b-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b404b-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b404b-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b404b-112">Element Information</span></span>



| <span data-ttu-id="b404b-113">Nome</span><span class="sxs-lookup"><span data-stu-id="b404b-113">Name</span></span> | <span data-ttu-id="b404b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b404b-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b404b-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b404b-115">Element Type</span></span> <br/>   | <span data-ttu-id="b404b-116">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="b404b-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b404b-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b404b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b404b-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="b404b-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b404b-119">Note</span><span class="sxs-lookup"><span data-stu-id="b404b-119">Notes</span></span> <br/>          | <span data-ttu-id="b404b-120">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il printTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="b404b-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="b404b-121">Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="b404b-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="b404b-122">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="b404b-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="b404b-123">Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="b404b-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="b404b-124">Ciò non è sicuro perché potrebbero non risolversi come previsto e potrebbero creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b404b-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b404b-125">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b404b-125">Structural Content</span></span>

<span data-ttu-id="b404b-126">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b404b-126">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b404b-127">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="b404b-127">Structure Variables</span></span>

<span data-ttu-id="b404b-128">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b404b-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b404b-129">Nome</span><span class="sxs-lookup"><span data-stu-id="b404b-129">Name</span></span>                               | <span data-ttu-id="b404b-130">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b404b-130">Data type</span></span>         | <span data-ttu-id="b404b-131">Unità</span><span class="sxs-lookup"><span data-stu-id="b404b-131">Unit</span></span>                  | <span data-ttu-id="b404b-132">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="b404b-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b404b-133">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="b404b-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b404b-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b404b-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b404b-135">string</span><span class="sxs-lookup"><span data-stu-id="b404b-135">string</span></span><br/> | <span data-ttu-id="b404b-136">caratteri</span><span class="sxs-lookup"><span data-stu-id="b404b-136">characters</span></span><br/> | <span data-ttu-id="b404b-137">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="b404b-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b404b-138">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="b404b-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b404b-139">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="b404b-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b404b-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b404b-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b404b-141">string</span><span class="sxs-lookup"><span data-stu-id="b404b-141">string</span></span><br/> | <span data-ttu-id="b404b-142">n/d</span><span class="sxs-lookup"><span data-stu-id="b404b-142">n/a</span></span><br/>        | <span data-ttu-id="b404b-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="b404b-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b404b-144">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b404b-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b404b-145">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b404b-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b404b-146">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="b404b-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b404b-147">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="b404b-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b404b-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b404b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b404b-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b404b-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




