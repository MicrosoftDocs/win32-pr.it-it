---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998428"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="13e5e-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="13e5e-104">JobAccountingSheet</span></span>

<span data-ttu-id="13e5e-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="13e5e-105">This topic is not current.</span></span> <span data-ttu-id="13e5e-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="13e5e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="13e5e-107">Descrive la scheda contabilità da visualizzare come output per il processo.</span><span class="sxs-lookup"><span data-stu-id="13e5e-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="13e5e-108">L'output del foglio contabilità deve essere quello predefinito pageMediaSize e l'uso del valore predefinito PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="13e5e-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="13e5e-109">La contabilità deve essere isolata dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="13e5e-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="13e5e-110">Ciò significa che qualsiasi opzione di completamento o elaborazione (ad esempio JobDuplex, JobStaple o JobBinding) non deve includere la contabilità.</span><span class="sxs-lookup"><span data-stu-id="13e5e-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="13e5e-111">La contabilità può essere la prima o l'ultima pagina del processo a discrezione dell'implementatore.</span><span class="sxs-lookup"><span data-stu-id="13e5e-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="13e5e-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="13e5e-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="13e5e-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="13e5e-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="13e5e-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="13e5e-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="13e5e-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="13e5e-115">Element Information</span></span>



| <span data-ttu-id="13e5e-116">Nome</span><span class="sxs-lookup"><span data-stu-id="13e5e-116">Name</span></span> | <span data-ttu-id="13e5e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="13e5e-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="13e5e-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="13e5e-118">Element Type</span></span> <br/>   | <span data-ttu-id="13e5e-119">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="13e5e-119">Feature</span></span><br/> |
| <span data-ttu-id="13e5e-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="13e5e-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="13e5e-121">Processo</span><span class="sxs-lookup"><span data-stu-id="13e5e-121">Job</span></span><br/>     |
| <span data-ttu-id="13e5e-122">Note</span><span class="sxs-lookup"><span data-stu-id="13e5e-122">Notes</span></span> <br/>          | <span data-ttu-id="13e5e-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="13e5e-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="13e5e-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="13e5e-124">Structural Content</span></span>

<span data-ttu-id="13e5e-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="13e5e-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="13e5e-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="13e5e-126">Structure Variables</span></span>

<span data-ttu-id="13e5e-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="13e5e-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="13e5e-128">Nome</span><span class="sxs-lookup"><span data-stu-id="13e5e-128">Name</span></span>                               | <span data-ttu-id="13e5e-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="13e5e-129">Data type</span></span>         | <span data-ttu-id="13e5e-130">Unità</span><span class="sxs-lookup"><span data-stu-id="13e5e-130">Unit</span></span>                  | <span data-ttu-id="13e5e-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="13e5e-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="13e5e-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="13e5e-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="13e5e-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="13e5e-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="13e5e-134">string</span><span class="sxs-lookup"><span data-stu-id="13e5e-134">string</span></span><br/> | <span data-ttu-id="13e5e-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="13e5e-135">characters</span></span><br/> | <span data-ttu-id="13e5e-136">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="13e5e-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="13e5e-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="13e5e-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="13e5e-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="13e5e-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="13e5e-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="13e5e-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="13e5e-140">string</span><span class="sxs-lookup"><span data-stu-id="13e5e-140">string</span></span><br/> | <span data-ttu-id="13e5e-141">n/d</span><span class="sxs-lookup"><span data-stu-id="13e5e-141">n/a</span></span><br/>        | <span data-ttu-id="13e5e-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="13e5e-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="13e5e-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="13e5e-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="13e5e-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="13e5e-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="13e5e-145">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="13e5e-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="13e5e-146">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="13e5e-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="13e5e-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13e5e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e5e-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="13e5e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




