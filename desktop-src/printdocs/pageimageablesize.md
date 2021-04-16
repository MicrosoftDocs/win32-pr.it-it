---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104570616"
---
# <a name="pageimageablesize"></a><span data-ttu-id="3fceb-104">PageImageableSize dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="3fceb-104">PageImageableSize</span></span>

<span data-ttu-id="3fceb-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3fceb-105">This topic is not current.</span></span> <span data-ttu-id="3fceb-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3fceb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3fceb-107">Descrive l'area di disegno con immagine per il layout e il rendering.</span><span class="sxs-lookup"><span data-stu-id="3fceb-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="3fceb-108">Questa operazione verrà segnalata in base a PageMediaSize e PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="3fceb-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="3fceb-109">I diagrammi seguenti illustrano l'utilizzo delle variabili PageImageableSize dell'oggetto in base a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="3fceb-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![diagramma che mostra le misurazioni di pagina](images/local-1641910626-image.png)

-   [<span data-ttu-id="3fceb-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3fceb-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3fceb-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="3fceb-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3fceb-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3fceb-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3fceb-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3fceb-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="3fceb-115">Nome</span><span class="sxs-lookup"><span data-stu-id="3fceb-115">Name</span></span>                       |                     |
| <span data-ttu-id="3fceb-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="3fceb-116">Element Type</span></span><br/>    | <span data-ttu-id="3fceb-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fceb-117">Property</span></span><br/> |
| <span data-ttu-id="3fceb-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="3fceb-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3fceb-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="3fceb-119">Page</span></span><br/>     |
| <span data-ttu-id="3fceb-120">Note</span><span class="sxs-lookup"><span data-stu-id="3fceb-120">Notes</span></span> <br/>          | <span data-ttu-id="3fceb-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="3fceb-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3fceb-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="3fceb-122">Structural Content</span></span>

<span data-ttu-id="3fceb-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="3fceb-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3fceb-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="3fceb-124">Structure Variables</span></span>

<span data-ttu-id="3fceb-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="3fceb-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3fceb-126">Nome</span><span class="sxs-lookup"><span data-stu-id="3fceb-126">Name</span></span>                                    | <span data-ttu-id="3fceb-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3fceb-127">Data type</span></span>          | <span data-ttu-id="3fceb-128">Unità</span><span class="sxs-lookup"><span data-stu-id="3fceb-128">Unit</span></span>               | <span data-ttu-id="3fceb-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="3fceb-129">Supported values</span></span>                       | <span data-ttu-id="3fceb-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="3fceb-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fceb-131">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="3fceb-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="3fceb-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="3fceb-132">integer</span></span><br/> | <span data-ttu-id="3fceb-133">micron</span><span class="sxs-lookup"><span data-stu-id="3fceb-133">microns</span></span><br/> | <span data-ttu-id="3fceb-134">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="3fceb-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="3fceb-135">Specifica la dimensione orizzontale della dimensione del supporto dell'applicazione rispetto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="3fceb-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="3fceb-136">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="3fceb-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="3fceb-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="3fceb-137">integer</span></span><br/> | <span data-ttu-id="3fceb-138">micron</span><span class="sxs-lookup"><span data-stu-id="3fceb-138">microns</span></span><br/> | <span data-ttu-id="3fceb-139">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="3fceb-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="3fceb-140">Specifica la dimensione verticale della dimensione del supporto dell'applicazione rispetto a PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="3fceb-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="3fceb-141">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="3fceb-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="3fceb-142">numero intero</span><span class="sxs-lookup"><span data-stu-id="3fceb-142">integer</span></span><br/> | <span data-ttu-id="3fceb-143">micron</span><span class="sxs-lookup"><span data-stu-id="3fceb-143">microns</span></span><br/> | <span data-ttu-id="3fceb-144">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="3fceb-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="3fceb-145">Specifica l'origine orizzontale dell'area stampabile rispetto alla dimensione del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3fceb-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="3fceb-146">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="3fceb-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="3fceb-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="3fceb-147">integer</span></span><br/> | <span data-ttu-id="3fceb-148">micron</span><span class="sxs-lookup"><span data-stu-id="3fceb-148">microns</span></span><br/> | <span data-ttu-id="3fceb-149">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="3fceb-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="3fceb-150">Specifica l'origine verticale dell'area stampabile rispetto alla dimensione del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3fceb-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="3fceb-151">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="3fceb-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="3fceb-152">numero intero</span><span class="sxs-lookup"><span data-stu-id="3fceb-152">integer</span></span><br/> | <span data-ttu-id="3fceb-153">micron</span><span class="sxs-lookup"><span data-stu-id="3fceb-153">microns</span></span><br/> | <span data-ttu-id="3fceb-154">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="3fceb-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="3fceb-155">Specifica la distanza orizzontale tra l'origine e il limite delimitatore delle dimensioni del supporto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3fceb-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="3fceb-156">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="3fceb-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="3fceb-157">numero intero</span><span class="sxs-lookup"><span data-stu-id="3fceb-157">integer</span></span><br/> | <span data-ttu-id="3fceb-158">micron</span><span class="sxs-lookup"><span data-stu-id="3fceb-158">microns</span></span><br/> | <span data-ttu-id="3fceb-159">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="3fceb-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="3fceb-160">Specifica la distanza verticale tra l'origine e il limite delimitatore delle dimensioni del supporto dell'applicazione Canvas.</span><span class="sxs-lookup"><span data-stu-id="3fceb-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3fceb-161">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="3fceb-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3fceb-162">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3fceb-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3fceb-163">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="3fceb-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3fceb-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fceb-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fceb-165">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3fceb-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




