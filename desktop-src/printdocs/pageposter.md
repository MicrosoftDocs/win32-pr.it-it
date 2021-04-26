---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46cad46abcad7541f1282d691c950211bb7670c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996088"
---
# <a name="pageposter"></a><span data-ttu-id="a9ccc-104">PagePoster</span><span class="sxs-lookup"><span data-stu-id="a9ccc-104">PagePoster</span></span>

<span data-ttu-id="a9ccc-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-105">This topic is not current.</span></span> <span data-ttu-id="a9ccc-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a9ccc-107">Descrive l'output di una singola pagina in più fogli multimediali fisici.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-107">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="a9ccc-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a9ccc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a9ccc-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a9ccc-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a9ccc-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a9ccc-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a9ccc-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a9ccc-111">Element Information</span></span>



| <span data-ttu-id="a9ccc-112">Nome</span><span class="sxs-lookup"><span data-stu-id="a9ccc-112">Name</span></span> | <span data-ttu-id="a9ccc-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ccc-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a9ccc-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a9ccc-114">Element Type</span></span> <br/>   | <span data-ttu-id="a9ccc-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="a9ccc-115">Feature</span></span><br/> |
| <span data-ttu-id="a9ccc-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a9ccc-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a9ccc-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="a9ccc-117">Page</span></span><br/>    |
| <span data-ttu-id="a9ccc-118">Note</span><span class="sxs-lookup"><span data-stu-id="a9ccc-118">Notes</span></span> <br/>          | <span data-ttu-id="a9ccc-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="a9ccc-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a9ccc-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a9ccc-120">Structural Content</span></span>

<span data-ttu-id="a9ccc-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="a9ccc-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="a9ccc-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="a9ccc-122">Structure Variables</span></span>

<span data-ttu-id="a9ccc-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a9ccc-124">Nome</span><span class="sxs-lookup"><span data-stu-id="a9ccc-124">Name</span></span>                               | <span data-ttu-id="a9ccc-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a9ccc-125">Data type</span></span>          | <span data-ttu-id="a9ccc-126">Unità</span><span class="sxs-lookup"><span data-stu-id="a9ccc-126">Unit</span></span>                  | <span data-ttu-id="a9ccc-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="a9ccc-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a9ccc-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a9ccc-128">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a9ccc-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a9ccc-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a9ccc-130">string</span><span class="sxs-lookup"><span data-stu-id="a9ccc-130">string</span></span><br/>  | <span data-ttu-id="a9ccc-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="a9ccc-131">characters</span></span><br/> | <span data-ttu-id="a9ccc-132">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a9ccc-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a9ccc-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a9ccc-134">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="a9ccc-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="a9ccc-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a9ccc-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a9ccc-136">string</span><span class="sxs-lookup"><span data-stu-id="a9ccc-136">string</span></span><br/>  | <span data-ttu-id="a9ccc-137">n/d</span><span class="sxs-lookup"><span data-stu-id="a9ccc-137">n/a</span></span><br/>        | <span data-ttu-id="a9ccc-138">True, False</span><span class="sxs-lookup"><span data-stu-id="a9ccc-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="a9ccc-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="a9ccc-140">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="a9ccc-140">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="a9ccc-141">numero intero</span><span class="sxs-lookup"><span data-stu-id="a9ccc-141">integer</span></span><br/> | <span data-ttu-id="a9ccc-142">pagine</span><span class="sxs-lookup"><span data-stu-id="a9ccc-142">pages</span></span><br/>      | <span data-ttu-id="a9ccc-143">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-143">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="a9ccc-144">Specifica il numero di fogli fisici per pagina logica.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-144">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a9ccc-145">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a9ccc-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a9ccc-146">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="a9ccc-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a9ccc-147">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="a9ccc-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a9ccc-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9ccc-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9ccc-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a9ccc-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




