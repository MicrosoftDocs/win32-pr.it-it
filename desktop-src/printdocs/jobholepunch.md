---
description: Ottenere informazioni sull'elemento configurabile dall'utente JobHolePunch. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549359"
---
# <a name="jobholepunch"></a><span data-ttu-id="54794-105">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="54794-105">JobHolePunch</span></span>

<span data-ttu-id="54794-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="54794-106">This topic is not current.</span></span> <span data-ttu-id="54794-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="54794-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54794-108">Descrive le caratteristiche di emissione del foro dell'output.</span><span class="sxs-lookup"><span data-stu-id="54794-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="54794-109">Tutti i documenti vengono riuniti insieme.</span><span class="sxs-lookup"><span data-stu-id="54794-109">All documents are punched together.</span></span> <span data-ttu-id="54794-110">Le parole chiave JobHolePunch e DocumentHolePunch si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="54794-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="54794-111">Entrambi non devono essere specificati contemporaneamente in un documento PrintTicket o Funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="54794-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="54794-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="54794-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="54794-113">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="54794-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="54794-114">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="54794-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="54794-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="54794-115">Element Information</span></span>



| <span data-ttu-id="54794-116">Nome</span><span class="sxs-lookup"><span data-stu-id="54794-116">Name</span></span> | <span data-ttu-id="54794-117">Valore</span><span class="sxs-lookup"><span data-stu-id="54794-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54794-118">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="54794-118">Element Type</span></span> <br/>   | <span data-ttu-id="54794-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="54794-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="54794-120">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="54794-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="54794-121">Processo</span><span class="sxs-lookup"><span data-stu-id="54794-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="54794-122">Note</span><span class="sxs-lookup"><span data-stu-id="54794-122">Notes</span></span> <br/>          | <span data-ttu-id="54794-123">Top, Bottom, Left e Right sono relativi a PageImageableSize, dove TopLeft è denotato dall'origine dell'asse x e dell'asse y.</span><span class="sxs-lookup"><span data-stu-id="54794-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="54794-124">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="54794-124">Structural Content</span></span>

<span data-ttu-id="54794-125">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="54794-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="54794-126">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="54794-126">Structure Variables</span></span>

<span data-ttu-id="54794-127">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="54794-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="54794-128">Nome</span><span class="sxs-lookup"><span data-stu-id="54794-128">Name</span></span>                               | <span data-ttu-id="54794-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="54794-129">Data type</span></span>         | <span data-ttu-id="54794-130">Unità</span><span class="sxs-lookup"><span data-stu-id="54794-130">Unit</span></span>                  | <span data-ttu-id="54794-131">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="54794-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="54794-132">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="54794-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="54794-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="54794-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="54794-134">string</span><span class="sxs-lookup"><span data-stu-id="54794-134">string</span></span><br/> | <span data-ttu-id="54794-135">caratteri</span><span class="sxs-lookup"><span data-stu-id="54794-135">characters</span></span><br/> | <span data-ttu-id="54794-136">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="54794-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="54794-137">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="54794-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="54794-138">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="54794-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="54794-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="54794-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="54794-140">string</span><span class="sxs-lookup"><span data-stu-id="54794-140">string</span></span><br/> | <span data-ttu-id="54794-141">n/d</span><span class="sxs-lookup"><span data-stu-id="54794-141">n/a</span></span><br/>        | <span data-ttu-id="54794-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="54794-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="54794-143">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="54794-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="54794-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="54794-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="54794-145">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="54794-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="54794-146">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="54794-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="54794-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54794-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54794-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="54794-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




