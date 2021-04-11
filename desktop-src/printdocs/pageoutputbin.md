---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bae72b69f83697cc2f482f21995acb587a2ace
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234616"
---
# <a name="pageoutputbin"></a><span data-ttu-id="fb25d-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="fb25d-104">PageOutputBin</span></span>

<span data-ttu-id="fb25d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="fb25d-105">This topic is not current.</span></span> <span data-ttu-id="fb25d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fb25d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fb25d-107">Descrive l'elenco completo dei cestini supportati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb25d-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="fb25d-108">Consente di specificare il contenitore di output in base a ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="fb25d-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="fb25d-109">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda. è necessario specificare solo un oggetto PrintTicket o un documento sulle funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="fb25d-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="fb25d-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fb25d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fb25d-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="fb25d-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fb25d-112">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="fb25d-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fb25d-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fb25d-113">Element Information</span></span>



| <span data-ttu-id="fb25d-114">Nome</span><span class="sxs-lookup"><span data-stu-id="fb25d-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="fb25d-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="fb25d-115">Element Type</span></span> <br/>   | <span data-ttu-id="fb25d-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="fb25d-116">Feature</span></span><br/> |
| <span data-ttu-id="fb25d-117">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="fb25d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fb25d-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="fb25d-118">Page</span></span><br/>    |
| <span data-ttu-id="fb25d-119">Note</span><span class="sxs-lookup"><span data-stu-id="fb25d-119">Notes</span></span> <br/>          | <span data-ttu-id="fb25d-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="fb25d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="fb25d-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="fb25d-121">Structural Content</span></span>

<span data-ttu-id="fb25d-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="fb25d-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="fb25d-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="fb25d-123">Structure Variables</span></span>

<span data-ttu-id="fb25d-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="fb25d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fb25d-125">Nome</span><span class="sxs-lookup"><span data-stu-id="fb25d-125">Name</span></span>                                   | <span data-ttu-id="fb25d-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fb25d-126">Data type</span></span>          | <span data-ttu-id="fb25d-127">Unità</span><span class="sxs-lookup"><span data-stu-id="fb25d-127">Unit</span></span>                  | <span data-ttu-id="fb25d-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="fb25d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fb25d-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="fb25d-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb25d-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fb25d-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="fb25d-131">string</span><span class="sxs-lookup"><span data-stu-id="fb25d-131">string</span></span><br/>  | <span data-ttu-id="fb25d-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="fb25d-132">characters</span></span><br/> | <span data-ttu-id="fb25d-133">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fb25d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fb25d-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="fb25d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fb25d-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="fb25d-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="fb25d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="fb25d-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="fb25d-137">string</span><span class="sxs-lookup"><span data-stu-id="fb25d-137">string</span></span><br/>  | <span data-ttu-id="fb25d-138">n/d</span><span class="sxs-lookup"><span data-stu-id="fb25d-138">n/a</span></span><br/>        | <span data-ttu-id="fb25d-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="fb25d-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fb25d-140">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fb25d-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="fb25d-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="fb25d-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="fb25d-142">string</span><span class="sxs-lookup"><span data-stu-id="fb25d-142">string</span></span><br/>  | <span data-ttu-id="fb25d-143">n/d</span><span class="sxs-lookup"><span data-stu-id="fb25d-143">n/a</span></span><br/>        | <span data-ttu-id="fb25d-144">FaceDownTray, FaceUpTray, MailBox, sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="fb25d-144">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="fb25d-145">Specifica il tipo generale del cestino.</span><span class="sxs-lookup"><span data-stu-id="fb25d-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="fb25d-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="fb25d-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="fb25d-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="fb25d-147">integer</span></span><br/> | <span data-ttu-id="fb25d-148">fogli</span><span class="sxs-lookup"><span data-stu-id="fb25d-148">sheets</span></span><br/>     | <span data-ttu-id="fb25d-149">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="fb25d-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="fb25d-150">Specifica la capacità del supporto in numero di pagine (livello completo) del cestino.</span><span class="sxs-lookup"><span data-stu-id="fb25d-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fb25d-151">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="fb25d-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fb25d-152">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fb25d-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fb25d-153">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="fb25d-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fb25d-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb25d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb25d-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="fb25d-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




