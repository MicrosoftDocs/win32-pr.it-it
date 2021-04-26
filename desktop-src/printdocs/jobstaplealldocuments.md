---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9abf6184c3164e0e5a1492911e15794ea7e1d948
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993908"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="bd38e-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="bd38e-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="bd38e-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="bd38e-105">This topic is not current.</span></span> <span data-ttu-id="bd38e-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bd38e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bd38e-107">Descrive le caratteristiche di graffatura dell'output.</span><span class="sxs-lookup"><span data-stu-id="bd38e-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="bd38e-108">Tutti i documenti nel processo vengono graffati insieme.</span><span class="sxs-lookup"><span data-stu-id="bd38e-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="bd38e-109">Le parole chiave JobStapleAllDocuments e DocumentStaple si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="bd38e-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="bd38e-110">Il driver deve determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="bd38e-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="bd38e-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bd38e-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bd38e-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bd38e-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bd38e-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bd38e-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bd38e-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bd38e-114">Element Information</span></span>



| <span data-ttu-id="bd38e-115">Nome</span><span class="sxs-lookup"><span data-stu-id="bd38e-115">Name</span></span> | <span data-ttu-id="bd38e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bd38e-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bd38e-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="bd38e-117">Element Type</span></span> <br/>   | <span data-ttu-id="bd38e-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="bd38e-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="bd38e-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="bd38e-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bd38e-120">Processo</span><span class="sxs-lookup"><span data-stu-id="bd38e-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="bd38e-121">Note</span><span class="sxs-lookup"><span data-stu-id="bd38e-121">Notes</span></span> <br/>          | <span data-ttu-id="bd38e-122">Top, Bottom, Left e Right sono relativi a PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="bd38e-122">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bd38e-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bd38e-123">Structural Content</span></span>

<span data-ttu-id="bd38e-124">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="bd38e-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="bd38e-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="bd38e-125">Structure Variables</span></span>

<span data-ttu-id="bd38e-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="bd38e-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bd38e-127">Nome</span><span class="sxs-lookup"><span data-stu-id="bd38e-127">Name</span></span>                               | <span data-ttu-id="bd38e-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bd38e-128">Data type</span></span>          | <span data-ttu-id="bd38e-129">Unità</span><span class="sxs-lookup"><span data-stu-id="bd38e-129">Unit</span></span>                       | <span data-ttu-id="bd38e-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="bd38e-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bd38e-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="bd38e-131">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd38e-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="bd38e-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bd38e-133">string</span><span class="sxs-lookup"><span data-stu-id="bd38e-133">string</span></span><br/>  | <span data-ttu-id="bd38e-134">Caratteri</span><span class="sxs-lookup"><span data-stu-id="bd38e-134">Characters</span></span><br/>      | <span data-ttu-id="bd38e-135">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="bd38e-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bd38e-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="bd38e-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bd38e-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="bd38e-137">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="bd38e-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bd38e-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bd38e-139">string</span><span class="sxs-lookup"><span data-stu-id="bd38e-139">string</span></span><br/>  | <span data-ttu-id="bd38e-140">n/d</span><span class="sxs-lookup"><span data-stu-id="bd38e-140">n/a</span></span><br/>             | <span data-ttu-id="bd38e-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="bd38e-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bd38e-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bd38e-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="bd38e-143">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="bd38e-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="bd38e-144">numero intero</span><span class="sxs-lookup"><span data-stu-id="bd38e-144">integer</span></span><br/> | <span data-ttu-id="bd38e-145">gradi</span><span class="sxs-lookup"><span data-stu-id="bd38e-145">degrees</span></span><br/>         | <span data-ttu-id="bd38e-146">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="bd38e-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="bd38e-147">Specifica l'angolo di graffatura rispetto alla larghezza di PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="bd38e-147">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="bd38e-148">L'angolo di graffatura viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="bd38e-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="bd38e-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="bd38e-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="bd38e-150">numero intero</span><span class="sxs-lookup"><span data-stu-id="bd38e-150">integer</span></span><br/> | <span data-ttu-id="bd38e-151">fogli di supporti</span><span class="sxs-lookup"><span data-stu-id="bd38e-151">sheets of media</span></span><br/> | <span data-ttu-id="bd38e-152">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="bd38e-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="bd38e-153">Specifica il numero di fogli supportati dall'opzione di graffatura per l'oggetto MediaType attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="bd38e-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bd38e-154">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bd38e-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bd38e-155">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="bd38e-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bd38e-156">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="bd38e-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
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

## <a name="related-topics"></a><span data-ttu-id="bd38e-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd38e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd38e-158">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="bd38e-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




