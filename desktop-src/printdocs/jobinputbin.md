---
description: Informazioni sull'elemento JobInputBin, che descrive il bin di input installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929df4cb4871e5a8d2ebacfe533b5da3ad9babf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408894"
---
# <a name="jobinputbin"></a><span data-ttu-id="1c1a6-103">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="1c1a6-103">JobInputBin</span></span>

<span data-ttu-id="1c1a6-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-104">This topic is not current.</span></span> <span data-ttu-id="1c1a6-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1c1a6-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1c1a6-106">Descrive il bin di input installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="1c1a6-107">Consente la specifica del contenitore di input in base al processo.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-107">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="1c1a6-108">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="1c1a6-109">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1c1a6-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1c1a6-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1c1a6-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1c1a6-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1c1a6-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1c1a6-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1c1a6-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1c1a6-113">Element Information</span></span>



| <span data-ttu-id="1c1a6-114">Nome</span><span class="sxs-lookup"><span data-stu-id="1c1a6-114">Name</span></span> | <span data-ttu-id="1c1a6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1c1a6-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1c1a6-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1c1a6-116">Element Type</span></span> <br/>   | <span data-ttu-id="1c1a6-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="1c1a6-117">Feature</span></span><br/> |
| <span data-ttu-id="1c1a6-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1c1a6-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1c1a6-119">Processo</span><span class="sxs-lookup"><span data-stu-id="1c1a6-119">Job</span></span><br/>     |
| <span data-ttu-id="1c1a6-120">Note</span><span class="sxs-lookup"><span data-stu-id="1c1a6-120">Notes</span></span> <br/>          | <span data-ttu-id="1c1a6-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="1c1a6-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1c1a6-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1c1a6-122">Structural Content</span></span>

<span data-ttu-id="1c1a6-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="1c1a6-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="1c1a6-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="1c1a6-124">Structure Variables</span></span>

<span data-ttu-id="1c1a6-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1c1a6-126">Nome</span><span class="sxs-lookup"><span data-stu-id="1c1a6-126">Name</span></span>                                   | <span data-ttu-id="1c1a6-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1c1a6-127">Data type</span></span>          | <span data-ttu-id="1c1a6-128">Unità</span><span class="sxs-lookup"><span data-stu-id="1c1a6-128">Unit</span></span>                  | <span data-ttu-id="1c1a6-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="1c1a6-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1c1a6-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="1c1a6-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1a6-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="1c1a6-132">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-132">string</span></span><br/>  | <span data-ttu-id="1c1a6-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="1c1a6-133">characters</span></span><br/> | <span data-ttu-id="1c1a6-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="1c1a6-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1c1a6-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1c1a6-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="1c1a6-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="1c1a6-138">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-138">string</span></span><br/>  | <span data-ttu-id="1c1a6-139">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-139">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1c1a6-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1c1a6-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="1c1a6-143">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-143">string</span></span><br/>  | <span data-ttu-id="1c1a6-144">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-144">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1c1a6-146">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1c1a6-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="1c1a6-148">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-148">string</span></span><br/>  | <span data-ttu-id="1c1a6-149">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-149">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="1c1a6-151">Specifica il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="1c1a6-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="1c1a6-153">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-153">string</span></span><br/>  | <span data-ttu-id="1c1a6-154">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-154">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-155">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="1c1a6-156">Specifica il meccanismo di avanzamento del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="1c1a6-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="1c1a6-158">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-158">string</span></span><br/>  | <span data-ttu-id="1c1a6-159">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-159">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-160">Alto, Standard.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1c1a6-161">Specifica se il bin è un bin a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="1c1a6-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="1c1a6-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1c1a6-163">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-163">string</span></span><br/>  | <span data-ttu-id="1c1a6-164">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-164">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-165">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1c1a6-166">Specifica la capacità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1c1a6-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1c1a6-168">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-168">string</span></span><br/>  | <span data-ttu-id="1c1a6-169">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-169">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-170">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1c1a6-171">Specifica la funzionalità di rilevamento automatico del tipo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1c1a6-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="1c1a6-173">numero intero</span><span class="sxs-lookup"><span data-stu-id="1c1a6-173">integer</span></span><br/> | <span data-ttu-id="1c1a6-174">Fogli</span><span class="sxs-lookup"><span data-stu-id="1c1a6-174">sheets</span></span><br/>     | <span data-ttu-id="1c1a6-175">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="1c1a6-176">Specifica la capacità media in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="1c1a6-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="1c1a6-178">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-178">string</span></span><br/>  | <span data-ttu-id="1c1a6-179">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-179">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-180">Diritto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="1c1a6-181">Specifica le caratteristiche del percorso multimediale.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="1c1a6-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="1c1a6-183">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-183">string</span></span><br/>  | <span data-ttu-id="1c1a6-184">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-184">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-185">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="1c1a6-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1c1a6-186">Specifica se i supporti devono essere stampati a faccia in su o a faccia in giù.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="1c1a6-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="1c1a6-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="1c1a6-188">string</span><span class="sxs-lookup"><span data-stu-id="1c1a6-188">string</span></span><br/>  | <span data-ttu-id="1c1a6-189">n/d</span><span class="sxs-lookup"><span data-stu-id="1c1a6-189">n/a</span></span><br/>        | <span data-ttu-id="1c1a6-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="1c1a6-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="1c1a6-191">Specifica se il supporto viene alimentato per primo dal bordo lungo o dal bordo corto.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1c1a6-192">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1c1a6-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1c1a6-193">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="1c1a6-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1c1a6-194">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="1c1a6-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="1c1a6-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c1a6-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c1a6-196">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1c1a6-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




