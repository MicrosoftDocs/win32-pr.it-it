---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c438cd0f33bc7b3a80fc3e654e0d64831e3b6777
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996928"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="5d69c-104">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="5d69c-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="5d69c-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5d69c-105">This topic is not current.</span></span> <span data-ttu-id="5d69c-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5d69c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5d69c-107">Descrive il foglio banner da visualizzare come output per il processo.</span><span class="sxs-lookup"><span data-stu-id="5d69c-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="5d69c-108">Il foglio banner deve essere restituito nel valore pageMediaSize predefinito e usando il pageMediaType predefinito.</span><span class="sxs-lookup"><span data-stu-id="5d69c-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="5d69c-109">Il foglio banner deve essere isolato dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="5d69c-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="5d69c-110">Ciò significa che qualsiasi opzione di completamento o elaborazione (ad esempio JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments) non deve includere il foglio banner.</span><span class="sxs-lookup"><span data-stu-id="5d69c-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="5d69c-111">Il foglio banner deve essere il primo foglio del processo.</span><span class="sxs-lookup"><span data-stu-id="5d69c-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="5d69c-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5d69c-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5d69c-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5d69c-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5d69c-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5d69c-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5d69c-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5d69c-115">Element Information</span></span>



| <span data-ttu-id="5d69c-116">Nome</span><span class="sxs-lookup"><span data-stu-id="5d69c-116">Name</span></span> | <span data-ttu-id="5d69c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5d69c-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d69c-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5d69c-118">Element Type</span></span> <br/>   | <span data-ttu-id="5d69c-119">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="5d69c-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5d69c-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5d69c-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5d69c-121">Processo</span><span class="sxs-lookup"><span data-stu-id="5d69c-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5d69c-122">Note</span><span class="sxs-lookup"><span data-stu-id="5d69c-122">Notes</span></span> <br/>          | <span data-ttu-id="5d69c-123">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="5d69c-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="5d69c-124">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="5d69c-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="5d69c-125">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="5d69c-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="5d69c-126">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="5d69c-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="5d69c-127">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5d69c-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5d69c-128">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5d69c-128">Structural Content</span></span>

<span data-ttu-id="5d69c-129">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5d69c-129">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5d69c-130">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="5d69c-130">Structure Variables</span></span>

<span data-ttu-id="5d69c-131">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5d69c-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5d69c-132">Nome</span><span class="sxs-lookup"><span data-stu-id="5d69c-132">Name</span></span>                               | <span data-ttu-id="5d69c-133">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5d69c-133">Data type</span></span>         | <span data-ttu-id="5d69c-134">Unità</span><span class="sxs-lookup"><span data-stu-id="5d69c-134">Unit</span></span>                  | <span data-ttu-id="5d69c-135">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="5d69c-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5d69c-136">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5d69c-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5d69c-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5d69c-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5d69c-138">string</span><span class="sxs-lookup"><span data-stu-id="5d69c-138">string</span></span><br/> | <span data-ttu-id="5d69c-139">caratteri</span><span class="sxs-lookup"><span data-stu-id="5d69c-139">characters</span></span><br/> | <span data-ttu-id="5d69c-140">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5d69c-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5d69c-141">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5d69c-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5d69c-142">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5d69c-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5d69c-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5d69c-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5d69c-144">string</span><span class="sxs-lookup"><span data-stu-id="5d69c-144">string</span></span><br/> | <span data-ttu-id="5d69c-145">n/d</span><span class="sxs-lookup"><span data-stu-id="5d69c-145">n/a</span></span><br/>        | <span data-ttu-id="5d69c-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="5d69c-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5d69c-147">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5d69c-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5d69c-148">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5d69c-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5d69c-149">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="5d69c-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5d69c-150">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="5d69c-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5d69c-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d69c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d69c-152">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5d69c-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




