---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f87782d6cf9aae5c34d36603f025e803f47db3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998098"
---
# <a name="jobinputbin"></a><span data-ttu-id="1df18-104">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="1df18-104">JobInputBin</span></span>

<span data-ttu-id="1df18-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1df18-105">This topic is not current.</span></span> <span data-ttu-id="1df18-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1df18-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1df18-107">Descrive il contenitore di input installato in un dispositivo o l'elenco completo dei bin supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1df18-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="1df18-108">Consente di specificare il contenitore di input in base al processo.</span><span class="sxs-lookup"><span data-stu-id="1df18-108">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="1df18-109">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="1df18-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="1df18-110">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="1df18-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1df18-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1df18-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1df18-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1df18-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1df18-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1df18-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1df18-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1df18-114">Element Information</span></span>



| <span data-ttu-id="1df18-115">Nome</span><span class="sxs-lookup"><span data-stu-id="1df18-115">Name</span></span> | <span data-ttu-id="1df18-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1df18-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1df18-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1df18-117">Element Type</span></span> <br/>   | <span data-ttu-id="1df18-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="1df18-118">Feature</span></span><br/> |
| <span data-ttu-id="1df18-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1df18-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1df18-120">Processo</span><span class="sxs-lookup"><span data-stu-id="1df18-120">Job</span></span><br/>     |
| <span data-ttu-id="1df18-121">Note</span><span class="sxs-lookup"><span data-stu-id="1df18-121">Notes</span></span> <br/>          | <span data-ttu-id="1df18-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="1df18-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1df18-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1df18-123">Structural Content</span></span>

<span data-ttu-id="1df18-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="1df18-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1df18-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="1df18-125">Structure Variables</span></span>

<span data-ttu-id="1df18-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1df18-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1df18-127">Nome</span><span class="sxs-lookup"><span data-stu-id="1df18-127">Name</span></span>                                   | <span data-ttu-id="1df18-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1df18-128">Data type</span></span>          | <span data-ttu-id="1df18-129">Unità</span><span class="sxs-lookup"><span data-stu-id="1df18-129">Unit</span></span>                  | <span data-ttu-id="1df18-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="1df18-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1df18-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="1df18-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1df18-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1df18-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="1df18-133">string</span><span class="sxs-lookup"><span data-stu-id="1df18-133">string</span></span><br/>  | <span data-ttu-id="1df18-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="1df18-134">characters</span></span><br/> | <span data-ttu-id="1df18-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="1df18-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1df18-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="1df18-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1df18-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="1df18-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="1df18-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="1df18-139">string</span><span class="sxs-lookup"><span data-stu-id="1df18-139">string</span></span><br/>  | <span data-ttu-id="1df18-140">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-140">n/a</span></span><br/>        | <span data-ttu-id="1df18-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="1df18-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1df18-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1df18-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1df18-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="1df18-144">string</span><span class="sxs-lookup"><span data-stu-id="1df18-144">string</span></span><br/>  | <span data-ttu-id="1df18-145">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-145">n/a</span></span><br/>        | <span data-ttu-id="1df18-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="1df18-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1df18-147">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1df18-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1df18-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="1df18-149">string</span><span class="sxs-lookup"><span data-stu-id="1df18-149">string</span></span><br/>  | <span data-ttu-id="1df18-150">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-150">n/a</span></span><br/>        | <span data-ttu-id="1df18-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="1df18-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="1df18-152">Specifica il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="1df18-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="1df18-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="1df18-154">string</span><span class="sxs-lookup"><span data-stu-id="1df18-154">string</span></span><br/>  | <span data-ttu-id="1df18-155">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-155">n/a</span></span><br/>        | <span data-ttu-id="1df18-156">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="1df18-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="1df18-157">Specifica il meccanismo di avanzamento del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1df18-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="1df18-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="1df18-159">string</span><span class="sxs-lookup"><span data-stu-id="1df18-159">string</span></span><br/>  | <span data-ttu-id="1df18-160">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-160">n/a</span></span><br/>        | <span data-ttu-id="1df18-161">Alto, Standard.</span><span class="sxs-lookup"><span data-stu-id="1df18-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1df18-162">Specifica se il bin è un bin a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="1df18-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="1df18-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1df18-164">string</span><span class="sxs-lookup"><span data-stu-id="1df18-164">string</span></span><br/>  | <span data-ttu-id="1df18-165">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-165">n/a</span></span><br/>        | <span data-ttu-id="1df18-166">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="1df18-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1df18-167">Specifica la capacità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1df18-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1df18-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1df18-169">string</span><span class="sxs-lookup"><span data-stu-id="1df18-169">string</span></span><br/>  | <span data-ttu-id="1df18-170">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-170">n/a</span></span><br/>        | <span data-ttu-id="1df18-171">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="1df18-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1df18-172">Specifica la funzionalità di rilevamento automatico del tipo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1df18-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1df18-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="1df18-174">numero intero</span><span class="sxs-lookup"><span data-stu-id="1df18-174">integer</span></span><br/> | <span data-ttu-id="1df18-175">Fogli</span><span class="sxs-lookup"><span data-stu-id="1df18-175">sheets</span></span><br/>     | <span data-ttu-id="1df18-176">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1df18-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="1df18-177">Specifica la capacità multimediale in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1df18-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="1df18-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="1df18-179">string</span><span class="sxs-lookup"><span data-stu-id="1df18-179">string</span></span><br/>  | <span data-ttu-id="1df18-180">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-180">n/a</span></span><br/>        | <span data-ttu-id="1df18-181">Straight, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="1df18-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="1df18-182">Specifica le caratteristiche del percorso del supporto.</span><span class="sxs-lookup"><span data-stu-id="1df18-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="1df18-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="1df18-184">string</span><span class="sxs-lookup"><span data-stu-id="1df18-184">string</span></span><br/>  | <span data-ttu-id="1df18-185">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-185">n/a</span></span><br/>        | <span data-ttu-id="1df18-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="1df18-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1df18-187">Specifica se i supporti devono essere stampati a faccia in su o in giù.</span><span class="sxs-lookup"><span data-stu-id="1df18-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="1df18-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="1df18-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="1df18-189">string</span><span class="sxs-lookup"><span data-stu-id="1df18-189">string</span></span><br/>  | <span data-ttu-id="1df18-190">n/d</span><span class="sxs-lookup"><span data-stu-id="1df18-190">n/a</span></span><br/>        | <span data-ttu-id="1df18-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="1df18-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="1df18-192">Specifica se i supporti vengono prima alimentato dal bordo lungo o dal bordo breve.</span><span class="sxs-lookup"><span data-stu-id="1df18-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1df18-193">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1df18-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1df18-194">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="1df18-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1df18-195">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="1df18-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1df18-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1df18-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df18-197">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1df18-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




