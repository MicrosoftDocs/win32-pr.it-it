---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973433ac7f6e051d4656777696cc3a37cedd953b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999218"
---
# <a name="joboutputbin"></a><span data-ttu-id="46ea8-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="46ea8-104">JobOutputBin</span></span>

<span data-ttu-id="46ea8-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="46ea8-105">This topic is not current.</span></span> <span data-ttu-id="46ea8-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="46ea8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46ea8-107">Descrive il bin di output installato in un dispositivo o l'elenco completo dei bin supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46ea8-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="46ea8-108">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda solo in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="46ea8-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="46ea8-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="46ea8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="46ea8-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="46ea8-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="46ea8-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="46ea8-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="46ea8-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="46ea8-112">Element Information</span></span>



| <span data-ttu-id="46ea8-113">Nome</span><span class="sxs-lookup"><span data-stu-id="46ea8-113">Name</span></span> | <span data-ttu-id="46ea8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="46ea8-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="46ea8-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="46ea8-115">Element Type</span></span> <br/>   | <span data-ttu-id="46ea8-116">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="46ea8-116">Feature</span></span><br/> |
| <span data-ttu-id="46ea8-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="46ea8-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="46ea8-118">Processo</span><span class="sxs-lookup"><span data-stu-id="46ea8-118">Job</span></span><br/>     |
| <span data-ttu-id="46ea8-119">Note</span><span class="sxs-lookup"><span data-stu-id="46ea8-119">Notes</span></span> <br/>          | <span data-ttu-id="46ea8-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="46ea8-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="46ea8-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="46ea8-121">Structural Content</span></span>

<span data-ttu-id="46ea8-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="46ea8-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="46ea8-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="46ea8-123">Structure Variables</span></span>

<span data-ttu-id="46ea8-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="46ea8-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="46ea8-125">Nome</span><span class="sxs-lookup"><span data-stu-id="46ea8-125">Name</span></span>                                   | <span data-ttu-id="46ea8-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="46ea8-126">Data type</span></span>          | <span data-ttu-id="46ea8-127">Unità</span><span class="sxs-lookup"><span data-stu-id="46ea8-127">Unit</span></span>                  | <span data-ttu-id="46ea8-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="46ea8-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="46ea8-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="46ea8-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46ea8-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="46ea8-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="46ea8-131">string</span><span class="sxs-lookup"><span data-stu-id="46ea8-131">string</span></span><br/>  | <span data-ttu-id="46ea8-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="46ea8-132">characters</span></span><br/> | <span data-ttu-id="46ea8-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="46ea8-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="46ea8-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="46ea8-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="46ea8-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="46ea8-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="46ea8-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="46ea8-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="46ea8-137">string</span><span class="sxs-lookup"><span data-stu-id="46ea8-137">string</span></span><br/>  | <span data-ttu-id="46ea8-138">n/d</span><span class="sxs-lookup"><span data-stu-id="46ea8-138">n/a</span></span><br/>        | <span data-ttu-id="46ea8-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="46ea8-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="46ea8-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="46ea8-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="46ea8-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="46ea8-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="46ea8-142">string</span><span class="sxs-lookup"><span data-stu-id="46ea8-142">string</span></span><br/>  | <span data-ttu-id="46ea8-143">n/d</span><span class="sxs-lookup"><span data-stu-id="46ea8-143">n/a</span></span><br/>        | <span data-ttu-id="46ea8-144">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="46ea8-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="46ea8-145">Specifica il tipo generale del contenitore.</span><span class="sxs-lookup"><span data-stu-id="46ea8-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="46ea8-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="46ea8-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="46ea8-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="46ea8-147">integer</span></span><br/> | <span data-ttu-id="46ea8-148">Fogli</span><span class="sxs-lookup"><span data-stu-id="46ea8-148">sheets</span></span><br/>     | <span data-ttu-id="46ea8-149">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46ea8-149">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="46ea8-150">Specifica la capacità multimediale in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="46ea8-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="46ea8-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="46ea8-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="46ea8-152">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="46ea8-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="46ea8-153">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="46ea8-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="46ea8-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46ea8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46ea8-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="46ea8-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




