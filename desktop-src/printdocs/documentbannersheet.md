---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac772fdbd9bf378716c42362dc1657a100f1231
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321095"
---
# <a name="documentbannersheet"></a><span data-ttu-id="04d2a-104">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="04d2a-104">DocumentBannerSheet</span></span>

<span data-ttu-id="04d2a-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="04d2a-105">This topic is not current.</span></span> <span data-ttu-id="04d2a-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="04d2a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="04d2a-107">Descrive il foglio banner da restituire per un documento specifico.</span><span class="sxs-lookup"><span data-stu-id="04d2a-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="04d2a-108">Il foglio banner deve essere output sul valore predefinito PageMediaSize, usando il valore predefinito di PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="04d2a-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="04d2a-109">Il foglio banner deve anche essere isolato dal resto del documento.</span><span class="sxs-lookup"><span data-stu-id="04d2a-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="04d2a-110">Ciò significa che tutte le opzioni di completamento o elaborazione dei documenti, ad esempio DocumentDuplex, DocumentStaple o documento, non devono includere il foglio banner.</span><span class="sxs-lookup"><span data-stu-id="04d2a-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="04d2a-111">Il foglio banner potrebbe non essere isolato dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="04d2a-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="04d2a-112">Ciò significa che tutte le opzioni di completamento o elaborazione dei processi possono includere il foglio banner del documento.</span><span class="sxs-lookup"><span data-stu-id="04d2a-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="04d2a-113">Il foglio banner dovrebbe essere visualizzato come primo foglio del documento.</span><span class="sxs-lookup"><span data-stu-id="04d2a-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="04d2a-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="04d2a-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="04d2a-115">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="04d2a-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="04d2a-116">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="04d2a-116">Element Information</span></span>



| <span data-ttu-id="04d2a-117">Nome</span><span class="sxs-lookup"><span data-stu-id="04d2a-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d2a-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="04d2a-118">Element Type</span></span> <br/>   | <span data-ttu-id="04d2a-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="04d2a-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="04d2a-120">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="04d2a-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="04d2a-121">Documento</span><span class="sxs-lookup"><span data-stu-id="04d2a-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="04d2a-122">Note</span><span class="sxs-lookup"><span data-stu-id="04d2a-122">Notes</span></span> <br/>          | <span data-ttu-id="04d2a-123">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="04d2a-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="04d2a-124">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="04d2a-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="04d2a-125">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="04d2a-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="04d2a-126">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="04d2a-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="04d2a-127">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="04d2a-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="04d2a-128">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="04d2a-128">Structural Content</span></span>

<span data-ttu-id="04d2a-129">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="04d2a-129">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="04d2a-130">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="04d2a-130">Structure Variables</span></span>

<span data-ttu-id="04d2a-131">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="04d2a-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="04d2a-132">Nome</span><span class="sxs-lookup"><span data-stu-id="04d2a-132">Name</span></span>                               | <span data-ttu-id="04d2a-133">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="04d2a-133">Data type</span></span>         | <span data-ttu-id="04d2a-134">Unità</span><span class="sxs-lookup"><span data-stu-id="04d2a-134">Unit</span></span>                   | <span data-ttu-id="04d2a-135">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="04d2a-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="04d2a-136">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="04d2a-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="04d2a-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="04d2a-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="04d2a-138">string</span><span class="sxs-lookup"><span data-stu-id="04d2a-138">string</span></span><br/> | <span data-ttu-id="04d2a-139">caratteri</span><span class="sxs-lookup"><span data-stu-id="04d2a-139">characters</span></span> <br/> | <span data-ttu-id="04d2a-140">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="04d2a-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="04d2a-141">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="04d2a-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="04d2a-142">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="04d2a-142">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="04d2a-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="04d2a-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="04d2a-144">string</span><span class="sxs-lookup"><span data-stu-id="04d2a-144">string</span></span><br/> | <span data-ttu-id="04d2a-145">n/d</span><span class="sxs-lookup"><span data-stu-id="04d2a-145">n/a</span></span><br/>         | <span data-ttu-id="04d2a-146">True, False</span><span class="sxs-lookup"><span data-stu-id="04d2a-146">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="04d2a-147">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="04d2a-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="04d2a-148">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="04d2a-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="04d2a-149">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="04d2a-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="04d2a-150">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="04d2a-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="04d2a-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04d2a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04d2a-152">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="04d2a-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




