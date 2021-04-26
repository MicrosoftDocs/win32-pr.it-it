---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557a742604f6e643e8812493049b7f2b118e262c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997528"
---
# <a name="pageoutputbin"></a><span data-ttu-id="e4a9c-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="e4a9c-104">PageOutputBin</span></span>

<span data-ttu-id="e4a9c-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-105">This topic is not current.</span></span> <span data-ttu-id="e4a9c-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e4a9c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e4a9c-107">Descrive l'elenco completo dei bin supportati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="e4a9c-108">Consente la specifica del contenitore di output per ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="e4a9c-109">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda solo in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="e4a9c-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e4a9c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e4a9c-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e4a9c-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e4a9c-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e4a9c-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e4a9c-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e4a9c-113">Element Information</span></span>



| <span data-ttu-id="e4a9c-114">Nome</span><span class="sxs-lookup"><span data-stu-id="e4a9c-114">Name</span></span> | <span data-ttu-id="e4a9c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e4a9c-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e4a9c-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e4a9c-116">Element Type</span></span> <br/>   | <span data-ttu-id="e4a9c-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="e4a9c-117">Feature</span></span><br/> |
| <span data-ttu-id="e4a9c-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e4a9c-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e4a9c-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="e4a9c-119">Page</span></span><br/>    |
| <span data-ttu-id="e4a9c-120">Note</span><span class="sxs-lookup"><span data-stu-id="e4a9c-120">Notes</span></span> <br/>          | <span data-ttu-id="e4a9c-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="e4a9c-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e4a9c-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e4a9c-122">Structural Content</span></span>

<span data-ttu-id="e4a9c-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e4a9c-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="e4a9c-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e4a9c-124">Structure Variables</span></span>

<span data-ttu-id="e4a9c-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e4a9c-126">Nome</span><span class="sxs-lookup"><span data-stu-id="e4a9c-126">Name</span></span>                                   | <span data-ttu-id="e4a9c-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e4a9c-127">Data type</span></span>          | <span data-ttu-id="e4a9c-128">Unità</span><span class="sxs-lookup"><span data-stu-id="e4a9c-128">Unit</span></span>                  | <span data-ttu-id="e4a9c-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e4a9c-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e4a9c-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e4a9c-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a9c-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e4a9c-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="e4a9c-132">string</span><span class="sxs-lookup"><span data-stu-id="e4a9c-132">string</span></span><br/>  | <span data-ttu-id="e4a9c-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="e4a9c-133">characters</span></span><br/> | <span data-ttu-id="e4a9c-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="e4a9c-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e4a9c-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e4a9c-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="e4a9c-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e4a9c-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="e4a9c-138">string</span><span class="sxs-lookup"><span data-stu-id="e4a9c-138">string</span></span><br/>  | <span data-ttu-id="e4a9c-139">n/d</span><span class="sxs-lookup"><span data-stu-id="e4a9c-139">n/a</span></span><br/>        | <span data-ttu-id="e4a9c-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e4a9c-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="e4a9c-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="e4a9c-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="e4a9c-143">string</span><span class="sxs-lookup"><span data-stu-id="e4a9c-143">string</span></span><br/>  | <span data-ttu-id="e4a9c-144">n/d</span><span class="sxs-lookup"><span data-stu-id="e4a9c-144">n/a</span></span><br/>        | <span data-ttu-id="e4a9c-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="e4a9c-146">Specifica il tipo generale del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="e4a9c-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="e4a9c-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="e4a9c-148">numero intero</span><span class="sxs-lookup"><span data-stu-id="e4a9c-148">integer</span></span><br/> | <span data-ttu-id="e4a9c-149">Fogli</span><span class="sxs-lookup"><span data-stu-id="e4a9c-149">sheets</span></span><br/>     | <span data-ttu-id="e4a9c-150">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-150">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e4a9c-151">Specifica la capacità multimediale in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e4a9c-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e4a9c-152">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e4a9c-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e4a9c-153">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="e4a9c-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e4a9c-154">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="e4a9c-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="related-topics"></a><span data-ttu-id="e4a9c-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4a9c-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4a9c-156">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e4a9c-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




