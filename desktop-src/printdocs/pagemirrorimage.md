---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: a05357c0-6a82-42ff-b4f8-d3e0ee089055
title: PageMirrorImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d9fe0a82ad14c149849c3bf6bf0c5de6144571
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994468"
---
# <a name="pagemirrorimage"></a><span data-ttu-id="ef10f-104">PageMirrorImage</span><span class="sxs-lookup"><span data-stu-id="ef10f-104">PageMirrorImage</span></span>

<span data-ttu-id="ef10f-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ef10f-105">This topic is not current.</span></span> <span data-ttu-id="ef10f-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ef10f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ef10f-107">Descrive l'impostazione di mirroring dell'output.</span><span class="sxs-lookup"><span data-stu-id="ef10f-107">Describes the mirroring setting of the output.</span></span>

-   [<span data-ttu-id="ef10f-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ef10f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ef10f-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ef10f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ef10f-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ef10f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ef10f-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ef10f-111">Element Information</span></span>



| <span data-ttu-id="ef10f-112">Nome</span><span class="sxs-lookup"><span data-stu-id="ef10f-112">Name</span></span> | <span data-ttu-id="ef10f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ef10f-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ef10f-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ef10f-114">Element Type</span></span> <br/>   | <span data-ttu-id="ef10f-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="ef10f-115">Feature</span></span><br/> |
| <span data-ttu-id="ef10f-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="ef10f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ef10f-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="ef10f-117">Page</span></span><br/>    |
| <span data-ttu-id="ef10f-118">Note</span><span class="sxs-lookup"><span data-stu-id="ef10f-118">Notes</span></span> <br/>          | <span data-ttu-id="ef10f-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="ef10f-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ef10f-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ef10f-120">Structural Content</span></span>

<span data-ttu-id="ef10f-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="ef10f-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
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

## <a name="structure-variables"></a><span data-ttu-id="ef10f-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ef10f-122">Structure Variables</span></span>

<span data-ttu-id="ef10f-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ef10f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ef10f-124">Nome</span><span class="sxs-lookup"><span data-stu-id="ef10f-124">Name</span></span>                               | <span data-ttu-id="ef10f-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ef10f-125">Data type</span></span>         | <span data-ttu-id="ef10f-126">Unità</span><span class="sxs-lookup"><span data-stu-id="ef10f-126">Unit</span></span>                  | <span data-ttu-id="ef10f-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ef10f-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ef10f-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ef10f-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ef10f-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ef10f-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ef10f-130">string</span><span class="sxs-lookup"><span data-stu-id="ef10f-130">string</span></span><br/> | <span data-ttu-id="ef10f-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="ef10f-131">characters</span></span><br/> | <span data-ttu-id="ef10f-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ef10f-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ef10f-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ef10f-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ef10f-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="ef10f-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ef10f-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ef10f-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ef10f-136">string</span><span class="sxs-lookup"><span data-stu-id="ef10f-136">string</span></span><br/> | <span data-ttu-id="ef10f-137">n/d</span><span class="sxs-lookup"><span data-stu-id="ef10f-137">n/a</span></span><br/>        | <span data-ttu-id="ef10f-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="ef10f-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ef10f-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ef10f-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ef10f-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ef10f-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ef10f-141">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="ef10f-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ef10f-142">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="ef10f-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be mirrored parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:MirrorImageWidth" />
  <!-- Specifies the output should be mirrored parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:MirrorImageHeight" />
  <!-- Specifies the output should not be mirrored. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="ef10f-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef10f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef10f-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ef10f-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




