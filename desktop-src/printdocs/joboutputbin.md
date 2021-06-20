---
description: Informazioni sull'elemento JobOutputBin, che descrive il bin di output installato in un dispositivo o l'elenco completo dei bin supportati per un dispositivo.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408854"
---
# <a name="joboutputbin"></a><span data-ttu-id="72e37-103">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="72e37-103">JobOutputBin</span></span>

<span data-ttu-id="72e37-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="72e37-104">This topic is not current.</span></span> <span data-ttu-id="72e37-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="72e37-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72e37-106">Descrive il bin di output installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72e37-106">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="72e37-107">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda solo in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="72e37-107">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="72e37-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="72e37-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72e37-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="72e37-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="72e37-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="72e37-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="72e37-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="72e37-111">Element Information</span></span>



| <span data-ttu-id="72e37-112">Nome</span><span class="sxs-lookup"><span data-stu-id="72e37-112">Name</span></span> | <span data-ttu-id="72e37-113">Valore</span><span class="sxs-lookup"><span data-stu-id="72e37-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="72e37-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="72e37-114">Element Type</span></span> <br/>   | <span data-ttu-id="72e37-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="72e37-115">Feature</span></span><br/> |
| <span data-ttu-id="72e37-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="72e37-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72e37-117">Processo</span><span class="sxs-lookup"><span data-stu-id="72e37-117">Job</span></span><br/>     |
| <span data-ttu-id="72e37-118">Note</span><span class="sxs-lookup"><span data-stu-id="72e37-118">Notes</span></span> <br/>          | <span data-ttu-id="72e37-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="72e37-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="72e37-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="72e37-120">Structural Content</span></span>

<span data-ttu-id="72e37-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="72e37-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="72e37-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="72e37-122">Structure Variables</span></span>

<span data-ttu-id="72e37-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="72e37-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72e37-124">Nome</span><span class="sxs-lookup"><span data-stu-id="72e37-124">Name</span></span>                                   | <span data-ttu-id="72e37-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="72e37-125">Data type</span></span>          | <span data-ttu-id="72e37-126">Unità</span><span class="sxs-lookup"><span data-stu-id="72e37-126">Unit</span></span>                  | <span data-ttu-id="72e37-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="72e37-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="72e37-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="72e37-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72e37-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="72e37-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="72e37-130">string</span><span class="sxs-lookup"><span data-stu-id="72e37-130">string</span></span><br/>  | <span data-ttu-id="72e37-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="72e37-131">characters</span></span><br/> | <span data-ttu-id="72e37-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="72e37-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="72e37-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="72e37-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="72e37-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="72e37-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="72e37-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="72e37-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="72e37-136">string</span><span class="sxs-lookup"><span data-stu-id="72e37-136">string</span></span><br/>  | <span data-ttu-id="72e37-137">n/d</span><span class="sxs-lookup"><span data-stu-id="72e37-137">n/a</span></span><br/>        | <span data-ttu-id="72e37-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="72e37-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="72e37-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="72e37-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="72e37-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="72e37-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="72e37-141">string</span><span class="sxs-lookup"><span data-stu-id="72e37-141">string</span></span><br/>  | <span data-ttu-id="72e37-142">n/d</span><span class="sxs-lookup"><span data-stu-id="72e37-142">n/a</span></span><br/>        | <span data-ttu-id="72e37-143">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="72e37-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="72e37-144">Specifica il tipo generale del contenitore.</span><span class="sxs-lookup"><span data-stu-id="72e37-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="72e37-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="72e37-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="72e37-146">numero intero</span><span class="sxs-lookup"><span data-stu-id="72e37-146">integer</span></span><br/> | <span data-ttu-id="72e37-147">Fogli</span><span class="sxs-lookup"><span data-stu-id="72e37-147">sheets</span></span><br/>     | <span data-ttu-id="72e37-148">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72e37-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="72e37-149">Specifica la capacità media in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="72e37-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="72e37-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="72e37-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="72e37-151">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="72e37-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="72e37-152">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="72e37-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="72e37-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72e37-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72e37-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="72e37-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




