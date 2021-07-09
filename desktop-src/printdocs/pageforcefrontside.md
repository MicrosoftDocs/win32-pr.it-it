---
description: Informazioni sull'elemento configurabile dall'utente PageForceFrontSide. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549189"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="96e1c-105">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="96e1c-105">PageForceFrontSide</span></span>

<span data-ttu-id="96e1c-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="96e1c-106">This topic is not current.</span></span> <span data-ttu-id="96e1c-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="96e1c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="96e1c-108">Forza la visualizzazione dell'output nella parte anteriore di un foglio multimediale.</span><span class="sxs-lookup"><span data-stu-id="96e1c-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="96e1c-109">Pertinente ai fogli multimediali con superfici diverse su ogni lato.</span><span class="sxs-lookup"><span data-stu-id="96e1c-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="96e1c-110">Nei casi in cui questa funzionalità interferisce con le opzioni di elaborazione(ad esempio DocumentDuplex), PageForceFrontSide ha la precedenza per la pagina specifica a cui si applica la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="96e1c-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="96e1c-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="96e1c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="96e1c-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="96e1c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="96e1c-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="96e1c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="96e1c-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="96e1c-114">Element Information</span></span>



| <span data-ttu-id="96e1c-115">Nome</span><span class="sxs-lookup"><span data-stu-id="96e1c-115">Name</span></span> | <span data-ttu-id="96e1c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="96e1c-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="96e1c-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="96e1c-117">Element Type</span></span> <br/>   | <span data-ttu-id="96e1c-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="96e1c-118">Feature</span></span><br/> |
| <span data-ttu-id="96e1c-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="96e1c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="96e1c-120">Pagina</span><span class="sxs-lookup"><span data-stu-id="96e1c-120">Page</span></span><br/>    |
| <span data-ttu-id="96e1c-121">Note</span><span class="sxs-lookup"><span data-stu-id="96e1c-121">Notes</span></span> <br/>          | <span data-ttu-id="96e1c-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="96e1c-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="96e1c-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="96e1c-123">Structural Content</span></span>

<span data-ttu-id="96e1c-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="96e1c-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="96e1c-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="96e1c-125">Structure Variables</span></span>

<span data-ttu-id="96e1c-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="96e1c-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="96e1c-127">Nome</span><span class="sxs-lookup"><span data-stu-id="96e1c-127">Name</span></span>                               | <span data-ttu-id="96e1c-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="96e1c-128">Data type</span></span>         | <span data-ttu-id="96e1c-129">Unità</span><span class="sxs-lookup"><span data-stu-id="96e1c-129">Unit</span></span>                  | <span data-ttu-id="96e1c-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="96e1c-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="96e1c-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="96e1c-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="96e1c-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="96e1c-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="96e1c-133">string</span><span class="sxs-lookup"><span data-stu-id="96e1c-133">string</span></span><br/> | <span data-ttu-id="96e1c-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="96e1c-134">characters</span></span><br/> | <span data-ttu-id="96e1c-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="96e1c-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="96e1c-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="96e1c-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="96e1c-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="96e1c-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="96e1c-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="96e1c-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="96e1c-139">string</span><span class="sxs-lookup"><span data-stu-id="96e1c-139">string</span></span><br/> | <span data-ttu-id="96e1c-140">n/d</span><span class="sxs-lookup"><span data-stu-id="96e1c-140">n/a</span></span><br/>        | <span data-ttu-id="96e1c-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="96e1c-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="96e1c-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="96e1c-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="96e1c-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="96e1c-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="96e1c-144">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="96e1c-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="96e1c-145">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="96e1c-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="96e1c-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96e1c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96e1c-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="96e1c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




