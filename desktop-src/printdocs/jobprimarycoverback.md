---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 83626e3c-1ce8-4c91-b656-9f0c06c5b1ec
title: JobPrimaryCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073e65f80c3bee31423d0cf813d454a32e6f559b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321150"
---
# <a name="jobprimarycoverback"></a><span data-ttu-id="48345-104">JobPrimaryCoverBack</span><span class="sxs-lookup"><span data-stu-id="48345-104">JobPrimaryCoverBack</span></span>

<span data-ttu-id="48345-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="48345-105">This topic is not current.</span></span> <span data-ttu-id="48345-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="48345-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="48345-107">Viene descritto il foglio di copertura back (Ending).</span><span class="sxs-lookup"><span data-stu-id="48345-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="48345-108">Ogni processo avrà un foglio primario separato.</span><span class="sxs-lookup"><span data-stu-id="48345-108">Each job will have a separate primary sheet.</span></span> <span data-ttu-id="48345-109">Il foglio di copertura deve essere stampato in PageMediaSize e PageMediaType usato per la pagina finale del processo.</span><span class="sxs-lookup"><span data-stu-id="48345-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the job.</span></span> <span data-ttu-id="48345-110">Il foglio di copertura deve essere integrato in opzioni di elaborazione, ad esempio JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously, come indicato dall'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="48345-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="48345-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="48345-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="48345-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="48345-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="48345-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="48345-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="48345-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="48345-114">Element Information</span></span>



| <span data-ttu-id="48345-115">Nome</span><span class="sxs-lookup"><span data-stu-id="48345-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48345-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="48345-116">Element Type</span></span> <br/>   | <span data-ttu-id="48345-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="48345-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="48345-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="48345-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="48345-119">Processo</span><span class="sxs-lookup"><span data-stu-id="48345-119">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48345-120">Note</span><span class="sxs-lookup"><span data-stu-id="48345-120">Notes</span></span> <br/>          | <span data-ttu-id="48345-121">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="48345-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="48345-122">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="48345-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="48345-123">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="48345-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="48345-124">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="48345-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="48345-125">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48345-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="48345-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="48345-126">Structural Content</span></span>

<span data-ttu-id="48345-127">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="48345-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
  <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  <!-- Specifies the XPS part name for the back cover sheet. -->
  <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="48345-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="48345-128">Structure Variables</span></span>

<span data-ttu-id="48345-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="48345-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="48345-130">Nome</span><span class="sxs-lookup"><span data-stu-id="48345-130">Name</span></span>                               | <span data-ttu-id="48345-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="48345-131">Data type</span></span>         | <span data-ttu-id="48345-132">Unità</span><span class="sxs-lookup"><span data-stu-id="48345-132">Unit</span></span>                  | <span data-ttu-id="48345-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="48345-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="48345-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="48345-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="48345-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="48345-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="48345-136">string</span><span class="sxs-lookup"><span data-stu-id="48345-136">string</span></span><br/> | <span data-ttu-id="48345-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="48345-137">characters</span></span><br/> | <span data-ttu-id="48345-138">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="48345-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="48345-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="48345-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="48345-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="48345-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="48345-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="48345-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="48345-142">string</span><span class="sxs-lookup"><span data-stu-id="48345-142">string</span></span><br/> | <span data-ttu-id="48345-143">n/d</span><span class="sxs-lookup"><span data-stu-id="48345-143">n/a</span></span><br/>        | <span data-ttu-id="48345-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="48345-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="48345-145">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="48345-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="48345-146">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="48345-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="48345-147">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="48345-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="48345-148">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="48345-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="48345-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48345-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48345-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="48345-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




