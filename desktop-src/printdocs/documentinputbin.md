---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321147"
---
# <a name="documentinputbin"></a><span data-ttu-id="cdf8a-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="cdf8a-104">DocumentInputBin</span></span>

<span data-ttu-id="cdf8a-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-105">This topic is not current.</span></span> <span data-ttu-id="cdf8a-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cdf8a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cdf8a-107">Descrive il contenitore di input installato in un dispositivo o l'elenco completo di contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="cdf8a-108">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="cdf8a-109">Non devono essere specificati contemporaneamente in un documento di funzionalità di stampa o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="cdf8a-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cdf8a-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="cdf8a-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="cdf8a-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="cdf8a-112">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="cdf8a-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cdf8a-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cdf8a-113">Element Information</span></span>



| <span data-ttu-id="cdf8a-114">Nome</span><span class="sxs-lookup"><span data-stu-id="cdf8a-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf8a-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="cdf8a-115">Element Type</span></span> <br/>   | <span data-ttu-id="cdf8a-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="cdf8a-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="cdf8a-117">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="cdf8a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cdf8a-118">Documento</span><span class="sxs-lookup"><span data-stu-id="cdf8a-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="cdf8a-119">Note</span><span class="sxs-lookup"><span data-stu-id="cdf8a-119">Notes</span></span> <br/>          | <span data-ttu-id="cdf8a-120">I contenitori supportati che non sono attualmente installati devono essere contrassegnati come limitati nel documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="cdf8a-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="cdf8a-121">Structural Content</span></span>

<span data-ttu-id="cdf8a-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="cdf8a-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="cdf8a-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="cdf8a-123">Structure Variables</span></span>

<span data-ttu-id="cdf8a-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cdf8a-125">Nome</span><span class="sxs-lookup"><span data-stu-id="cdf8a-125">Name</span></span>                                   | <span data-ttu-id="cdf8a-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cdf8a-126">Data type</span></span>          | <span data-ttu-id="cdf8a-127">Unità</span><span class="sxs-lookup"><span data-stu-id="cdf8a-127">Unit</span></span>                  | <span data-ttu-id="cdf8a-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="cdf8a-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cdf8a-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="cdf8a-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf8a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="cdf8a-131">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-131">string</span></span><br/>  | <span data-ttu-id="cdf8a-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="cdf8a-132">characters</span></span><br/> | <span data-ttu-id="cdf8a-133">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cdf8a-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cdf8a-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cdf8a-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="cdf8a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="cdf8a-137">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-137">string</span></span><br/>  | <span data-ttu-id="cdf8a-138">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-138">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cdf8a-140">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="cdf8a-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="cdf8a-142">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-142">string</span></span><br/>  | <span data-ttu-id="cdf8a-143">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-143">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cdf8a-145">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="cdf8a-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="cdf8a-147">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-147">string</span></span><br/>  | <span data-ttu-id="cdf8a-148">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-148">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="cdf8a-150">Specifica il tipo del cestino.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="cdf8a-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="cdf8a-152">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-152">string</span></span><br/>  | <span data-ttu-id="cdf8a-153">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-153">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-154">Automatico, manuale.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="cdf8a-155">Specifica il meccanismo di feed del cestino.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="cdf8a-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="cdf8a-157">numero intero</span><span class="sxs-lookup"><span data-stu-id="cdf8a-157">integer</span></span><br/> | <span data-ttu-id="cdf8a-158">fogli</span><span class="sxs-lookup"><span data-stu-id="cdf8a-158">sheets</span></span><br/>     | <span data-ttu-id="cdf8a-159">Limite massimo di Integer consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="cdf8a-160">Specifica se il cestino è un contenitore a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="cdf8a-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="cdf8a-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="cdf8a-162">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-162">string</span></span><br/>  | <span data-ttu-id="cdf8a-163">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-163">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-164">Supportato, nessuno.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="cdf8a-165">Specifica la capacità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="cdf8a-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="cdf8a-167">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-167">string</span></span><br/>  | <span data-ttu-id="cdf8a-168">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-168">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-169">Supportato, nessuno.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="cdf8a-170">Specifica la capacità del supporto in numero di pagine (livello completo) del cestino.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="cdf8a-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="cdf8a-172">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-172">string</span></span><br/>  | <span data-ttu-id="cdf8a-173">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-173">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-174">Dritto, serpentine.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="cdf8a-175">Specifica le caratteristiche del percorso del supporto.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="cdf8a-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="cdf8a-177">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-177">string</span></span><br/>  | <span data-ttu-id="cdf8a-178">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-178">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-179">FaceUp, faccia a faccia</span><span class="sxs-lookup"><span data-stu-id="cdf8a-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="cdf8a-180">Specifica se i supporti devono essere stampati o in basso.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="cdf8a-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="cdf8a-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="cdf8a-182">string</span><span class="sxs-lookup"><span data-stu-id="cdf8a-182">string</span></span><br/>  | <span data-ttu-id="cdf8a-183">n/d</span><span class="sxs-lookup"><span data-stu-id="cdf8a-183">n/a</span></span><br/>        | <span data-ttu-id="cdf8a-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="cdf8a-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="cdf8a-185">Specifica se il supporto viene alimentato prima o dopo un bordo breve.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cdf8a-186">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cdf8a-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cdf8a-187">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cdf8a-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cdf8a-188">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="cdf8a-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="cdf8a-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdf8a-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf8a-190">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="cdf8a-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




