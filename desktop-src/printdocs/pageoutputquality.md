---
description: Informazioni sull'elemento PageOutputQuality configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395590"
---
# <a name="pageoutputquality"></a><span data-ttu-id="a31e3-105">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="a31e3-105">PageOutputQuality</span></span>

<span data-ttu-id="a31e3-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a31e3-106">This topic is not current.</span></span> <span data-ttu-id="a31e3-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a31e3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a31e3-108">Descrive il livello di qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="a31e3-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="a31e3-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a31e3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a31e3-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a31e3-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a31e3-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a31e3-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a31e3-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a31e3-112">Element Information</span></span>



| <span data-ttu-id="a31e3-113">Nome</span><span class="sxs-lookup"><span data-stu-id="a31e3-113">Name</span></span> | <span data-ttu-id="a31e3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a31e3-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a31e3-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a31e3-115">Element Type</span></span> <br/>   | <span data-ttu-id="a31e3-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="a31e3-116">Feature</span></span><br/> |
| <span data-ttu-id="a31e3-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a31e3-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a31e3-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="a31e3-118">Page</span></span><br/>    |
| <span data-ttu-id="a31e3-119">Note</span><span class="sxs-lookup"><span data-stu-id="a31e3-119">Notes</span></span> <br/>          | <span data-ttu-id="a31e3-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="a31e3-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a31e3-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a31e3-121">Structural Content</span></span>

<span data-ttu-id="a31e3-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="a31e3-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="a31e3-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="a31e3-123">Structure Variables</span></span>

<span data-ttu-id="a31e3-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a31e3-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a31e3-125">Nome</span><span class="sxs-lookup"><span data-stu-id="a31e3-125">Name</span></span>                               | <span data-ttu-id="a31e3-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a31e3-126">Data type</span></span>         | <span data-ttu-id="a31e3-127">Unità</span><span class="sxs-lookup"><span data-stu-id="a31e3-127">Unit</span></span>                  | <span data-ttu-id="a31e3-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="a31e3-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a31e3-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a31e3-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a31e3-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a31e3-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a31e3-131">string</span><span class="sxs-lookup"><span data-stu-id="a31e3-131">string</span></span><br/> | <span data-ttu-id="a31e3-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="a31e3-132">characters</span></span><br/> | <span data-ttu-id="a31e3-133">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a31e3-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a31e3-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a31e3-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a31e3-135">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="a31e3-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a31e3-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a31e3-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a31e3-137">string</span><span class="sxs-lookup"><span data-stu-id="a31e3-137">string</span></span><br/> | <span data-ttu-id="a31e3-138">n/d</span><span class="sxs-lookup"><span data-stu-id="a31e3-138">n/a</span></span><br/>        | <span data-ttu-id="a31e3-139">True, False</span><span class="sxs-lookup"><span data-stu-id="a31e3-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a31e3-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a31e3-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a31e3-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a31e3-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a31e3-142">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="a31e3-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a31e3-143">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="a31e3-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="a31e3-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a31e3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a31e3-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a31e3-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




