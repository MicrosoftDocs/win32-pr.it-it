---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d4bfb09a1c3f6f43f11886685a0edfcf2bbd92
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997048"
---
# <a name="documentrollcut"></a><span data-ttu-id="6264b-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="6264b-104">DocumentRollCut</span></span>

<span data-ttu-id="6264b-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6264b-105">This topic is not current.</span></span> <span data-ttu-id="6264b-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6264b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6264b-107">Descrive il metodo di taglio per la carta a rullo.</span><span class="sxs-lookup"><span data-stu-id="6264b-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="6264b-108">Ogni documento viene gestito separatamente.</span><span class="sxs-lookup"><span data-stu-id="6264b-108">Each document is handled separately.</span></span> <span data-ttu-id="6264b-109">Le opzioni specificate descrivono i diversi metodi per il roll cut.</span><span class="sxs-lookup"><span data-stu-id="6264b-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="6264b-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6264b-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6264b-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6264b-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6264b-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6264b-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6264b-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6264b-113">Element Information</span></span>



| <span data-ttu-id="6264b-114">Nome</span><span class="sxs-lookup"><span data-stu-id="6264b-114">Name</span></span> | <span data-ttu-id="6264b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6264b-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="6264b-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6264b-116">Element Type</span></span> <br/>   | <span data-ttu-id="6264b-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="6264b-117">Feature</span></span><br/>  |
| <span data-ttu-id="6264b-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6264b-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6264b-119">Documento</span><span class="sxs-lookup"><span data-stu-id="6264b-119">Document</span></span><br/> |
| <span data-ttu-id="6264b-120">Note</span><span class="sxs-lookup"><span data-stu-id="6264b-120">Notes</span></span> <br/>          | <span data-ttu-id="6264b-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="6264b-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="6264b-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6264b-122">Structural Content</span></span>

<span data-ttu-id="6264b-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6264b-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6264b-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6264b-124">Structure Variables</span></span>

<span data-ttu-id="6264b-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6264b-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6264b-126">Nome</span><span class="sxs-lookup"><span data-stu-id="6264b-126">Name</span></span>                               | <span data-ttu-id="6264b-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6264b-127">Data type</span></span>         | <span data-ttu-id="6264b-128">Unità</span><span class="sxs-lookup"><span data-stu-id="6264b-128">Unit</span></span>                  | <span data-ttu-id="6264b-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6264b-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6264b-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6264b-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6264b-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6264b-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6264b-132">string</span><span class="sxs-lookup"><span data-stu-id="6264b-132">string</span></span><br/> | <span data-ttu-id="6264b-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="6264b-133">characters</span></span><br/> | <span data-ttu-id="6264b-134">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6264b-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6264b-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6264b-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6264b-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6264b-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6264b-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6264b-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6264b-138">string</span><span class="sxs-lookup"><span data-stu-id="6264b-138">string</span></span><br/> | <span data-ttu-id="6264b-139">n/d</span><span class="sxs-lookup"><span data-stu-id="6264b-139">n/a</span></span><br/>        | <span data-ttu-id="6264b-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="6264b-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6264b-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6264b-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6264b-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6264b-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6264b-143">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="6264b-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6264b-144">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6264b-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6264b-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6264b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6264b-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6264b-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




