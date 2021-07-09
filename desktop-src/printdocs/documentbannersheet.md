---
description: Informazioni sull'elemento configurabile dall'utente DocumentBannerSheet. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548769"
---
# <a name="documentbannersheet"></a><span data-ttu-id="51b4b-105">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="51b4b-105">DocumentBannerSheet</span></span>

<span data-ttu-id="51b4b-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="51b4b-106">This topic is not current.</span></span> <span data-ttu-id="51b4b-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="51b4b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="51b4b-108">Descrive il foglio banner da visualizzare come output per un documento specifico.</span><span class="sxs-lookup"><span data-stu-id="51b4b-108">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="51b4b-109">Il foglio banner deve essere restituito nel valore pageMediaSize predefinito, usando il valore predefinito PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="51b4b-109">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="51b4b-110">Anche il foglio banner deve essere isolato dal resto del documento.</span><span class="sxs-lookup"><span data-stu-id="51b4b-110">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="51b4b-111">Ciò significa che tutte le opzioni di completamento o elaborazione dei documenti (ad esempio DocumentDuplex, DocumentStaple o DocumentBinding) non devono includere il foglio banner.</span><span class="sxs-lookup"><span data-stu-id="51b4b-111">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="51b4b-112">Il foglio banner può essere isolato o meno dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="51b4b-112">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="51b4b-113">Ciò significa che qualsiasi opzione di completamento o elaborazione del processo può includere il foglio banner del documento.</span><span class="sxs-lookup"><span data-stu-id="51b4b-113">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="51b4b-114">Il foglio banner deve essere il primo foglio del documento.</span><span class="sxs-lookup"><span data-stu-id="51b4b-114">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="51b4b-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="51b4b-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="51b4b-116">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="51b4b-116">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="51b4b-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="51b4b-117">Element Information</span></span>



| <span data-ttu-id="51b4b-118">Nome</span><span class="sxs-lookup"><span data-stu-id="51b4b-118">Name</span></span> | <span data-ttu-id="51b4b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="51b4b-119">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51b4b-120">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="51b4b-120">Element Type</span></span> <br/>   | <span data-ttu-id="51b4b-121">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="51b4b-121">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="51b4b-122">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="51b4b-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="51b4b-123">Documento</span><span class="sxs-lookup"><span data-stu-id="51b4b-123">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="51b4b-124">Note</span><span class="sxs-lookup"><span data-stu-id="51b4b-124">Notes</span></span> <br/>          | <span data-ttu-id="51b4b-125">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket DEVE fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="51b4b-125">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="51b4b-126">Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="51b4b-126">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="51b4b-127">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="51b4b-127">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="51b4b-128">Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="51b4b-128">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="51b4b-129">Ciò non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="51b4b-129">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="51b4b-130">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="51b4b-130">Structural Content</span></span>

<span data-ttu-id="51b4b-131">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="51b4b-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="51b4b-132">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="51b4b-132">Structure Variables</span></span>

<span data-ttu-id="51b4b-133">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="51b4b-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="51b4b-134">Nome</span><span class="sxs-lookup"><span data-stu-id="51b4b-134">Name</span></span>                               | <span data-ttu-id="51b4b-135">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="51b4b-135">Data type</span></span>         | <span data-ttu-id="51b4b-136">Unità</span><span class="sxs-lookup"><span data-stu-id="51b4b-136">Unit</span></span>                   | <span data-ttu-id="51b4b-137">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="51b4b-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="51b4b-138">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="51b4b-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="51b4b-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="51b4b-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="51b4b-140">string</span><span class="sxs-lookup"><span data-stu-id="51b4b-140">string</span></span><br/> | <span data-ttu-id="51b4b-141">caratteri</span><span class="sxs-lookup"><span data-stu-id="51b4b-141">characters</span></span> <br/> | <span data-ttu-id="51b4b-142">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="51b4b-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="51b4b-143">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="51b4b-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="51b4b-144">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="51b4b-144">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="51b4b-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="51b4b-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="51b4b-146">string</span><span class="sxs-lookup"><span data-stu-id="51b4b-146">string</span></span><br/> | <span data-ttu-id="51b4b-147">n/d</span><span class="sxs-lookup"><span data-stu-id="51b4b-147">n/a</span></span><br/>         | <span data-ttu-id="51b4b-148">True, False</span><span class="sxs-lookup"><span data-stu-id="51b4b-148">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="51b4b-149">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="51b4b-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="51b4b-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="51b4b-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="51b4b-151">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="51b4b-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="51b4b-152">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="51b4b-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="51b4b-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51b4b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51b4b-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="51b4b-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




