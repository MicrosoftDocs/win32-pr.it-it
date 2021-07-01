---
description: Informazioni sull'elemento PageScaling. Questo elemento descrive le caratteristiche di ridimensionamento dell'output.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: Scalabilità di pagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795332f38da331a9f16b614154bf0a9270e613de
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119036"
---
# <a name="pagescaling"></a><span data-ttu-id="7c6b9-104">Scalabilità di pagine</span><span class="sxs-lookup"><span data-stu-id="7c6b9-104">PageScaling</span></span>

<span data-ttu-id="7c6b9-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-105">This topic is not current.</span></span> <span data-ttu-id="7c6b9-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7c6b9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7c6b9-107">Descrive le caratteristiche di ridimensionamento dell'output.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="7c6b9-108">Alcune opzioni di questa funzionalità richiedono che il consumer sia in grado di determinare le caratteristiche delle "dimensioni del contenuto dell'applicazione".</span><span class="sxs-lookup"><span data-stu-id="7c6b9-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="7c6b9-109">In assenza della possibilità di determinare queste caratteristiche, il consumer deve impostare come predefinita l'opzione identity.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="7c6b9-110">Queste caratteristiche sono:</span><span class="sxs-lookup"><span data-stu-id="7c6b9-110">These characteristics are:</span></span>



| <span data-ttu-id="7c6b9-111">Caratteristica di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="7c6b9-111">Scaling characteristic</span></span>                         | <span data-ttu-id="7c6b9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c6b9-112">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6b9-113">Dimensioni del supporto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7c6b9-113">Application Media Size</span></span>   | <span data-ttu-id="7c6b9-114">Dimensioni dei supporti definiti dal layout dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-114">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="7c6b9-115">Le dimensioni del supporto dell'applicazione possono corrispondere o meno a un oggetto PageMediaSize supportato dal consumer.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-115">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="7c6b9-116">Dimensioni del contenuto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7c6b9-116">Application Content Size</span></span> | <span data-ttu-id="7c6b9-117">Dimensioni dei supporti definiti dal layout dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-117">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="7c6b9-118">Le dimensioni del supporto dell'applicazione possono corrispondere o meno a un oggetto PageMediaSize supportato dal consumer.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-118">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="7c6b9-119">Application Bleed Size</span><span class="sxs-lookup"><span data-stu-id="7c6b9-119">Application Bleed Size</span></span>   | <span data-ttu-id="7c6b9-120">Offset ed estensione dell'area di smarginamento dell'applicazione, una casella di overflow utilizzata dall'applicazione per la registrazione e il layout, in relazione alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-120">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="7c6b9-121">L'area smarsata sarà maggiore o uguale alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-121">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="7c6b9-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7c6b9-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7c6b9-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7c6b9-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7c6b9-124">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7c6b9-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7c6b9-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7c6b9-125">Element Information</span></span>



| <span data-ttu-id="7c6b9-126">Nome</span><span class="sxs-lookup"><span data-stu-id="7c6b9-126">Name</span></span> | <span data-ttu-id="7c6b9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7c6b9-127">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6b9-128">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7c6b9-128">Element Type</span></span> <br/>   | <span data-ttu-id="7c6b9-129">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="7c6b9-129">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="7c6b9-130">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7c6b9-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7c6b9-131">Pagina</span><span class="sxs-lookup"><span data-stu-id="7c6b9-131">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="7c6b9-132">Note</span><span class="sxs-lookup"><span data-stu-id="7c6b9-132">Notes</span></span> <br/>          | <span data-ttu-id="7c6b9-133">Top, Bottom, Left e Right sono relativi a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-133">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="7c6b9-134">Le coordinate sono relative a PageImageableSize, dove l'origine di è relativa all'origine di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-134">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7c6b9-135">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7c6b9-135">Structural Content</span></span>

<span data-ttu-id="7c6b9-136">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7c6b9-136">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="7c6b9-137">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="7c6b9-137">Structure Variables</span></span>

<span data-ttu-id="7c6b9-138">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-138">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7c6b9-139">Nome</span><span class="sxs-lookup"><span data-stu-id="7c6b9-139">Name</span></span>                               | <span data-ttu-id="7c6b9-140">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7c6b9-140">Data type</span></span>         | <span data-ttu-id="7c6b9-141">Unità</span><span class="sxs-lookup"><span data-stu-id="7c6b9-141">Unit</span></span>                  | <span data-ttu-id="7c6b9-142">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="7c6b9-142">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7c6b9-143">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7c6b9-143">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7c6b9-144">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7c6b9-144">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7c6b9-145">string</span><span class="sxs-lookup"><span data-stu-id="7c6b9-145">string</span></span><br/> | <span data-ttu-id="7c6b9-146">caratteri</span><span class="sxs-lookup"><span data-stu-id="7c6b9-146">characters</span></span><br/> | <span data-ttu-id="7c6b9-147">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7c6b9-147">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7c6b9-148">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-148">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7c6b9-149">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-149">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7c6b9-150">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7c6b9-150">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7c6b9-151">string</span><span class="sxs-lookup"><span data-stu-id="7c6b9-151">string</span></span><br/> | <span data-ttu-id="7c6b9-152">n/d</span><span class="sxs-lookup"><span data-stu-id="7c6b9-152">n/a</span></span><br/>        | <span data-ttu-id="7c6b9-153">True, False.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-153">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7c6b9-154">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7c6b9-154">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7c6b9-155">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7c6b9-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7c6b9-156">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="7c6b9-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7c6b9-157">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="7c6b9-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7c6b9-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c6b9-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c6b9-159">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7c6b9-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




