---
description: Ottenere informazioni sull'elemento PageInputBin configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549169"
---
# <a name="pageinputbin"></a><span data-ttu-id="bc954-105">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="bc954-105">PageInputBin</span></span>

<span data-ttu-id="bc954-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="bc954-106">This topic is not current.</span></span> <span data-ttu-id="bc954-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bc954-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc954-108">Descrive il bin di input installato in un dispositivo o l'elenco completo dei contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc954-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="bc954-109">Consente la specifica del contenitore di input per ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="bc954-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="bc954-110">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="bc954-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="bc954-111">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="bc954-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="bc954-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bc954-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bc954-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bc954-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bc954-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bc954-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bc954-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bc954-115">Element Information</span></span>



| <span data-ttu-id="bc954-116">Nome</span><span class="sxs-lookup"><span data-stu-id="bc954-116">Name</span></span> | <span data-ttu-id="bc954-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bc954-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="bc954-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="bc954-118">Element Type</span></span> <br/>   | <span data-ttu-id="bc954-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="bc954-119">Feature</span></span><br/> |
| <span data-ttu-id="bc954-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="bc954-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bc954-121">Pagina</span><span class="sxs-lookup"><span data-stu-id="bc954-121">Page</span></span><br/>    |
| <span data-ttu-id="bc954-122">Note</span><span class="sxs-lookup"><span data-stu-id="bc954-122">Notes</span></span> <br/>          | <span data-ttu-id="bc954-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="bc954-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="bc954-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bc954-124">Structural Content</span></span>

<span data-ttu-id="bc954-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="bc954-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="bc954-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="bc954-126">Structure Variables</span></span>

<span data-ttu-id="bc954-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="bc954-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bc954-128">Nome</span><span class="sxs-lookup"><span data-stu-id="bc954-128">Name</span></span>                                   | <span data-ttu-id="bc954-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bc954-129">Data type</span></span>          | <span data-ttu-id="bc954-130">Unità</span><span class="sxs-lookup"><span data-stu-id="bc954-130">Unit</span></span>                  | <span data-ttu-id="bc954-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="bc954-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bc954-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="bc954-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc954-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="bc954-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="bc954-134">string</span><span class="sxs-lookup"><span data-stu-id="bc954-134">string</span></span><br/>  | <span data-ttu-id="bc954-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="bc954-135">characters</span></span><br/> | <span data-ttu-id="bc954-136">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="bc954-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bc954-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="bc954-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bc954-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="bc954-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="bc954-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="bc954-140">string</span><span class="sxs-lookup"><span data-stu-id="bc954-140">string</span></span><br/>  | <span data-ttu-id="bc954-141">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-141">n/a</span></span><br/>        | <span data-ttu-id="bc954-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="bc954-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bc954-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bc954-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="bc954-144">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="bc954-145">string</span><span class="sxs-lookup"><span data-stu-id="bc954-145">string</span></span><br/>  | <span data-ttu-id="bc954-146">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-146">n/a</span></span><br/>        | <span data-ttu-id="bc954-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="bc954-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bc954-148">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bc954-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="bc954-149">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="bc954-150">string</span><span class="sxs-lookup"><span data-stu-id="bc954-150">string</span></span><br/>  | <span data-ttu-id="bc954-151">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-151">n/a</span></span><br/>        | <span data-ttu-id="bc954-152">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="bc954-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="bc954-153">Specifica il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="bc954-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="bc954-154">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="bc954-155">string</span><span class="sxs-lookup"><span data-stu-id="bc954-155">string</span></span><br/>  | <span data-ttu-id="bc954-156">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-156">n/a</span></span><br/>        | <span data-ttu-id="bc954-157">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="bc954-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="bc954-158">Specifica il meccanismo di avanzamento del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bc954-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="bc954-159">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="bc954-160">string</span><span class="sxs-lookup"><span data-stu-id="bc954-160">string</span></span><br/>  | <span data-ttu-id="bc954-161">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-161">n/a</span></span><br/>        | <span data-ttu-id="bc954-162">Alto, Standard.</span><span class="sxs-lookup"><span data-stu-id="bc954-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="bc954-163">Specifica se il bin è un bin a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="bc954-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="bc954-164">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="bc954-165">string</span><span class="sxs-lookup"><span data-stu-id="bc954-165">string</span></span><br/>  | <span data-ttu-id="bc954-166">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-166">n/a</span></span><br/>        | <span data-ttu-id="bc954-167">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="bc954-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="bc954-168">Specifica la capacità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc954-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="bc954-169">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="bc954-170">string</span><span class="sxs-lookup"><span data-stu-id="bc954-170">string</span></span><br/>  | <span data-ttu-id="bc954-171">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-171">n/a</span></span><br/>        | <span data-ttu-id="bc954-172">Supportato, Nessuno.</span><span class="sxs-lookup"><span data-stu-id="bc954-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="bc954-173">Specifica la funzionalità di rilevamento automatico del tipo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc954-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="bc954-174">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="bc954-175">numero intero</span><span class="sxs-lookup"><span data-stu-id="bc954-175">integer</span></span><br/> | <span data-ttu-id="bc954-176">Fogli</span><span class="sxs-lookup"><span data-stu-id="bc954-176">sheets</span></span><br/>     | <span data-ttu-id="bc954-177">Vincolo integer massimo consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc954-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="bc954-178">Specifica la capacità media in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bc954-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="bc954-179">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="bc954-180">string</span><span class="sxs-lookup"><span data-stu-id="bc954-180">string</span></span><br/>  | <span data-ttu-id="bc954-181">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-181">n/a</span></span><br/>        | <span data-ttu-id="bc954-182">Diritto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="bc954-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="bc954-183">Specifica le caratteristiche del percorso del supporto.</span><span class="sxs-lookup"><span data-stu-id="bc954-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="bc954-184">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="bc954-185">string</span><span class="sxs-lookup"><span data-stu-id="bc954-185">string</span></span><br/>  | <span data-ttu-id="bc954-186">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-186">n/a</span></span><br/>        | <span data-ttu-id="bc954-187">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="bc954-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="bc954-188">Specifica se i supporti devono essere stampati a faccia in su o a faccia in giù.</span><span class="sxs-lookup"><span data-stu-id="bc954-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="bc954-189">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="bc954-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="bc954-190">string</span><span class="sxs-lookup"><span data-stu-id="bc954-190">string</span></span><br/>  | <span data-ttu-id="bc954-191">n/d</span><span class="sxs-lookup"><span data-stu-id="bc954-191">n/a</span></span><br/>        | <span data-ttu-id="bc954-192">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="bc954-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="bc954-193">Specifica se il supporto viene alimentato per primo dal bordo lungo o dal bordo corto.</span><span class="sxs-lookup"><span data-stu-id="bc954-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bc954-194">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bc954-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bc954-195">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="bc954-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bc954-196">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="bc954-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="bc954-197">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc954-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc954-198">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="bc954-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




