---
description: Informazioni sull'elemento PageOutputColor configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548989"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="7d1e1-105">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="7d1e1-105">PageOutputColor</span></span>

<span data-ttu-id="7d1e1-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-106">This topic is not current.</span></span> <span data-ttu-id="7d1e1-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7d1e1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7d1e1-108">Descrive le caratteristiche delle impostazioni dei colori per l'output.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="7d1e1-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7d1e1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7d1e1-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7d1e1-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7d1e1-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7d1e1-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7d1e1-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7d1e1-112">Element Information</span></span>



| <span data-ttu-id="7d1e1-113">Nome</span><span class="sxs-lookup"><span data-stu-id="7d1e1-113">Name</span></span> | <span data-ttu-id="7d1e1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7d1e1-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7d1e1-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7d1e1-115">Element Type</span></span> <br/>   | <span data-ttu-id="7d1e1-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="7d1e1-116">Feature</span></span><br/> |
| <span data-ttu-id="7d1e1-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7d1e1-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7d1e1-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="7d1e1-118">Page</span></span><br/>    |
| <span data-ttu-id="7d1e1-119">Note</span><span class="sxs-lookup"><span data-stu-id="7d1e1-119">Notes</span></span> <br/>          | <span data-ttu-id="7d1e1-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="7d1e1-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7d1e1-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7d1e1-121">Structural Content</span></span>

<span data-ttu-id="7d1e1-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7d1e1-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7d1e1-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="7d1e1-123">Structure Variables</span></span>

<span data-ttu-id="7d1e1-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7d1e1-125">Nome</span><span class="sxs-lookup"><span data-stu-id="7d1e1-125">Name</span></span>                                   | <span data-ttu-id="7d1e1-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7d1e1-126">Data type</span></span>          | <span data-ttu-id="7d1e1-127">Unità</span><span class="sxs-lookup"><span data-stu-id="7d1e1-127">Unit</span></span>                      | <span data-ttu-id="7d1e1-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="7d1e1-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7d1e1-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7d1e1-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d1e1-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7d1e1-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="7d1e1-131">string</span><span class="sxs-lookup"><span data-stu-id="7d1e1-131">string</span></span><br/>  | <span data-ttu-id="7d1e1-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="7d1e1-132">characters</span></span><br/>     | <span data-ttu-id="7d1e1-133">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7d1e1-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7d1e1-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7d1e1-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="7d1e1-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7d1e1-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="7d1e1-137">string</span><span class="sxs-lookup"><span data-stu-id="7d1e1-137">string</span></span><br/>  | <span data-ttu-id="7d1e1-138">n/d</span><span class="sxs-lookup"><span data-stu-id="7d1e1-138">n/a</span></span><br/>            | <span data-ttu-id="7d1e1-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7d1e1-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="7d1e1-141">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="7d1e1-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="7d1e1-142">numero intero</span><span class="sxs-lookup"><span data-stu-id="7d1e1-142">integer</span></span><br/> | <span data-ttu-id="7d1e1-143">bit per pixel</span><span class="sxs-lookup"><span data-stu-id="7d1e1-143">bits per pixel</span></span><br/> | <span data-ttu-id="7d1e1-144">Maggiore di 0, minore del valore massimo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="7d1e1-145">Valore numerico che indica il numero di bit per pixel dei dati di colore supportati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="7d1e1-146">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="7d1e1-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="7d1e1-147">numero intero</span><span class="sxs-lookup"><span data-stu-id="7d1e1-147">integer</span></span><br/> | <span data-ttu-id="7d1e1-148">bit per pixel</span><span class="sxs-lookup"><span data-stu-id="7d1e1-148">bits per pixel</span></span><br/> | <span data-ttu-id="7d1e1-149">Maggiore di 0, minore del valore massimo di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="7d1e1-150">Valore numerico che indica il numero di bit per pixel che il driver principale deve usare per il buffer di rendering della bitmap.</span><span class="sxs-lookup"><span data-stu-id="7d1e1-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7d1e1-151">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7d1e1-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7d1e1-152">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="7d1e1-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7d1e1-153">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="7d1e1-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7d1e1-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d1e1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d1e1-155">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7d1e1-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




