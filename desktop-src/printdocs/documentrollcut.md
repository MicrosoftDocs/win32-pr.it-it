---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a20c02c50638d532660845efc1b3894f4a7e1
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234604"
---
# <a name="documentrollcut"></a><span data-ttu-id="6397e-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="6397e-104">DocumentRollCut</span></span>

<span data-ttu-id="6397e-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6397e-105">This topic is not current.</span></span> <span data-ttu-id="6397e-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6397e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6397e-107">Viene descritto il metodo di taglio per il Roll Paper.</span><span class="sxs-lookup"><span data-stu-id="6397e-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="6397e-108">Ogni documento viene gestito separatamente.</span><span class="sxs-lookup"><span data-stu-id="6397e-108">Each document is handled separately.</span></span> <span data-ttu-id="6397e-109">Le opzioni specificate descrivono i diversi metodi per il roll Cut.</span><span class="sxs-lookup"><span data-stu-id="6397e-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="6397e-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6397e-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6397e-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6397e-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6397e-112">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6397e-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6397e-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6397e-113">Element Information</span></span>



| <span data-ttu-id="6397e-114">Nome</span><span class="sxs-lookup"><span data-stu-id="6397e-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="6397e-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6397e-115">Element Type</span></span> <br/>   | <span data-ttu-id="6397e-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="6397e-116">Feature</span></span><br/>  |
| <span data-ttu-id="6397e-117">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="6397e-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6397e-118">Documento</span><span class="sxs-lookup"><span data-stu-id="6397e-118">Document</span></span><br/> |
| <span data-ttu-id="6397e-119">Note</span><span class="sxs-lookup"><span data-stu-id="6397e-119">Notes</span></span> <br/>          | <span data-ttu-id="6397e-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="6397e-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="6397e-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6397e-121">Structural Content</span></span>

<span data-ttu-id="6397e-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="6397e-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="6397e-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6397e-123">Structure Variables</span></span>

<span data-ttu-id="6397e-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6397e-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6397e-125">Nome</span><span class="sxs-lookup"><span data-stu-id="6397e-125">Name</span></span>                               | <span data-ttu-id="6397e-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6397e-126">Data type</span></span>         | <span data-ttu-id="6397e-127">Unità</span><span class="sxs-lookup"><span data-stu-id="6397e-127">Unit</span></span>                  | <span data-ttu-id="6397e-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6397e-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6397e-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6397e-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6397e-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6397e-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6397e-131">string</span><span class="sxs-lookup"><span data-stu-id="6397e-131">string</span></span><br/> | <span data-ttu-id="6397e-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="6397e-132">characters</span></span><br/> | <span data-ttu-id="6397e-133">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6397e-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6397e-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6397e-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6397e-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6397e-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6397e-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6397e-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6397e-137">string</span><span class="sxs-lookup"><span data-stu-id="6397e-137">string</span></span><br/> | <span data-ttu-id="6397e-138">n/d</span><span class="sxs-lookup"><span data-stu-id="6397e-138">n/a</span></span><br/>        | <span data-ttu-id="6397e-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="6397e-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6397e-140">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6397e-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6397e-141">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6397e-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6397e-142">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6397e-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6397e-143">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6397e-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="6397e-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6397e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6397e-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6397e-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




