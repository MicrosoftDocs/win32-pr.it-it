---
description: Informazioni sull'elemento JobStapleAllDocuments, che descrive le caratteristiche di graffatura dell'output.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2cda02c452ebb053c71811fb2642cea7371b2f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409134"
---
# <a name="documentstaple"></a><span data-ttu-id="058d1-103">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="058d1-103">DocumentStaple</span></span>

<span data-ttu-id="058d1-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="058d1-104">This topic is not current.</span></span> <span data-ttu-id="058d1-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="058d1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="058d1-106">Descrive le caratteristiche di graffatura dell'output.</span><span class="sxs-lookup"><span data-stu-id="058d1-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="058d1-107">Ogni documento viene graffato separatamente.</span><span class="sxs-lookup"><span data-stu-id="058d1-107">Each document is stapled separately.</span></span> <span data-ttu-id="058d1-108">Le parole chiave JobStapleAllDocuments e DocumentStaple si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="058d1-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="058d1-109">Il driver deve determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="058d1-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="058d1-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="058d1-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="058d1-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="058d1-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="058d1-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="058d1-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="058d1-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="058d1-113">Element Information</span></span>



| <span data-ttu-id="058d1-114">Nome</span><span class="sxs-lookup"><span data-stu-id="058d1-114">Name</span></span> | <span data-ttu-id="058d1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="058d1-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="058d1-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="058d1-116">Element Type</span></span> <br/>   | <span data-ttu-id="058d1-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="058d1-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="058d1-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="058d1-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="058d1-119">Documento</span><span class="sxs-lookup"><span data-stu-id="058d1-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="058d1-120">Note</span><span class="sxs-lookup"><span data-stu-id="058d1-120">Notes</span></span> <br/>          | <span data-ttu-id="058d1-121">Top, Bottom, Left e Right sono relativi a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="058d1-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="058d1-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="058d1-122">Structural Content</span></span>

<span data-ttu-id="058d1-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="058d1-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="058d1-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="058d1-124">Structure Variables</span></span>

<span data-ttu-id="058d1-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="058d1-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="058d1-126">Nome</span><span class="sxs-lookup"><span data-stu-id="058d1-126">Name</span></span>                               | <span data-ttu-id="058d1-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="058d1-127">Data type</span></span>          | <span data-ttu-id="058d1-128">Unità</span><span class="sxs-lookup"><span data-stu-id="058d1-128">Unit</span></span>                       | <span data-ttu-id="058d1-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="058d1-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="058d1-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="058d1-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058d1-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="058d1-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="058d1-132">string</span><span class="sxs-lookup"><span data-stu-id="058d1-132">string</span></span><br/>  | <span data-ttu-id="058d1-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="058d1-133">characters</span></span><br/>      | <span data-ttu-id="058d1-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="058d1-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="058d1-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="058d1-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="058d1-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="058d1-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="058d1-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="058d1-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="058d1-138">string</span><span class="sxs-lookup"><span data-stu-id="058d1-138">string</span></span><br/>  | <span data-ttu-id="058d1-139">n/d</span><span class="sxs-lookup"><span data-stu-id="058d1-139">n/a</span></span><br/>             | <span data-ttu-id="058d1-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="058d1-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="058d1-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="058d1-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="058d1-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="058d1-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="058d1-143">numero intero</span><span class="sxs-lookup"><span data-stu-id="058d1-143">integer</span></span><br/> | <span data-ttu-id="058d1-144">gradi</span><span class="sxs-lookup"><span data-stu-id="058d1-144">degrees</span></span><br/>         | <span data-ttu-id="058d1-145">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="058d1-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="058d1-146">Specifica l'angolo di graffatura rispetto alla direzione X di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="058d1-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="058d1-147">L'angolo di graffatura viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="058d1-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="058d1-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="058d1-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="058d1-149">numero intero</span><span class="sxs-lookup"><span data-stu-id="058d1-149">integer</span></span><br/> | <span data-ttu-id="058d1-150">fogli di supporti</span><span class="sxs-lookup"><span data-stu-id="058d1-150">sheets of media</span></span><br/> | <span data-ttu-id="058d1-151">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="058d1-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="058d1-152">Specifica il numero di fogli supportati dall'opzione di graffatura per l'oggetto MediaType attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="058d1-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="058d1-153">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="058d1-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="058d1-154">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi .</span><span class="sxs-lookup"><span data-stu-id="058d1-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="058d1-155">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="058d1-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="058d1-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="058d1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="058d1-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="058d1-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




