---
description: Ottenere informazioni sull'elemento pagePoster configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548969"
---
# <a name="pageposter"></a><span data-ttu-id="0ab02-105">PagePoster</span><span class="sxs-lookup"><span data-stu-id="0ab02-105">PagePoster</span></span>

<span data-ttu-id="0ab02-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0ab02-106">This topic is not current.</span></span> <span data-ttu-id="0ab02-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0ab02-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0ab02-108">Descrive l'output di una singola pagina in più fogli multimediali fisici.</span><span class="sxs-lookup"><span data-stu-id="0ab02-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="0ab02-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0ab02-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0ab02-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0ab02-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0ab02-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0ab02-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0ab02-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0ab02-112">Element Information</span></span>



| <span data-ttu-id="0ab02-113">Nome</span><span class="sxs-lookup"><span data-stu-id="0ab02-113">Name</span></span> | <span data-ttu-id="0ab02-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0ab02-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0ab02-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0ab02-115">Element Type</span></span> <br/>   | <span data-ttu-id="0ab02-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="0ab02-116">Feature</span></span><br/> |
| <span data-ttu-id="0ab02-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0ab02-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0ab02-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="0ab02-118">Page</span></span><br/>    |
| <span data-ttu-id="0ab02-119">Note</span><span class="sxs-lookup"><span data-stu-id="0ab02-119">Notes</span></span> <br/>          | <span data-ttu-id="0ab02-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="0ab02-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0ab02-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="0ab02-121">Structural Content</span></span>

<span data-ttu-id="0ab02-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0ab02-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0ab02-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="0ab02-123">Structure Variables</span></span>

<span data-ttu-id="0ab02-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0ab02-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0ab02-125">Nome</span><span class="sxs-lookup"><span data-stu-id="0ab02-125">Name</span></span>                               | <span data-ttu-id="0ab02-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0ab02-126">Data type</span></span>          | <span data-ttu-id="0ab02-127">Unità</span><span class="sxs-lookup"><span data-stu-id="0ab02-127">Unit</span></span>                  | <span data-ttu-id="0ab02-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="0ab02-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0ab02-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="0ab02-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0ab02-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0ab02-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0ab02-131">string</span><span class="sxs-lookup"><span data-stu-id="0ab02-131">string</span></span><br/>  | <span data-ttu-id="0ab02-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="0ab02-132">characters</span></span><br/> | <span data-ttu-id="0ab02-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="0ab02-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0ab02-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="0ab02-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0ab02-135">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="0ab02-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="0ab02-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0ab02-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0ab02-137">string</span><span class="sxs-lookup"><span data-stu-id="0ab02-137">string</span></span><br/>  | <span data-ttu-id="0ab02-138">n/d</span><span class="sxs-lookup"><span data-stu-id="0ab02-138">n/a</span></span><br/>        | <span data-ttu-id="0ab02-139">True, False</span><span class="sxs-lookup"><span data-stu-id="0ab02-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="0ab02-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0ab02-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="0ab02-141">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="0ab02-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="0ab02-142">numero intero</span><span class="sxs-lookup"><span data-stu-id="0ab02-142">integer</span></span><br/> | <span data-ttu-id="0ab02-143">pagine</span><span class="sxs-lookup"><span data-stu-id="0ab02-143">pages</span></span><br/>      | <span data-ttu-id="0ab02-144">Maggiore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="0ab02-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="0ab02-145">Specifica il numero di fogli fisici per pagina logica.</span><span class="sxs-lookup"><span data-stu-id="0ab02-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0ab02-146">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="0ab02-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0ab02-147">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="0ab02-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0ab02-148">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="0ab02-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0ab02-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ab02-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ab02-150">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0ab02-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




