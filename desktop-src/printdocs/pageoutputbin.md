---
description: Informazioni sull'elemento PageOutputBin configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9963bf2ca7a2dd60be37c797a27c6ff09b1206
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548999"
---
# <a name="pageoutputbin"></a><span data-ttu-id="27c1c-105">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="27c1c-105">PageOutputBin</span></span>

<span data-ttu-id="27c1c-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="27c1c-106">This topic is not current.</span></span> <span data-ttu-id="27c1c-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="27c1c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27c1c-108">Descrive l'elenco completo dei bin supportati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27c1c-108">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="27c1c-109">Consente di specificare il contenitore di output per pagina.</span><span class="sxs-lookup"><span data-stu-id="27c1c-109">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="27c1c-110">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda solo se ne deve essere specificata una in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="27c1c-110">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="27c1c-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="27c1c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27c1c-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="27c1c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="27c1c-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="27c1c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="27c1c-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="27c1c-114">Element Information</span></span>



| <span data-ttu-id="27c1c-115">Nome</span><span class="sxs-lookup"><span data-stu-id="27c1c-115">Name</span></span> | <span data-ttu-id="27c1c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="27c1c-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="27c1c-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="27c1c-117">Element Type</span></span> <br/>   | <span data-ttu-id="27c1c-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="27c1c-118">Feature</span></span><br/> |
| <span data-ttu-id="27c1c-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="27c1c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27c1c-120">Pagina</span><span class="sxs-lookup"><span data-stu-id="27c1c-120">Page</span></span><br/>    |
| <span data-ttu-id="27c1c-121">Note</span><span class="sxs-lookup"><span data-stu-id="27c1c-121">Notes</span></span> <br/>          | <span data-ttu-id="27c1c-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="27c1c-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="27c1c-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="27c1c-123">Structural Content</span></span>

<span data-ttu-id="27c1c-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="27c1c-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="27c1c-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="27c1c-125">Structure Variables</span></span>

<span data-ttu-id="27c1c-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="27c1c-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27c1c-127">Nome</span><span class="sxs-lookup"><span data-stu-id="27c1c-127">Name</span></span>                                   | <span data-ttu-id="27c1c-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="27c1c-128">Data type</span></span>          | <span data-ttu-id="27c1c-129">Unità</span><span class="sxs-lookup"><span data-stu-id="27c1c-129">Unit</span></span>                  | <span data-ttu-id="27c1c-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="27c1c-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="27c1c-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="27c1c-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="27c1c-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="27c1c-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="27c1c-133">string</span><span class="sxs-lookup"><span data-stu-id="27c1c-133">string</span></span><br/>  | <span data-ttu-id="27c1c-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="27c1c-134">characters</span></span><br/> | <span data-ttu-id="27c1c-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="27c1c-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="27c1c-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="27c1c-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="27c1c-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="27c1c-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="27c1c-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="27c1c-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="27c1c-139">string</span><span class="sxs-lookup"><span data-stu-id="27c1c-139">string</span></span><br/>  | <span data-ttu-id="27c1c-140">n/d</span><span class="sxs-lookup"><span data-stu-id="27c1c-140">n/a</span></span><br/>        | <span data-ttu-id="27c1c-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="27c1c-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="27c1c-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="27c1c-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="27c1c-143">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="27c1c-143">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="27c1c-144">string</span><span class="sxs-lookup"><span data-stu-id="27c1c-144">string</span></span><br/>  | <span data-ttu-id="27c1c-145">n/d</span><span class="sxs-lookup"><span data-stu-id="27c1c-145">n/a</span></span><br/>        | <span data-ttu-id="27c1c-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span><span class="sxs-lookup"><span data-stu-id="27c1c-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="27c1c-147">Specifica il tipo generale del contenitore.</span><span class="sxs-lookup"><span data-stu-id="27c1c-147">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="27c1c-148">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="27c1c-148">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="27c1c-149">numero intero</span><span class="sxs-lookup"><span data-stu-id="27c1c-149">integer</span></span><br/> | <span data-ttu-id="27c1c-150">Fogli</span><span class="sxs-lookup"><span data-stu-id="27c1c-150">sheets</span></span><br/>     | <span data-ttu-id="27c1c-151">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="27c1c-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="27c1c-152">Specifica la capacità multimediale in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="27c1c-152">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="27c1c-153">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="27c1c-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="27c1c-154">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="27c1c-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="27c1c-155">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="27c1c-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="27c1c-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27c1c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c1c-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="27c1c-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




