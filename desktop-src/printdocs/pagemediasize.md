---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 6f99f54b-c401-42ea-8715-95a2aad73042
title: Pagemediasize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbaef403027190676b57455aa460198c2868424
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995520"
---
# <a name="pagemediasize"></a><span data-ttu-id="ef66d-104">Pagemediasize</span><span class="sxs-lookup"><span data-stu-id="ef66d-104">PageMediaSize</span></span>

<span data-ttu-id="ef66d-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ef66d-105">This topic is not current.</span></span> <span data-ttu-id="ef66d-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ef66d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ef66d-107">Descrive le dimensioni dei supporti fisici usati per l'output.</span><span class="sxs-lookup"><span data-stu-id="ef66d-107">Describes the physical media dimensions used for the output.</span></span>

<span data-ttu-id="ef66d-108">Il diagramma seguente illustra l'utilizzo della variabile PageMediaSize (come esempio viene usata l'opzione ISOA4).</span><span class="sxs-lookup"><span data-stu-id="ef66d-108">The following diagram illustrates the PageMediaSize variable usage (option ISOA4 is used as an example).</span></span>

![diagramma che mostra le dimensioni della pagina](images/local-1594393517-pagemediasizepic.gif)

-   [<span data-ttu-id="ef66d-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ef66d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ef66d-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ef66d-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ef66d-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ef66d-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ef66d-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ef66d-113">Element Information</span></span>



|                            |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ef66d-114">Nome</span><span class="sxs-lookup"><span data-stu-id="ef66d-114">Name</span></span> | <span data-ttu-id="ef66d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ef66d-115">Value</span></span> |
| <span data-ttu-id="ef66d-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ef66d-116">Element Type</span></span> <br/>   | <span data-ttu-id="ef66d-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="ef66d-117">Feature</span></span><br/> |
| <span data-ttu-id="ef66d-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="ef66d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ef66d-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="ef66d-119">Page</span></span><br/>    |
| <span data-ttu-id="ef66d-120">Note</span><span class="sxs-lookup"><span data-stu-id="ef66d-120">Notes</span></span> <br/>          | <span data-ttu-id="ef66d-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="ef66d-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ef66d-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ef66d-122">Structural Content</span></span>

<span data-ttu-id="ef66d-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="ef66d-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">_MediaSizeWidth_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">_MediaSizeHeight_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="ef66d-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ef66d-124">Structure Variables</span></span>

<span data-ttu-id="ef66d-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ef66d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ef66d-126">Nome</span><span class="sxs-lookup"><span data-stu-id="ef66d-126">Name</span></span>                                | <span data-ttu-id="ef66d-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ef66d-127">Data type</span></span>          | <span data-ttu-id="ef66d-128">Unità</span><span class="sxs-lookup"><span data-stu-id="ef66d-128">Unit</span></span>                  | <span data-ttu-id="ef66d-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ef66d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ef66d-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ef66d-130">Summary</span></span>                                                                                                                                                                   |
|-------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef66d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-131">\_OptionName\_</span></span><br/>           | <span data-ttu-id="ef66d-132">string</span><span class="sxs-lookup"><span data-stu-id="ef66d-132">string</span></span><br/>  | <span data-ttu-id="ef66d-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="ef66d-133">characters</span></span><br/> | <span data-ttu-id="ef66d-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ef66d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ef66d-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ef66d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ef66d-136">Specifica il nome del supporto.</span><span class="sxs-lookup"><span data-stu-id="ef66d-136">Specifies the name of the media.</span></span> <span data-ttu-id="ef66d-137">La denominazione deve usare la convenzione seguente: " \_ OptionNameStandard \_ "" \_ OptionNameCommonName \_ "" \_ OptionNameDescriptor \_ ".</span><span class="sxs-lookup"><span data-stu-id="ef66d-137">The naming should use the following convention: "\_OptionNameStandard\_""\_OptionNameCommonName\_""\_OptionNameDescriptor\_".</span></span><br/> |
| <span data-ttu-id="ef66d-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-138">\_IdentityOptionValue\_</span></span><br/>  | <span data-ttu-id="ef66d-139">string</span><span class="sxs-lookup"><span data-stu-id="ef66d-139">string</span></span><br/>  | <span data-ttu-id="ef66d-140">n/d</span><span class="sxs-lookup"><span data-stu-id="ef66d-140">n/a</span></span><br/>        | <span data-ttu-id="ef66d-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="ef66d-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ef66d-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ef66d-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                              |
| <span data-ttu-id="ef66d-143">\_OptionNameStandard\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-143">\_OptionNameStandard\_</span></span><br/>   | <span data-ttu-id="ef66d-144">string</span><span class="sxs-lookup"><span data-stu-id="ef66d-144">string</span></span><br/>  | <span data-ttu-id="ef66d-145">caratteri</span><span class="sxs-lookup"><span data-stu-id="ef66d-145">characters</span></span><br/> | <span data-ttu-id="ef66d-146">'ISO', 'JIS', 'Japan', 'NorthAmerica', 'OtherMetric', 'PRC', none.</span><span class="sxs-lookup"><span data-stu-id="ef66d-146">'ISO', 'JIS', 'Japan', 'NorthAmerica', 'OtherMetric', 'PRC', none.</span></span><br/>                                                                                                         | <span data-ttu-id="ef66d-147">Indica se le dimensioni del supporto sono definite da uno standard specifico.</span><span class="sxs-lookup"><span data-stu-id="ef66d-147">Indicates if the media size is defined by a particular standard.</span></span><br/>                                                                                               |
| <span data-ttu-id="ef66d-148">\_OptionNameCommonName\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-148">\_OptionNameCommonName\_</span></span><br/> | <span data-ttu-id="ef66d-149">string</span><span class="sxs-lookup"><span data-stu-id="ef66d-149">string</span></span><br/>  | <span data-ttu-id="ef66d-150">caratteri</span><span class="sxs-lookup"><span data-stu-id="ef66d-150">characters</span></span><br/> | <span data-ttu-id="ef66d-151">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ef66d-151">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ef66d-152">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ef66d-152">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ef66d-153">Nome comune per le dimensioni del supporto.</span><span class="sxs-lookup"><span data-stu-id="ef66d-153">Common Name for the media size.</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ef66d-154">\_OptionNameDescriptor\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-154">\_OptionNameDescriptor\_</span></span><br/> | <span data-ttu-id="ef66d-155">string</span><span class="sxs-lookup"><span data-stu-id="ef66d-155">string</span></span><br/>  | <span data-ttu-id="ef66d-156">caratteri</span><span class="sxs-lookup"><span data-stu-id="ef66d-156">characters</span></span><br/> | <span data-ttu-id="ef66d-157">Big, Envelope, Extra, Plus, Postcard, Rotated, Sheet, 'none'.</span><span class="sxs-lookup"><span data-stu-id="ef66d-157">Big, Envelope, Extra, Plus, Postcard, Rotated, Sheet, 'none'.</span></span><br/>                                                                                                              | <span data-ttu-id="ef66d-158">Big, Envelope, Extra, Plus, Postcard, Rotated, Sheet, 'none'.</span><span class="sxs-lookup"><span data-stu-id="ef66d-158">Big, Envelope, Extra, Plus, Postcard, Rotated, Sheet, 'none'.</span></span><br/>                                                                                                  |
| <span data-ttu-id="ef66d-159">\_MediaSizeWidth\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-159">\_MediaSizeWidth\_</span></span><br/>       | <span data-ttu-id="ef66d-160">numero intero</span><span class="sxs-lookup"><span data-stu-id="ef66d-160">integer</span></span><br/> | <span data-ttu-id="ef66d-161">Micron</span><span class="sxs-lookup"><span data-stu-id="ef66d-161">microns</span></span><br/>    | <span data-ttu-id="ef66d-162">Maggiore di 0, minore delle dimensioni massime del supporto per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef66d-162">Greater than 0, less than maximum support media size for device.</span></span><br/>                                                                                                           | <span data-ttu-id="ef66d-163">Specifica la larghezza del supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="ef66d-163">Specifies the width of the physical media.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="ef66d-164">\_MediaSizeHeight\_</span><span class="sxs-lookup"><span data-stu-id="ef66d-164">\_MediaSizeHeight\_</span></span><br/>      | <span data-ttu-id="ef66d-165">numero intero</span><span class="sxs-lookup"><span data-stu-id="ef66d-165">integer</span></span><br/> | <span data-ttu-id="ef66d-166">Micron</span><span class="sxs-lookup"><span data-stu-id="ef66d-166">microns</span></span><br/>    | <span data-ttu-id="ef66d-167">Maggiore di 0, minore delle dimensioni massime del supporto per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef66d-167">Greater than 0, less than maximum support media size for device.</span></span><br/>                                                                                                           | <span data-ttu-id="ef66d-168">Specifica l'altezza del supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="ef66d-168">Specifies the height of the physical media.</span></span><br/>                                                                                                                    |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ef66d-169">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ef66d-169">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ef66d-170">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` nomi .</span><span class="sxs-lookup"><span data-stu-id="ef66d-170">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="ef66d-171">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="ef66d-171">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom media size.  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:CustomMediaSize">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom media size (PostScript specific).  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:PSCustomMediaSize">
    <!-- Specifies the height of the page parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeight">
      <psf:ParameterRef name="psk:PageMediaSizePSHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the offset parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeightOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSHeightOffset" />
    </psf:ScoredProperty>
    <!-- Specifies the orientation relative to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSOrientation">
      <psf:ParameterRef name="psk:PageMediaSizePSOrientation" />
    </psf:ScoredProperty>
    <!-- Specifies the width of the page perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidth">
      <psf:ParameterRef name="psk:PageMediaSizePSWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the offset perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidthOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSWidthOffset" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1189000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">26000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">322000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">445000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235500</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">174000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1414000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">31000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">201000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">276000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">28000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6C5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOSRA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">320000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">450000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanQuadrupleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">296000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1456000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">32000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x14">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica11x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica9x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureASheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureBSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1219200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1117600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaExecutive">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">184150</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">266700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanLegalFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanStandardFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegal">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegalExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetter">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterPlus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322326</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaMonarchEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNote">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">225425</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber11Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">263525</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber12Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120650</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber14Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">292100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaPersonalEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">92075</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaQuarto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">275000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaStatement">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">139700</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperA">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">227000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">356000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperB">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">305000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">487000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloid">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloidExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">296926</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA4Plus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA3Plus">
    - <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">329000</psf:Value>
    </psf:ScoredProperty>
    - <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">483000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricFolio">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricInviteEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricItalianEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KBig">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Roll04Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll06Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">152400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll08Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll12Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll15Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll18Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll22Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll24Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll30Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">762000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll36Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll54Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1371600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanLPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">89000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Japan2LPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">178000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">152400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica5x7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica8x10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x12">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica14x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">355600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:BusinessCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">55000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CreditCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">54000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">86000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>   
```

## <a name="related-topics"></a><span data-ttu-id="ef66d-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef66d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef66d-173">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ef66d-173">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
