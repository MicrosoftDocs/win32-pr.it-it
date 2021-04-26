---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e5ae88213af15b53f71e406b4caf791b80f286f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998218"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="36bcc-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="36bcc-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="36bcc-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="36bcc-105">This topic is not current.</span></span> <span data-ttu-id="36bcc-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="36bcc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="36bcc-107">Descrive le caratteristiche duplex dell'output.</span><span class="sxs-lookup"><span data-stu-id="36bcc-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="36bcc-108">La funzionalità duplex consente la stampa su entrambi i lati del supporto.</span><span class="sxs-lookup"><span data-stu-id="36bcc-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="36bcc-109">Tutti i documenti nel processo sono duplex in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="36bcc-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="36bcc-110">JobDuplexAllDocumentsContiguously e DocumentDuplex si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="36bcc-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="36bcc-111">Il driver deve determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="36bcc-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="36bcc-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="36bcc-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="36bcc-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="36bcc-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="36bcc-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="36bcc-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="36bcc-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="36bcc-115">Element Information</span></span>



| <span data-ttu-id="36bcc-116">Nome</span><span class="sxs-lookup"><span data-stu-id="36bcc-116">Name</span></span> | <span data-ttu-id="36bcc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="36bcc-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="36bcc-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="36bcc-118">Element Type</span></span> <br/>   | <span data-ttu-id="36bcc-119">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="36bcc-119">Feature</span></span><br/> |
| <span data-ttu-id="36bcc-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="36bcc-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="36bcc-121">Processo</span><span class="sxs-lookup"><span data-stu-id="36bcc-121">Job</span></span><br/>     |
| <span data-ttu-id="36bcc-122">Note</span><span class="sxs-lookup"><span data-stu-id="36bcc-122">Notes</span></span> <br/>          | <span data-ttu-id="36bcc-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="36bcc-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="36bcc-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="36bcc-124">Structural Content</span></span>

<span data-ttu-id="36bcc-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="36bcc-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="36bcc-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="36bcc-126">Structure Variables</span></span>

<span data-ttu-id="36bcc-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="36bcc-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="36bcc-128">Nome</span><span class="sxs-lookup"><span data-stu-id="36bcc-128">Name</span></span>                               | <span data-ttu-id="36bcc-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="36bcc-129">Data type</span></span>         | <span data-ttu-id="36bcc-130">Unità</span><span class="sxs-lookup"><span data-stu-id="36bcc-130">Unit</span></span>                  | <span data-ttu-id="36bcc-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="36bcc-131">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="36bcc-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="36bcc-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bcc-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="36bcc-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="36bcc-134">string</span><span class="sxs-lookup"><span data-stu-id="36bcc-134">string</span></span><br/> | <span data-ttu-id="36bcc-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="36bcc-135">characters</span></span><br/> | <span data-ttu-id="36bcc-136">Nome completo valido come definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="36bcc-136">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="36bcc-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="36bcc-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="36bcc-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="36bcc-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="36bcc-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="36bcc-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="36bcc-140">string</span><span class="sxs-lookup"><span data-stu-id="36bcc-140">string</span></span><br/> | <span data-ttu-id="36bcc-141">n/d</span><span class="sxs-lookup"><span data-stu-id="36bcc-141">n/a</span></span><br/>        | <span data-ttu-id="36bcc-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="36bcc-142">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="36bcc-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="36bcc-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="36bcc-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="36bcc-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="36bcc-145">string</span><span class="sxs-lookup"><span data-stu-id="36bcc-145">string</span></span><br/> | <span data-ttu-id="36bcc-146">n/d</span><span class="sxs-lookup"><span data-stu-id="36bcc-146">n/a</span></span><br/>        | <span data-ttu-id="36bcc-147">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="36bcc-147">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="36bcc-148">Definisce la modalità duplex.</span><span class="sxs-lookup"><span data-stu-id="36bcc-148">Defines the duplex mode.</span></span> <span data-ttu-id="36bcc-149">Il duplex automatico viene eseguito dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="36bcc-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="36bcc-150">Il duplex manuale viene eseguito dal software e dall'utente.</span><span class="sxs-lookup"><span data-stu-id="36bcc-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="36bcc-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="36bcc-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="36bcc-152">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="36bcc-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="36bcc-153">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="36bcc-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="36bcc-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36bcc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bcc-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="36bcc-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




