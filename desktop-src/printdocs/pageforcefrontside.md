---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e363050034137bcfb3ff2b779ecda05200865312
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996938"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="3b32f-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="3b32f-104">PageForceFrontSide</span></span>

<span data-ttu-id="3b32f-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="3b32f-105">This topic is not current.</span></span> <span data-ttu-id="3b32f-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3b32f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3b32f-107">Forza la visualizzazione dell'output nella parte anteriore di un foglio multimediale.</span><span class="sxs-lookup"><span data-stu-id="3b32f-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="3b32f-108">Pertinente ai fogli multimediali con superfici diverse su ogni lato.</span><span class="sxs-lookup"><span data-stu-id="3b32f-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="3b32f-109">Nei casi in cui questa funzionalità interferisce con le opzioni di elaborazione (ad esempio DocumentDuplex), PageForceFrontSide ha la precedenza per la pagina specifica a cui si applica la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3b32f-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="3b32f-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3b32f-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3b32f-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="3b32f-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3b32f-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3b32f-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3b32f-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3b32f-113">Element Information</span></span>



| <span data-ttu-id="3b32f-114">Nome</span><span class="sxs-lookup"><span data-stu-id="3b32f-114">Name</span></span> | <span data-ttu-id="3b32f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3b32f-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="3b32f-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="3b32f-116">Element Type</span></span> <br/>   | <span data-ttu-id="3b32f-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="3b32f-117">Feature</span></span><br/> |
| <span data-ttu-id="3b32f-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="3b32f-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3b32f-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="3b32f-119">Page</span></span><br/>    |
| <span data-ttu-id="3b32f-120">Note</span><span class="sxs-lookup"><span data-stu-id="3b32f-120">Notes</span></span> <br/>          | <span data-ttu-id="3b32f-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="3b32f-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="3b32f-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="3b32f-122">Structural Content</span></span>

<span data-ttu-id="3b32f-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="3b32f-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="3b32f-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="3b32f-124">Structure Variables</span></span>

<span data-ttu-id="3b32f-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="3b32f-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3b32f-126">Nome</span><span class="sxs-lookup"><span data-stu-id="3b32f-126">Name</span></span>                               | <span data-ttu-id="3b32f-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3b32f-127">Data type</span></span>         | <span data-ttu-id="3b32f-128">Unità</span><span class="sxs-lookup"><span data-stu-id="3b32f-128">Unit</span></span>                  | <span data-ttu-id="3b32f-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="3b32f-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3b32f-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="3b32f-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3b32f-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="3b32f-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3b32f-132">string</span><span class="sxs-lookup"><span data-stu-id="3b32f-132">string</span></span><br/> | <span data-ttu-id="3b32f-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="3b32f-133">characters</span></span><br/> | <span data-ttu-id="3b32f-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="3b32f-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3b32f-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="3b32f-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3b32f-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="3b32f-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3b32f-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3b32f-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3b32f-138">string</span><span class="sxs-lookup"><span data-stu-id="3b32f-138">string</span></span><br/> | <span data-ttu-id="3b32f-139">n/d</span><span class="sxs-lookup"><span data-stu-id="3b32f-139">n/a</span></span><br/>        | <span data-ttu-id="3b32f-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="3b32f-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3b32f-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3b32f-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3b32f-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3b32f-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3b32f-143">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="3b32f-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3b32f-144">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="3b32f-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="3b32f-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b32f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b32f-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3b32f-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




