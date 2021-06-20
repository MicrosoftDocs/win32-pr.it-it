---
description: Informazioni sull'elemento DocumentCoverBack, che descrive il foglio di presentazione. Ogni documento avrà un foglio separato.
ms.assetid: 29d0bf2d-4897-43ed-ba3d-0b38b2f30375
title: DocumentCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5c75fd4bbce89bbc707c17a82202846cf2490a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409384"
---
# <a name="documentcoverback"></a><span data-ttu-id="23174-104">DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="23174-104">DocumentCoverBack</span></span>

<span data-ttu-id="23174-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="23174-105">This topic is not current.</span></span> <span data-ttu-id="23174-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="23174-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="23174-107">Descrive il foglio di presentazione posteriore (finale).</span><span class="sxs-lookup"><span data-stu-id="23174-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="23174-108">Ogni documento avrà un foglio separato.</span><span class="sxs-lookup"><span data-stu-id="23174-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="23174-109">Il foglio di presentazione deve essere stampato nelle proprietà PageMediaSize e PageMediaType usate per la pagina finale del documento.</span><span class="sxs-lookup"><span data-stu-id="23174-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the document.</span></span> <span data-ttu-id="23174-110">Il foglio di presentazione deve essere integrato nelle opzioni di elaborazione(ad esempio DocumentDuplex, DocumentNUp) come indicato dall'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="23174-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="23174-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="23174-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="23174-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="23174-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="23174-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="23174-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="23174-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="23174-114">Element Information</span></span>



| <span data-ttu-id="23174-115">Nome</span><span class="sxs-lookup"><span data-stu-id="23174-115">Name</span></span> | <span data-ttu-id="23174-116">Valore</span><span class="sxs-lookup"><span data-stu-id="23174-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23174-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="23174-117">Element Type</span></span> <br/>   | <span data-ttu-id="23174-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="23174-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="23174-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="23174-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="23174-120">Documento</span><span class="sxs-lookup"><span data-stu-id="23174-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="23174-121">Note</span><span class="sxs-lookup"><span data-stu-id="23174-121">Notes</span></span> <br/>          | <span data-ttu-id="23174-122">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il printTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="23174-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="23174-123">Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="23174-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="23174-124">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="23174-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="23174-125">Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="23174-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="23174-126">Ciò non è sicuro perché potrebbero non risolversi come previsto e potrebbero creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="23174-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="23174-127">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="23174-127">Structural Content</span></span>

<span data-ttu-id="23174-128">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="23174-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!--Specifies the XPS specific part name for the back cover sheet-->
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="23174-129">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="23174-129">Structure Variables</span></span>

<span data-ttu-id="23174-130">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="23174-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="23174-131">Nome</span><span class="sxs-lookup"><span data-stu-id="23174-131">Name</span></span>                               | <span data-ttu-id="23174-132">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="23174-132">Data type</span></span>         | <span data-ttu-id="23174-133">Unità</span><span class="sxs-lookup"><span data-stu-id="23174-133">Unit</span></span>                  | <span data-ttu-id="23174-134">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="23174-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="23174-135">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="23174-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="23174-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="23174-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="23174-137">string</span><span class="sxs-lookup"><span data-stu-id="23174-137">string</span></span><br/> | <span data-ttu-id="23174-138">caratteri</span><span class="sxs-lookup"><span data-stu-id="23174-138">characters</span></span><br/> | <span data-ttu-id="23174-139">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="23174-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="23174-140">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="23174-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="23174-141">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="23174-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="23174-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="23174-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="23174-143">string</span><span class="sxs-lookup"><span data-stu-id="23174-143">string</span></span><br/> | <span data-ttu-id="23174-144">n/d</span><span class="sxs-lookup"><span data-stu-id="23174-144">n/a</span></span><br/>        | <span data-ttu-id="23174-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="23174-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="23174-146">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="23174-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="23174-147">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="23174-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="23174-148">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="23174-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="23174-149">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="23174-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="23174-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23174-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23174-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="23174-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




