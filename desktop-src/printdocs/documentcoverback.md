---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 29d0bf2d-4897-43ed-ba3d-0b38b2f30375
title: DocumentCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5822921fe3dc1852100569b29a1ded8b37bc9aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994538"
---
# <a name="documentcoverback"></a><span data-ttu-id="edd9b-104">DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="edd9b-104">DocumentCoverBack</span></span>

<span data-ttu-id="edd9b-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="edd9b-105">This topic is not current.</span></span> <span data-ttu-id="edd9b-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="edd9b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="edd9b-107">Descrive il frontespizio posteriore (finale).</span><span class="sxs-lookup"><span data-stu-id="edd9b-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="edd9b-108">Ogni documento avrà un foglio separato.</span><span class="sxs-lookup"><span data-stu-id="edd9b-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="edd9b-109">Il foglio di presentazione deve essere stampato nelle proprietà PageMediaSize e PageMediaType usate per la pagina finale del documento.</span><span class="sxs-lookup"><span data-stu-id="edd9b-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the document.</span></span> <span data-ttu-id="edd9b-110">Il foglio di presentazione deve essere integrato nelle opzioni di elaborazione, ad esempio DocumentDuplex, DocumentNUp, come indicato dall'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="edd9b-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="edd9b-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="edd9b-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="edd9b-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="edd9b-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="edd9b-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="edd9b-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="edd9b-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="edd9b-114">Element Information</span></span>



| <span data-ttu-id="edd9b-115">Nome</span><span class="sxs-lookup"><span data-stu-id="edd9b-115">Name</span></span> | <span data-ttu-id="edd9b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="edd9b-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="edd9b-117">Element Type</span></span> <br/>   | <span data-ttu-id="edd9b-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="edd9b-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="edd9b-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="edd9b-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="edd9b-120">Documento</span><span class="sxs-lookup"><span data-stu-id="edd9b-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="edd9b-121">Note</span><span class="sxs-lookup"><span data-stu-id="edd9b-121">Notes</span></span> <br/>          | <span data-ttu-id="edd9b-122">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="edd9b-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="edd9b-123">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="edd9b-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="edd9b-124">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="edd9b-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="edd9b-125">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="edd9b-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="edd9b-126">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="edd9b-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="edd9b-127">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="edd9b-127">Structural Content</span></span>

<span data-ttu-id="edd9b-128">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="edd9b-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="edd9b-129">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="edd9b-129">Structure Variables</span></span>

<span data-ttu-id="edd9b-130">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="edd9b-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="edd9b-131">Nome</span><span class="sxs-lookup"><span data-stu-id="edd9b-131">Name</span></span>                               | <span data-ttu-id="edd9b-132">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="edd9b-132">Data type</span></span>         | <span data-ttu-id="edd9b-133">Unità</span><span class="sxs-lookup"><span data-stu-id="edd9b-133">Unit</span></span>                  | <span data-ttu-id="edd9b-134">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="edd9b-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="edd9b-135">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="edd9b-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="edd9b-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="edd9b-137">string</span><span class="sxs-lookup"><span data-stu-id="edd9b-137">string</span></span><br/> | <span data-ttu-id="edd9b-138">caratteri</span><span class="sxs-lookup"><span data-stu-id="edd9b-138">characters</span></span><br/> | <span data-ttu-id="edd9b-139">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="edd9b-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="edd9b-140">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="edd9b-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="edd9b-141">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="edd9b-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="edd9b-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="edd9b-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="edd9b-143">string</span><span class="sxs-lookup"><span data-stu-id="edd9b-143">string</span></span><br/> | <span data-ttu-id="edd9b-144">n/d</span><span class="sxs-lookup"><span data-stu-id="edd9b-144">n/a</span></span><br/>        | <span data-ttu-id="edd9b-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="edd9b-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="edd9b-146">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="edd9b-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="edd9b-147">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="edd9b-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="edd9b-148">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="edd9b-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="edd9b-149">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="edd9b-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="edd9b-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="edd9b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd9b-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="edd9b-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




