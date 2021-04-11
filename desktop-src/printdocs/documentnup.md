---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234611"
---
# <a name="documentnup"></a><span data-ttu-id="29b95-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="29b95-104">DocumentNUp</span></span>

<span data-ttu-id="29b95-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="29b95-105">This topic is not current.</span></span> <span data-ttu-id="29b95-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="29b95-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="29b95-107">Descrive l'output e il formato di più pagine logiche in un singolo foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="29b95-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="29b95-108">Ogni documento viene compilato separatamente.</span><span class="sxs-lookup"><span data-stu-id="29b95-108">Each document is compiled separately.</span></span> <span data-ttu-id="29b95-109">DocumentNUp e JobNUpAllDocumentsContiguously si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="29b95-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="29b95-110">Spetta al driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="29b95-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="29b95-111">Il diagramma seguente illustra un esempio con il documento 1 contenente tre pagine e il documento 2 contenente 2 pagine.</span><span class="sxs-lookup"><span data-stu-id="29b95-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="29b95-112">Ogni documento è duplexed separatamente.</span><span class="sxs-lookup"><span data-stu-id="29b95-112">Each document is duplexed separately.</span></span> <span data-ttu-id="29b95-113">La direzione di presentazione mostrata di seguito è l'opzione RightBottom.</span><span class="sxs-lookup"><span data-stu-id="29b95-113">The presentation direction shown below is the RightBottom option.</span></span>

![diagramma che mostra la disposizione delle pagine documento in un singolo foglio in base all'impostazione DocumentNUp](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="29b95-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="29b95-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="29b95-116">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="29b95-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="29b95-117">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="29b95-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="29b95-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="29b95-118">Element Information</span></span>



| <span data-ttu-id="29b95-119">Nome</span><span class="sxs-lookup"><span data-stu-id="29b95-119">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b95-120">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="29b95-120">Element Type</span></span> <br/>   | <span data-ttu-id="29b95-121">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="29b95-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="29b95-122">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="29b95-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="29b95-123">Documento</span><span class="sxs-lookup"><span data-stu-id="29b95-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="29b95-124">Note</span><span class="sxs-lookup"><span data-stu-id="29b95-124">Notes</span></span> <br/>          | <span data-ttu-id="29b95-125">In alto, in basso, a sinistra e a destra sono relativi a PageImageableSize dell'oggetto, dove la parte superiore è indicata dall'origine dell'asse x e dall'asse y.</span><span class="sxs-lookup"><span data-stu-id="29b95-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="29b95-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="29b95-126">Structural Content</span></span>

<span data-ttu-id="29b95-127">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="29b95-127">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="29b95-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="29b95-128">Structure Variables</span></span>

<span data-ttu-id="29b95-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="29b95-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="29b95-130">Nome</span><span class="sxs-lookup"><span data-stu-id="29b95-130">Name</span></span>                                           | <span data-ttu-id="29b95-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="29b95-131">Data type</span></span>          | <span data-ttu-id="29b95-132">Unità</span><span class="sxs-lookup"><span data-stu-id="29b95-132">Unit</span></span>                     | <span data-ttu-id="29b95-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="29b95-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="29b95-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="29b95-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b95-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="29b95-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="29b95-136">string</span><span class="sxs-lookup"><span data-stu-id="29b95-136">string</span></span><br/>  | <span data-ttu-id="29b95-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="29b95-137">characters</span></span><br/>    | <span data-ttu-id="29b95-138">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="29b95-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="29b95-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="29b95-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="29b95-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="29b95-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="29b95-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="29b95-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="29b95-142">string</span><span class="sxs-lookup"><span data-stu-id="29b95-142">string</span></span><br/>  | <span data-ttu-id="29b95-143">n/d</span><span class="sxs-lookup"><span data-stu-id="29b95-143">n/a</span></span><br/>           | <span data-ttu-id="29b95-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="29b95-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="29b95-145">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="29b95-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="29b95-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="29b95-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="29b95-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="29b95-147">integer</span></span><br/> | <span data-ttu-id="29b95-148">Pagine logiche</span><span class="sxs-lookup"><span data-stu-id="29b95-148">Logical pages</span></span><br/> | <span data-ttu-id="29b95-149">Tutti i numeri interi (maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="29b95-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="29b95-150">Specifica il numero di pagine logiche per foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="29b95-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="29b95-151">Il set supportato può essere qualsiasi set di numeri interi, ad esempio</span><span class="sxs-lookup"><span data-stu-id="29b95-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="29b95-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="29b95-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="29b95-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="29b95-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="29b95-154">string</span><span class="sxs-lookup"><span data-stu-id="29b95-154">string</span></span><br/>  | <span data-ttu-id="29b95-155">caratteri</span><span class="sxs-lookup"><span data-stu-id="29b95-155">characters</span></span><br/>    | <span data-ttu-id="29b95-156">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="29b95-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="29b95-157">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="29b95-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="29b95-158">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="29b95-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="29b95-159">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="29b95-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="29b95-160">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="29b95-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="29b95-161">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="29b95-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="29b95-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29b95-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29b95-163">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="29b95-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




