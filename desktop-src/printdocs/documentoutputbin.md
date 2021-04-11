---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444ca63fee0b76f17909b1aa08e65cd468537dee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234599"
---
# <a name="documentoutputbin"></a><span data-ttu-id="8c448-104">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="8c448-104">DocumentOutputBin</span></span>

<span data-ttu-id="8c448-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8c448-105">This topic is not current.</span></span> <span data-ttu-id="8c448-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8c448-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8c448-107">Descrive l'elenco completo dei cestini supportati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c448-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="8c448-108">Consente di specificare il cestino di output in base al documento.</span><span class="sxs-lookup"><span data-stu-id="8c448-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="8c448-109">Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda. è necessario specificare solo un oggetto PrintTicket o un documento sulle funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c448-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="8c448-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8c448-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="8c448-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="8c448-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="8c448-112">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="8c448-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8c448-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8c448-113">Element Information</span></span>



| <span data-ttu-id="8c448-114">Nome</span><span class="sxs-lookup"><span data-stu-id="8c448-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="8c448-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="8c448-115">Element Type</span></span> <br/>   | <span data-ttu-id="8c448-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="8c448-116">Feature</span></span><br/>  |
| <span data-ttu-id="8c448-117">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="8c448-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8c448-118">Documento</span><span class="sxs-lookup"><span data-stu-id="8c448-118">Document</span></span><br/> |
| <span data-ttu-id="8c448-119">Note</span><span class="sxs-lookup"><span data-stu-id="8c448-119">Notes</span></span> <br/>          | <span data-ttu-id="8c448-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="8c448-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="8c448-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="8c448-121">Structural Content</span></span>

<span data-ttu-id="8c448-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="8c448-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8c448-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="8c448-123">Structure Variables</span></span>

<span data-ttu-id="8c448-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="8c448-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8c448-125">Nome</span><span class="sxs-lookup"><span data-stu-id="8c448-125">Name</span></span>                                   | <span data-ttu-id="8c448-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8c448-126">Data type</span></span>          | <span data-ttu-id="8c448-127">Unità</span><span class="sxs-lookup"><span data-stu-id="8c448-127">Unit</span></span>                  | <span data-ttu-id="8c448-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="8c448-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="8c448-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="8c448-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c448-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8c448-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="8c448-131">string</span><span class="sxs-lookup"><span data-stu-id="8c448-131">string</span></span><br/>  | <span data-ttu-id="8c448-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="8c448-132">characters</span></span><br/> | <span data-ttu-id="8c448-133">Nome completo valido definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="8c448-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="8c448-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8c448-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8c448-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="8c448-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="8c448-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8c448-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="8c448-137">string</span><span class="sxs-lookup"><span data-stu-id="8c448-137">string</span></span><br/>  | <span data-ttu-id="8c448-138">n/d</span><span class="sxs-lookup"><span data-stu-id="8c448-138">n/a</span></span><br/>        | <span data-ttu-id="8c448-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="8c448-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="8c448-140">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8c448-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="8c448-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="8c448-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="8c448-142">string</span><span class="sxs-lookup"><span data-stu-id="8c448-142">string</span></span><br/>  | <span data-ttu-id="8c448-143">n/d</span><span class="sxs-lookup"><span data-stu-id="8c448-143">n/a</span></span><br/>        | <span data-ttu-id="8c448-144">MailBox, sorter, Stacker, Finisher, None.</span><span class="sxs-lookup"><span data-stu-id="8c448-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="8c448-145">Specifica il tipo generale del cestino.</span><span class="sxs-lookup"><span data-stu-id="8c448-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="8c448-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="8c448-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="8c448-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="8c448-147">integer</span></span><br/> | <span data-ttu-id="8c448-148">fogli</span><span class="sxs-lookup"><span data-stu-id="8c448-148">sheets</span></span><br/>     | <span data-ttu-id="8c448-149">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="8c448-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="8c448-150">Specifica la capacità del supporto in numero di pagine (livello completo) del cestino.</span><span class="sxs-lookup"><span data-stu-id="8c448-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8c448-151">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="8c448-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8c448-152">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8c448-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8c448-153">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="8c448-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8c448-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c448-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c448-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="8c448-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




