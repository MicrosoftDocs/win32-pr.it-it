---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959613299c53996ce7d66171d2da1518f28b9298
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993998"
---
# <a name="documentcollate"></a><span data-ttu-id="5a5d4-104">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="5a5d4-104">DocumentCollate</span></span>

<span data-ttu-id="5a5d4-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-105">This topic is not current.</span></span> <span data-ttu-id="5a5d4-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a5d4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a5d4-107">Descrive le caratteristiche di confronto dell'output.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="5a5d4-108">Tutte le pagine in ogni singolo documento vengono fascicolate.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="5a5d4-109">DocumentCollate e JobCollateAlldocuments si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="5a5d4-110">Il comportamento e l'implementazione di se vengono implementate entrambe o solo una di queste parole chiave vengono lasciati al driver.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="5a5d4-111">Di seguito sono riportate le regole da seguire per l'implementazione di Collate</span><span class="sxs-lookup"><span data-stu-id="5a5d4-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="5a5d4-112">Definizione e regole degli elementi</span><span class="sxs-lookup"><span data-stu-id="5a5d4-112">Element Definition and Rules</span></span>

<span data-ttu-id="5a5d4-113">È prima necessario seguire le regole per JobCollateAllDocument e quindi applicare le regole per DocumentCollate per il funzionamento degli scenari.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="5a5d4-114">Si noti che in un'impostazione di conversione da PrintTicket a Devmode, in cui JobCollateAllDocuments non è supportato dal driver, è compito del driver scegliere il comportamento appropriato da adottare (JobCollateAllDocuments = ON o OFF).</span><span class="sxs-lookup"><span data-stu-id="5a5d4-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="5a5d4-115">Inoltre, la scelta può essere modificata a seconda delle altre impostazioni di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="5a5d4-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="5a5d4-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="5a5d4-117">ON: stampare copie (DocumentCopiesAllPages) di ogni documento, ripetere JobCopiesAllDocuments volte.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="5a5d4-118">OFF: per ogni documento, la stampa (JobCopiesAllDocuments x DocumentCopiesAllPages) viene copiata insieme.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="5a5d4-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="5a5d4-119">DocumentCollate</span></span>

<span data-ttu-id="5a5d4-120">ON: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di un documento stampato in modo contiguo, fascicolare i fogli in tale documento.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="5a5d4-121">OFF: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) stampate in modo contiguo, stampare tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di ogni foglio insieme.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="5a5d4-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5a5d4-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="5a5d4-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5a5d4-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="5a5d4-124">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="5a5d4-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5a5d4-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5a5d4-125">Element Information</span></span>



| <span data-ttu-id="5a5d4-126">Nome</span><span class="sxs-lookup"><span data-stu-id="5a5d4-126">Name</span></span> | <span data-ttu-id="5a5d4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5a5d4-127">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="5a5d4-128">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5a5d4-128">Element Type</span></span> <br/>   | <span data-ttu-id="5a5d4-129">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="5a5d4-129">Feature</span></span><br/>  |
| <span data-ttu-id="5a5d4-130">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5a5d4-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a5d4-131">Documento</span><span class="sxs-lookup"><span data-stu-id="5a5d4-131">Document</span></span><br/> |
| <span data-ttu-id="5a5d4-132">Note</span><span class="sxs-lookup"><span data-stu-id="5a5d4-132">Notes</span></span> <br/>          | <span data-ttu-id="5a5d4-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="5a5d4-133">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="5a5d4-134">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5a5d4-134">Structural Content</span></span>

<span data-ttu-id="5a5d4-135">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5a5d4-135">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5a5d4-136">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="5a5d4-136">Structure Variables</span></span>

<span data-ttu-id="5a5d4-137">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a5d4-138">Nome</span><span class="sxs-lookup"><span data-stu-id="5a5d4-138">Name</span></span>                               | <span data-ttu-id="5a5d4-139">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5a5d4-139">Data type</span></span>         | <span data-ttu-id="5a5d4-140">Unità</span><span class="sxs-lookup"><span data-stu-id="5a5d4-140">Unit</span></span>                  | <span data-ttu-id="5a5d4-141">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="5a5d4-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5a5d4-142">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5a5d4-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5a5d4-143">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5a5d4-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5a5d4-144">string</span><span class="sxs-lookup"><span data-stu-id="5a5d4-144">string</span></span><br/> | <span data-ttu-id="5a5d4-145">caratteri</span><span class="sxs-lookup"><span data-stu-id="5a5d4-145">characters</span></span><br/> | <span data-ttu-id="5a5d4-146">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5a5d4-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5a5d4-147">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5a5d4-148">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5a5d4-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5a5d4-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5a5d4-150">string</span><span class="sxs-lookup"><span data-stu-id="5a5d4-150">string</span></span><br/> | <span data-ttu-id="5a5d4-151">n/d</span><span class="sxs-lookup"><span data-stu-id="5a5d4-151">n/a</span></span><br/>        | <span data-ttu-id="5a5d4-152">True, False.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5a5d4-153">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5a5d4-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5a5d4-154">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5a5d4-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5a5d4-155">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="5a5d4-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5a5d4-156">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="5a5d4-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5a5d4-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a5d4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a5d4-158">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5a5d4-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




