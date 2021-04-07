---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c8d84b099fb11aa97dea6f242f08acdd532105
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103886060"
---
# <a name="pageinputbin"></a><span data-ttu-id="ed754-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="ed754-104">PageInputBin</span></span>

<span data-ttu-id="ed754-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ed754-105">This topic is not current.</span></span> <span data-ttu-id="ed754-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ed754-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ed754-107">Descrive il contenitore di input installato in un dispositivo o l'elenco completo di contenitori supportati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed754-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="ed754-108">Consente di specificare il contenitore di input in base alla pagina.</span><span class="sxs-lookup"><span data-stu-id="ed754-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="ed754-109">Le parole chiave JobInputBin, DocumentInputBin e PageInputBin si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="ed754-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="ed754-110">Non devono essere specificati contemporaneamente in un documento di funzionalità di stampa o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ed754-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="ed754-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ed754-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ed754-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ed754-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ed754-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ed754-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ed754-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ed754-114">Element Information</span></span>



| <span data-ttu-id="ed754-115">Nome</span><span class="sxs-lookup"><span data-stu-id="ed754-115">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ed754-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ed754-116">Element Type</span></span> <br/>   | <span data-ttu-id="ed754-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="ed754-117">Feature</span></span><br/> |
| <span data-ttu-id="ed754-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="ed754-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ed754-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="ed754-119">Page</span></span><br/>    |
| <span data-ttu-id="ed754-120">Note</span><span class="sxs-lookup"><span data-stu-id="ed754-120">Notes</span></span> <br/>          | <span data-ttu-id="ed754-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="ed754-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ed754-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ed754-122">Structural Content</span></span>

<span data-ttu-id="ed754-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ed754-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ed754-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ed754-124">Structure Variables</span></span>

<span data-ttu-id="ed754-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ed754-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ed754-126">Nome</span><span class="sxs-lookup"><span data-stu-id="ed754-126">Name</span></span>                                   | <span data-ttu-id="ed754-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ed754-127">Data type</span></span>          | <span data-ttu-id="ed754-128">Unità</span><span class="sxs-lookup"><span data-stu-id="ed754-128">Unit</span></span>                  | <span data-ttu-id="ed754-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ed754-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ed754-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ed754-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed754-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ed754-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="ed754-132">string</span><span class="sxs-lookup"><span data-stu-id="ed754-132">string</span></span><br/>  | <span data-ttu-id="ed754-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="ed754-133">characters</span></span><br/> | <span data-ttu-id="ed754-134">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ed754-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ed754-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ed754-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ed754-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="ed754-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="ed754-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="ed754-138">string</span><span class="sxs-lookup"><span data-stu-id="ed754-138">string</span></span><br/>  | <span data-ttu-id="ed754-139">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-139">n/a</span></span><br/>        | <span data-ttu-id="ed754-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="ed754-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ed754-141">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ed754-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="ed754-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="ed754-143">string</span><span class="sxs-lookup"><span data-stu-id="ed754-143">string</span></span><br/>  | <span data-ttu-id="ed754-144">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-144">n/a</span></span><br/>        | <span data-ttu-id="ed754-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="ed754-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ed754-146">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ed754-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="ed754-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="ed754-148">string</span><span class="sxs-lookup"><span data-stu-id="ed754-148">string</span></span><br/>  | <span data-ttu-id="ed754-149">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-149">n/a</span></span><br/>        | <span data-ttu-id="ed754-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="ed754-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="ed754-151">Specifica il tipo del cestino.</span><span class="sxs-lookup"><span data-stu-id="ed754-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="ed754-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="ed754-153">string</span><span class="sxs-lookup"><span data-stu-id="ed754-153">string</span></span><br/>  | <span data-ttu-id="ed754-154">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-154">n/a</span></span><br/>        | <span data-ttu-id="ed754-155">Automatico, manuale.</span><span class="sxs-lookup"><span data-stu-id="ed754-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="ed754-156">Specifica il meccanismo di feed del cestino.</span><span class="sxs-lookup"><span data-stu-id="ed754-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="ed754-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="ed754-158">string</span><span class="sxs-lookup"><span data-stu-id="ed754-158">string</span></span><br/>  | <span data-ttu-id="ed754-159">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-159">n/a</span></span><br/>        | <span data-ttu-id="ed754-160">Alta, standard.</span><span class="sxs-lookup"><span data-stu-id="ed754-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="ed754-161">Specifica se il cestino è un contenitore a capacità elevata (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="ed754-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="ed754-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="ed754-163">string</span><span class="sxs-lookup"><span data-stu-id="ed754-163">string</span></span><br/>  | <span data-ttu-id="ed754-164">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-164">n/a</span></span><br/>        | <span data-ttu-id="ed754-165">Supportato, nessuno.</span><span class="sxs-lookup"><span data-stu-id="ed754-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="ed754-166">Specifica la capacità di rilevamento automatico delle dimensioni dei supporti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed754-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="ed754-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="ed754-168">string</span><span class="sxs-lookup"><span data-stu-id="ed754-168">string</span></span><br/>  | <span data-ttu-id="ed754-169">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-169">n/a</span></span><br/>        | <span data-ttu-id="ed754-170">Supportato, nessuno.</span><span class="sxs-lookup"><span data-stu-id="ed754-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="ed754-171">Specifica la funzionalità di rilevamento automatico del tipo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed754-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="ed754-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="ed754-173">numero intero</span><span class="sxs-lookup"><span data-stu-id="ed754-173">integer</span></span><br/> | <span data-ttu-id="ed754-174">fogli</span><span class="sxs-lookup"><span data-stu-id="ed754-174">sheets</span></span><br/>     | <span data-ttu-id="ed754-175">Limite massimo di Integer consentito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed754-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="ed754-176">Specifica la capacità del supporto in numero di pagine (livello completo) del cestino.</span><span class="sxs-lookup"><span data-stu-id="ed754-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="ed754-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="ed754-178">string</span><span class="sxs-lookup"><span data-stu-id="ed754-178">string</span></span><br/>  | <span data-ttu-id="ed754-179">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-179">n/a</span></span><br/>        | <span data-ttu-id="ed754-180">Dritto, serpentine.</span><span class="sxs-lookup"><span data-stu-id="ed754-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="ed754-181">Specifica le caratteristiche del percorso del supporto.</span><span class="sxs-lookup"><span data-stu-id="ed754-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="ed754-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="ed754-183">string</span><span class="sxs-lookup"><span data-stu-id="ed754-183">string</span></span><br/>  | <span data-ttu-id="ed754-184">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-184">n/a</span></span><br/>        | <span data-ttu-id="ed754-185">FaceUp, faccia a faccia</span><span class="sxs-lookup"><span data-stu-id="ed754-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="ed754-186">Specifica se i supporti devono essere stampati o in basso.</span><span class="sxs-lookup"><span data-stu-id="ed754-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="ed754-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="ed754-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="ed754-188">string</span><span class="sxs-lookup"><span data-stu-id="ed754-188">string</span></span><br/>  | <span data-ttu-id="ed754-189">n/d</span><span class="sxs-lookup"><span data-stu-id="ed754-189">n/a</span></span><br/>        | <span data-ttu-id="ed754-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="ed754-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="ed754-191">Specifica se il supporto viene alimentato prima o dopo un bordo breve.</span><span class="sxs-lookup"><span data-stu-id="ed754-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ed754-192">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ed754-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ed754-193">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ed754-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ed754-194">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="ed754-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ed754-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed754-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed754-196">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ed754-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




