---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6d906833dc067155c9d98d50ed47e898a446e2
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351906"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="516c7-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="516c7-104">JobAccountingSheet</span></span>

<span data-ttu-id="516c7-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="516c7-105">This topic is not current.</span></span> <span data-ttu-id="516c7-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="516c7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="516c7-107">Descrive il foglio contabilità per l'output del processo.</span><span class="sxs-lookup"><span data-stu-id="516c7-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="516c7-108">Il foglio di contabilità deve essere output sul valore predefinito di PageMediaSize e usare il valore predefinito di PageMediaType.</span><span class="sxs-lookup"><span data-stu-id="516c7-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="516c7-109">Il foglio di contabilità deve essere isolato dal resto del processo.</span><span class="sxs-lookup"><span data-stu-id="516c7-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="516c7-110">Ciò significa che qualsiasi opzione di completamento o elaborazione, ad esempio JobDuplex, JobStaple o JobBinding, non deve includere il foglio contabilità.</span><span class="sxs-lookup"><span data-stu-id="516c7-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="516c7-111">Il foglio contabilità può essere presente come prima o ultima pagina del processo a discrezione dell'implementatore.</span><span class="sxs-lookup"><span data-stu-id="516c7-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="516c7-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="516c7-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="516c7-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="516c7-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="516c7-114">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="516c7-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="516c7-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="516c7-115">Element Information</span></span>



| <span data-ttu-id="516c7-116">Nome</span><span class="sxs-lookup"><span data-stu-id="516c7-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="516c7-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="516c7-117">Element Type</span></span> <br/>   | <span data-ttu-id="516c7-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="516c7-118">Feature</span></span><br/> |
| <span data-ttu-id="516c7-119">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="516c7-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="516c7-120">Processo</span><span class="sxs-lookup"><span data-stu-id="516c7-120">Job</span></span><br/>     |
| <span data-ttu-id="516c7-121">Note</span><span class="sxs-lookup"><span data-stu-id="516c7-121">Notes</span></span> <br/>          | <span data-ttu-id="516c7-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="516c7-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="516c7-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="516c7-123">Structural Content</span></span>

<span data-ttu-id="516c7-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="516c7-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="516c7-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="516c7-125">Structure Variables</span></span>

<span data-ttu-id="516c7-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="516c7-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="516c7-127">Nome</span><span class="sxs-lookup"><span data-stu-id="516c7-127">Name</span></span>                               | <span data-ttu-id="516c7-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="516c7-128">Data type</span></span>         | <span data-ttu-id="516c7-129">Unità</span><span class="sxs-lookup"><span data-stu-id="516c7-129">Unit</span></span>                  | <span data-ttu-id="516c7-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="516c7-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="516c7-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="516c7-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="516c7-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="516c7-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="516c7-133">string</span><span class="sxs-lookup"><span data-stu-id="516c7-133">string</span></span><br/> | <span data-ttu-id="516c7-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="516c7-134">characters</span></span><br/> | <span data-ttu-id="516c7-135">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="516c7-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="516c7-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="516c7-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="516c7-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="516c7-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="516c7-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="516c7-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="516c7-139">string</span><span class="sxs-lookup"><span data-stu-id="516c7-139">string</span></span><br/> | <span data-ttu-id="516c7-140">n/d</span><span class="sxs-lookup"><span data-stu-id="516c7-140">n/a</span></span><br/>        | <span data-ttu-id="516c7-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="516c7-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="516c7-142">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="516c7-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="516c7-143">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="516c7-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="516c7-144">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="516c7-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="516c7-145">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="516c7-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="516c7-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="516c7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="516c7-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="516c7-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




