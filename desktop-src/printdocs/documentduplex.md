---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234607"
---
# <a name="documentduplex"></a><span data-ttu-id="b5ab0-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="b5ab0-104">DocumentDuplex</span></span>

<span data-ttu-id="b5ab0-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-105">This topic is not current.</span></span> <span data-ttu-id="b5ab0-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b5ab0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b5ab0-107">Descrive le caratteristiche duplex dell'output.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="b5ab0-108">La funzionalità duplex consente la stampa su entrambi i lati del supporto.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="b5ab0-109">Ogni documento è duplexed separatamente.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-109">Each document is duplexed separately.</span></span> <span data-ttu-id="b5ab0-110">DocumentDuplex e JobDuplexAllDocumentsContiguously si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="b5ab0-111">Spetta al driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="b5ab0-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b5ab0-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b5ab0-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b5ab0-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b5ab0-114">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b5ab0-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b5ab0-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b5ab0-115">Element Information</span></span>



| <span data-ttu-id="b5ab0-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b5ab0-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="b5ab0-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b5ab0-117">Element Type</span></span> <br/>   | <span data-ttu-id="b5ab0-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="b5ab0-118">Feature</span></span><br/>  |
| <span data-ttu-id="b5ab0-119">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="b5ab0-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b5ab0-120">Documento</span><span class="sxs-lookup"><span data-stu-id="b5ab0-120">Document</span></span><br/> |
| <span data-ttu-id="b5ab0-121">Note</span><span class="sxs-lookup"><span data-stu-id="b5ab0-121">Notes</span></span> <br/>          | <span data-ttu-id="b5ab0-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="b5ab0-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b5ab0-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b5ab0-123">Structural Content</span></span>

<span data-ttu-id="b5ab0-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b5ab0-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b5ab0-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="b5ab0-125">Structure Variables</span></span>

<span data-ttu-id="b5ab0-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b5ab0-127">Nome</span><span class="sxs-lookup"><span data-stu-id="b5ab0-127">Name</span></span>                               | <span data-ttu-id="b5ab0-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b5ab0-128">Data type</span></span>         | <span data-ttu-id="b5ab0-129">Unità</span><span class="sxs-lookup"><span data-stu-id="b5ab0-129">Unit</span></span>                  | <span data-ttu-id="b5ab0-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="b5ab0-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b5ab0-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="b5ab0-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ab0-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b5ab0-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b5ab0-133">string</span><span class="sxs-lookup"><span data-stu-id="b5ab0-133">string</span></span><br/> | <span data-ttu-id="b5ab0-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="b5ab0-134">characters</span></span><br/> | <span data-ttu-id="b5ab0-135">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b5ab0-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b5ab0-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b5ab0-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="b5ab0-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b5ab0-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b5ab0-139">string</span><span class="sxs-lookup"><span data-stu-id="b5ab0-139">string</span></span><br/> | <span data-ttu-id="b5ab0-140">n/d</span><span class="sxs-lookup"><span data-stu-id="b5ab0-140">n/a</span></span><br/>        | <span data-ttu-id="b5ab0-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b5ab0-142">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="b5ab0-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="b5ab0-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="b5ab0-144">string</span><span class="sxs-lookup"><span data-stu-id="b5ab0-144">string</span></span><br/> | <span data-ttu-id="b5ab0-145">n/d</span><span class="sxs-lookup"><span data-stu-id="b5ab0-145">n/a</span></span><br/>        | <span data-ttu-id="b5ab0-146">Automatico, manuale.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="b5ab0-147">Definisce la modalità duplex.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-147">Defines the duplex mode.</span></span> <span data-ttu-id="b5ab0-148">Il duplex automatico viene eseguito dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="b5ab0-149">Il duplexing manuale viene eseguito dal software e dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b5ab0-150">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b5ab0-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b5ab0-151">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b5ab0-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b5ab0-152">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="b5ab0-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b5ab0-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5ab0-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ab0-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b5ab0-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




