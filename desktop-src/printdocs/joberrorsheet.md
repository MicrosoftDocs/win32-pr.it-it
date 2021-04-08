---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9d613bf3b3af980b5cb8e916eac115cd1a0cb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103886062"
---
# <a name="joberrorsheet"></a><span data-ttu-id="adeab-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="adeab-104">JobErrorSheet</span></span>

<span data-ttu-id="adeab-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="adeab-105">This topic is not current.</span></span> <span data-ttu-id="adeab-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="adeab-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="adeab-107">Descrive l'output del foglio di errore.</span><span class="sxs-lookup"><span data-stu-id="adeab-107">Describes the error sheet output.</span></span> <span data-ttu-id="adeab-108">L'intero processo avrà un solo foglio errori.</span><span class="sxs-lookup"><span data-stu-id="adeab-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="adeab-109">Il foglio di errore deve essere restituito nel PageMediaSize predefinito e usare il PageMediaType predefinito.</span><span class="sxs-lookup"><span data-stu-id="adeab-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="adeab-110">Il foglio di errore deve essere isolato dalla parte rimanente del processo.</span><span class="sxs-lookup"><span data-stu-id="adeab-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="adeab-111">Ciò significa che qualsiasi opzione di completamento o elaborazione, ad esempio JobDuplex, JobStaple o JobBinding, non deve includere il foglio errori.</span><span class="sxs-lookup"><span data-stu-id="adeab-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="adeab-112">Il foglio di errore dovrebbe essere visualizzato come foglio finale del processo.</span><span class="sxs-lookup"><span data-stu-id="adeab-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="adeab-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="adeab-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="adeab-114">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="adeab-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="adeab-115">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="adeab-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="adeab-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="adeab-116">Element Information</span></span>



| <span data-ttu-id="adeab-117">Nome</span><span class="sxs-lookup"><span data-stu-id="adeab-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adeab-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="adeab-118">Element Type</span></span> <br/>   | <span data-ttu-id="adeab-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="adeab-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="adeab-120">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="adeab-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="adeab-121">Processo</span><span class="sxs-lookup"><span data-stu-id="adeab-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="adeab-122">Note</span><span class="sxs-lookup"><span data-stu-id="adeab-122">Notes</span></span> <br/>          | <span data-ttu-id="adeab-123">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="adeab-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="adeab-124">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="adeab-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="adeab-125">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="adeab-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="adeab-126">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="adeab-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="adeab-127">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="adeab-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="adeab-128">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="adeab-128">Structural Content</span></span>

<span data-ttu-id="adeab-129">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="adeab-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="adeab-130">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="adeab-130">Structure Variables</span></span>

<span data-ttu-id="adeab-131">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="adeab-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="adeab-132">Nome</span><span class="sxs-lookup"><span data-stu-id="adeab-132">Name</span></span>                                             | <span data-ttu-id="adeab-133">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="adeab-133">Data type</span></span>         | <span data-ttu-id="adeab-134">Unità</span><span class="sxs-lookup"><span data-stu-id="adeab-134">Unit</span></span>                  | <span data-ttu-id="adeab-135">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="adeab-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="adeab-136">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="adeab-136">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="adeab-137">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="adeab-137">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="adeab-138">string</span><span class="sxs-lookup"><span data-stu-id="adeab-138">string</span></span><br/> | <span data-ttu-id="adeab-139">caratteri</span><span class="sxs-lookup"><span data-stu-id="adeab-139">characters</span></span><br/> | <span data-ttu-id="adeab-140">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="adeab-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="adeab-141">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="adeab-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="adeab-142">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="adeab-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="adeab-143">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="adeab-143">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="adeab-144">string</span><span class="sxs-lookup"><span data-stu-id="adeab-144">string</span></span><br/> | <span data-ttu-id="adeab-145">n/d</span><span class="sxs-lookup"><span data-stu-id="adeab-145">n/a</span></span><br/>        | <span data-ttu-id="adeab-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="adeab-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="adeab-147">Definisce i criteri di selezione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="adeab-147">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="adeab-148">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="adeab-148">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="adeab-149">string</span><span class="sxs-lookup"><span data-stu-id="adeab-149">string</span></span><br/> | <span data-ttu-id="adeab-150">n/d</span><span class="sxs-lookup"><span data-stu-id="adeab-150">n/a</span></span><br/>        | <span data-ttu-id="adeab-151">Nome completo valido definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="adeab-151">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="adeab-152">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="adeab-152">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="adeab-153">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="adeab-153">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="adeab-154">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="adeab-154">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="adeab-155">string</span><span class="sxs-lookup"><span data-stu-id="adeab-155">string</span></span><br/> | <span data-ttu-id="adeab-156">n/d</span><span class="sxs-lookup"><span data-stu-id="adeab-156">n/a</span></span><br/>        | <span data-ttu-id="adeab-157">True, False.</span><span class="sxs-lookup"><span data-stu-id="adeab-157">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="adeab-158">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="adeab-158">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="adeab-159">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="adeab-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="adeab-160">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="adeab-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="adeab-161">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="adeab-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="adeab-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="adeab-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adeab-163">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="adeab-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




