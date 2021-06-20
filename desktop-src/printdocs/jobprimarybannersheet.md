---
description: Informazioni sull'elemento JobPrimaryBannerSheet, che descrive il foglio banner da visualizzare come output per il processo.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39922f65d71ea0cc6d6de6103bc159f79467038f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408754"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="6ca23-103">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="6ca23-103">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="6ca23-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6ca23-104">This topic is not current.</span></span> <span data-ttu-id="6ca23-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6ca23-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ca23-106">Descrive il foglio di intestazione da visualizzare come output per il processo.</span><span class="sxs-lookup"><span data-stu-id="6ca23-106">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="6ca23-107">Il foglio banner deve essere restituito nel valore pageMediaSize predefinito e usando il pageMediaType predefinito.</span><span class="sxs-lookup"><span data-stu-id="6ca23-107">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="6ca23-108">Il foglio banner deve essere isolato dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="6ca23-108">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="6ca23-109">Ciò significa che qualsiasi opzione di completamento o elaborazione (ad esempio JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments) non deve includere il foglio banner.</span><span class="sxs-lookup"><span data-stu-id="6ca23-109">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="6ca23-110">Il foglio banner deve essere il primo foglio del processo.</span><span class="sxs-lookup"><span data-stu-id="6ca23-110">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="6ca23-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6ca23-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6ca23-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6ca23-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6ca23-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6ca23-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6ca23-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6ca23-114">Element Information</span></span>



| <span data-ttu-id="6ca23-115">Nome</span><span class="sxs-lookup"><span data-stu-id="6ca23-115">Name</span></span> | <span data-ttu-id="6ca23-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6ca23-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca23-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6ca23-117">Element Type</span></span> <br/>   | <span data-ttu-id="6ca23-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="6ca23-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6ca23-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6ca23-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6ca23-120">Processo</span><span class="sxs-lookup"><span data-stu-id="6ca23-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6ca23-121">Note</span><span class="sxs-lookup"><span data-stu-id="6ca23-121">Notes</span></span> <br/>          | <span data-ttu-id="6ca23-122">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="6ca23-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6ca23-123">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="6ca23-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6ca23-124">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="6ca23-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6ca23-125">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="6ca23-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6ca23-126">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6ca23-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6ca23-127">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6ca23-127">Structural Content</span></span>

<span data-ttu-id="6ca23-128">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6ca23-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="6ca23-129">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6ca23-129">Structure Variables</span></span>

<span data-ttu-id="6ca23-130">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6ca23-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6ca23-131">Nome</span><span class="sxs-lookup"><span data-stu-id="6ca23-131">Name</span></span>                               | <span data-ttu-id="6ca23-132">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6ca23-132">Data type</span></span>         | <span data-ttu-id="6ca23-133">Unità</span><span class="sxs-lookup"><span data-stu-id="6ca23-133">Unit</span></span>                  | <span data-ttu-id="6ca23-134">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6ca23-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6ca23-135">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6ca23-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6ca23-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6ca23-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6ca23-137">string</span><span class="sxs-lookup"><span data-stu-id="6ca23-137">string</span></span><br/> | <span data-ttu-id="6ca23-138">caratteri</span><span class="sxs-lookup"><span data-stu-id="6ca23-138">characters</span></span><br/> | <span data-ttu-id="6ca23-139">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6ca23-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6ca23-140">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6ca23-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6ca23-141">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6ca23-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6ca23-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6ca23-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6ca23-143">string</span><span class="sxs-lookup"><span data-stu-id="6ca23-143">string</span></span><br/> | <span data-ttu-id="6ca23-144">n/d</span><span class="sxs-lookup"><span data-stu-id="6ca23-144">n/a</span></span><br/>        | <span data-ttu-id="6ca23-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="6ca23-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6ca23-146">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6ca23-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6ca23-147">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6ca23-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6ca23-148">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi .</span><span class="sxs-lookup"><span data-stu-id="6ca23-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6ca23-149">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6ca23-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6ca23-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ca23-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ca23-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6ca23-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




