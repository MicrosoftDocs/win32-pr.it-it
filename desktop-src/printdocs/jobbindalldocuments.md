---
description: Informazioni sull'elemento JobBindAllDocuments, che descrive il metodo di associazione. Tutti i documenti nel processo sono associati tra loro.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5abff455756b2abc1d84bf2cff470fa49c93278
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409084"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="16955-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="16955-104">JobBindAllDocuments</span></span>

<span data-ttu-id="16955-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="16955-105">This topic is not current.</span></span> <span data-ttu-id="16955-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16955-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16955-107">Descrive il metodo di associazione.</span><span class="sxs-lookup"><span data-stu-id="16955-107">Describes the method of binding.</span></span> <span data-ttu-id="16955-108">Tutti i documenti nel processo sono associati tra loro.</span><span class="sxs-lookup"><span data-stu-id="16955-108">All documents in the job are bound together.</span></span> <span data-ttu-id="16955-109">JobBindAllDocuments e DocumentBinding si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="16955-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="16955-110">È responsabilità del driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="16955-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="16955-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16955-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="16955-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="16955-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="16955-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="16955-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="16955-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16955-114">Element Information</span></span>



| <span data-ttu-id="16955-115">Nome</span><span class="sxs-lookup"><span data-stu-id="16955-115">Name</span></span> | <span data-ttu-id="16955-116">Valore</span><span class="sxs-lookup"><span data-stu-id="16955-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="16955-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="16955-117">Element Type</span></span> <br/>   | <span data-ttu-id="16955-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="16955-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="16955-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="16955-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="16955-120">Processo</span><span class="sxs-lookup"><span data-stu-id="16955-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="16955-121">Note</span><span class="sxs-lookup"><span data-stu-id="16955-121">Notes</span></span> <br/>          | <span data-ttu-id="16955-122">Top, Bottom, Left e Right sono relativi a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="16955-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="16955-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="16955-123">Structural Content</span></span>

<span data-ttu-id="16955-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="16955-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="16955-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="16955-125">Structure Variables</span></span>

<span data-ttu-id="16955-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="16955-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="16955-127">Nome</span><span class="sxs-lookup"><span data-stu-id="16955-127">Name</span></span>                               | <span data-ttu-id="16955-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="16955-128">Data type</span></span>          | <span data-ttu-id="16955-129">Unità</span><span class="sxs-lookup"><span data-stu-id="16955-129">Unit</span></span>                  | <span data-ttu-id="16955-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="16955-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="16955-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="16955-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16955-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="16955-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="16955-133">string</span><span class="sxs-lookup"><span data-stu-id="16955-133">string</span></span><br/>  | <span data-ttu-id="16955-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="16955-134">characters</span></span><br/> | <span data-ttu-id="16955-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="16955-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="16955-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="16955-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="16955-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="16955-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="16955-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="16955-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="16955-139">string</span><span class="sxs-lookup"><span data-stu-id="16955-139">string</span></span><br/>  | <span data-ttu-id="16955-140">n/d</span><span class="sxs-lookup"><span data-stu-id="16955-140">n/a</span></span><br/>        | <span data-ttu-id="16955-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="16955-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="16955-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="16955-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="16955-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="16955-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="16955-144">numero intero</span><span class="sxs-lookup"><span data-stu-id="16955-144">integer</span></span><br/> | <span data-ttu-id="16955-145">Micron</span><span class="sxs-lookup"><span data-stu-id="16955-145">microns</span></span><br/>    | <span data-ttu-id="16955-146">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="16955-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="16955-147">Definisce la barra di associazione minima per l'associazione finale specificata.</span><span class="sxs-lookup"><span data-stu-id="16955-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="16955-148">La barra di margine viene misurata in micron rispetto al bordo della dimensione fisica dei supporti.</span><span class="sxs-lookup"><span data-stu-id="16955-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="16955-149">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="16955-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="16955-150">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="16955-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="16955-151">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="16955-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="16955-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16955-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16955-153">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="16955-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




