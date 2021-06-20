---
description: Informazioni sull'elemento DocumentInputBin, che descrive il bin di input installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452e2f94b3e75a2b0555610db26d69e2a2f7548b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409304"
---
# <a name="documentinputbin"></a><span data-ttu-id="f5707-103">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="f5707-103">DocumentInputBin</span></span>

<span data-ttu-id="f5707-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f5707-104">This topic is not current.</span></span> <span data-ttu-id="f5707-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f5707-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f5707-106">Descrive il bin di input installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5707-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="f5707-107">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f5707-107">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="f5707-108">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="f5707-108">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="f5707-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5707-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="f5707-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f5707-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="f5707-111">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="f5707-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f5707-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5707-112">Element Information</span></span>



| <span data-ttu-id="f5707-113">Nome</span><span class="sxs-lookup"><span data-stu-id="f5707-113">Name</span></span> | <span data-ttu-id="f5707-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f5707-114">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5707-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f5707-115">Element Type</span></span> <br/>   | <span data-ttu-id="f5707-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="f5707-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="f5707-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f5707-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f5707-118">Documento</span><span class="sxs-lookup"><span data-stu-id="f5707-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="f5707-119">Note</span><span class="sxs-lookup"><span data-stu-id="f5707-119">Notes</span></span> <br/>          | <span data-ttu-id="f5707-120">I bin supportati che non sono attualmente installati devono essere contrassegnati come vincolati nel documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f5707-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f5707-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f5707-121">Structural Content</span></span>

<span data-ttu-id="f5707-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f5707-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f5707-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="f5707-123">Structure Variables</span></span>

<span data-ttu-id="f5707-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f5707-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f5707-125">Nome</span><span class="sxs-lookup"><span data-stu-id="f5707-125">Name</span></span>                                   | <span data-ttu-id="f5707-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5707-126">Data type</span></span>          | <span data-ttu-id="f5707-127">Unità</span><span class="sxs-lookup"><span data-stu-id="f5707-127">Unit</span></span>                  | <span data-ttu-id="f5707-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="f5707-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f5707-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f5707-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5707-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f5707-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="f5707-131">string</span><span class="sxs-lookup"><span data-stu-id="f5707-131">string</span></span><br/>  | <span data-ttu-id="f5707-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="f5707-132">characters</span></span><br/> | <span data-ttu-id="f5707-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f5707-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f5707-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="f5707-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f5707-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="f5707-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="f5707-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="f5707-137">string</span><span class="sxs-lookup"><span data-stu-id="f5707-137">string</span></span><br/>  | <span data-ttu-id="f5707-138">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-138">n/a</span></span><br/>        | <span data-ttu-id="f5707-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="f5707-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f5707-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f5707-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="f5707-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="f5707-142">string</span><span class="sxs-lookup"><span data-stu-id="f5707-142">string</span></span><br/>  | <span data-ttu-id="f5707-143">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-143">n/a</span></span><br/>        | <span data-ttu-id="f5707-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="f5707-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f5707-145">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f5707-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="f5707-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="f5707-147">string</span><span class="sxs-lookup"><span data-stu-id="f5707-147">string</span></span><br/>  | <span data-ttu-id="f5707-148">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-148">n/a</span></span><br/>        | <span data-ttu-id="f5707-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="f5707-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="f5707-150">Specifica il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="f5707-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="f5707-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="f5707-152">string</span><span class="sxs-lookup"><span data-stu-id="f5707-152">string</span></span><br/>  | <span data-ttu-id="f5707-153">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-153">n/a</span></span><br/>        | <span data-ttu-id="f5707-154">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="f5707-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="f5707-155">Specifica il meccanismo di avanzamento del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f5707-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="f5707-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="f5707-157">numero intero</span><span class="sxs-lookup"><span data-stu-id="f5707-157">integer</span></span><br/> | <span data-ttu-id="f5707-158">Fogli</span><span class="sxs-lookup"><span data-stu-id="f5707-158">sheets</span></span><br/>     | <span data-ttu-id="f5707-159">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5707-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="f5707-160">Specifica se il bin è un bin a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="f5707-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="f5707-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="f5707-162">string</span><span class="sxs-lookup"><span data-stu-id="f5707-162">string</span></span><br/>  | <span data-ttu-id="f5707-163">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-163">n/a</span></span><br/>        | <span data-ttu-id="f5707-164">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f5707-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="f5707-165">Specifica la funzionalità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5707-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="f5707-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="f5707-167">string</span><span class="sxs-lookup"><span data-stu-id="f5707-167">string</span></span><br/>  | <span data-ttu-id="f5707-168">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-168">n/a</span></span><br/>        | <span data-ttu-id="f5707-169">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f5707-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="f5707-170">Specifica la capacità dei supporti in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f5707-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="f5707-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="f5707-172">string</span><span class="sxs-lookup"><span data-stu-id="f5707-172">string</span></span><br/>  | <span data-ttu-id="f5707-173">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-173">n/a</span></span><br/>        | <span data-ttu-id="f5707-174">Diritto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="f5707-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="f5707-175">Specifica le caratteristiche del percorso multimediale.</span><span class="sxs-lookup"><span data-stu-id="f5707-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="f5707-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="f5707-177">string</span><span class="sxs-lookup"><span data-stu-id="f5707-177">string</span></span><br/>  | <span data-ttu-id="f5707-178">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-178">n/a</span></span><br/>        | <span data-ttu-id="f5707-179">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="f5707-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="f5707-180">Specifica se i supporti devono essere stampati a faccia in su o a faccia in giù.</span><span class="sxs-lookup"><span data-stu-id="f5707-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="f5707-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5707-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="f5707-182">string</span><span class="sxs-lookup"><span data-stu-id="f5707-182">string</span></span><br/>  | <span data-ttu-id="f5707-183">n/d</span><span class="sxs-lookup"><span data-stu-id="f5707-183">n/a</span></span><br/>        | <span data-ttu-id="f5707-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="f5707-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="f5707-185">Specifica se il supporto viene alimentato per primo dal bordo lungo o dal bordo corto.</span><span class="sxs-lookup"><span data-stu-id="f5707-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f5707-186">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f5707-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f5707-187">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="f5707-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f5707-188">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="f5707-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f5707-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5707-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5707-190">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f5707-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




