---
description: Informazioni sull'elemento JobDuplexAllDocumentsContiguously, che descrive le caratteristiche duplex dell'output.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a8911a4c62644bfc073a2a9c1dcfd67dad536a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408954"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="a7099-103">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="a7099-103">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="a7099-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a7099-104">This topic is not current.</span></span> <span data-ttu-id="a7099-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7099-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a7099-106">Descrive le caratteristiche duplex dell'output.</span><span class="sxs-lookup"><span data-stu-id="a7099-106">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="a7099-107">La funzionalità duplex consente la stampa su entrambi i lati del supporto.</span><span class="sxs-lookup"><span data-stu-id="a7099-107">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="a7099-108">Tutti i documenti nel processo vengono duplex in modo contiguo.</span><span class="sxs-lookup"><span data-stu-id="a7099-108">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="a7099-109">JobDuplexAllDocumentsContiguously e DocumentDuplex si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="a7099-109">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="a7099-110">È responsabilità del driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="a7099-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="a7099-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a7099-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a7099-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a7099-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a7099-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a7099-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a7099-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a7099-114">Element Information</span></span>



| <span data-ttu-id="a7099-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a7099-115">Name</span></span> | <span data-ttu-id="a7099-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a7099-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a7099-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a7099-117">Element Type</span></span> <br/>   | <span data-ttu-id="a7099-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="a7099-118">Feature</span></span><br/> |
| <span data-ttu-id="a7099-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a7099-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a7099-120">Processo</span><span class="sxs-lookup"><span data-stu-id="a7099-120">Job</span></span><br/>     |
| <span data-ttu-id="a7099-121">Note</span><span class="sxs-lookup"><span data-stu-id="a7099-121">Notes</span></span> <br/>          | <span data-ttu-id="a7099-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="a7099-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a7099-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a7099-123">Structural Content</span></span>

<span data-ttu-id="a7099-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="a7099-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a7099-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="a7099-125">Structure Variables</span></span>

<span data-ttu-id="a7099-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a7099-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a7099-127">Nome</span><span class="sxs-lookup"><span data-stu-id="a7099-127">Name</span></span>                               | <span data-ttu-id="a7099-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a7099-128">Data type</span></span>         | <span data-ttu-id="a7099-129">Unità</span><span class="sxs-lookup"><span data-stu-id="a7099-129">Unit</span></span>                  | <span data-ttu-id="a7099-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="a7099-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="a7099-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a7099-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7099-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a7099-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a7099-133">string</span><span class="sxs-lookup"><span data-stu-id="a7099-133">string</span></span><br/> | <span data-ttu-id="a7099-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="a7099-134">characters</span></span><br/> | <span data-ttu-id="a7099-135">Nome completo valido come definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="a7099-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="a7099-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a7099-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a7099-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="a7099-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="a7099-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a7099-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a7099-139">string</span><span class="sxs-lookup"><span data-stu-id="a7099-139">string</span></span><br/> | <span data-ttu-id="a7099-140">n/d</span><span class="sxs-lookup"><span data-stu-id="a7099-140">n/a</span></span><br/>        | <span data-ttu-id="a7099-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="a7099-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="a7099-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a7099-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="a7099-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="a7099-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="a7099-144">string</span><span class="sxs-lookup"><span data-stu-id="a7099-144">string</span></span><br/> | <span data-ttu-id="a7099-145">n/d</span><span class="sxs-lookup"><span data-stu-id="a7099-145">n/a</span></span><br/>        | <span data-ttu-id="a7099-146">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="a7099-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="a7099-147">Definisce la modalità duplex.</span><span class="sxs-lookup"><span data-stu-id="a7099-147">Defines the duplex mode.</span></span> <span data-ttu-id="a7099-148">Il duplex automatico viene eseguito dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="a7099-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="a7099-149">Il duplex manuale viene eseguito dal software e dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a7099-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a7099-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a7099-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a7099-151">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="a7099-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a7099-152">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="a7099-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a7099-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7099-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7099-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a7099-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




