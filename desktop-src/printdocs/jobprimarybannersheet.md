---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc44973b06dc99c86ca9d50717ca9bf2b6335fa
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321126"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="483d8-104">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="483d8-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="483d8-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="483d8-105">This topic is not current.</span></span> <span data-ttu-id="483d8-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="483d8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="483d8-107">Descrive il foglio banner da visualizzare come output per il processo.</span><span class="sxs-lookup"><span data-stu-id="483d8-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="483d8-108">Il foglio banner deve essere output sul PageMediaSize predefinito e usando il PageMediaType predefinito.</span><span class="sxs-lookup"><span data-stu-id="483d8-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="483d8-109">Il foglio banner deve essere isolato dalla parte rimanente del processo.</span><span class="sxs-lookup"><span data-stu-id="483d8-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="483d8-110">Ciò significa che qualsiasi opzione di completamento o elaborazione, ad esempio JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments, non deve includere il foglio banner.</span><span class="sxs-lookup"><span data-stu-id="483d8-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="483d8-111">Il foglio banner dovrebbe essere visualizzato come primo foglio del processo.</span><span class="sxs-lookup"><span data-stu-id="483d8-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="483d8-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="483d8-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="483d8-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="483d8-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="483d8-114">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="483d8-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="483d8-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="483d8-115">Element Information</span></span>



| <span data-ttu-id="483d8-116">Nome</span><span class="sxs-lookup"><span data-stu-id="483d8-116">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="483d8-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="483d8-117">Element Type</span></span> <br/>   | <span data-ttu-id="483d8-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="483d8-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="483d8-119">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="483d8-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="483d8-120">Processo</span><span class="sxs-lookup"><span data-stu-id="483d8-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="483d8-121">Note</span><span class="sxs-lookup"><span data-stu-id="483d8-121">Notes</span></span> <br/>          | <span data-ttu-id="483d8-122">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="483d8-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="483d8-123">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="483d8-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="483d8-124">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="483d8-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="483d8-125">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="483d8-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="483d8-126">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="483d8-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="483d8-127">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="483d8-127">Structural Content</span></span>

<span data-ttu-id="483d8-128">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="483d8-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="483d8-129">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="483d8-129">Structure Variables</span></span>

<span data-ttu-id="483d8-130">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="483d8-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="483d8-131">Nome</span><span class="sxs-lookup"><span data-stu-id="483d8-131">Name</span></span>                               | <span data-ttu-id="483d8-132">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="483d8-132">Data type</span></span>         | <span data-ttu-id="483d8-133">Unità</span><span class="sxs-lookup"><span data-stu-id="483d8-133">Unit</span></span>                  | <span data-ttu-id="483d8-134">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="483d8-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="483d8-135">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="483d8-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="483d8-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="483d8-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="483d8-137">string</span><span class="sxs-lookup"><span data-stu-id="483d8-137">string</span></span><br/> | <span data-ttu-id="483d8-138">caratteri</span><span class="sxs-lookup"><span data-stu-id="483d8-138">characters</span></span><br/> | <span data-ttu-id="483d8-139">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="483d8-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="483d8-140">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="483d8-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="483d8-141">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="483d8-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="483d8-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="483d8-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="483d8-143">string</span><span class="sxs-lookup"><span data-stu-id="483d8-143">string</span></span><br/> | <span data-ttu-id="483d8-144">n/d</span><span class="sxs-lookup"><span data-stu-id="483d8-144">n/a</span></span><br/>        | <span data-ttu-id="483d8-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="483d8-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="483d8-146">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="483d8-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="483d8-147">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="483d8-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="483d8-148">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="483d8-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="483d8-149">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="483d8-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="483d8-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="483d8-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="483d8-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="483d8-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




