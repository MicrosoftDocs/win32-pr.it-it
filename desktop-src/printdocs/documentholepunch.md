---
description: Informazioni sull'elemento DocumentHolePunch, che descrive le caratteristiche di emissione del foro dell'output.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409293"
---
# <a name="documentholepunch"></a><span data-ttu-id="4ad9a-103">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="4ad9a-103">DocumentHolePunch</span></span>

<span data-ttu-id="4ad9a-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-104">This topic is not current.</span></span> <span data-ttu-id="4ad9a-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4ad9a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ad9a-106">Descrive le caratteristiche di emissione dei fori dell'output.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="4ad9a-107">Ogni documento viene esportato separatamente.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-107">Each document is punched separately.</span></span> <span data-ttu-id="4ad9a-108">Le parole chiave JobHolePunch e DocumentHolePunch si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="4ad9a-109">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="4ad9a-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4ad9a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4ad9a-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="4ad9a-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4ad9a-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4ad9a-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4ad9a-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4ad9a-113">Element Information</span></span>



| <span data-ttu-id="4ad9a-114">Nome</span><span class="sxs-lookup"><span data-stu-id="4ad9a-114">Name</span></span> | <span data-ttu-id="4ad9a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4ad9a-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="4ad9a-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="4ad9a-116">Element Type</span></span> <br/>   | <span data-ttu-id="4ad9a-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="4ad9a-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="4ad9a-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="4ad9a-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4ad9a-119">Documento</span><span class="sxs-lookup"><span data-stu-id="4ad9a-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="4ad9a-120">Note</span><span class="sxs-lookup"><span data-stu-id="4ad9a-120">Notes</span></span> <br/>          | <span data-ttu-id="4ad9a-121">Top, Bottom, Left e Right sono relativi a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4ad9a-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="4ad9a-122">Structural Content</span></span>

<span data-ttu-id="4ad9a-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="4ad9a-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="4ad9a-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="4ad9a-124">Structure Variables</span></span>

<span data-ttu-id="4ad9a-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4ad9a-126">Nome</span><span class="sxs-lookup"><span data-stu-id="4ad9a-126">Name</span></span>                               | <span data-ttu-id="4ad9a-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4ad9a-127">Data type</span></span>         | <span data-ttu-id="4ad9a-128">Unità</span><span class="sxs-lookup"><span data-stu-id="4ad9a-128">Unit</span></span>                  | <span data-ttu-id="4ad9a-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="4ad9a-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4ad9a-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="4ad9a-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4ad9a-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="4ad9a-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4ad9a-132">string</span><span class="sxs-lookup"><span data-stu-id="4ad9a-132">string</span></span><br/> | <span data-ttu-id="4ad9a-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="4ad9a-133">characters</span></span><br/> | <span data-ttu-id="4ad9a-134">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4ad9a-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4ad9a-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4ad9a-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4ad9a-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4ad9a-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4ad9a-138">string</span><span class="sxs-lookup"><span data-stu-id="4ad9a-138">string</span></span><br/> | <span data-ttu-id="4ad9a-139">n/d</span><span class="sxs-lookup"><span data-stu-id="4ad9a-139">n/a</span></span><br/>        | <span data-ttu-id="4ad9a-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4ad9a-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4ad9a-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4ad9a-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4ad9a-143">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="4ad9a-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4ad9a-144">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="4ad9a-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="4ad9a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ad9a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ad9a-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4ad9a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




