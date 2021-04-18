---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: Documento di
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139cc40701624041a57e4fa69edc084f88c1972b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321140"
---
# <a name="documentbinding"></a><span data-ttu-id="03d2d-104">Documento di</span><span class="sxs-lookup"><span data-stu-id="03d2d-104">DocumentBinding</span></span>

<span data-ttu-id="03d2d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="03d2d-105">This topic is not current.</span></span> <span data-ttu-id="03d2d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="03d2d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="03d2d-107">Descrive il metodo di associazione.</span><span class="sxs-lookup"><span data-stu-id="03d2d-107">Describes the method of binding.</span></span> <span data-ttu-id="03d2d-108">Ogni documento è associato separatamente.</span><span class="sxs-lookup"><span data-stu-id="03d2d-108">Each document is bound separately.</span></span> <span data-ttu-id="03d2d-109">La documentazione e JobBindAllDocuments si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="03d2d-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="03d2d-110">Spetta al driver determinare la gestione dei vincoli tra le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="03d2d-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="03d2d-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="03d2d-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="03d2d-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="03d2d-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="03d2d-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="03d2d-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="03d2d-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="03d2d-114">Element Information</span></span>



| <span data-ttu-id="03d2d-115">Nome</span><span class="sxs-lookup"><span data-stu-id="03d2d-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d2d-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="03d2d-116">Element Type</span></span> <br/>   | <span data-ttu-id="03d2d-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="03d2d-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="03d2d-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="03d2d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="03d2d-119">Documento</span><span class="sxs-lookup"><span data-stu-id="03d2d-119">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="03d2d-120">Note</span><span class="sxs-lookup"><span data-stu-id="03d2d-120">Notes</span></span> <br/>          | <span data-ttu-id="03d2d-121">In alto, in basso, a sinistra e a destra sono relativi a PageImageableSize dell'oggetto, dove la parte superiore è indicata dall'origine dell'asse x e dall'asse y.</span><span class="sxs-lookup"><span data-stu-id="03d2d-121">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="03d2d-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="03d2d-122">Structural Content</span></span>

<span data-ttu-id="03d2d-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="03d2d-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="03d2d-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="03d2d-124">Structure Variables</span></span>

<span data-ttu-id="03d2d-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="03d2d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="03d2d-126">Nome</span><span class="sxs-lookup"><span data-stu-id="03d2d-126">Name</span></span>                               | <span data-ttu-id="03d2d-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="03d2d-127">Data type</span></span>          | <span data-ttu-id="03d2d-128">Unità</span><span class="sxs-lookup"><span data-stu-id="03d2d-128">Unit</span></span>                  | <span data-ttu-id="03d2d-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="03d2d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="03d2d-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="03d2d-130">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d2d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="03d2d-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="03d2d-132">string</span><span class="sxs-lookup"><span data-stu-id="03d2d-132">string</span></span><br/>  | <span data-ttu-id="03d2d-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="03d2d-133">characters</span></span><br/> | <span data-ttu-id="03d2d-134">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="03d2d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="03d2d-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="03d2d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="03d2d-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="03d2d-136">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="03d2d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="03d2d-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="03d2d-138">string</span><span class="sxs-lookup"><span data-stu-id="03d2d-138">string</span></span><br/>  | <span data-ttu-id="03d2d-139">n/d</span><span class="sxs-lookup"><span data-stu-id="03d2d-139">n/a</span></span><br/>        | <span data-ttu-id="03d2d-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="03d2d-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="03d2d-141">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="03d2d-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="03d2d-142">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="03d2d-142">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="03d2d-143">Integer</span><span class="sxs-lookup"><span data-stu-id="03d2d-143">Integer</span></span><br/> | <span data-ttu-id="03d2d-144">micron</span><span class="sxs-lookup"><span data-stu-id="03d2d-144">microns</span></span><br/>    | <span data-ttu-id="03d2d-145">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="03d2d-145">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="03d2d-146">Definisce la barra di associazione minima per l'associazione finale specificata.</span><span class="sxs-lookup"><span data-stu-id="03d2d-146">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="03d2d-147">La gronda viene misurata in micron rispetto al bordo della dimensione media fisica.</span><span class="sxs-lookup"><span data-stu-id="03d2d-147">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="03d2d-148">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="03d2d-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="03d2d-149">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="03d2d-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="03d2d-150">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="03d2d-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="03d2d-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03d2d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d2d-152">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="03d2d-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




