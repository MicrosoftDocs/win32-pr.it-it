---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996108"
---
# <a name="pageimageablesize"></a><span data-ttu-id="21bf4-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="21bf4-104">PageImageableSize</span></span>

<span data-ttu-id="21bf4-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="21bf4-105">This topic is not current.</span></span> <span data-ttu-id="21bf4-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="21bf4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="21bf4-107">Descrive l'area di disegno con immagine per il layout e il rendering.</span><span class="sxs-lookup"><span data-stu-id="21bf4-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="21bf4-108">Verrà segnalato in base a PageMediaSize e PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="21bf4-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="21bf4-109">I diagrammi seguenti illustrano l'utilizzo delle variabili PageImageableSize in base a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="21bf4-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagramma che mostra le misurazioni della pagina](images/local-1641910626-image.png)

-   [<span data-ttu-id="21bf4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="21bf4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="21bf4-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="21bf4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="21bf4-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="21bf4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="21bf4-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="21bf4-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="21bf4-115">Nome</span><span class="sxs-lookup"><span data-stu-id="21bf4-115">Name</span></span> | <span data-ttu-id="21bf4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="21bf4-116">Value</span></span> |
| <span data-ttu-id="21bf4-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="21bf4-117">Element Type</span></span><br/>    | <span data-ttu-id="21bf4-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="21bf4-118">Property</span></span><br/> |
| <span data-ttu-id="21bf4-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="21bf4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="21bf4-120">Pagina</span><span class="sxs-lookup"><span data-stu-id="21bf4-120">Page</span></span><br/>     |
| <span data-ttu-id="21bf4-121">Note</span><span class="sxs-lookup"><span data-stu-id="21bf4-121">Notes</span></span> <br/>          | <span data-ttu-id="21bf4-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="21bf4-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="21bf4-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="21bf4-123">Structural Content</span></span>

<span data-ttu-id="21bf4-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="21bf4-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="21bf4-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="21bf4-125">Structure Variables</span></span>

<span data-ttu-id="21bf4-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="21bf4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="21bf4-127">Nome</span><span class="sxs-lookup"><span data-stu-id="21bf4-127">Name</span></span>                                    | <span data-ttu-id="21bf4-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="21bf4-128">Data type</span></span>          | <span data-ttu-id="21bf4-129">Unità</span><span class="sxs-lookup"><span data-stu-id="21bf4-129">Unit</span></span>               | <span data-ttu-id="21bf4-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="21bf4-130">Supported values</span></span>                       | <span data-ttu-id="21bf4-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="21bf4-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21bf4-132">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="21bf4-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="21bf4-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="21bf4-133">integer</span></span><br/> | <span data-ttu-id="21bf4-134">Micron</span><span class="sxs-lookup"><span data-stu-id="21bf4-134">microns</span></span><br/> | <span data-ttu-id="21bf4-135">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="21bf4-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="21bf4-136">Specifica la dimensione orizzontale del supporto dell'applicazione rispetto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="21bf4-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="21bf4-137">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="21bf4-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="21bf4-138">numero intero</span><span class="sxs-lookup"><span data-stu-id="21bf4-138">integer</span></span><br/> | <span data-ttu-id="21bf4-139">Micron</span><span class="sxs-lookup"><span data-stu-id="21bf4-139">microns</span></span><br/> | <span data-ttu-id="21bf4-140">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="21bf4-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="21bf4-141">Specifica la dimensione verticale delle dimensioni dei supporti dell'applicazione rispetto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="21bf4-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="21bf4-142">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="21bf4-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="21bf4-143">numero intero</span><span class="sxs-lookup"><span data-stu-id="21bf4-143">integer</span></span><br/> | <span data-ttu-id="21bf4-144">Micron</span><span class="sxs-lookup"><span data-stu-id="21bf4-144">microns</span></span><br/> | <span data-ttu-id="21bf4-145">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="21bf4-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="21bf4-146">Specifica l'origine orizzontale dell'area immagine rispetto alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21bf4-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="21bf4-147">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="21bf4-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="21bf4-148">numero intero</span><span class="sxs-lookup"><span data-stu-id="21bf4-148">integer</span></span><br/> | <span data-ttu-id="21bf4-149">Micron</span><span class="sxs-lookup"><span data-stu-id="21bf4-149">microns</span></span><br/> | <span data-ttu-id="21bf4-150">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="21bf4-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="21bf4-151">Specifica l'origine verticale dell'area immagine rispetto alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21bf4-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="21bf4-152">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="21bf4-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="21bf4-153">numero intero</span><span class="sxs-lookup"><span data-stu-id="21bf4-153">integer</span></span><br/> | <span data-ttu-id="21bf4-154">Micron</span><span class="sxs-lookup"><span data-stu-id="21bf4-154">microns</span></span><br/> | <span data-ttu-id="21bf4-155">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="21bf4-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="21bf4-156">Specifica la distanza orizzontale tra l'origine e il limite di delimitazione delle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21bf4-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="21bf4-157">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="21bf4-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="21bf4-158">numero intero</span><span class="sxs-lookup"><span data-stu-id="21bf4-158">integer</span></span><br/> | <span data-ttu-id="21bf4-159">Micron</span><span class="sxs-lookup"><span data-stu-id="21bf4-159">microns</span></span><br/> | <span data-ttu-id="21bf4-160">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="21bf4-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="21bf4-161">Specifica la distanza verticale tra l'origine e il limite di delimitazione delle dimensioni del supporto dell'applicazione canvas.</span><span class="sxs-lookup"><span data-stu-id="21bf4-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="21bf4-162">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="21bf4-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="21bf4-163">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="21bf4-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="21bf4-164">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="21bf4-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="21bf4-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21bf4-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21bf4-166">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="21bf4-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




