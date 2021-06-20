---
description: Informazioni sull'elemento DocumentSeparatorSheet, che descrive l'utilizzo del foglio separatore per un documento.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38195c2d1c52e5c02d9da4844b5fa981866a61bc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409164"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="4b326-103">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="4b326-103">DocumentSeparatorSheet</span></span>

<span data-ttu-id="4b326-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="4b326-104">This topic is not current.</span></span> <span data-ttu-id="4b326-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4b326-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b326-106">Descrive l'utilizzo del foglio separatore per un documento.</span><span class="sxs-lookup"><span data-stu-id="4b326-106">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="4b326-107">I fogli separatori dovrebbero essere visualizzati nell'output come indicato dall'opzione specificata di seguito.</span><span class="sxs-lookup"><span data-stu-id="4b326-107">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="4b326-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4b326-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4b326-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="4b326-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4b326-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4b326-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4b326-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4b326-111">Element Information</span></span>



| <span data-ttu-id="4b326-112">Nome</span><span class="sxs-lookup"><span data-stu-id="4b326-112">Name</span></span> | <span data-ttu-id="4b326-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4b326-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="4b326-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="4b326-114">Element Type</span></span> <br/>   | <span data-ttu-id="4b326-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="4b326-115">Feature</span></span><br/>  |
| <span data-ttu-id="4b326-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="4b326-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4b326-117">Documento</span><span class="sxs-lookup"><span data-stu-id="4b326-117">Document</span></span><br/> |
| <span data-ttu-id="4b326-118">Note</span><span class="sxs-lookup"><span data-stu-id="4b326-118">Notes</span></span> <br/>          | <span data-ttu-id="4b326-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="4b326-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="4b326-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="4b326-120">Structural Content</span></span>

<span data-ttu-id="4b326-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="4b326-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4b326-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="4b326-122">Structure Variables</span></span>

<span data-ttu-id="4b326-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="4b326-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4b326-124">Nome</span><span class="sxs-lookup"><span data-stu-id="4b326-124">Name</span></span>                               | <span data-ttu-id="4b326-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4b326-125">Data type</span></span>         | <span data-ttu-id="4b326-126">Unità</span><span class="sxs-lookup"><span data-stu-id="4b326-126">Unit</span></span>                  | <span data-ttu-id="4b326-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="4b326-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4b326-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="4b326-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4b326-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="4b326-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4b326-130">string</span><span class="sxs-lookup"><span data-stu-id="4b326-130">string</span></span><br/> | <span data-ttu-id="4b326-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="4b326-131">characters</span></span><br/> | <span data-ttu-id="4b326-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4b326-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4b326-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="4b326-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4b326-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="4b326-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4b326-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4b326-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4b326-136">string</span><span class="sxs-lookup"><span data-stu-id="4b326-136">string</span></span><br/> | <span data-ttu-id="4b326-137">n/d</span><span class="sxs-lookup"><span data-stu-id="4b326-137">n/a</span></span><br/>        | <span data-ttu-id="4b326-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="4b326-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4b326-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4b326-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4b326-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4b326-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4b326-141">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="4b326-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4b326-142">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="4b326-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4b326-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b326-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b326-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4b326-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




