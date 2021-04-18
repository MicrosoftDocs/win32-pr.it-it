---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722e5db4f1a3bfebe8895c8a0777a849a88f11e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351986"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="aef9b-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="aef9b-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="aef9b-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="aef9b-105">This topic is not current.</span></span> <span data-ttu-id="aef9b-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aef9b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aef9b-107">Descrive l'utilizzo del foglio separatore per un documento.</span><span class="sxs-lookup"><span data-stu-id="aef9b-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="aef9b-108">I fogli separatore verranno visualizzati nell'output come indicato dall'opzione specificata di seguito.</span><span class="sxs-lookup"><span data-stu-id="aef9b-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="aef9b-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="aef9b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aef9b-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="aef9b-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="aef9b-111">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="aef9b-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aef9b-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="aef9b-112">Element Information</span></span>



| <span data-ttu-id="aef9b-113">Nome</span><span class="sxs-lookup"><span data-stu-id="aef9b-113">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="aef9b-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="aef9b-114">Element Type</span></span> <br/>   | <span data-ttu-id="aef9b-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="aef9b-115">Feature</span></span><br/>  |
| <span data-ttu-id="aef9b-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="aef9b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aef9b-117">Documento</span><span class="sxs-lookup"><span data-stu-id="aef9b-117">Document</span></span><br/> |
| <span data-ttu-id="aef9b-118">Note</span><span class="sxs-lookup"><span data-stu-id="aef9b-118">Notes</span></span> <br/>          | <span data-ttu-id="aef9b-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="aef9b-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="aef9b-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="aef9b-120">Structural Content</span></span>

<span data-ttu-id="aef9b-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="aef9b-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="aef9b-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="aef9b-122">Structure Variables</span></span>

<span data-ttu-id="aef9b-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="aef9b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aef9b-124">Nome</span><span class="sxs-lookup"><span data-stu-id="aef9b-124">Name</span></span>                               | <span data-ttu-id="aef9b-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="aef9b-125">Data type</span></span>         | <span data-ttu-id="aef9b-126">Unità</span><span class="sxs-lookup"><span data-stu-id="aef9b-126">Unit</span></span>                  | <span data-ttu-id="aef9b-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="aef9b-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="aef9b-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="aef9b-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aef9b-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="aef9b-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="aef9b-130">string</span><span class="sxs-lookup"><span data-stu-id="aef9b-130">string</span></span><br/> | <span data-ttu-id="aef9b-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="aef9b-131">characters</span></span><br/> | <span data-ttu-id="aef9b-132">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="aef9b-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="aef9b-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="aef9b-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aef9b-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="aef9b-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="aef9b-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="aef9b-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="aef9b-136">string</span><span class="sxs-lookup"><span data-stu-id="aef9b-136">string</span></span><br/> | <span data-ttu-id="aef9b-137">n/d</span><span class="sxs-lookup"><span data-stu-id="aef9b-137">n/a</span></span><br/>        | <span data-ttu-id="aef9b-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="aef9b-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="aef9b-139">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aef9b-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aef9b-140">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="aef9b-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aef9b-141">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="aef9b-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aef9b-142">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="aef9b-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="aef9b-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aef9b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aef9b-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="aef9b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




