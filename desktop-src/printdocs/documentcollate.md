---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b022d9c8067f330e14697932382c4c8f058a8f3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321118"
---
# <a name="documentcollate"></a><span data-ttu-id="f4866-104">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="f4866-104">DocumentCollate</span></span>

<span data-ttu-id="f4866-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f4866-105">This topic is not current.</span></span> <span data-ttu-id="f4866-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f4866-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f4866-107">Descrive le caratteristiche di ordinamento dell'output.</span><span class="sxs-lookup"><span data-stu-id="f4866-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="f4866-108">Tutte le pagine di ogni singolo documento vengono confrontate.</span><span class="sxs-lookup"><span data-stu-id="f4866-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="f4866-109">DocumentCollate e JobCollateAlldocuments si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f4866-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="f4866-110">Il comportamento e l'implementazione di se viene implementata una o solo una di queste parole chiave viene lasciata al driver.</span><span class="sxs-lookup"><span data-stu-id="f4866-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="f4866-111">Di seguito sono riportate le regole che devono essere seguite per l'implementazione delle regole di confronto</span><span class="sxs-lookup"><span data-stu-id="f4866-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="f4866-112">Definizione e regole degli elementi</span><span class="sxs-lookup"><span data-stu-id="f4866-112">Element Definition and Rules</span></span>

<span data-ttu-id="f4866-113">È necessario innanzitutto seguire le regole per JobCollateAllDocument e quindi applicare le regole per DocumentCollate in modo che gli scenari funzionino.</span><span class="sxs-lookup"><span data-stu-id="f4866-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="f4866-114">Si noti che in un'impostazione di conversione da PrintTicket a DEVMODE, in cui JobCollateAllDocuments non è supportato dal driver, spetta al driver scegliere il comportamento appropriato da eseguire (JobCollateAllDocuments = ON o OFF).</span><span class="sxs-lookup"><span data-stu-id="f4866-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="f4866-115">Inoltre, è possibile modificare la scelta a seconda delle altre impostazioni di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="f4866-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="f4866-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="f4866-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="f4866-117">ON: Print (DocumentCopiesAllPages) copia di ogni documento, ripete JobCopiesAllDocuments volte.</span><span class="sxs-lookup"><span data-stu-id="f4866-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="f4866-118">DISATTIVATO: per ogni documento, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia insieme.</span><span class="sxs-lookup"><span data-stu-id="f4866-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="f4866-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="f4866-119">DocumentCollate</span></span>

<span data-ttu-id="f4866-120">ON: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di un documento stampato in modo contiguo, fascicola i fogli del documento.</span><span class="sxs-lookup"><span data-stu-id="f4866-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="f4866-121">DISATTIVATO: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) stampate in modo contiguo, stampa tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di ogni foglio.</span><span class="sxs-lookup"><span data-stu-id="f4866-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="f4866-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f4866-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="f4866-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f4866-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="f4866-124">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="f4866-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f4866-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f4866-125">Element Information</span></span>



| <span data-ttu-id="f4866-126">Nome</span><span class="sxs-lookup"><span data-stu-id="f4866-126">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="f4866-127">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f4866-127">Element Type</span></span> <br/>   | <span data-ttu-id="f4866-128">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="f4866-128">Feature</span></span><br/>  |
| <span data-ttu-id="f4866-129">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="f4866-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f4866-130">Documento</span><span class="sxs-lookup"><span data-stu-id="f4866-130">Document</span></span><br/> |
| <span data-ttu-id="f4866-131">Note</span><span class="sxs-lookup"><span data-stu-id="f4866-131">Notes</span></span> <br/>          | <span data-ttu-id="f4866-132">nessuno</span><span class="sxs-lookup"><span data-stu-id="f4866-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="f4866-133">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f4866-133">Structural Content</span></span>

<span data-ttu-id="f4866-134">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f4866-134">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f4866-135">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="f4866-135">Structure Variables</span></span>

<span data-ttu-id="f4866-136">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f4866-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f4866-137">Nome</span><span class="sxs-lookup"><span data-stu-id="f4866-137">Name</span></span>                               | <span data-ttu-id="f4866-138">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f4866-138">Data type</span></span>         | <span data-ttu-id="f4866-139">Unità</span><span class="sxs-lookup"><span data-stu-id="f4866-139">Unit</span></span>                  | <span data-ttu-id="f4866-140">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="f4866-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f4866-141">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f4866-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f4866-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f4866-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f4866-143">string</span><span class="sxs-lookup"><span data-stu-id="f4866-143">string</span></span><br/> | <span data-ttu-id="f4866-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="f4866-144">characters</span></span><br/> | <span data-ttu-id="f4866-145">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f4866-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f4866-146">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4866-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f4866-147">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="f4866-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f4866-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f4866-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f4866-149">string</span><span class="sxs-lookup"><span data-stu-id="f4866-149">string</span></span><br/> | <span data-ttu-id="f4866-150">n/d</span><span class="sxs-lookup"><span data-stu-id="f4866-150">n/a</span></span><br/>        | <span data-ttu-id="f4866-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="f4866-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f4866-152">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f4866-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f4866-153">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="f4866-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f4866-154">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f4866-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f4866-155">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="f4866-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f4866-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4866-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4866-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f4866-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




