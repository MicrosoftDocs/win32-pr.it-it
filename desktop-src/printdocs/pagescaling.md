---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41af04cc5657360fcc8d4b15812e9c2dd6b9fb06
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321157"
---
# <a name="pagescaling"></a><span data-ttu-id="167cd-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="167cd-104">PageScaling</span></span>

<span data-ttu-id="167cd-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="167cd-105">This topic is not current.</span></span> <span data-ttu-id="167cd-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="167cd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="167cd-107">Descrive le caratteristiche di scalabilità dell'output.</span><span class="sxs-lookup"><span data-stu-id="167cd-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="167cd-108">Per alcune opzioni di questa funzionalità è necessario che il consumer sia in grado di determinare le caratteristiche delle "dimensioni del contenuto dell'applicazione".</span><span class="sxs-lookup"><span data-stu-id="167cd-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="167cd-109">In assenza della possibilità di determinare queste caratteristiche, il consumer deve essere impostato sull'opzione Identity.</span><span class="sxs-lookup"><span data-stu-id="167cd-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="167cd-110">Queste caratteristiche sono:</span><span class="sxs-lookup"><span data-stu-id="167cd-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="167cd-111">Dimensioni supporti applicazione</span><span class="sxs-lookup"><span data-stu-id="167cd-111">Application Media Size</span></span>   | <span data-ttu-id="167cd-112">Dimensioni del supporto definito dal layout dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="167cd-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="167cd-113">Le dimensioni del supporto dell'applicazione possono corrispondere o meno a un PageMediaSize supportato dal consumer.</span><span class="sxs-lookup"><span data-stu-id="167cd-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="167cd-114">Dimensioni contenuto applicazione</span><span class="sxs-lookup"><span data-stu-id="167cd-114">Application Content Size</span></span> | <span data-ttu-id="167cd-115">Dimensioni del supporto definito dal layout dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="167cd-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="167cd-116">Le dimensioni del supporto dell'applicazione possono corrispondere o meno a un PageMediaSize supportato dal consumer.</span><span class="sxs-lookup"><span data-stu-id="167cd-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="167cd-117">Dimensioni del Bleed dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="167cd-117">Application Bleed Size</span></span>   | <span data-ttu-id="167cd-118">Offset e extent dell'area di Bleed dell'applicazione, una casella di overflow utilizzata dall'applicazione per la registrazione e il layout in relazione alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="167cd-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="167cd-119">L'area di spurgo sarà maggiore o uguale alla dimensione del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="167cd-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="167cd-120">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="167cd-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="167cd-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="167cd-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="167cd-122">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="167cd-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="167cd-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="167cd-123">Element Information</span></span>



| <span data-ttu-id="167cd-124">Nome</span><span class="sxs-lookup"><span data-stu-id="167cd-124">Name</span></span>                       |                                                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="167cd-125">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="167cd-125">Element Type</span></span> <br/>   | <span data-ttu-id="167cd-126">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="167cd-126">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="167cd-127">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="167cd-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="167cd-128">Pagina</span><span class="sxs-lookup"><span data-stu-id="167cd-128">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="167cd-129">Note</span><span class="sxs-lookup"><span data-stu-id="167cd-129">Notes</span></span> <br/>          | <span data-ttu-id="167cd-130">Top, Bottom, Left e Right sono relativi a PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="167cd-130">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="167cd-131">Le coordinate sono relative a PageImageableSize dell'oggetto, dove l'origine di è relativa all'origine di PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="167cd-131">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="167cd-132">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="167cd-132">Structural Content</span></span>

<span data-ttu-id="167cd-133">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="167cd-133">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="167cd-134">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="167cd-134">Structure Variables</span></span>

<span data-ttu-id="167cd-135">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="167cd-135">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="167cd-136">Nome</span><span class="sxs-lookup"><span data-stu-id="167cd-136">Name</span></span>                               | <span data-ttu-id="167cd-137">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="167cd-137">Data type</span></span>         | <span data-ttu-id="167cd-138">Unità</span><span class="sxs-lookup"><span data-stu-id="167cd-138">Unit</span></span>                  | <span data-ttu-id="167cd-139">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="167cd-139">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="167cd-140">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="167cd-140">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="167cd-141">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="167cd-141">\_OptionName\_</span></span><br/>          | <span data-ttu-id="167cd-142">string</span><span class="sxs-lookup"><span data-stu-id="167cd-142">string</span></span><br/> | <span data-ttu-id="167cd-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="167cd-143">characters</span></span><br/> | <span data-ttu-id="167cd-144">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="167cd-144">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="167cd-145">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="167cd-145">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="167cd-146">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="167cd-146">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="167cd-147">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="167cd-147">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="167cd-148">string</span><span class="sxs-lookup"><span data-stu-id="167cd-148">string</span></span><br/> | <span data-ttu-id="167cd-149">n/d</span><span class="sxs-lookup"><span data-stu-id="167cd-149">n/a</span></span><br/>        | <span data-ttu-id="167cd-150">True, False.</span><span class="sxs-lookup"><span data-stu-id="167cd-150">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="167cd-151">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="167cd-151">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="167cd-152">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="167cd-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="167cd-153">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="167cd-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="167cd-154">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="167cd-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="167cd-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="167cd-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="167cd-156">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="167cd-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




