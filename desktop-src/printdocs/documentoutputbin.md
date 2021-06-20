---
description: Informazioni su DocumentOutputBin, che descrive l'elenco completo dei bin supportati per il dispositivo e consente di specificare il bin di output per ogni documento.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409244"
---
# <a name="documentoutputbin"></a><span data-ttu-id="99a3f-103">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="99a3f-103">DocumentOutputBin</span></span>

<span data-ttu-id="99a3f-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="99a3f-104">This topic is not current.</span></span> <span data-ttu-id="99a3f-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="99a3f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="99a3f-106">Descrive l'elenco completo dei bin supportati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99a3f-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="99a3f-107">Consente di specificare il bin di output per ogni documento.</span><span class="sxs-lookup"><span data-stu-id="99a3f-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="99a3f-108">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda solo in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="99a3f-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="99a3f-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="99a3f-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="99a3f-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="99a3f-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="99a3f-111">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="99a3f-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="99a3f-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="99a3f-112">Element Information</span></span>



| <span data-ttu-id="99a3f-113">Nome</span><span class="sxs-lookup"><span data-stu-id="99a3f-113">Name</span></span> | <span data-ttu-id="99a3f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="99a3f-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="99a3f-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="99a3f-115">Element Type</span></span> <br/>   | <span data-ttu-id="99a3f-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="99a3f-116">Feature</span></span><br/>  |
| <span data-ttu-id="99a3f-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="99a3f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="99a3f-118">Documento</span><span class="sxs-lookup"><span data-stu-id="99a3f-118">Document</span></span><br/> |
| <span data-ttu-id="99a3f-119">Note</span><span class="sxs-lookup"><span data-stu-id="99a3f-119">Notes</span></span> <br/>          | <span data-ttu-id="99a3f-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="99a3f-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="99a3f-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="99a3f-121">Structural Content</span></span>

<span data-ttu-id="99a3f-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="99a3f-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="99a3f-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="99a3f-123">Structure Variables</span></span>

<span data-ttu-id="99a3f-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="99a3f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="99a3f-125">Nome</span><span class="sxs-lookup"><span data-stu-id="99a3f-125">Name</span></span>                                   | <span data-ttu-id="99a3f-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="99a3f-126">Data type</span></span>          | <span data-ttu-id="99a3f-127">Unità</span><span class="sxs-lookup"><span data-stu-id="99a3f-127">Unit</span></span>                  | <span data-ttu-id="99a3f-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="99a3f-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="99a3f-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="99a3f-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99a3f-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="99a3f-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="99a3f-131">string</span><span class="sxs-lookup"><span data-stu-id="99a3f-131">string</span></span><br/>  | <span data-ttu-id="99a3f-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="99a3f-132">characters</span></span><br/> | <span data-ttu-id="99a3f-133">Nome completo valido come definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="99a3f-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="99a3f-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="99a3f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="99a3f-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="99a3f-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="99a3f-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="99a3f-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="99a3f-137">string</span><span class="sxs-lookup"><span data-stu-id="99a3f-137">string</span></span><br/>  | <span data-ttu-id="99a3f-138">n/d</span><span class="sxs-lookup"><span data-stu-id="99a3f-138">n/a</span></span><br/>        | <span data-ttu-id="99a3f-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="99a3f-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="99a3f-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="99a3f-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="99a3f-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="99a3f-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="99a3f-142">string</span><span class="sxs-lookup"><span data-stu-id="99a3f-142">string</span></span><br/>  | <span data-ttu-id="99a3f-143">n/d</span><span class="sxs-lookup"><span data-stu-id="99a3f-143">n/a</span></span><br/>        | <span data-ttu-id="99a3f-144">MailBox, Sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="99a3f-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="99a3f-145">Specifica il tipo generale del contenitore.</span><span class="sxs-lookup"><span data-stu-id="99a3f-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="99a3f-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="99a3f-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="99a3f-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="99a3f-147">integer</span></span><br/> | <span data-ttu-id="99a3f-148">Fogli</span><span class="sxs-lookup"><span data-stu-id="99a3f-148">sheets</span></span><br/>     | <span data-ttu-id="99a3f-149">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="99a3f-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="99a3f-150">Specifica la capacità media in numero di pagine (livello completo) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="99a3f-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="99a3f-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="99a3f-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="99a3f-152">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="99a3f-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="99a3f-153">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="99a3f-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="99a3f-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99a3f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a3f-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="99a3f-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




