---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3576611dcdc746342b8ed1b2c3d7ebf8fb779
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103969019"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="0f5b0-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="0f5b0-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="0f5b0-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-105">This topic is not current.</span></span> <span data-ttu-id="0f5b0-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0f5b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0f5b0-107">Descrive le caratteristiche di graffatura dell'output.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="0f5b0-108">Tutti i documenti del processo vengono graffettati insieme.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="0f5b0-109">Le parole chiave JobStapleAllDocuments e DocumentStaple si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="0f5b0-110">Spetta al driver determinare la gestione dei vincoli tra queste parole chiave.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="0f5b0-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0f5b0-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0f5b0-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0f5b0-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0f5b0-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0f5b0-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0f5b0-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0f5b0-114">Element Information</span></span>



| <span data-ttu-id="0f5b0-115">Nome</span><span class="sxs-lookup"><span data-stu-id="0f5b0-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0f5b0-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0f5b0-116">Element Type</span></span> <br/>   | <span data-ttu-id="0f5b0-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="0f5b0-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="0f5b0-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="0f5b0-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0f5b0-119">Processo</span><span class="sxs-lookup"><span data-stu-id="0f5b0-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="0f5b0-120">Note</span><span class="sxs-lookup"><span data-stu-id="0f5b0-120">Notes</span></span> <br/>          | <span data-ttu-id="0f5b0-121">Top, Bottom, Left e Right sono relativi a PageImageableSize dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="0f5b0-121">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0f5b0-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0f5b0-122">Structural Content</span></span>

<span data-ttu-id="0f5b0-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="0f5b0-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0f5b0-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="0f5b0-124">Structure Variables</span></span>

<span data-ttu-id="0f5b0-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0f5b0-126">Nome</span><span class="sxs-lookup"><span data-stu-id="0f5b0-126">Name</span></span>                               | <span data-ttu-id="0f5b0-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0f5b0-127">Data type</span></span>          | <span data-ttu-id="0f5b0-128">Unità</span><span class="sxs-lookup"><span data-stu-id="0f5b0-128">Unit</span></span>                       | <span data-ttu-id="0f5b0-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="0f5b0-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0f5b0-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="0f5b0-130">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5b0-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0f5b0-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0f5b0-132">string</span><span class="sxs-lookup"><span data-stu-id="0f5b0-132">string</span></span><br/>  | <span data-ttu-id="0f5b0-133">Caratteri</span><span class="sxs-lookup"><span data-stu-id="0f5b0-133">Characters</span></span><br/>      | <span data-ttu-id="0f5b0-134">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0f5b0-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0f5b0-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0f5b0-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-136">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="0f5b0-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0f5b0-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0f5b0-138">string</span><span class="sxs-lookup"><span data-stu-id="0f5b0-138">string</span></span><br/>  | <span data-ttu-id="0f5b0-139">n/d</span><span class="sxs-lookup"><span data-stu-id="0f5b0-139">n/a</span></span><br/>             | <span data-ttu-id="0f5b0-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0f5b0-141">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="0f5b0-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="0f5b0-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="0f5b0-143">numero intero</span><span class="sxs-lookup"><span data-stu-id="0f5b0-143">integer</span></span><br/> | <span data-ttu-id="0f5b0-144">gradi</span><span class="sxs-lookup"><span data-stu-id="0f5b0-144">degrees</span></span><br/>         | <span data-ttu-id="0f5b0-145">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0f5b0-146">Specifica l'angolo della graffetta, relativo alla larghezza del PageImageableSize dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-146">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="0f5b0-147">L'angolo della graffetta viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="0f5b0-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="0f5b0-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="0f5b0-149">numero intero</span><span class="sxs-lookup"><span data-stu-id="0f5b0-149">integer</span></span><br/> | <span data-ttu-id="0f5b0-150">fogli di supporti</span><span class="sxs-lookup"><span data-stu-id="0f5b0-150">sheets of media</span></span><br/> | <span data-ttu-id="0f5b0-151">Maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="0f5b0-152">Specifica il numero di fogli supportati dall'opzione di pinzatura per il MediaType attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0f5b0-153">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="0f5b0-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0f5b0-154">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0f5b0-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0f5b0-155">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="0f5b0-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0f5b0-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f5b0-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f5b0-157">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0f5b0-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




