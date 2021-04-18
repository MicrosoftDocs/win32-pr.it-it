---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d0e0e47aa89a3cb6380a78dd49312d17f88ab8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321152"
---
# <a name="pagewatermark"></a><span data-ttu-id="ee4f8-104">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="ee4f8-104">PageWatermark</span></span>

<span data-ttu-id="ee4f8-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-105">This topic is not current.</span></span> <span data-ttu-id="ee4f8-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ee4f8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee4f8-107">Descrive l'impostazione della filigrana dell'output e le caratteristiche della filigrana.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="ee4f8-108">Le filigrane si applicano alla pagina logica, non alla pagina fisica.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="ee4f8-109">Se, ad esempio, DocumentDuplex è abilitato, verrà visualizzata una filigrana in ogni pagina di nstallazione in ogni foglio.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="ee4f8-110">Se DocumentDuplex, PagesPerSheet = 2, ogni foglio avrà 2 filigrane.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="ee4f8-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ee4f8-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ee4f8-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ee4f8-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ee4f8-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ee4f8-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ee4f8-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ee4f8-114">Element Information</span></span>



| <span data-ttu-id="ee4f8-115">Nome</span><span class="sxs-lookup"><span data-stu-id="ee4f8-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f8-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ee4f8-116">Element Type</span></span> <br/>   | <span data-ttu-id="ee4f8-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="ee4f8-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ee4f8-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="ee4f8-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ee4f8-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="ee4f8-119">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="ee4f8-120">Note</span><span class="sxs-lookup"><span data-stu-id="ee4f8-120">Notes</span></span> <br/>          | <span data-ttu-id="ee4f8-121">Le coordinate sono relative a PageImageableSize dell'oggetto, in cui l'origine della filigrana è relativa all'origine di PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-121">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ee4f8-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ee4f8-122">Structural Content</span></span>

<span data-ttu-id="ee4f8-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ee4f8-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ee4f8-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ee4f8-124">Structure Variables</span></span>

<span data-ttu-id="ee4f8-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ee4f8-126">Nome</span><span class="sxs-lookup"><span data-stu-id="ee4f8-126">Name</span></span>                               | <span data-ttu-id="ee4f8-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ee4f8-127">Data type</span></span>         | <span data-ttu-id="ee4f8-128">Unità</span><span class="sxs-lookup"><span data-stu-id="ee4f8-128">Unit</span></span>                  | <span data-ttu-id="ee4f8-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ee4f8-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ee4f8-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ee4f8-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f8-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ee4f8-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ee4f8-132">string</span><span class="sxs-lookup"><span data-stu-id="ee4f8-132">string</span></span><br/> | <span data-ttu-id="ee4f8-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="ee4f8-133">characters</span></span><br/> | <span data-ttu-id="ee4f8-134">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ee4f8-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ee4f8-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ee4f8-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ee4f8-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ee4f8-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ee4f8-138">string</span><span class="sxs-lookup"><span data-stu-id="ee4f8-138">string</span></span><br/> | <span data-ttu-id="ee4f8-139">n/d</span><span class="sxs-lookup"><span data-stu-id="ee4f8-139">n/a</span></span><br/>        | <span data-ttu-id="ee4f8-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ee4f8-141">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ee4f8-142">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ee4f8-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ee4f8-143">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ee4f8-144">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="ee4f8-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ee4f8-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee4f8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f8-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ee4f8-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




