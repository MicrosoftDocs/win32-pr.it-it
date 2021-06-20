---
description: Informazioni sull'elemento DocumentNUp, che descrive l'output e il formato di più pagine logiche in un singolo foglio fisico.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b49bd4fa3eb9f2b3b0083fc8022dbd6f41d090e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409264"
---
# <a name="documentnup"></a><span data-ttu-id="c6eb5-103">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="c6eb5-103">DocumentNUp</span></span>

<span data-ttu-id="c6eb5-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-104">This topic is not current.</span></span> <span data-ttu-id="c6eb5-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c6eb5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c6eb5-106">Descrive l'output e il formato di più pagine logiche in un singolo foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-106">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="c6eb5-107">Ogni documento viene compilato separatamente.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-107">Each document is compiled separately.</span></span> <span data-ttu-id="c6eb5-108">DocumentNUp e JobNUpAllDocumentsContiguously si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-108">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="c6eb5-109">Il driver deve determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="c6eb5-110">Il diagramma seguente illustra un esempio con il documento 1 contenente 3 pagine e il documento 2 contenente 2 pagine.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="c6eb5-111">Ogni documento viene duplexato separatamente.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-111">Each document is duplexed separately.</span></span> <span data-ttu-id="c6eb5-112">La direzione della presentazione illustrata di seguito è l'opzione RightBottom.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-112">The presentation direction shown below is the RightBottom option.</span></span>

![diagramma che illustra come le pagine del documento vengono disposte su un singolo foglio in base all'impostazione documentnup](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="c6eb5-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c6eb5-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c6eb5-115">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="c6eb5-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c6eb5-116">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c6eb5-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c6eb5-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c6eb5-117">Element Information</span></span>



| <span data-ttu-id="c6eb5-118">Nome</span><span class="sxs-lookup"><span data-stu-id="c6eb5-118">Name</span></span> | <span data-ttu-id="c6eb5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c6eb5-119">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6eb5-120">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c6eb5-120">Element Type</span></span> <br/>   | <span data-ttu-id="c6eb5-121">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="c6eb5-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c6eb5-122">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="c6eb5-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c6eb5-123">Documento</span><span class="sxs-lookup"><span data-stu-id="c6eb5-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="c6eb5-124">Note</span><span class="sxs-lookup"><span data-stu-id="c6eb5-124">Notes</span></span> <br/>          | <span data-ttu-id="c6eb5-125">Top, Bottom, Left e Right sono relativi a PageImageableSize, dove TopLeft è denotato dall'origine dell'asse x e dell'asse y.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c6eb5-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="c6eb5-126">Structural Content</span></span>

<span data-ttu-id="c6eb5-127">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c6eb5-127">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="c6eb5-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="c6eb5-128">Structure Variables</span></span>

<span data-ttu-id="c6eb5-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c6eb5-130">Nome</span><span class="sxs-lookup"><span data-stu-id="c6eb5-130">Name</span></span>                                           | <span data-ttu-id="c6eb5-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c6eb5-131">Data type</span></span>          | <span data-ttu-id="c6eb5-132">Unità</span><span class="sxs-lookup"><span data-stu-id="c6eb5-132">Unit</span></span>                     | <span data-ttu-id="c6eb5-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="c6eb5-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c6eb5-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="c6eb5-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6eb5-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c6eb5-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="c6eb5-136">string</span><span class="sxs-lookup"><span data-stu-id="c6eb5-136">string</span></span><br/>  | <span data-ttu-id="c6eb5-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="c6eb5-137">characters</span></span><br/>    | <span data-ttu-id="c6eb5-138">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c6eb5-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c6eb5-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c6eb5-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="c6eb5-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c6eb5-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="c6eb5-142">string</span><span class="sxs-lookup"><span data-stu-id="c6eb5-142">string</span></span><br/>  | <span data-ttu-id="c6eb5-143">n/d</span><span class="sxs-lookup"><span data-stu-id="c6eb5-143">n/a</span></span><br/>           | <span data-ttu-id="c6eb5-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c6eb5-145">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="c6eb5-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="c6eb5-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="c6eb5-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="c6eb5-147">integer</span></span><br/> | <span data-ttu-id="c6eb5-148">Pagine logiche</span><span class="sxs-lookup"><span data-stu-id="c6eb5-148">Logical pages</span></span><br/> | <span data-ttu-id="c6eb5-149">Tutti i numeri interi (maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="c6eb5-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="c6eb5-150">Specifica il numero di pagine logiche per foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="c6eb5-151">Il set supportato può essere qualsiasi set di numeri interi, ad esempio</span><span class="sxs-lookup"><span data-stu-id="c6eb5-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="c6eb5-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="c6eb5-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="c6eb5-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="c6eb5-154">string</span><span class="sxs-lookup"><span data-stu-id="c6eb5-154">string</span></span><br/>  | <span data-ttu-id="c6eb5-155">caratteri</span><span class="sxs-lookup"><span data-stu-id="c6eb5-155">characters</span></span><br/>    | <span data-ttu-id="c6eb5-156">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="c6eb5-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c6eb5-157">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c6eb5-158">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c6eb5-159">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="c6eb5-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c6eb5-160">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="c6eb5-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c6eb5-161">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="c6eb5-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c6eb5-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6eb5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6eb5-163">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c6eb5-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




