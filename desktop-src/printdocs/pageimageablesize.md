---
description: Informazioni sull'elemento pageImageableSize configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395306"
---
# <a name="pageimageablesize"></a><span data-ttu-id="f3ae0-105">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="f3ae0-105">PageImageableSize</span></span>

<span data-ttu-id="f3ae0-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-106">This topic is not current.</span></span> <span data-ttu-id="f3ae0-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f3ae0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f3ae0-108">Descrive l'area di disegno con immagini per il layout e il rendering.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="f3ae0-109">Verrà segnalato in base a PageMediaSize e PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="f3ae0-110">I diagrammi seguenti illustrano l'utilizzo delle variabili PageImageableSize in base a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagramma che mostra le misurazioni della pagina](images/local-1641910626-image.png)

-   [<span data-ttu-id="f3ae0-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3ae0-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f3ae0-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f3ae0-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f3ae0-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f3ae0-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f3ae0-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3ae0-115">Element Information</span></span>

| <span data-ttu-id="f3ae0-116">Nome</span><span class="sxs-lookup"><span data-stu-id="f3ae0-116">Name</span></span>                 | <span data-ttu-id="f3ae0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f3ae0-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="f3ae0-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f3ae0-118">Element Type</span></span><br/>    | <span data-ttu-id="f3ae0-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3ae0-119">Property</span></span><br/> |
| <span data-ttu-id="f3ae0-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f3ae0-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f3ae0-121">Pagina</span><span class="sxs-lookup"><span data-stu-id="f3ae0-121">Page</span></span><br/>     |
| <span data-ttu-id="f3ae0-122">Note</span><span class="sxs-lookup"><span data-stu-id="f3ae0-122">Notes</span></span> <br/>          | <span data-ttu-id="f3ae0-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="f3ae0-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="f3ae0-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f3ae0-124">Structural Content</span></span>

<span data-ttu-id="f3ae0-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f3ae0-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f3ae0-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="f3ae0-126">Structure Variables</span></span>

<span data-ttu-id="f3ae0-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f3ae0-128">Nome</span><span class="sxs-lookup"><span data-stu-id="f3ae0-128">Name</span></span>                                    | <span data-ttu-id="f3ae0-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f3ae0-129">Data type</span></span>          | <span data-ttu-id="f3ae0-130">Unità</span><span class="sxs-lookup"><span data-stu-id="f3ae0-130">Unit</span></span>               | <span data-ttu-id="f3ae0-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="f3ae0-131">Supported values</span></span>                       | <span data-ttu-id="f3ae0-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f3ae0-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ae0-133">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="f3ae0-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="f3ae0-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3ae0-134">integer</span></span><br/> | <span data-ttu-id="f3ae0-135">Micron</span><span class="sxs-lookup"><span data-stu-id="f3ae0-135">microns</span></span><br/> | <span data-ttu-id="f3ae0-136">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="f3ae0-137">Specifica la dimensione orizzontale delle dimensioni dei supporti dell'applicazione rispetto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="f3ae0-138">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="f3ae0-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="f3ae0-139">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3ae0-139">integer</span></span><br/> | <span data-ttu-id="f3ae0-140">Micron</span><span class="sxs-lookup"><span data-stu-id="f3ae0-140">microns</span></span><br/> | <span data-ttu-id="f3ae0-141">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="f3ae0-142">Specifica la dimensione verticale delle dimensioni dei supporti dell'applicazione rispetto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="f3ae0-143">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="f3ae0-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="f3ae0-144">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3ae0-144">integer</span></span><br/> | <span data-ttu-id="f3ae0-145">Micron</span><span class="sxs-lookup"><span data-stu-id="f3ae0-145">microns</span></span><br/> | <span data-ttu-id="f3ae0-146">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="f3ae0-147">Specifica l'origine orizzontale dell'area immagine rispetto alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="f3ae0-148">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="f3ae0-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="f3ae0-149">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3ae0-149">integer</span></span><br/> | <span data-ttu-id="f3ae0-150">Micron</span><span class="sxs-lookup"><span data-stu-id="f3ae0-150">microns</span></span><br/> | <span data-ttu-id="f3ae0-151">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="f3ae0-152">Specifica l'origine verticale dell'area immagine rispetto alle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="f3ae0-153">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="f3ae0-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="f3ae0-154">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3ae0-154">integer</span></span><br/> | <span data-ttu-id="f3ae0-155">Micron</span><span class="sxs-lookup"><span data-stu-id="f3ae0-155">microns</span></span><br/> | <span data-ttu-id="f3ae0-156">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="f3ae0-157">Specifica la distanza orizzontale tra l'origine e il limite di delimitazione delle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="f3ae0-158">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="f3ae0-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="f3ae0-159">numero intero</span><span class="sxs-lookup"><span data-stu-id="f3ae0-159">integer</span></span><br/> | <span data-ttu-id="f3ae0-160">Micron</span><span class="sxs-lookup"><span data-stu-id="f3ae0-160">microns</span></span><br/> | <span data-ttu-id="f3ae0-161">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="f3ae0-162">Specifica la distanza verticale tra l'origine e il limite di delimitazione delle dimensioni del supporto dell'applicazione canvas.</span><span class="sxs-lookup"><span data-stu-id="f3ae0-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f3ae0-163">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f3ae0-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f3ae0-164">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="f3ae0-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f3ae0-165">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="f3ae0-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f3ae0-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3ae0-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3ae0-167">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f3ae0-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




