---
description: Informazioni sull'elemento DocumentCollate, che descrive le caratteristiche di confronto dell'output.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409454"
---
# <a name="documentcollate"></a><span data-ttu-id="23097-103">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="23097-103">DocumentCollate</span></span>

<span data-ttu-id="23097-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="23097-104">This topic is not current.</span></span> <span data-ttu-id="23097-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="23097-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="23097-106">Descrive le caratteristiche di confronto dell'output.</span><span class="sxs-lookup"><span data-stu-id="23097-106">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="23097-107">Tutte le pagine in ogni singolo documento vengono fascicolate.</span><span class="sxs-lookup"><span data-stu-id="23097-107">All pages in each individual document are collated.</span></span> <span data-ttu-id="23097-108">DocumentCollate e JobCollateAlldocuments si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="23097-108">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="23097-109">Il comportamento e l'implementazione di se vengono implementate entrambe o solo una di queste parole chiave vengono lasciati al driver.</span><span class="sxs-lookup"><span data-stu-id="23097-109">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="23097-110">Di seguito sono riportate le regole da seguire per l'implementazione di Collate</span><span class="sxs-lookup"><span data-stu-id="23097-110">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="23097-111">Definizione e regole degli elementi</span><span class="sxs-lookup"><span data-stu-id="23097-111">Element Definition and Rules</span></span>

<span data-ttu-id="23097-112">È prima necessario seguire le regole per JobCollateAllDocument e quindi applicare le regole per DocumentCollate per il funzionamento degli scenari.</span><span class="sxs-lookup"><span data-stu-id="23097-112">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="23097-113">Si noti che in un'impostazione di conversione da PrintTicket a Devmode, in cui JobCollateAllDocuments non è supportato dal driver, è compito del driver scegliere il comportamento appropriato da adottare (JobCollateAllDocuments = ON o OFF).</span><span class="sxs-lookup"><span data-stu-id="23097-113">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="23097-114">Inoltre, la scelta può essere modificata a seconda delle altre impostazioni di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="23097-114">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="23097-115">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="23097-115">JobCollateAllDocuments</span></span>

<span data-ttu-id="23097-116">ON: stampare copie (DocumentCopiesAllPages) di ogni documento, ripetere JobCopiesAllDocuments volte.</span><span class="sxs-lookup"><span data-stu-id="23097-116">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="23097-117">OFF: per ogni documento, la stampa (JobCopiesAllDocuments x DocumentCopiesAllPages) viene copiata insieme.</span><span class="sxs-lookup"><span data-stu-id="23097-117">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="23097-118">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="23097-118">DocumentCollate</span></span>

<span data-ttu-id="23097-119">ON: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di un documento stampato in modo contiguo, fascicolare i fogli in tale documento.</span><span class="sxs-lookup"><span data-stu-id="23097-119">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="23097-120">OFF: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) stampate in modo contiguo, stampare tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di ogni foglio insieme.</span><span class="sxs-lookup"><span data-stu-id="23097-120">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="23097-121">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="23097-121">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="23097-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="23097-122">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="23097-123">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="23097-123">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="23097-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="23097-124">Element Information</span></span>



| <span data-ttu-id="23097-125">Nome</span><span class="sxs-lookup"><span data-stu-id="23097-125">Name</span></span> | <span data-ttu-id="23097-126">Valore</span><span class="sxs-lookup"><span data-stu-id="23097-126">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="23097-127">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="23097-127">Element Type</span></span> <br/>   | <span data-ttu-id="23097-128">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="23097-128">Feature</span></span><br/>  |
| <span data-ttu-id="23097-129">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="23097-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="23097-130">Documento</span><span class="sxs-lookup"><span data-stu-id="23097-130">Document</span></span><br/> |
| <span data-ttu-id="23097-131">Note</span><span class="sxs-lookup"><span data-stu-id="23097-131">Notes</span></span> <br/>          | <span data-ttu-id="23097-132">nessuno</span><span class="sxs-lookup"><span data-stu-id="23097-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="23097-133">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="23097-133">Structural Content</span></span>

<span data-ttu-id="23097-134">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="23097-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="23097-135">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="23097-135">Structure Variables</span></span>

<span data-ttu-id="23097-136">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="23097-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="23097-137">Nome</span><span class="sxs-lookup"><span data-stu-id="23097-137">Name</span></span>                               | <span data-ttu-id="23097-138">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="23097-138">Data type</span></span>         | <span data-ttu-id="23097-139">Unità</span><span class="sxs-lookup"><span data-stu-id="23097-139">Unit</span></span>                  | <span data-ttu-id="23097-140">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="23097-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="23097-141">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="23097-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="23097-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="23097-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="23097-143">string</span><span class="sxs-lookup"><span data-stu-id="23097-143">string</span></span><br/> | <span data-ttu-id="23097-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="23097-144">characters</span></span><br/> | <span data-ttu-id="23097-145">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="23097-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="23097-146">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="23097-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="23097-147">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="23097-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="23097-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="23097-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="23097-149">string</span><span class="sxs-lookup"><span data-stu-id="23097-149">string</span></span><br/> | <span data-ttu-id="23097-150">n/d</span><span class="sxs-lookup"><span data-stu-id="23097-150">n/a</span></span><br/>        | <span data-ttu-id="23097-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="23097-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="23097-152">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="23097-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="23097-153">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="23097-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="23097-154">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi .</span><span class="sxs-lookup"><span data-stu-id="23097-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="23097-155">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="23097-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="23097-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23097-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23097-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="23097-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




