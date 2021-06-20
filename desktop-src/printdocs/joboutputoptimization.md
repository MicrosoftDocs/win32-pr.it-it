---
description: Informazioni su JobOutputOptimization, che descrive l'elaborazione del processo, destinata a ottimizzare l'output per scenari di utilizzo specifici, come indicato dall'opzione specificata.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbb65f86b5ed4fd30c056e234b88197d4ab475d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408794"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="6fc95-103">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="6fc95-103">JobOutputOptimization</span></span>

<span data-ttu-id="6fc95-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6fc95-104">This topic is not current.</span></span> <span data-ttu-id="6fc95-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6fc95-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6fc95-106">Descrive l'elaborazione del processo, destinata a ottimizzare l'output per scenari di utilizzo specifici, come indicato dall'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="6fc95-106">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="6fc95-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fc95-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6fc95-108">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6fc95-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6fc95-109">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fc95-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6fc95-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fc95-110">Element Information</span></span>



| <span data-ttu-id="6fc95-111">Nome</span><span class="sxs-lookup"><span data-stu-id="6fc95-111">Name</span></span> | <span data-ttu-id="6fc95-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6fc95-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6fc95-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6fc95-113">Element Type</span></span> <br/>   | <span data-ttu-id="6fc95-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="6fc95-114">Feature</span></span><br/> |
| <span data-ttu-id="6fc95-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6fc95-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6fc95-116">Processo</span><span class="sxs-lookup"><span data-stu-id="6fc95-116">Job</span></span><br/>     |
| <span data-ttu-id="6fc95-117">Note</span><span class="sxs-lookup"><span data-stu-id="6fc95-117">Notes</span></span> <br/>          | <span data-ttu-id="6fc95-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="6fc95-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6fc95-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6fc95-119">Structural Content</span></span>

<span data-ttu-id="6fc95-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6fc95-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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

## <a name="structure-variables"></a><span data-ttu-id="6fc95-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6fc95-121">Structure Variables</span></span>

<span data-ttu-id="6fc95-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6fc95-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6fc95-123">Nome</span><span class="sxs-lookup"><span data-stu-id="6fc95-123">Name</span></span>                               | <span data-ttu-id="6fc95-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6fc95-124">Data type</span></span>         | <span data-ttu-id="6fc95-125">Unità</span><span class="sxs-lookup"><span data-stu-id="6fc95-125">Unit</span></span>                  | <span data-ttu-id="6fc95-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6fc95-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6fc95-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6fc95-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6fc95-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6fc95-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6fc95-129">string</span><span class="sxs-lookup"><span data-stu-id="6fc95-129">string</span></span><br/> | <span data-ttu-id="6fc95-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="6fc95-130">characters</span></span><br/> | <span data-ttu-id="6fc95-131">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6fc95-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6fc95-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6fc95-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6fc95-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6fc95-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6fc95-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6fc95-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6fc95-135">string</span><span class="sxs-lookup"><span data-stu-id="6fc95-135">string</span></span><br/> | <span data-ttu-id="6fc95-136">n/d</span><span class="sxs-lookup"><span data-stu-id="6fc95-136">n/a</span></span><br/>        | <span data-ttu-id="6fc95-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="6fc95-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6fc95-138">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6fc95-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6fc95-139">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fc95-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6fc95-140">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="6fc95-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6fc95-141">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6fc95-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="6fc95-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fc95-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fc95-143">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6fc95-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




