---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c63238c290d6b8f0bb208e94e52dc66c8d2e6be
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994478"
---
# <a name="pageoutputquality"></a><span data-ttu-id="66766-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="66766-104">PageOutputQuality</span></span>

<span data-ttu-id="66766-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="66766-105">This topic is not current.</span></span> <span data-ttu-id="66766-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="66766-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="66766-107">Descrive il livello di qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="66766-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="66766-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="66766-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="66766-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="66766-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="66766-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="66766-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="66766-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="66766-111">Element Information</span></span>



| <span data-ttu-id="66766-112">Nome</span><span class="sxs-lookup"><span data-stu-id="66766-112">Name</span></span> | <span data-ttu-id="66766-113">Valore</span><span class="sxs-lookup"><span data-stu-id="66766-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="66766-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="66766-114">Element Type</span></span> <br/>   | <span data-ttu-id="66766-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="66766-115">Feature</span></span><br/> |
| <span data-ttu-id="66766-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="66766-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="66766-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="66766-117">Page</span></span><br/>    |
| <span data-ttu-id="66766-118">Note</span><span class="sxs-lookup"><span data-stu-id="66766-118">Notes</span></span> <br/>          | <span data-ttu-id="66766-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="66766-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="66766-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="66766-120">Structural Content</span></span>

<span data-ttu-id="66766-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="66766-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="66766-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="66766-122">Structure Variables</span></span>

<span data-ttu-id="66766-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="66766-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="66766-124">Nome</span><span class="sxs-lookup"><span data-stu-id="66766-124">Name</span></span>                               | <span data-ttu-id="66766-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="66766-125">Data type</span></span>         | <span data-ttu-id="66766-126">Unità</span><span class="sxs-lookup"><span data-stu-id="66766-126">Unit</span></span>                  | <span data-ttu-id="66766-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="66766-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="66766-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="66766-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="66766-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="66766-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="66766-130">string</span><span class="sxs-lookup"><span data-stu-id="66766-130">string</span></span><br/> | <span data-ttu-id="66766-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="66766-131">characters</span></span><br/> | <span data-ttu-id="66766-132">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="66766-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="66766-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="66766-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="66766-134">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="66766-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="66766-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="66766-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="66766-136">string</span><span class="sxs-lookup"><span data-stu-id="66766-136">string</span></span><br/> | <span data-ttu-id="66766-137">n/d</span><span class="sxs-lookup"><span data-stu-id="66766-137">n/a</span></span><br/>        | <span data-ttu-id="66766-138">True, False</span><span class="sxs-lookup"><span data-stu-id="66766-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="66766-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="66766-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="66766-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="66766-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="66766-141">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="66766-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="66766-142">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="66766-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="66766-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66766-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66766-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="66766-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




