---
description: Informazioni sull'elemento JobAccountingSheet, che descrive il foglio contabilità da visualizzare come output per il processo.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499d78db7a967e256ee79cd6e0c35d2f7d59dff4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409095"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="f58b9-103">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="f58b9-103">JobAccountingSheet</span></span>

<span data-ttu-id="f58b9-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f58b9-104">This topic is not current.</span></span> <span data-ttu-id="f58b9-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f58b9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f58b9-106">Descrive la scheda contabilità da visualizzare come output per il processo.</span><span class="sxs-lookup"><span data-stu-id="f58b9-106">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="f58b9-107">L'output del foglio contabilità deve essere quello predefinito pageMediaSize e l'uso del valore predefinito PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="f58b9-107">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="f58b9-108">La contabilità deve essere isolata dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="f58b9-108">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="f58b9-109">Ciò significa che qualsiasi opzione di completamento o elaborazione (ad esempio JobDuplex, JobStaple o JobBinding) non deve includere la contabilità.</span><span class="sxs-lookup"><span data-stu-id="f58b9-109">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="f58b9-110">La contabilità può essere la prima o l'ultima pagina del processo a discrezione dell'implementatore.</span><span class="sxs-lookup"><span data-stu-id="f58b9-110">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="f58b9-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f58b9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f58b9-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f58b9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f58b9-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f58b9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f58b9-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f58b9-114">Element Information</span></span>



| <span data-ttu-id="f58b9-115">Nome</span><span class="sxs-lookup"><span data-stu-id="f58b9-115">Name</span></span> | <span data-ttu-id="f58b9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f58b9-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f58b9-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f58b9-117">Element Type</span></span> <br/>   | <span data-ttu-id="f58b9-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="f58b9-118">Feature</span></span><br/> |
| <span data-ttu-id="f58b9-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f58b9-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f58b9-120">Processo</span><span class="sxs-lookup"><span data-stu-id="f58b9-120">Job</span></span><br/>     |
| <span data-ttu-id="f58b9-121">Note</span><span class="sxs-lookup"><span data-stu-id="f58b9-121">Notes</span></span> <br/>          | <span data-ttu-id="f58b9-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="f58b9-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f58b9-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f58b9-123">Structural Content</span></span>

<span data-ttu-id="f58b9-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f58b9-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="f58b9-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="f58b9-125">Structure Variables</span></span>

<span data-ttu-id="f58b9-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f58b9-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f58b9-127">Nome</span><span class="sxs-lookup"><span data-stu-id="f58b9-127">Name</span></span>                               | <span data-ttu-id="f58b9-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f58b9-128">Data type</span></span>         | <span data-ttu-id="f58b9-129">Unità</span><span class="sxs-lookup"><span data-stu-id="f58b9-129">Unit</span></span>                  | <span data-ttu-id="f58b9-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="f58b9-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f58b9-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f58b9-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f58b9-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f58b9-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f58b9-133">string</span><span class="sxs-lookup"><span data-stu-id="f58b9-133">string</span></span><br/> | <span data-ttu-id="f58b9-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="f58b9-134">characters</span></span><br/> | <span data-ttu-id="f58b9-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f58b9-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f58b9-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="f58b9-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f58b9-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="f58b9-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f58b9-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f58b9-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f58b9-139">string</span><span class="sxs-lookup"><span data-stu-id="f58b9-139">string</span></span><br/> | <span data-ttu-id="f58b9-140">n/d</span><span class="sxs-lookup"><span data-stu-id="f58b9-140">n/a</span></span><br/>        | <span data-ttu-id="f58b9-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="f58b9-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f58b9-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f58b9-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f58b9-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f58b9-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f58b9-144">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="f58b9-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f58b9-145">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="f58b9-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="f58b9-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f58b9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f58b9-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f58b9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




