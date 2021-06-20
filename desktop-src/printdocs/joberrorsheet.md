---
description: Informazioni sull'elemento JobErrorSheet, che descrive l'output del foglio di errore. L'intero processo avrà un singolo foglio di errore.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcee6c50d482793eeef96e29ad98385da11a4e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408904"
---
# <a name="joberrorsheet"></a><span data-ttu-id="2135b-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="2135b-104">JobErrorSheet</span></span>

<span data-ttu-id="2135b-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="2135b-105">This topic is not current.</span></span> <span data-ttu-id="2135b-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2135b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2135b-107">Descrive l'output del foglio di errore.</span><span class="sxs-lookup"><span data-stu-id="2135b-107">Describes the error sheet output.</span></span> <span data-ttu-id="2135b-108">L'intero processo avrà un singolo foglio di errore.</span><span class="sxs-lookup"><span data-stu-id="2135b-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="2135b-109">Il foglio di errore deve essere restituito nell'oggetto PageMediaSize predefinito e usando pageMediaType predefinito.</span><span class="sxs-lookup"><span data-stu-id="2135b-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="2135b-110">Il foglio degli errori deve essere isolato dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="2135b-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="2135b-111">Ciò significa che qualsiasi opzione di completamento o elaborazione (ad esempio JobDuplex, JobStaple o JobBinding) non deve includere il foglio di errore.</span><span class="sxs-lookup"><span data-stu-id="2135b-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="2135b-112">Il foglio degli errori deve essere visualizzato come foglio finale del processo.</span><span class="sxs-lookup"><span data-stu-id="2135b-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="2135b-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2135b-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2135b-114">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="2135b-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2135b-115">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2135b-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2135b-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2135b-116">Element Information</span></span>



| <span data-ttu-id="2135b-117">Nome</span><span class="sxs-lookup"><span data-stu-id="2135b-117">Name</span></span> | <span data-ttu-id="2135b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2135b-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2135b-119">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="2135b-119">Element Type</span></span> <br/>   | <span data-ttu-id="2135b-120">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="2135b-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2135b-121">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="2135b-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2135b-122">Processo</span><span class="sxs-lookup"><span data-stu-id="2135b-122">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2135b-123">Note</span><span class="sxs-lookup"><span data-stu-id="2135b-123">Notes</span></span> <br/>          | <span data-ttu-id="2135b-124">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="2135b-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="2135b-125">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="2135b-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="2135b-126">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="2135b-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="2135b-127">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="2135b-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="2135b-128">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2135b-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2135b-129">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="2135b-129">Structural Content</span></span>

<span data-ttu-id="2135b-130">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="2135b-130">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2135b-131">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="2135b-131">Structure Variables</span></span>

<span data-ttu-id="2135b-132">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="2135b-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2135b-133">Nome</span><span class="sxs-lookup"><span data-stu-id="2135b-133">Name</span></span>                                             | <span data-ttu-id="2135b-134">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2135b-134">Data type</span></span>         | <span data-ttu-id="2135b-135">Unità</span><span class="sxs-lookup"><span data-stu-id="2135b-135">Unit</span></span>                  | <span data-ttu-id="2135b-136">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="2135b-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2135b-137">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="2135b-137">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2135b-138">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="2135b-138">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="2135b-139">string</span><span class="sxs-lookup"><span data-stu-id="2135b-139">string</span></span><br/> | <span data-ttu-id="2135b-140">caratteri</span><span class="sxs-lookup"><span data-stu-id="2135b-140">characters</span></span><br/> | <span data-ttu-id="2135b-141">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="2135b-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2135b-142">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="2135b-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2135b-143">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="2135b-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2135b-144">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2135b-144">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2135b-145">string</span><span class="sxs-lookup"><span data-stu-id="2135b-145">string</span></span><br/> | <span data-ttu-id="2135b-146">n/d</span><span class="sxs-lookup"><span data-stu-id="2135b-146">n/a</span></span><br/>        | <span data-ttu-id="2135b-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="2135b-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2135b-148">Definisce i criteri di selezione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2135b-148">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="2135b-149">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2135b-149">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="2135b-150">string</span><span class="sxs-lookup"><span data-stu-id="2135b-150">string</span></span><br/> | <span data-ttu-id="2135b-151">n/d</span><span class="sxs-lookup"><span data-stu-id="2135b-151">n/a</span></span><br/>        | <span data-ttu-id="2135b-152">Nome completo valido come definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="2135b-152">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="2135b-153">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="2135b-153">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="2135b-154">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="2135b-154">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2135b-155">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2135b-155">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="2135b-156">string</span><span class="sxs-lookup"><span data-stu-id="2135b-156">string</span></span><br/> | <span data-ttu-id="2135b-157">n/d</span><span class="sxs-lookup"><span data-stu-id="2135b-157">n/a</span></span><br/>        | <span data-ttu-id="2135b-158">True, False.</span><span class="sxs-lookup"><span data-stu-id="2135b-158">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2135b-159">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2135b-159">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2135b-160">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2135b-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2135b-161">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi .</span><span class="sxs-lookup"><span data-stu-id="2135b-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2135b-162">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="2135b-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2135b-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2135b-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2135b-164">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="2135b-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




