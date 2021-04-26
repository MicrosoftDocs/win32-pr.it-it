---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f90620ac99bf97e85acb22c723a938c31605bd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998088"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="0493a-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="0493a-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="0493a-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0493a-105">This topic is not current.</span></span> <span data-ttu-id="0493a-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0493a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0493a-107">Descrive l'output di più pagine logiche in un singolo foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="0493a-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="0493a-108">Tutti i documenti nel processo vengono compilati in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="0493a-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="0493a-109">JobNUpAllDocumentsContiguously e DocumentNUp si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="0493a-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="0493a-110">Il driver deve determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="0493a-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="0493a-111">Il diagramma seguente illustra un esempio con il documento 1 contenente 3 pagine e il documento 2 contenente 2 pagine.</span><span class="sxs-lookup"><span data-stu-id="0493a-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="0493a-112">Ogni documento nel processo è duplex in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="0493a-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="0493a-113">Le indicazioni per la presentazione mostrate nell'esempio sono l'opzione RightBottom.</span><span class="sxs-lookup"><span data-stu-id="0493a-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![diagramma che illustra come le pagine del documento vengono disposte su un singolo foglio in base all'impostazione documentnup](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="0493a-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0493a-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0493a-116">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0493a-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0493a-117">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0493a-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0493a-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0493a-118">Element Information</span></span>



| <span data-ttu-id="0493a-119">Nome</span><span class="sxs-lookup"><span data-stu-id="0493a-119">Name</span></span> | <span data-ttu-id="0493a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0493a-120">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0493a-121">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0493a-121">Element Type</span></span> <br/>   | <span data-ttu-id="0493a-122">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="0493a-122">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="0493a-123">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0493a-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0493a-124">Processo</span><span class="sxs-lookup"><span data-stu-id="0493a-124">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="0493a-125">Note</span><span class="sxs-lookup"><span data-stu-id="0493a-125">Notes</span></span> <br/>          | <span data-ttu-id="0493a-126">Top, Bottom, Left e Right sono relativi a PageImageableSize, dove TopLeft è denotato dall'origine dell'altezza e della larghezza.</span><span class="sxs-lookup"><span data-stu-id="0493a-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0493a-127">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0493a-127">Structural Content</span></span>

<span data-ttu-id="0493a-128">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0493a-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0493a-129">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="0493a-129">Structure Variables</span></span>

<span data-ttu-id="0493a-130">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0493a-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0493a-131">Nome</span><span class="sxs-lookup"><span data-stu-id="0493a-131">Name</span></span>                                           | <span data-ttu-id="0493a-132">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0493a-132">Data type</span></span>          | <span data-ttu-id="0493a-133">Unità</span><span class="sxs-lookup"><span data-stu-id="0493a-133">Unit</span></span>                     | <span data-ttu-id="0493a-134">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="0493a-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0493a-135">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="0493a-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0493a-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0493a-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="0493a-137">string</span><span class="sxs-lookup"><span data-stu-id="0493a-137">string</span></span><br/>  | <span data-ttu-id="0493a-138">caratteri</span><span class="sxs-lookup"><span data-stu-id="0493a-138">characters</span></span><br/>    | <span data-ttu-id="0493a-139">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="0493a-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0493a-140">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="0493a-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0493a-141">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="0493a-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="0493a-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0493a-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="0493a-143">string</span><span class="sxs-lookup"><span data-stu-id="0493a-143">string</span></span><br/>  | <span data-ttu-id="0493a-144">n/d</span><span class="sxs-lookup"><span data-stu-id="0493a-144">n/a</span></span><br/>           | <span data-ttu-id="0493a-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="0493a-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0493a-146">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0493a-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="0493a-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="0493a-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="0493a-148">numero intero</span><span class="sxs-lookup"><span data-stu-id="0493a-148">integer</span></span><br/> | <span data-ttu-id="0493a-149">Pagine logiche</span><span class="sxs-lookup"><span data-stu-id="0493a-149">Logical pages</span></span><br/> | <span data-ttu-id="0493a-150">Tutti i numeri interi (maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="0493a-150">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="0493a-151">Specifica il numero di pagine logiche per foglio fisico.</span><span class="sxs-lookup"><span data-stu-id="0493a-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="0493a-152">Il set supportato può essere qualsiasi set di numeri interi, ad esempio</span><span class="sxs-lookup"><span data-stu-id="0493a-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="0493a-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="0493a-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="0493a-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="0493a-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="0493a-155">string</span><span class="sxs-lookup"><span data-stu-id="0493a-155">string</span></span><br/>  | <span data-ttu-id="0493a-156">caratteri</span><span class="sxs-lookup"><span data-stu-id="0493a-156">characters</span></span><br/>    | <span data-ttu-id="0493a-157">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="0493a-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0493a-158">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="0493a-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0493a-159">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="0493a-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0493a-160">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0493a-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0493a-161">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="0493a-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0493a-162">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="0493a-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0493a-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0493a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0493a-164">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0493a-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




