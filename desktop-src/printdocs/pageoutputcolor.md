---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234615"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="b14e4-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="b14e4-104">PageOutputColor</span></span>

<span data-ttu-id="b14e4-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b14e4-105">This topic is not current.</span></span> <span data-ttu-id="b14e4-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b14e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b14e4-107">Descrive le caratteristiche delle impostazioni dei colori per l'output.</span><span class="sxs-lookup"><span data-stu-id="b14e4-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="b14e4-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b14e4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b14e4-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b14e4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b14e4-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b14e4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b14e4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b14e4-111">Element Information</span></span>



| <span data-ttu-id="b14e4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b14e4-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="b14e4-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b14e4-113">Element Type</span></span> <br/>   | <span data-ttu-id="b14e4-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="b14e4-114">Feature</span></span><br/> |
| <span data-ttu-id="b14e4-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="b14e4-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b14e4-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="b14e4-116">Page</span></span><br/>    |
| <span data-ttu-id="b14e4-117">Note</span><span class="sxs-lookup"><span data-stu-id="b14e4-117">Notes</span></span> <br/>          | <span data-ttu-id="b14e4-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="b14e4-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b14e4-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b14e4-119">Structural Content</span></span>

<span data-ttu-id="b14e4-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b14e4-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b14e4-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="b14e4-121">Structure Variables</span></span>

<span data-ttu-id="b14e4-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b14e4-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b14e4-123">Nome</span><span class="sxs-lookup"><span data-stu-id="b14e4-123">Name</span></span>                                   | <span data-ttu-id="b14e4-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b14e4-124">Data type</span></span>          | <span data-ttu-id="b14e4-125">Unità</span><span class="sxs-lookup"><span data-stu-id="b14e4-125">Unit</span></span>                      | <span data-ttu-id="b14e4-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="b14e4-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b14e4-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="b14e4-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14e4-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b14e4-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="b14e4-129">string</span><span class="sxs-lookup"><span data-stu-id="b14e4-129">string</span></span><br/>  | <span data-ttu-id="b14e4-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="b14e4-130">characters</span></span><br/>     | <span data-ttu-id="b14e4-131">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b14e4-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b14e4-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="b14e4-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b14e4-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="b14e4-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="b14e4-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b14e4-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="b14e4-135">string</span><span class="sxs-lookup"><span data-stu-id="b14e4-135">string</span></span><br/>  | <span data-ttu-id="b14e4-136">n/d</span><span class="sxs-lookup"><span data-stu-id="b14e4-136">n/a</span></span><br/>            | <span data-ttu-id="b14e4-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="b14e4-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b14e4-138">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b14e4-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="b14e4-139">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="b14e4-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="b14e4-140">numero intero</span><span class="sxs-lookup"><span data-stu-id="b14e4-140">integer</span></span><br/> | <span data-ttu-id="b14e4-141">bit per pixel</span><span class="sxs-lookup"><span data-stu-id="b14e4-141">bits per pixel</span></span><br/> | <span data-ttu-id="b14e4-142">Maggiore di 0, minore del valore massimo per il supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14e4-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="b14e4-143">Valore numerico che indica il numero di bit per pixel dei dati di colore supportati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="b14e4-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="b14e4-144">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="b14e4-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="b14e4-145">numero intero</span><span class="sxs-lookup"><span data-stu-id="b14e4-145">integer</span></span><br/> | <span data-ttu-id="b14e4-146">bit per pixel</span><span class="sxs-lookup"><span data-stu-id="b14e4-146">bits per pixel</span></span><br/> | <span data-ttu-id="b14e4-147">Maggiore di 0, minore del valore massimo per il supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14e4-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="b14e4-148">Valore numerico che indica il numero di bit per pixel che il driver principale deve usare per il buffer di rendering bitmap.</span><span class="sxs-lookup"><span data-stu-id="b14e4-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b14e4-149">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="b14e4-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b14e4-150">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b14e4-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b14e4-151">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="b14e4-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b14e4-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b14e4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b14e4-153">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b14e4-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




