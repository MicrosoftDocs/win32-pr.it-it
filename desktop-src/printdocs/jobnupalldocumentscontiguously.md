---
description: Informazioni sull'elemento JobNUpAllDocumentsContiguously, che descrive l'output di più pagine logiche in un singolo foglio fisico.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408864"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="5a509-103">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="5a509-103">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="5a509-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5a509-104">This topic is not current.</span></span> <span data-ttu-id="5a509-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a509-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a509-106">Descrive l'output di più pagine logiche in un singolo foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="5a509-106">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="5a509-107">Tutti i documenti nel processo vengono compilati insieme in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="5a509-107">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="5a509-108">JobNUpAllDocumentsContiguously e DocumentNUp si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="5a509-108">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="5a509-109">È responsabilità del driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="5a509-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="5a509-110">Il diagramma seguente illustra un esempio con il documento 1 contenente 3 pagine e il documento 2 contenente 2 pagine.</span><span class="sxs-lookup"><span data-stu-id="5a509-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="5a509-111">Ogni documento del processo è duplex in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="5a509-111">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="5a509-112">Le direzioni di presentazione mostrate nell'esempio sono l'opzione RightBottom.</span><span class="sxs-lookup"><span data-stu-id="5a509-112">The presentation directions shown in the example is the RightBottom option.</span></span>

![diagramma che mostra come vengono disposte le pagine del documento in un singolo foglio in base all'impostazione di documentnup](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="5a509-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5a509-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5a509-115">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5a509-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5a509-116">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5a509-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5a509-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5a509-117">Element Information</span></span>



| <span data-ttu-id="5a509-118">Nome</span><span class="sxs-lookup"><span data-stu-id="5a509-118">Name</span></span> | <span data-ttu-id="5a509-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5a509-119">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a509-120">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5a509-120">Element Type</span></span> <br/>   | <span data-ttu-id="5a509-121">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5a509-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="5a509-122">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5a509-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a509-123">Processo</span><span class="sxs-lookup"><span data-stu-id="5a509-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="5a509-124">Note</span><span class="sxs-lookup"><span data-stu-id="5a509-124">Notes</span></span> <br/>          | <span data-ttu-id="5a509-125">Top, Bottom, Left e Right sono relativi a PageImageableSize, dove TopLeft è denotato dall'origine dell'altezza e della larghezza.</span><span class="sxs-lookup"><span data-stu-id="5a509-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5a509-126">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5a509-126">Structural Content</span></span>

<span data-ttu-id="5a509-127">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5a509-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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

## <a name="structure-variables"></a><span data-ttu-id="5a509-128">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="5a509-128">Structure Variables</span></span>

<span data-ttu-id="5a509-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5a509-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a509-130">Nome</span><span class="sxs-lookup"><span data-stu-id="5a509-130">Name</span></span>                                           | <span data-ttu-id="5a509-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5a509-131">Data type</span></span>          | <span data-ttu-id="5a509-132">Unità</span><span class="sxs-lookup"><span data-stu-id="5a509-132">Unit</span></span>                     | <span data-ttu-id="5a509-133">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="5a509-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5a509-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5a509-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a509-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5a509-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="5a509-136">string</span><span class="sxs-lookup"><span data-stu-id="5a509-136">string</span></span><br/>  | <span data-ttu-id="5a509-137">caratteri</span><span class="sxs-lookup"><span data-stu-id="5a509-137">characters</span></span><br/>    | <span data-ttu-id="5a509-138">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5a509-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5a509-139">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a509-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5a509-140">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5a509-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="5a509-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5a509-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="5a509-142">string</span><span class="sxs-lookup"><span data-stu-id="5a509-142">string</span></span><br/>  | <span data-ttu-id="5a509-143">n/d</span><span class="sxs-lookup"><span data-stu-id="5a509-143">n/a</span></span><br/>           | <span data-ttu-id="5a509-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="5a509-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5a509-145">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5a509-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="5a509-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="5a509-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="5a509-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="5a509-147">integer</span></span><br/> | <span data-ttu-id="5a509-148">Pagine logiche</span><span class="sxs-lookup"><span data-stu-id="5a509-148">Logical pages</span></span><br/> | <span data-ttu-id="5a509-149">Tutti i numeri interi (maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="5a509-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="5a509-150">Specifica il numero di pagine logiche per foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="5a509-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="5a509-151">Il set supportato può essere qualsiasi set di numeri interi, ad esempio</span><span class="sxs-lookup"><span data-stu-id="5a509-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="5a509-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="5a509-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="5a509-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="5a509-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="5a509-154">string</span><span class="sxs-lookup"><span data-stu-id="5a509-154">string</span></span><br/>  | <span data-ttu-id="5a509-155">caratteri</span><span class="sxs-lookup"><span data-stu-id="5a509-155">characters</span></span><br/>    | <span data-ttu-id="5a509-156">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5a509-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5a509-157">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a509-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5a509-158">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5a509-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5a509-159">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5a509-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5a509-160">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="5a509-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5a509-161">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="5a509-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="5a509-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a509-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a509-163">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5a509-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




