---
description: Informazioni sull'elemento JobPageOrder, che definisce l'ordine delle pagine fisiche per l'output.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: JobPageOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2216330034c458095af7e67ff0904100126451
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408744"
---
# <a name="jobpageorder"></a><span data-ttu-id="d430e-103">JobPageOrder</span><span class="sxs-lookup"><span data-stu-id="d430e-103">JobPageOrder</span></span>

<span data-ttu-id="d430e-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="d430e-104">This topic is not current.</span></span> <span data-ttu-id="d430e-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d430e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d430e-106">Definisce l'ordine delle pagine fisiche per l'output.</span><span class="sxs-lookup"><span data-stu-id="d430e-106">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="d430e-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d430e-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d430e-108">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d430e-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d430e-109">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d430e-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d430e-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d430e-110">Element Information</span></span>



| <span data-ttu-id="d430e-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d430e-111">Name</span></span> | <span data-ttu-id="d430e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d430e-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d430e-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d430e-113">Element Type</span></span> <br/>   | <span data-ttu-id="d430e-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="d430e-114">Feature</span></span><br/> |
| <span data-ttu-id="d430e-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="d430e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d430e-116">Processo</span><span class="sxs-lookup"><span data-stu-id="d430e-116">Job</span></span><br/>     |
| <span data-ttu-id="d430e-117">Note</span><span class="sxs-lookup"><span data-stu-id="d430e-117">Notes</span></span> <br/>          | <span data-ttu-id="d430e-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="d430e-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d430e-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d430e-119">Structural Content</span></span>

<span data-ttu-id="d430e-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="d430e-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="d430e-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="d430e-121">Structure Variables</span></span>

<span data-ttu-id="d430e-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="d430e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d430e-123">Nome</span><span class="sxs-lookup"><span data-stu-id="d430e-123">Name</span></span>                               | <span data-ttu-id="d430e-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d430e-124">Data type</span></span>         | <span data-ttu-id="d430e-125">Unità</span><span class="sxs-lookup"><span data-stu-id="d430e-125">Unit</span></span>                  | <span data-ttu-id="d430e-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="d430e-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d430e-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="d430e-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d430e-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d430e-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d430e-129">string</span><span class="sxs-lookup"><span data-stu-id="d430e-129">string</span></span><br/> | <span data-ttu-id="d430e-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="d430e-130">characters</span></span><br/> | <span data-ttu-id="d430e-131">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d430e-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d430e-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="d430e-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d430e-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="d430e-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d430e-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d430e-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d430e-135">string</span><span class="sxs-lookup"><span data-stu-id="d430e-135">string</span></span><br/> | <span data-ttu-id="d430e-136">n/d</span><span class="sxs-lookup"><span data-stu-id="d430e-136">n/a</span></span><br/>        | <span data-ttu-id="d430e-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="d430e-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d430e-138">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d430e-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d430e-139">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d430e-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d430e-140">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="d430e-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d430e-141">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="d430e-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d430e-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d430e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d430e-143">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="d430e-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




