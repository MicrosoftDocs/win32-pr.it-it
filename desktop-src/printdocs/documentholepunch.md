---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825120996d0d488af347ed871386a12d7f8014a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997888"
---
# <a name="documentholepunch"></a><span data-ttu-id="2c37c-104">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="2c37c-104">DocumentHolePunch</span></span>

<span data-ttu-id="2c37c-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="2c37c-105">This topic is not current.</span></span> <span data-ttu-id="2c37c-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2c37c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c37c-107">Descrive le caratteristiche di foratura del foro dell'output.</span><span class="sxs-lookup"><span data-stu-id="2c37c-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="2c37c-108">Ogni documento viene perforato separatamente.</span><span class="sxs-lookup"><span data-stu-id="2c37c-108">Each document is punched separately.</span></span> <span data-ttu-id="2c37c-109">Le parole chiave JobHolePunch e DocumentHolePunch si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="2c37c-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="2c37c-110">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="2c37c-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="2c37c-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2c37c-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2c37c-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="2c37c-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2c37c-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2c37c-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2c37c-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2c37c-114">Element Information</span></span>



| <span data-ttu-id="2c37c-115">Nome</span><span class="sxs-lookup"><span data-stu-id="2c37c-115">Name</span></span> | <span data-ttu-id="2c37c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2c37c-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="2c37c-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="2c37c-117">Element Type</span></span> <br/>   | <span data-ttu-id="2c37c-118">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="2c37c-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="2c37c-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="2c37c-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2c37c-120">Documento</span><span class="sxs-lookup"><span data-stu-id="2c37c-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="2c37c-121">Note</span><span class="sxs-lookup"><span data-stu-id="2c37c-121">Notes</span></span> <br/>          | <span data-ttu-id="2c37c-122">Top, Bottom, Left e Right sono relativi a PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="2c37c-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2c37c-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="2c37c-123">Structural Content</span></span>

<span data-ttu-id="2c37c-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="2c37c-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2c37c-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="2c37c-125">Structure Variables</span></span>

<span data-ttu-id="2c37c-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="2c37c-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2c37c-127">Nome</span><span class="sxs-lookup"><span data-stu-id="2c37c-127">Name</span></span>                               | <span data-ttu-id="2c37c-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2c37c-128">Data type</span></span>         | <span data-ttu-id="2c37c-129">Unità</span><span class="sxs-lookup"><span data-stu-id="2c37c-129">Unit</span></span>                  | <span data-ttu-id="2c37c-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="2c37c-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2c37c-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="2c37c-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2c37c-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2c37c-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="2c37c-133">string</span><span class="sxs-lookup"><span data-stu-id="2c37c-133">string</span></span><br/> | <span data-ttu-id="2c37c-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="2c37c-134">characters</span></span><br/> | <span data-ttu-id="2c37c-135">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="2c37c-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2c37c-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c37c-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2c37c-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="2c37c-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2c37c-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2c37c-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="2c37c-139">string</span><span class="sxs-lookup"><span data-stu-id="2c37c-139">string</span></span><br/> | <span data-ttu-id="2c37c-140">n/d</span><span class="sxs-lookup"><span data-stu-id="2c37c-140">n/a</span></span><br/>        | <span data-ttu-id="2c37c-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="2c37c-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2c37c-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2c37c-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2c37c-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="2c37c-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2c37c-144">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="2c37c-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2c37c-145">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="2c37c-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2c37c-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c37c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c37c-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="2c37c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




