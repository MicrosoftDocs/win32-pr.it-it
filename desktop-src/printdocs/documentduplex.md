---
description: Informazioni sull'elemento DocumentDuplex, che descrive le caratteristiche duplex dell'output. La funzionalità duplex consente la stampa su entrambi i lati del supporto.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ad8521835213594f10507ab6fd4b9cca24040
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409344"
---
# <a name="documentduplex"></a><span data-ttu-id="58af2-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="58af2-104">DocumentDuplex</span></span>

<span data-ttu-id="58af2-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="58af2-105">This topic is not current.</span></span> <span data-ttu-id="58af2-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="58af2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58af2-107">Descrive le caratteristiche duplex dell'output.</span><span class="sxs-lookup"><span data-stu-id="58af2-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="58af2-108">La funzionalità duplex consente la stampa su entrambi i lati del supporto.</span><span class="sxs-lookup"><span data-stu-id="58af2-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="58af2-109">Ogni documento viene duplexato separatamente.</span><span class="sxs-lookup"><span data-stu-id="58af2-109">Each document is duplexed separately.</span></span> <span data-ttu-id="58af2-110">DocumentDuplex e JobDuplexAllDocumentsContiguously si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="58af2-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="58af2-111">È responsabilità del driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="58af2-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="58af2-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="58af2-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="58af2-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="58af2-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="58af2-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="58af2-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="58af2-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="58af2-115">Element Information</span></span>



| <span data-ttu-id="58af2-116">Nome</span><span class="sxs-lookup"><span data-stu-id="58af2-116">Name</span></span> | <span data-ttu-id="58af2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="58af2-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="58af2-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="58af2-118">Element Type</span></span> <br/>   | <span data-ttu-id="58af2-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="58af2-119">Feature</span></span><br/>  |
| <span data-ttu-id="58af2-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="58af2-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="58af2-121">Documento</span><span class="sxs-lookup"><span data-stu-id="58af2-121">Document</span></span><br/> |
| <span data-ttu-id="58af2-122">Note</span><span class="sxs-lookup"><span data-stu-id="58af2-122">Notes</span></span> <br/>          | <span data-ttu-id="58af2-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="58af2-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="58af2-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="58af2-124">Structural Content</span></span>

<span data-ttu-id="58af2-125">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="58af2-125">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
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

## <a name="structure-variables"></a><span data-ttu-id="58af2-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="58af2-126">Structure Variables</span></span>

<span data-ttu-id="58af2-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="58af2-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="58af2-128">Nome</span><span class="sxs-lookup"><span data-stu-id="58af2-128">Name</span></span>                               | <span data-ttu-id="58af2-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="58af2-129">Data type</span></span>         | <span data-ttu-id="58af2-130">Unità</span><span class="sxs-lookup"><span data-stu-id="58af2-130">Unit</span></span>                  | <span data-ttu-id="58af2-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="58af2-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="58af2-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="58af2-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58af2-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="58af2-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="58af2-134">string</span><span class="sxs-lookup"><span data-stu-id="58af2-134">string</span></span><br/> | <span data-ttu-id="58af2-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="58af2-135">characters</span></span><br/> | <span data-ttu-id="58af2-136">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="58af2-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="58af2-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="58af2-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="58af2-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="58af2-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="58af2-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="58af2-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="58af2-140">string</span><span class="sxs-lookup"><span data-stu-id="58af2-140">string</span></span><br/> | <span data-ttu-id="58af2-141">n/d</span><span class="sxs-lookup"><span data-stu-id="58af2-141">n/a</span></span><br/>        | <span data-ttu-id="58af2-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="58af2-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="58af2-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="58af2-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="58af2-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="58af2-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="58af2-145">string</span><span class="sxs-lookup"><span data-stu-id="58af2-145">string</span></span><br/> | <span data-ttu-id="58af2-146">n/d</span><span class="sxs-lookup"><span data-stu-id="58af2-146">n/a</span></span><br/>        | <span data-ttu-id="58af2-147">Automatico, Manuale.</span><span class="sxs-lookup"><span data-stu-id="58af2-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="58af2-148">Definisce la modalità duplex.</span><span class="sxs-lookup"><span data-stu-id="58af2-148">Defines the duplex mode.</span></span> <span data-ttu-id="58af2-149">Il duplex automatico viene eseguito dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="58af2-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="58af2-150">Il duplex manuale viene eseguito dal software e dall'utente.</span><span class="sxs-lookup"><span data-stu-id="58af2-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="58af2-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="58af2-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="58af2-152">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="58af2-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="58af2-153">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="58af2-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
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

## <a name="related-topics"></a><span data-ttu-id="58af2-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58af2-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58af2-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="58af2-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




