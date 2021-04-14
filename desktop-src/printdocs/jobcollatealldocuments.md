---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0406a5f9106cbe4cd2a8ccb0986a1bfacc95b916
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351911"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="d1ed6-104">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="d1ed6-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="d1ed6-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-105">This topic is not current.</span></span> <span data-ttu-id="d1ed6-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d1ed6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d1ed6-107">Descrive le caratteristiche di ordinamento dell'output.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="d1ed6-108">Tutti i documenti in ogni singolo processo vengono sottoposti a confronto.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="d1ed6-109">DocumentCollate e JobCollateAlldocuments si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="d1ed6-110">Il comportamento e l'implementazione di se viene implementata una o solo una di queste parole chiave viene lasciata al driver.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="d1ed6-111">Di seguito sono riportate le regole che devono essere seguite per l'implementazione delle regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="d1ed6-112">Definizione e regole degli elementi</span><span class="sxs-lookup"><span data-stu-id="d1ed6-112">Element Definition and Rules</span></span>

<span data-ttu-id="d1ed6-113">È necessario innanzitutto seguire le regole per JobCollateAllDocument e quindi applicare le regole per DocumentCollate in modo che gli scenari funzionino.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="d1ed6-114">Si noti che in un'impostazione di conversione da PrintTicket a DEVMODE, in cui JobCollateAllDocuments non è supportato dal driver, spetta al driver scegliere il comportamento appropriato da eseguire (JobCollateAllDocuments = ON o OFF).</span><span class="sxs-lookup"><span data-stu-id="d1ed6-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="d1ed6-115">Inoltre, è possibile modificare la scelta a seconda delle altre impostazioni di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="d1ed6-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="d1ed6-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="d1ed6-117">ON: Print (DocumentCopiesAllPages) copia di ogni documento, ripete JobCopiesAllDocuments volte.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="d1ed6-118">DISATTIVATO: per ogni documento, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia insieme.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="d1ed6-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="d1ed6-119">DocumentCollate</span></span>

<span data-ttu-id="d1ed6-120">ON: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di un documento stampato in modo contiguo, fascicola i fogli del documento.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="d1ed6-121">DISATTIVATO: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) stampate in modo contiguo, stampa tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di ogni foglio.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="d1ed6-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d1ed6-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d1ed6-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d1ed6-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d1ed6-124">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d1ed6-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="d1ed6-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d1ed6-125">Element Information</span></span>



| <span data-ttu-id="d1ed6-126">Nome</span><span class="sxs-lookup"><span data-stu-id="d1ed6-126">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="d1ed6-127">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d1ed6-127">Element Type</span></span> <br/>   | <span data-ttu-id="d1ed6-128">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="d1ed6-128">Feature</span></span><br/> |
| <span data-ttu-id="d1ed6-129">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="d1ed6-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d1ed6-130">Processo</span><span class="sxs-lookup"><span data-stu-id="d1ed6-130">Job</span></span><br/>     |
| <span data-ttu-id="d1ed6-131">Note</span><span class="sxs-lookup"><span data-stu-id="d1ed6-131">Notes</span></span> <br/>          | <span data-ttu-id="d1ed6-132">nessuno</span><span class="sxs-lookup"><span data-stu-id="d1ed6-132">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="d1ed6-133">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d1ed6-133">Structural Content</span></span>

<span data-ttu-id="d1ed6-134">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="d1ed6-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a><span data-ttu-id="d1ed6-135">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="d1ed6-135">Structure Variables</span></span>

<span data-ttu-id="d1ed6-136">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d1ed6-137">Nome</span><span class="sxs-lookup"><span data-stu-id="d1ed6-137">Name</span></span>                               | <span data-ttu-id="d1ed6-138">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d1ed6-138">Data type</span></span>         | <span data-ttu-id="d1ed6-139">Unità</span><span class="sxs-lookup"><span data-stu-id="d1ed6-139">Unit</span></span>                  | <span data-ttu-id="d1ed6-140">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="d1ed6-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d1ed6-141">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="d1ed6-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d1ed6-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d1ed6-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d1ed6-143">string</span><span class="sxs-lookup"><span data-stu-id="d1ed6-143">string</span></span><br/> | <span data-ttu-id="d1ed6-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="d1ed6-144">characters</span></span><br/> | <span data-ttu-id="d1ed6-145">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d1ed6-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d1ed6-146">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d1ed6-147">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d1ed6-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d1ed6-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d1ed6-149">string</span><span class="sxs-lookup"><span data-stu-id="d1ed6-149">string</span></span><br/> | <span data-ttu-id="d1ed6-150">n/d</span><span class="sxs-lookup"><span data-stu-id="d1ed6-150">n/a</span></span><br/>        | <span data-ttu-id="d1ed6-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d1ed6-152">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d1ed6-153">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="d1ed6-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d1ed6-154">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d1ed6-155">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="d1ed6-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




