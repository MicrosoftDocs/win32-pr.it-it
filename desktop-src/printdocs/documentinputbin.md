---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997768"
---
# <a name="documentinputbin"></a><span data-ttu-id="e2dd1-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="e2dd1-104">DocumentInputBin</span></span>

<span data-ttu-id="e2dd1-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-105">This topic is not current.</span></span> <span data-ttu-id="e2dd1-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e2dd1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e2dd1-107">Descrive il bin di input installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="e2dd1-108">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="e2dd1-109">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="e2dd1-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e2dd1-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="e2dd1-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e2dd1-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="e2dd1-112">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="e2dd1-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e2dd1-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e2dd1-113">Element Information</span></span>



| <span data-ttu-id="e2dd1-114">Nome</span><span class="sxs-lookup"><span data-stu-id="e2dd1-114">Name</span></span> | <span data-ttu-id="e2dd1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e2dd1-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dd1-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e2dd1-116">Element Type</span></span> <br/>   | <span data-ttu-id="e2dd1-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="e2dd1-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="e2dd1-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e2dd1-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e2dd1-119">Documento</span><span class="sxs-lookup"><span data-stu-id="e2dd1-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="e2dd1-120">Note</span><span class="sxs-lookup"><span data-stu-id="e2dd1-120">Notes</span></span> <br/>          | <span data-ttu-id="e2dd1-121">I bin supportati che non sono attualmente installati devono essere contrassegnati come vincolati nel documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e2dd1-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e2dd1-122">Structural Content</span></span>

<span data-ttu-id="e2dd1-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e2dd1-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e2dd1-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e2dd1-124">Structure Variables</span></span>

<span data-ttu-id="e2dd1-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e2dd1-126">Nome</span><span class="sxs-lookup"><span data-stu-id="e2dd1-126">Name</span></span>                                   | <span data-ttu-id="e2dd1-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e2dd1-127">Data type</span></span>          | <span data-ttu-id="e2dd1-128">Unità</span><span class="sxs-lookup"><span data-stu-id="e2dd1-128">Unit</span></span>                  | <span data-ttu-id="e2dd1-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e2dd1-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e2dd1-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e2dd1-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dd1-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="e2dd1-132">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-132">string</span></span><br/>  | <span data-ttu-id="e2dd1-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="e2dd1-133">characters</span></span><br/> | <span data-ttu-id="e2dd1-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e2dd1-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e2dd1-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e2dd1-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="e2dd1-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="e2dd1-138">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-138">string</span></span><br/>  | <span data-ttu-id="e2dd1-139">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-139">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e2dd1-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="e2dd1-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="e2dd1-143">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-143">string</span></span><br/>  | <span data-ttu-id="e2dd1-144">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-144">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e2dd1-146">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="e2dd1-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="e2dd1-148">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-148">string</span></span><br/>  | <span data-ttu-id="e2dd1-149">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-149">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="e2dd1-151">Specifica il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="e2dd1-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="e2dd1-153">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-153">string</span></span><br/>  | <span data-ttu-id="e2dd1-154">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-154">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-155">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="e2dd1-156">Specifica il meccanismo di feed del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="e2dd1-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="e2dd1-158">numero intero</span><span class="sxs-lookup"><span data-stu-id="e2dd1-158">integer</span></span><br/> | <span data-ttu-id="e2dd1-159">Fogli</span><span class="sxs-lookup"><span data-stu-id="e2dd1-159">sheets</span></span><br/>     | <span data-ttu-id="e2dd1-160">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="e2dd1-161">Specifica se il bin è un bin a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="e2dd1-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="e2dd1-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="e2dd1-163">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-163">string</span></span><br/>  | <span data-ttu-id="e2dd1-164">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-164">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-165">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="e2dd1-166">Specifica la capacità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="e2dd1-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="e2dd1-168">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-168">string</span></span><br/>  | <span data-ttu-id="e2dd1-169">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-169">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-170">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="e2dd1-171">Specifica la capacità multimediale in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="e2dd1-172">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="e2dd1-173">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-173">string</span></span><br/>  | <span data-ttu-id="e2dd1-174">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-174">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-175">Linea retta, serpentina.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="e2dd1-176">Specifica le caratteristiche del percorso del supporto.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="e2dd1-177">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="e2dd1-178">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-178">string</span></span><br/>  | <span data-ttu-id="e2dd1-179">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-179">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-180">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="e2dd1-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="e2dd1-181">Specifica se i supporti devono essere stampati a faccia in su o in giù.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="e2dd1-182">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="e2dd1-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="e2dd1-183">string</span><span class="sxs-lookup"><span data-stu-id="e2dd1-183">string</span></span><br/>  | <span data-ttu-id="e2dd1-184">n/d</span><span class="sxs-lookup"><span data-stu-id="e2dd1-184">n/a</span></span><br/>        | <span data-ttu-id="e2dd1-185">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="e2dd1-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="e2dd1-186">Specifica se i supporti vengono prima alimentato dal bordo lungo o dal bordo breve.</span><span class="sxs-lookup"><span data-stu-id="e2dd1-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e2dd1-187">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e2dd1-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e2dd1-188">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="e2dd1-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e2dd1-189">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="e2dd1-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e2dd1-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2dd1-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2dd1-191">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e2dd1-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




