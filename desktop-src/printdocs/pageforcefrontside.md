---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e357cf59bca455102f6ca29bd66bc09455ee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234608"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="8d27f-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="8d27f-104">PageForceFrontSide</span></span>

<span data-ttu-id="8d27f-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8d27f-105">This topic is not current.</span></span> <span data-ttu-id="8d27f-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8d27f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d27f-107">Forza la visualizzazione dell'output sulla parte anteriore di un foglio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8d27f-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="8d27f-108">Pertinente per i fogli multimediali con superfici diverse su ciascun lato.</span><span class="sxs-lookup"><span data-stu-id="8d27f-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="8d27f-109">Nei casi in cui questa funzionalità interferisce con le opzioni di elaborazione, ad esempio DocumentDuplex, PageForceFrontSide ha la precedenza sulla pagina specifica a cui si applica la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8d27f-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="8d27f-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8d27f-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8d27f-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="8d27f-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8d27f-112">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="8d27f-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8d27f-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8d27f-113">Element Information</span></span>



| <span data-ttu-id="8d27f-114">Nome</span><span class="sxs-lookup"><span data-stu-id="8d27f-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="8d27f-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="8d27f-115">Element Type</span></span> <br/>   | <span data-ttu-id="8d27f-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="8d27f-116">Feature</span></span><br/> |
| <span data-ttu-id="8d27f-117">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="8d27f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8d27f-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="8d27f-118">Page</span></span><br/>    |
| <span data-ttu-id="8d27f-119">Note</span><span class="sxs-lookup"><span data-stu-id="8d27f-119">Notes</span></span> <br/>          | <span data-ttu-id="8d27f-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="8d27f-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="8d27f-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="8d27f-121">Structural Content</span></span>

<span data-ttu-id="8d27f-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="8d27f-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8d27f-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="8d27f-123">Structure Variables</span></span>

<span data-ttu-id="8d27f-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="8d27f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8d27f-125">Nome</span><span class="sxs-lookup"><span data-stu-id="8d27f-125">Name</span></span>                               | <span data-ttu-id="8d27f-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8d27f-126">Data type</span></span>         | <span data-ttu-id="8d27f-127">Unità</span><span class="sxs-lookup"><span data-stu-id="8d27f-127">Unit</span></span>                  | <span data-ttu-id="8d27f-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="8d27f-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8d27f-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="8d27f-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8d27f-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8d27f-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8d27f-131">string</span><span class="sxs-lookup"><span data-stu-id="8d27f-131">string</span></span><br/> | <span data-ttu-id="8d27f-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="8d27f-132">characters</span></span><br/> | <span data-ttu-id="8d27f-133">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8d27f-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8d27f-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8d27f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8d27f-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="8d27f-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8d27f-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8d27f-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8d27f-137">string</span><span class="sxs-lookup"><span data-stu-id="8d27f-137">string</span></span><br/> | <span data-ttu-id="8d27f-138">n/d</span><span class="sxs-lookup"><span data-stu-id="8d27f-138">n/a</span></span><br/>        | <span data-ttu-id="8d27f-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="8d27f-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8d27f-140">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8d27f-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8d27f-141">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="8d27f-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8d27f-142">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8d27f-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8d27f-143">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="8d27f-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8d27f-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d27f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d27f-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="8d27f-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




