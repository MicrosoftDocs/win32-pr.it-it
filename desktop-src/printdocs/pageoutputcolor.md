---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4791ca4a53b8bdcc43a32c5c7aa5a1e38bbe1e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998048"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="b8748-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="b8748-104">PageOutputColor</span></span>

<span data-ttu-id="b8748-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b8748-105">This topic is not current.</span></span> <span data-ttu-id="b8748-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b8748-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b8748-107">Descrive le caratteristiche delle impostazioni del colore per l'output.</span><span class="sxs-lookup"><span data-stu-id="b8748-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="b8748-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b8748-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b8748-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b8748-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b8748-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b8748-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b8748-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b8748-111">Element Information</span></span>



| <span data-ttu-id="b8748-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b8748-112">Name</span></span> | <span data-ttu-id="b8748-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b8748-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b8748-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b8748-114">Element Type</span></span> <br/>   | <span data-ttu-id="b8748-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="b8748-115">Feature</span></span><br/> |
| <span data-ttu-id="b8748-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b8748-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b8748-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="b8748-117">Page</span></span><br/>    |
| <span data-ttu-id="b8748-118">Note</span><span class="sxs-lookup"><span data-stu-id="b8748-118">Notes</span></span> <br/>          | <span data-ttu-id="b8748-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="b8748-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b8748-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="b8748-120">Structural Content</span></span>

<span data-ttu-id="b8748-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b8748-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b8748-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="b8748-122">Structure Variables</span></span>

<span data-ttu-id="b8748-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b8748-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b8748-124">Nome</span><span class="sxs-lookup"><span data-stu-id="b8748-124">Name</span></span>                                   | <span data-ttu-id="b8748-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b8748-125">Data type</span></span>          | <span data-ttu-id="b8748-126">Unità</span><span class="sxs-lookup"><span data-stu-id="b8748-126">Unit</span></span>                      | <span data-ttu-id="b8748-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="b8748-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b8748-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="b8748-128">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8748-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b8748-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="b8748-130">string</span><span class="sxs-lookup"><span data-stu-id="b8748-130">string</span></span><br/>  | <span data-ttu-id="b8748-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="b8748-131">characters</span></span><br/>     | <span data-ttu-id="b8748-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="b8748-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b8748-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8748-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b8748-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="b8748-134">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="b8748-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b8748-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="b8748-136">string</span><span class="sxs-lookup"><span data-stu-id="b8748-136">string</span></span><br/>  | <span data-ttu-id="b8748-137">n/d</span><span class="sxs-lookup"><span data-stu-id="b8748-137">n/a</span></span><br/>            | <span data-ttu-id="b8748-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="b8748-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b8748-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b8748-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="b8748-140">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="b8748-140">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="b8748-141">numero intero</span><span class="sxs-lookup"><span data-stu-id="b8748-141">integer</span></span><br/> | <span data-ttu-id="b8748-142">bit per pixel</span><span class="sxs-lookup"><span data-stu-id="b8748-142">bits per pixel</span></span><br/> | <span data-ttu-id="b8748-143">Maggiore di 0, minore del valore massimo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8748-143">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="b8748-144">Valore numerico che indica il numero di bit per pixel dei dati di colore supportati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="b8748-144">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="b8748-145">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="b8748-145">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="b8748-146">numero intero</span><span class="sxs-lookup"><span data-stu-id="b8748-146">integer</span></span><br/> | <span data-ttu-id="b8748-147">bit per pixel</span><span class="sxs-lookup"><span data-stu-id="b8748-147">bits per pixel</span></span><br/> | <span data-ttu-id="b8748-148">Maggiore di 0, minore del valore massimo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8748-148">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="b8748-149">Valore numerico che indica il numero di bit per pixel che il driver principale deve usare per il buffer di rendering della bitmap.</span><span class="sxs-lookup"><span data-stu-id="b8748-149">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b8748-150">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="b8748-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b8748-151">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="b8748-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b8748-152">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="b8748-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b8748-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8748-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8748-154">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b8748-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




