---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76364aca1a9b6c8019a709c1cd0b7b1ad03020c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997748"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="22db5-104">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="22db5-104">JobOutputOptimization</span></span>

<span data-ttu-id="22db5-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="22db5-105">This topic is not current.</span></span> <span data-ttu-id="22db5-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="22db5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22db5-107">Descrive l'elaborazione del processo, progettata per ottimizzare l'output per scenari di utilizzo specifici, come indicato dall'opzione specificata.</span><span class="sxs-lookup"><span data-stu-id="22db5-107">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="22db5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22db5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22db5-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="22db5-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="22db5-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="22db5-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="22db5-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22db5-111">Element Information</span></span>



| <span data-ttu-id="22db5-112">Nome</span><span class="sxs-lookup"><span data-stu-id="22db5-112">Name</span></span> | <span data-ttu-id="22db5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="22db5-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="22db5-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="22db5-114">Element Type</span></span> <br/>   | <span data-ttu-id="22db5-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="22db5-115">Feature</span></span><br/> |
| <span data-ttu-id="22db5-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="22db5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22db5-117">Processo</span><span class="sxs-lookup"><span data-stu-id="22db5-117">Job</span></span><br/>     |
| <span data-ttu-id="22db5-118">Note</span><span class="sxs-lookup"><span data-stu-id="22db5-118">Notes</span></span> <br/>          | <span data-ttu-id="22db5-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="22db5-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="22db5-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="22db5-120">Structural Content</span></span>

<span data-ttu-id="22db5-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="22db5-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="22db5-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="22db5-122">Structure Variables</span></span>

<span data-ttu-id="22db5-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="22db5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22db5-124">Nome</span><span class="sxs-lookup"><span data-stu-id="22db5-124">Name</span></span>                               | <span data-ttu-id="22db5-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="22db5-125">Data type</span></span>         | <span data-ttu-id="22db5-126">Unità</span><span class="sxs-lookup"><span data-stu-id="22db5-126">Unit</span></span>                  | <span data-ttu-id="22db5-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="22db5-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="22db5-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="22db5-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="22db5-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="22db5-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="22db5-130">string</span><span class="sxs-lookup"><span data-stu-id="22db5-130">string</span></span><br/> | <span data-ttu-id="22db5-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="22db5-131">characters</span></span><br/> | <span data-ttu-id="22db5-132">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="22db5-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="22db5-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="22db5-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="22db5-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="22db5-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="22db5-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="22db5-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="22db5-136">string</span><span class="sxs-lookup"><span data-stu-id="22db5-136">string</span></span><br/> | <span data-ttu-id="22db5-137">n/d</span><span class="sxs-lookup"><span data-stu-id="22db5-137">n/a</span></span><br/>        | <span data-ttu-id="22db5-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="22db5-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="22db5-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="22db5-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="22db5-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="22db5-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="22db5-141">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="22db5-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="22db5-142">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="22db5-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="22db5-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22db5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22db5-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="22db5-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




