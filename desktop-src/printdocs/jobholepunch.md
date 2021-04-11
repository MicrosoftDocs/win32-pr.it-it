---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bcd709c6115a9f4af3084c28ca047950d1b81fd
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234596"
---
# <a name="jobholepunch"></a><span data-ttu-id="cbe6d-104">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="cbe6d-104">JobHolePunch</span></span>

<span data-ttu-id="cbe6d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-105">This topic is not current.</span></span> <span data-ttu-id="cbe6d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cbe6d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cbe6d-107">Descrive le caratteristiche di punzonatura dei fori dell'output.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="cbe6d-108">Tutti i documenti sono raggruppati.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-108">All documents are punched together.</span></span> <span data-ttu-id="cbe6d-109">Le parole chiave JobHolePunch e DocumentHolePunch si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="cbe6d-110">Non devono essere specificati contemporaneamente in un documento di funzionalità di stampa o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="cbe6d-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cbe6d-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cbe6d-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="cbe6d-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cbe6d-113">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cbe6d-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cbe6d-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cbe6d-114">Element Information</span></span>



| <span data-ttu-id="cbe6d-115">Nome</span><span class="sxs-lookup"><span data-stu-id="cbe6d-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe6d-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="cbe6d-116">Element Type</span></span> <br/>   | <span data-ttu-id="cbe6d-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="cbe6d-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="cbe6d-118">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="cbe6d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cbe6d-119">Processo</span><span class="sxs-lookup"><span data-stu-id="cbe6d-119">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="cbe6d-120">Note</span><span class="sxs-lookup"><span data-stu-id="cbe6d-120">Notes</span></span> <br/>          | <span data-ttu-id="cbe6d-121">In alto, in basso, a sinistra e a destra sono relativi a PageImageableSize dell'oggetto, dove la parte superiore è indicata dall'origine dell'asse x e dall'asse y.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-121">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="cbe6d-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="cbe6d-122">Structural Content</span></span>

<span data-ttu-id="cbe6d-123">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="cbe6d-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="cbe6d-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="cbe6d-124">Structure Variables</span></span>

<span data-ttu-id="cbe6d-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cbe6d-126">Nome</span><span class="sxs-lookup"><span data-stu-id="cbe6d-126">Name</span></span>                               | <span data-ttu-id="cbe6d-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cbe6d-127">Data type</span></span>         | <span data-ttu-id="cbe6d-128">Unità</span><span class="sxs-lookup"><span data-stu-id="cbe6d-128">Unit</span></span>                  | <span data-ttu-id="cbe6d-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="cbe6d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cbe6d-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="cbe6d-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cbe6d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cbe6d-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cbe6d-132">string</span><span class="sxs-lookup"><span data-stu-id="cbe6d-132">string</span></span><br/> | <span data-ttu-id="cbe6d-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="cbe6d-133">characters</span></span><br/> | <span data-ttu-id="cbe6d-134">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cbe6d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cbe6d-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cbe6d-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="cbe6d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cbe6d-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cbe6d-138">string</span><span class="sxs-lookup"><span data-stu-id="cbe6d-138">string</span></span><br/> | <span data-ttu-id="cbe6d-139">n/d</span><span class="sxs-lookup"><span data-stu-id="cbe6d-139">n/a</span></span><br/>        | <span data-ttu-id="cbe6d-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cbe6d-141">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cbe6d-142">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cbe6d-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cbe6d-143">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cbe6d-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cbe6d-144">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="cbe6d-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="cbe6d-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbe6d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbe6d-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="cbe6d-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




