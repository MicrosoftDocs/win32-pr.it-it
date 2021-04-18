---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43fcf4aaf389769625e2289a438d7d5c2be0b83
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321103"
---
# <a name="joboutputbin"></a><span data-ttu-id="5abb5-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="5abb5-104">JobOutputBin</span></span>

<span data-ttu-id="5abb5-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5abb5-105">This topic is not current.</span></span> <span data-ttu-id="5abb5-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5abb5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5abb5-107">Descrive il contenitore di output installato in un dispositivo o l'elenco completo di contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5abb5-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="5abb5-108">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda. è necessario specificare solo un oggetto PrintTicket o un documento sulle funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="5abb5-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="5abb5-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5abb5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5abb5-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5abb5-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5abb5-111">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5abb5-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5abb5-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5abb5-112">Element Information</span></span>



| <span data-ttu-id="5abb5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="5abb5-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="5abb5-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5abb5-114">Element Type</span></span> <br/>   | <span data-ttu-id="5abb5-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5abb5-115">Feature</span></span><br/> |
| <span data-ttu-id="5abb5-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="5abb5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5abb5-117">Processo</span><span class="sxs-lookup"><span data-stu-id="5abb5-117">Job</span></span><br/>     |
| <span data-ttu-id="5abb5-118">Note</span><span class="sxs-lookup"><span data-stu-id="5abb5-118">Notes</span></span> <br/>          | <span data-ttu-id="5abb5-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="5abb5-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5abb5-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5abb5-120">Structural Content</span></span>

<span data-ttu-id="5abb5-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="5abb5-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5abb5-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="5abb5-122">Structure Variables</span></span>

<span data-ttu-id="5abb5-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5abb5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5abb5-124">Nome</span><span class="sxs-lookup"><span data-stu-id="5abb5-124">Name</span></span>                                   | <span data-ttu-id="5abb5-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5abb5-125">Data type</span></span>          | <span data-ttu-id="5abb5-126">Unità</span><span class="sxs-lookup"><span data-stu-id="5abb5-126">Unit</span></span>                  | <span data-ttu-id="5abb5-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="5abb5-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5abb5-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5abb5-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5abb5-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5abb5-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="5abb5-130">string</span><span class="sxs-lookup"><span data-stu-id="5abb5-130">string</span></span><br/>  | <span data-ttu-id="5abb5-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="5abb5-131">characters</span></span><br/> | <span data-ttu-id="5abb5-132">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5abb5-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5abb5-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5abb5-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5abb5-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5abb5-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="5abb5-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5abb5-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="5abb5-136">string</span><span class="sxs-lookup"><span data-stu-id="5abb5-136">string</span></span><br/>  | <span data-ttu-id="5abb5-137">n/d</span><span class="sxs-lookup"><span data-stu-id="5abb5-137">n/a</span></span><br/>        | <span data-ttu-id="5abb5-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="5abb5-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5abb5-139">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5abb5-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="5abb5-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="5abb5-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="5abb5-141">string</span><span class="sxs-lookup"><span data-stu-id="5abb5-141">string</span></span><br/>  | <span data-ttu-id="5abb5-142">n/d</span><span class="sxs-lookup"><span data-stu-id="5abb5-142">n/a</span></span><br/>        | <span data-ttu-id="5abb5-143">MailBox, sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="5abb5-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="5abb5-144">Specifica il tipo generale del cestino.</span><span class="sxs-lookup"><span data-stu-id="5abb5-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="5abb5-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="5abb5-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="5abb5-146">numero intero</span><span class="sxs-lookup"><span data-stu-id="5abb5-146">integer</span></span><br/> | <span data-ttu-id="5abb5-147">fogli</span><span class="sxs-lookup"><span data-stu-id="5abb5-147">sheets</span></span><br/>     | <span data-ttu-id="5abb5-148">Limite massimo di Integer consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5abb5-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="5abb5-149">Specifica la capacità del supporto in numero di pagine (livello completo) del cestino.</span><span class="sxs-lookup"><span data-stu-id="5abb5-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5abb5-150">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5abb5-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5abb5-151">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5abb5-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5abb5-152">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="5abb5-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5abb5-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5abb5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abb5-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5abb5-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




