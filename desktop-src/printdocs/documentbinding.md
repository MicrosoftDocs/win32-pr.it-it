---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: Associazione documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4aeb31acb72932bbf272d52676b7795abe8311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996298"
---
# <a name="documentbinding"></a><span data-ttu-id="a9817-104">Associazione documento</span><span class="sxs-lookup"><span data-stu-id="a9817-104">DocumentBinding</span></span>

<span data-ttu-id="a9817-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a9817-105">This topic is not current.</span></span> <span data-ttu-id="a9817-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a9817-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a9817-107">Descrive il metodo di associazione.</span><span class="sxs-lookup"><span data-stu-id="a9817-107">Describes the method of binding.</span></span> <span data-ttu-id="a9817-108">Ogni documento è associato separatamente.</span><span class="sxs-lookup"><span data-stu-id="a9817-108">Each document is bound separately.</span></span> <span data-ttu-id="a9817-109">DocumentBinding e JobBindAllDocuments si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="a9817-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="a9817-110">È responsabilità del driver determinare la gestione dei vincoli tra parole chiave.</span><span class="sxs-lookup"><span data-stu-id="a9817-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="a9817-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a9817-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a9817-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a9817-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a9817-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a9817-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a9817-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a9817-114">Element Information</span></span>



| <span data-ttu-id="a9817-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a9817-115">Name</span></span> | <span data-ttu-id="a9817-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a9817-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9817-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a9817-117">Element Type</span></span> <br/>   | <span data-ttu-id="a9817-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="a9817-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a9817-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a9817-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a9817-120">Documento</span><span class="sxs-lookup"><span data-stu-id="a9817-120">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="a9817-121">Note</span><span class="sxs-lookup"><span data-stu-id="a9817-121">Notes</span></span> <br/>          | <span data-ttu-id="a9817-122">Top, Bottom, Left e Right sono relativi a PageImageableSize, dove TopLeft è denotato dall'origine dell'asse x e dell'asse y.</span><span class="sxs-lookup"><span data-stu-id="a9817-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a9817-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a9817-123">Structural Content</span></span>

<span data-ttu-id="a9817-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="a9817-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
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

## <a name="structure-variables"></a><span data-ttu-id="a9817-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="a9817-125">Structure Variables</span></span>

<span data-ttu-id="a9817-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a9817-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a9817-127">Nome</span><span class="sxs-lookup"><span data-stu-id="a9817-127">Name</span></span>                               | <span data-ttu-id="a9817-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a9817-128">Data type</span></span>          | <span data-ttu-id="a9817-129">Unità</span><span class="sxs-lookup"><span data-stu-id="a9817-129">Unit</span></span>                  | <span data-ttu-id="a9817-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="a9817-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a9817-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a9817-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9817-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a9817-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a9817-133">string</span><span class="sxs-lookup"><span data-stu-id="a9817-133">string</span></span><br/>  | <span data-ttu-id="a9817-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="a9817-134">characters</span></span><br/> | <span data-ttu-id="a9817-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a9817-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a9817-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9817-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a9817-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="a9817-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a9817-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a9817-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a9817-139">string</span><span class="sxs-lookup"><span data-stu-id="a9817-139">string</span></span><br/>  | <span data-ttu-id="a9817-140">n/d</span><span class="sxs-lookup"><span data-stu-id="a9817-140">n/a</span></span><br/>        | <span data-ttu-id="a9817-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="a9817-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a9817-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a9817-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="a9817-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="a9817-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="a9817-144">Intero</span><span class="sxs-lookup"><span data-stu-id="a9817-144">Integer</span></span><br/> | <span data-ttu-id="a9817-145">Micron</span><span class="sxs-lookup"><span data-stu-id="a9817-145">microns</span></span><br/>    | <span data-ttu-id="a9817-146">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="a9817-146">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="a9817-147">Definisce la distanza minima dell'associazione per l'associazione finale specificata.</span><span class="sxs-lookup"><span data-stu-id="a9817-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="a9817-148">La grondaia viene misurata in micron rispetto al bordo della dimensione dei supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="a9817-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a9817-149">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a9817-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a9817-150">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="a9817-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a9817-151">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="a9817-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale" >
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a9817-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9817-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9817-153">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a9817-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




