---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b143ea6a3e1edd667d56619c190d99d1de93496f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321137"
---
# <a name="documentcoverfront"></a><span data-ttu-id="eee5b-104">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="eee5b-104">DocumentCoverFront</span></span>

<span data-ttu-id="eee5b-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eee5b-105">This topic is not current.</span></span> <span data-ttu-id="eee5b-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eee5b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eee5b-107">Descrive il foglio di copertura anteriore (iniziale).</span><span class="sxs-lookup"><span data-stu-id="eee5b-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="eee5b-108">Ogni documento avrà un foglio separato.</span><span class="sxs-lookup"><span data-stu-id="eee5b-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="eee5b-109">Il foglio di copertura deve essere stampato in PageMediaSize e PageMediaType usato per la prima pagina del documento.</span><span class="sxs-lookup"><span data-stu-id="eee5b-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="eee5b-110">Il foglio di copertura deve essere integrato in opzioni di elaborazione, ad esempio DocumentDuplex, DocumentNUp, come indicato dall'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="eee5b-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="eee5b-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eee5b-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eee5b-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="eee5b-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eee5b-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eee5b-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eee5b-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eee5b-114">Element Information</span></span>



| <span data-ttu-id="eee5b-115">Nome</span><span class="sxs-lookup"><span data-stu-id="eee5b-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee5b-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="eee5b-116">Element Type</span></span> <br/>   | <span data-ttu-id="eee5b-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="eee5b-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="eee5b-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="eee5b-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eee5b-119">Documento</span><span class="sxs-lookup"><span data-stu-id="eee5b-119">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="eee5b-120">Note</span><span class="sxs-lookup"><span data-stu-id="eee5b-120">Notes</span></span> <br/>          | <span data-ttu-id="eee5b-121">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="eee5b-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="eee5b-122">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="eee5b-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="eee5b-123">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="eee5b-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="eee5b-124">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="eee5b-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="eee5b-125">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eee5b-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="eee5b-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="eee5b-126">Structural Content</span></span>

<span data-ttu-id="eee5b-127">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eee5b-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="eee5b-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="eee5b-128">Structure Variables</span></span>

<span data-ttu-id="eee5b-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="eee5b-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eee5b-130">Nome</span><span class="sxs-lookup"><span data-stu-id="eee5b-130">Name</span></span>                               | <span data-ttu-id="eee5b-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="eee5b-131">Data type</span></span>         | <span data-ttu-id="eee5b-132">Unità</span><span class="sxs-lookup"><span data-stu-id="eee5b-132">Unit</span></span>                  | <span data-ttu-id="eee5b-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="eee5b-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="eee5b-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="eee5b-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="eee5b-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="eee5b-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="eee5b-136">string</span><span class="sxs-lookup"><span data-stu-id="eee5b-136">string</span></span><br/> | <span data-ttu-id="eee5b-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="eee5b-137">characters</span></span><br/> | <span data-ttu-id="eee5b-138">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="eee5b-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="eee5b-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="eee5b-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="eee5b-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="eee5b-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="eee5b-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="eee5b-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="eee5b-142">string</span><span class="sxs-lookup"><span data-stu-id="eee5b-142">string</span></span><br/> | <span data-ttu-id="eee5b-143">n/d</span><span class="sxs-lookup"><span data-stu-id="eee5b-143">n/a</span></span><br/>        | <span data-ttu-id="eee5b-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="eee5b-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="eee5b-145">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="eee5b-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eee5b-146">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eee5b-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="eee5b-147">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="eee5b-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="eee5b-148">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="eee5b-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="eee5b-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eee5b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eee5b-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="eee5b-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




