---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8882c1a5aa026d06b43055a6a74a58c266ea009
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994497"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="6c79b-104">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="6c79b-104">PageNegativeImage</span></span>

<span data-ttu-id="6c79b-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6c79b-105">This topic is not current.</span></span> <span data-ttu-id="6c79b-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6c79b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6c79b-107">Descrive l'impostazione negativa dell'output.</span><span class="sxs-lookup"><span data-stu-id="6c79b-107">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="6c79b-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6c79b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6c79b-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6c79b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6c79b-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6c79b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6c79b-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6c79b-111">Element Information</span></span>



| <span data-ttu-id="6c79b-112">Nome</span><span class="sxs-lookup"><span data-stu-id="6c79b-112">Name</span></span> | <span data-ttu-id="6c79b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6c79b-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6c79b-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6c79b-114">Element Type</span></span> <br/>   | <span data-ttu-id="6c79b-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="6c79b-115">Feature</span></span><br/> |
| <span data-ttu-id="6c79b-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6c79b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6c79b-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="6c79b-117">Page</span></span><br/>    |
| <span data-ttu-id="6c79b-118">Note</span><span class="sxs-lookup"><span data-stu-id="6c79b-118">Notes</span></span> <br/>          | <span data-ttu-id="6c79b-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="6c79b-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6c79b-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6c79b-120">Structural Content</span></span>

<span data-ttu-id="6c79b-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6c79b-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
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

## <a name="structure-variables"></a><span data-ttu-id="6c79b-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6c79b-122">Structure Variables</span></span>

<span data-ttu-id="6c79b-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6c79b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6c79b-124">Nome</span><span class="sxs-lookup"><span data-stu-id="6c79b-124">Name</span></span>                               | <span data-ttu-id="6c79b-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6c79b-125">Data type</span></span>         | <span data-ttu-id="6c79b-126">Unità</span><span class="sxs-lookup"><span data-stu-id="6c79b-126">Unit</span></span>                  | <span data-ttu-id="6c79b-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6c79b-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6c79b-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6c79b-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6c79b-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6c79b-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6c79b-130">string</span><span class="sxs-lookup"><span data-stu-id="6c79b-130">string</span></span><br/> | <span data-ttu-id="6c79b-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="6c79b-131">characters</span></span><br/> | <span data-ttu-id="6c79b-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6c79b-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6c79b-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6c79b-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6c79b-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6c79b-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6c79b-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6c79b-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6c79b-136">string</span><span class="sxs-lookup"><span data-stu-id="6c79b-136">string</span></span><br/> | <span data-ttu-id="6c79b-137">n/d</span><span class="sxs-lookup"><span data-stu-id="6c79b-137">n/a</span></span><br/>        | <span data-ttu-id="6c79b-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="6c79b-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6c79b-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6c79b-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6c79b-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6c79b-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6c79b-141">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="6c79b-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6c79b-142">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6c79b-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="6c79b-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c79b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c79b-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6c79b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




