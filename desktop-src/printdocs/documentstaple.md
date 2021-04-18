---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9fe7edd7385761e779980cf5d1dbea7a979a1f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321108"
---
# <a name="documentstaple"></a><span data-ttu-id="5da2e-104">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="5da2e-104">DocumentStaple</span></span>

<span data-ttu-id="5da2e-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5da2e-105">This topic is not current.</span></span> <span data-ttu-id="5da2e-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5da2e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5da2e-107">Descrive le caratteristiche di graffatura dell'output.</span><span class="sxs-lookup"><span data-stu-id="5da2e-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="5da2e-108">Ogni documento viene pinzato separatamente.</span><span class="sxs-lookup"><span data-stu-id="5da2e-108">Each document is stapled separately.</span></span> <span data-ttu-id="5da2e-109">Le parole chiave JobStapleAllDocuments e DocumentStaple si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="5da2e-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="5da2e-110">Spetta al driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="5da2e-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="5da2e-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5da2e-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5da2e-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5da2e-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5da2e-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5da2e-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5da2e-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5da2e-114">Element Information</span></span>



| <span data-ttu-id="5da2e-115">Nome</span><span class="sxs-lookup"><span data-stu-id="5da2e-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5da2e-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5da2e-116">Element Type</span></span> <br/>   | <span data-ttu-id="5da2e-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5da2e-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="5da2e-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="5da2e-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5da2e-119">Documento</span><span class="sxs-lookup"><span data-stu-id="5da2e-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="5da2e-120">Note</span><span class="sxs-lookup"><span data-stu-id="5da2e-120">Notes</span></span> <br/>          | <span data-ttu-id="5da2e-121">Top, Bottom, Left e Right sono relativi a PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5da2e-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5da2e-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5da2e-122">Structural Content</span></span>

<span data-ttu-id="5da2e-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="5da2e-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="5da2e-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="5da2e-124">Structure Variables</span></span>

<span data-ttu-id="5da2e-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5da2e-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5da2e-126">Nome</span><span class="sxs-lookup"><span data-stu-id="5da2e-126">Name</span></span>                               | <span data-ttu-id="5da2e-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5da2e-127">Data type</span></span>          | <span data-ttu-id="5da2e-128">Unità</span><span class="sxs-lookup"><span data-stu-id="5da2e-128">Unit</span></span>                       | <span data-ttu-id="5da2e-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="5da2e-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5da2e-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5da2e-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da2e-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5da2e-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5da2e-132">string</span><span class="sxs-lookup"><span data-stu-id="5da2e-132">string</span></span><br/>  | <span data-ttu-id="5da2e-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="5da2e-133">characters</span></span><br/>      | <span data-ttu-id="5da2e-134">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5da2e-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5da2e-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5da2e-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5da2e-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5da2e-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="5da2e-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5da2e-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5da2e-138">string</span><span class="sxs-lookup"><span data-stu-id="5da2e-138">string</span></span><br/>  | <span data-ttu-id="5da2e-139">n/d</span><span class="sxs-lookup"><span data-stu-id="5da2e-139">n/a</span></span><br/>             | <span data-ttu-id="5da2e-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="5da2e-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5da2e-141">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5da2e-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="5da2e-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="5da2e-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="5da2e-143">numero intero</span><span class="sxs-lookup"><span data-stu-id="5da2e-143">integer</span></span><br/> | <span data-ttu-id="5da2e-144">gradi</span><span class="sxs-lookup"><span data-stu-id="5da2e-144">degrees</span></span><br/>         | <span data-ttu-id="5da2e-145">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="5da2e-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="5da2e-146">Specifica l'angolo di sutura, relativo alla direzione X di PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5da2e-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="5da2e-147">L'angolo della graffetta viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="5da2e-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="5da2e-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="5da2e-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="5da2e-149">numero intero</span><span class="sxs-lookup"><span data-stu-id="5da2e-149">integer</span></span><br/> | <span data-ttu-id="5da2e-150">fogli di supporti</span><span class="sxs-lookup"><span data-stu-id="5da2e-150">sheets of media</span></span><br/> | <span data-ttu-id="5da2e-151">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="5da2e-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="5da2e-152">Specifica il numero di fogli supportati dall'opzione di pinzatura per il MediaType attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="5da2e-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5da2e-153">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="5da2e-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5da2e-154">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5da2e-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5da2e-155">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="5da2e-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None" />
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5da2e-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5da2e-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da2e-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5da2e-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




