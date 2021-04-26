---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338a72baecc62d22ac63ef50d8ce8967c7fd534a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997038"
---
# <a name="documentstaple"></a><span data-ttu-id="05eb4-104">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="05eb4-104">DocumentStaple</span></span>

<span data-ttu-id="05eb4-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="05eb4-105">This topic is not current.</span></span> <span data-ttu-id="05eb4-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="05eb4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="05eb4-107">Descrive le caratteristiche di graffatura dell'output.</span><span class="sxs-lookup"><span data-stu-id="05eb4-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="05eb4-108">Ogni documento viene graffato separatamente.</span><span class="sxs-lookup"><span data-stu-id="05eb4-108">Each document is stapled separately.</span></span> <span data-ttu-id="05eb4-109">Le parole chiave JobStapleAllDocuments e DocumentStaple si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="05eb4-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="05eb4-110">Il driver deve determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="05eb4-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="05eb4-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="05eb4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="05eb4-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="05eb4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="05eb4-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="05eb4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="05eb4-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="05eb4-114">Element Information</span></span>



| <span data-ttu-id="05eb4-115">Nome</span><span class="sxs-lookup"><span data-stu-id="05eb4-115">Name</span></span> | <span data-ttu-id="05eb4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="05eb4-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="05eb4-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="05eb4-117">Element Type</span></span> <br/>   | <span data-ttu-id="05eb4-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="05eb4-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="05eb4-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="05eb4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="05eb4-120">Documento</span><span class="sxs-lookup"><span data-stu-id="05eb4-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="05eb4-121">Note</span><span class="sxs-lookup"><span data-stu-id="05eb4-121">Notes</span></span> <br/>          | <span data-ttu-id="05eb4-122">Top, Bottom, Left e Right sono relativi a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="05eb4-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="05eb4-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="05eb4-123">Structural Content</span></span>

<span data-ttu-id="05eb4-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="05eb4-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="05eb4-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="05eb4-125">Structure Variables</span></span>

<span data-ttu-id="05eb4-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="05eb4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="05eb4-127">Nome</span><span class="sxs-lookup"><span data-stu-id="05eb4-127">Name</span></span>                               | <span data-ttu-id="05eb4-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="05eb4-128">Data type</span></span>          | <span data-ttu-id="05eb4-129">Unità</span><span class="sxs-lookup"><span data-stu-id="05eb4-129">Unit</span></span>                       | <span data-ttu-id="05eb4-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="05eb4-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="05eb4-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="05eb4-131">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05eb4-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="05eb4-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="05eb4-133">string</span><span class="sxs-lookup"><span data-stu-id="05eb4-133">string</span></span><br/>  | <span data-ttu-id="05eb4-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="05eb4-134">characters</span></span><br/>      | <span data-ttu-id="05eb4-135">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="05eb4-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="05eb4-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="05eb4-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="05eb4-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="05eb4-137">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="05eb4-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="05eb4-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="05eb4-139">string</span><span class="sxs-lookup"><span data-stu-id="05eb4-139">string</span></span><br/>  | <span data-ttu-id="05eb4-140">n/d</span><span class="sxs-lookup"><span data-stu-id="05eb4-140">n/a</span></span><br/>             | <span data-ttu-id="05eb4-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="05eb4-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="05eb4-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="05eb4-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="05eb4-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="05eb4-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="05eb4-144">numero intero</span><span class="sxs-lookup"><span data-stu-id="05eb4-144">integer</span></span><br/> | <span data-ttu-id="05eb4-145">gradi</span><span class="sxs-lookup"><span data-stu-id="05eb4-145">degrees</span></span><br/>         | <span data-ttu-id="05eb4-146">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="05eb4-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="05eb4-147">Specifica l'angolo di graffatura rispetto alla direzione X di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="05eb4-147">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="05eb4-148">L'angolo di graffatura viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="05eb4-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="05eb4-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="05eb4-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="05eb4-150">numero intero</span><span class="sxs-lookup"><span data-stu-id="05eb4-150">integer</span></span><br/> | <span data-ttu-id="05eb4-151">fogli di supporti</span><span class="sxs-lookup"><span data-stu-id="05eb4-151">sheets of media</span></span><br/> | <span data-ttu-id="05eb4-152">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="05eb4-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="05eb4-153">Specifica il numero di fogli supportati dall'opzione di graffatura per l'oggetto MediaType attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="05eb4-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="05eb4-154">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="05eb4-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="05eb4-155">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="05eb4-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="05eb4-156">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="05eb4-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="05eb4-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05eb4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05eb4-158">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="05eb4-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




