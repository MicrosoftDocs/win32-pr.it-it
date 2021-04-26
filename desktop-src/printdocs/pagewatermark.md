---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16a475255e42bda8e60b3bfb2ab41ea3998738
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994458"
---
# <a name="pagewatermark"></a><span data-ttu-id="7e7a2-104">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="7e7a2-104">PageWatermark</span></span>

<span data-ttu-id="7e7a2-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-105">This topic is not current.</span></span> <span data-ttu-id="7e7a2-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7e7a2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7e7a2-107">Descrive l'impostazione del limite dell'output e le caratteristiche del limite.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="7e7a2-108">Le filigrane si applicano alla pagina logica, non alla pagina fisica.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="7e7a2-109">Ad esempio, se DocumentDuplex è abilitato, verrà visualizzata una filigrana in ogni pagina NUp in ogni foglio.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="7e7a2-110">Se DocumentDuplex, PagesPerSheet=2, ogni foglio avrà 2 filigrane.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="7e7a2-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7e7a2-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7e7a2-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7e7a2-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7e7a2-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7e7a2-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7e7a2-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7e7a2-114">Element Information</span></span>



| <span data-ttu-id="7e7a2-115">Nome</span><span class="sxs-lookup"><span data-stu-id="7e7a2-115">Name</span></span> | <span data-ttu-id="7e7a2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7e7a2-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7a2-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7e7a2-117">Element Type</span></span> <br/>   | <span data-ttu-id="7e7a2-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="7e7a2-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="7e7a2-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7e7a2-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7e7a2-120">Pagina</span><span class="sxs-lookup"><span data-stu-id="7e7a2-120">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="7e7a2-121">Note</span><span class="sxs-lookup"><span data-stu-id="7e7a2-121">Notes</span></span> <br/>          | <span data-ttu-id="7e7a2-122">Le coordinate sono relative a PageImageableSize, dove l'origine della filigrana è relativa all'origine di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-122">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7e7a2-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7e7a2-123">Structural Content</span></span>

<span data-ttu-id="7e7a2-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="7e7a2-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="7e7a2-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="7e7a2-125">Structure Variables</span></span>

<span data-ttu-id="7e7a2-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7e7a2-127">Nome</span><span class="sxs-lookup"><span data-stu-id="7e7a2-127">Name</span></span>                               | <span data-ttu-id="7e7a2-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7e7a2-128">Data type</span></span>         | <span data-ttu-id="7e7a2-129">Unità</span><span class="sxs-lookup"><span data-stu-id="7e7a2-129">Unit</span></span>                  | <span data-ttu-id="7e7a2-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="7e7a2-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7e7a2-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7e7a2-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7e7a2-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7e7a2-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7e7a2-133">string</span><span class="sxs-lookup"><span data-stu-id="7e7a2-133">string</span></span><br/> | <span data-ttu-id="7e7a2-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="7e7a2-134">characters</span></span><br/> | <span data-ttu-id="7e7a2-135">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7e7a2-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7e7a2-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7e7a2-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7e7a2-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7e7a2-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7e7a2-139">string</span><span class="sxs-lookup"><span data-stu-id="7e7a2-139">string</span></span><br/> | <span data-ttu-id="7e7a2-140">n/d</span><span class="sxs-lookup"><span data-stu-id="7e7a2-140">n/a</span></span><br/>        | <span data-ttu-id="7e7a2-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7e7a2-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7e7a2-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7e7a2-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7e7a2-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7e7a2-144">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="7e7a2-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7e7a2-145">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="7e7a2-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7e7a2-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e7a2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e7a2-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7e7a2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




