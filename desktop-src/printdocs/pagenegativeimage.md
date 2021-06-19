---
description: Informazioni sull'elemento pageNegativeImage configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1e1a9de2d82135adb82c68f45785ee3763e41a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395656"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="a56f0-105">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="a56f0-105">PageNegativeImage</span></span>

<span data-ttu-id="a56f0-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a56f0-106">This topic is not current.</span></span> <span data-ttu-id="a56f0-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a56f0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a56f0-108">Descrive l'impostazione negativa dell'output.</span><span class="sxs-lookup"><span data-stu-id="a56f0-108">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="a56f0-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a56f0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a56f0-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a56f0-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a56f0-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a56f0-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a56f0-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a56f0-112">Element Information</span></span>



| <span data-ttu-id="a56f0-113">Nome</span><span class="sxs-lookup"><span data-stu-id="a56f0-113">Name</span></span> | <span data-ttu-id="a56f0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a56f0-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a56f0-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a56f0-115">Element Type</span></span> <br/>   | <span data-ttu-id="a56f0-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="a56f0-116">Feature</span></span><br/> |
| <span data-ttu-id="a56f0-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a56f0-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a56f0-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="a56f0-118">Page</span></span><br/>    |
| <span data-ttu-id="a56f0-119">Note</span><span class="sxs-lookup"><span data-stu-id="a56f0-119">Notes</span></span> <br/>          | <span data-ttu-id="a56f0-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="a56f0-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="a56f0-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a56f0-121">Structural Content</span></span>

<span data-ttu-id="a56f0-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="a56f0-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a56f0-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="a56f0-123">Structure Variables</span></span>

<span data-ttu-id="a56f0-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a56f0-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a56f0-125">Nome</span><span class="sxs-lookup"><span data-stu-id="a56f0-125">Name</span></span>                               | <span data-ttu-id="a56f0-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a56f0-126">Data type</span></span>         | <span data-ttu-id="a56f0-127">Unità</span><span class="sxs-lookup"><span data-stu-id="a56f0-127">Unit</span></span>                  | <span data-ttu-id="a56f0-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="a56f0-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a56f0-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a56f0-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a56f0-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a56f0-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a56f0-131">string</span><span class="sxs-lookup"><span data-stu-id="a56f0-131">string</span></span><br/> | <span data-ttu-id="a56f0-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="a56f0-132">characters</span></span><br/> | <span data-ttu-id="a56f0-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a56f0-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a56f0-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a56f0-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a56f0-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="a56f0-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a56f0-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a56f0-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a56f0-137">string</span><span class="sxs-lookup"><span data-stu-id="a56f0-137">string</span></span><br/> | <span data-ttu-id="a56f0-138">n/d</span><span class="sxs-lookup"><span data-stu-id="a56f0-138">n/a</span></span><br/>        | <span data-ttu-id="a56f0-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="a56f0-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a56f0-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a56f0-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a56f0-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a56f0-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a56f0-142">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="a56f0-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a56f0-143">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="a56f0-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a56f0-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a56f0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a56f0-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a56f0-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




