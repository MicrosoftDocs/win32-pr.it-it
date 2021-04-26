---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6bd0d58c5b361b167d22c672b7e080e4498d3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997058"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="cf1c9-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="cf1c9-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="cf1c9-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-105">This topic is not current.</span></span> <span data-ttu-id="cf1c9-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cf1c9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cf1c9-107">Descrive l'utilizzo del foglio separatore per un documento.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="cf1c9-108">I fogli separatori dovrebbero essere visualizzati nell'output come indicato dall'opzione specificata di seguito.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="cf1c9-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cf1c9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cf1c9-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="cf1c9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cf1c9-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="cf1c9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cf1c9-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cf1c9-112">Element Information</span></span>



| <span data-ttu-id="cf1c9-113">Nome</span><span class="sxs-lookup"><span data-stu-id="cf1c9-113">Name</span></span> | <span data-ttu-id="cf1c9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cf1c9-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="cf1c9-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="cf1c9-115">Element Type</span></span> <br/>   | <span data-ttu-id="cf1c9-116">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="cf1c9-116">Feature</span></span><br/>  |
| <span data-ttu-id="cf1c9-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="cf1c9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cf1c9-118">Documento</span><span class="sxs-lookup"><span data-stu-id="cf1c9-118">Document</span></span><br/> |
| <span data-ttu-id="cf1c9-119">Note</span><span class="sxs-lookup"><span data-stu-id="cf1c9-119">Notes</span></span> <br/>          | <span data-ttu-id="cf1c9-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="cf1c9-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="cf1c9-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="cf1c9-121">Structural Content</span></span>

<span data-ttu-id="cf1c9-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="cf1c9-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="cf1c9-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="cf1c9-123">Structure Variables</span></span>

<span data-ttu-id="cf1c9-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cf1c9-125">Nome</span><span class="sxs-lookup"><span data-stu-id="cf1c9-125">Name</span></span>                               | <span data-ttu-id="cf1c9-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cf1c9-126">Data type</span></span>         | <span data-ttu-id="cf1c9-127">Unità</span><span class="sxs-lookup"><span data-stu-id="cf1c9-127">Unit</span></span>                  | <span data-ttu-id="cf1c9-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="cf1c9-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cf1c9-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="cf1c9-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cf1c9-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cf1c9-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cf1c9-131">string</span><span class="sxs-lookup"><span data-stu-id="cf1c9-131">string</span></span><br/> | <span data-ttu-id="cf1c9-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="cf1c9-132">characters</span></span><br/> | <span data-ttu-id="cf1c9-133">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="cf1c9-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cf1c9-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cf1c9-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="cf1c9-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cf1c9-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cf1c9-137">string</span><span class="sxs-lookup"><span data-stu-id="cf1c9-137">string</span></span><br/> | <span data-ttu-id="cf1c9-138">n/d</span><span class="sxs-lookup"><span data-stu-id="cf1c9-138">n/a</span></span><br/>        | <span data-ttu-id="cf1c9-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cf1c9-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cf1c9-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cf1c9-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="cf1c9-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cf1c9-142">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="cf1c9-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cf1c9-143">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="cf1c9-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="cf1c9-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf1c9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf1c9-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="cf1c9-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




