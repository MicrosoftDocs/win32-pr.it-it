---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 1e2cd767-685b-47d8-9020-a0a5dda63506
title: JobRollCutAtEndOfJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178b045546552048b2a66a1c0824645c1720b1a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993938"
---
# <a name="jobrollcutatendofjob"></a><span data-ttu-id="d78a3-104">JobRollCutAtEndOfJob</span><span class="sxs-lookup"><span data-stu-id="d78a3-104">JobRollCutAtEndOfJob</span></span>

<span data-ttu-id="d78a3-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="d78a3-105">This topic is not current.</span></span> <span data-ttu-id="d78a3-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d78a3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d78a3-107">Descrive il metodo di taglio per la carta rullo.</span><span class="sxs-lookup"><span data-stu-id="d78a3-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="d78a3-108">Il roll roll deve essere tagliato alla fine del processo.</span><span class="sxs-lookup"><span data-stu-id="d78a3-108">The roll should be cut at the end of the job.</span></span>

-   [<span data-ttu-id="d78a3-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d78a3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d78a3-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d78a3-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d78a3-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d78a3-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d78a3-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d78a3-112">Element Information</span></span>



| <span data-ttu-id="d78a3-113">Nome</span><span class="sxs-lookup"><span data-stu-id="d78a3-113">Name</span></span> | <span data-ttu-id="d78a3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d78a3-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d78a3-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d78a3-115">Element Type</span></span> <br/>   | <span data-ttu-id="d78a3-116">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="d78a3-116">Feature</span></span><br/> |
| <span data-ttu-id="d78a3-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="d78a3-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d78a3-118">Processo</span><span class="sxs-lookup"><span data-stu-id="d78a3-118">Job</span></span><br/>     |
| <span data-ttu-id="d78a3-119">Note</span><span class="sxs-lookup"><span data-stu-id="d78a3-119">Notes</span></span> <br/>          | <span data-ttu-id="d78a3-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="d78a3-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d78a3-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="d78a3-121">Structural Content</span></span>

<span data-ttu-id="d78a3-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="d78a3-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJobAtEndOfJob">
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

## <a name="structure-variables"></a><span data-ttu-id="d78a3-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="d78a3-123">Structure Variables</span></span>

<span data-ttu-id="d78a3-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="d78a3-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d78a3-125">Nome</span><span class="sxs-lookup"><span data-stu-id="d78a3-125">Name</span></span>                               | <span data-ttu-id="d78a3-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d78a3-126">Data type</span></span>         | <span data-ttu-id="d78a3-127">Unità</span><span class="sxs-lookup"><span data-stu-id="d78a3-127">Unit</span></span>                  | <span data-ttu-id="d78a3-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="d78a3-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d78a3-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="d78a3-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d78a3-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d78a3-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d78a3-131">string</span><span class="sxs-lookup"><span data-stu-id="d78a3-131">string</span></span><br/> | <span data-ttu-id="d78a3-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="d78a3-132">characters</span></span><br/> | <span data-ttu-id="d78a3-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d78a3-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d78a3-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="d78a3-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d78a3-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="d78a3-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d78a3-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d78a3-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d78a3-137">string</span><span class="sxs-lookup"><span data-stu-id="d78a3-137">string</span></span><br/> | <span data-ttu-id="d78a3-138">n/d</span><span class="sxs-lookup"><span data-stu-id="d78a3-138">n/a</span></span><br/>        | <span data-ttu-id="d78a3-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="d78a3-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d78a3-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d78a3-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d78a3-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="d78a3-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d78a3-142">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="d78a3-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d78a3-143">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="d78a3-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobRollCutAtEndOfJob">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies cutting at the edge of the image -->
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!--Specifies cutting for standard media size -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!--Specifies no job roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="d78a3-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d78a3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d78a3-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="d78a3-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




