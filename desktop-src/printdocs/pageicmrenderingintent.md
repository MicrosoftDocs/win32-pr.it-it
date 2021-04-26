---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17eea84ba45ea7c121080f7649b03492c6f3409
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995558"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="f5de7-104">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="f5de7-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="f5de7-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f5de7-105">This topic is not current.</span></span> <span data-ttu-id="f5de7-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f5de7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f5de7-107">Descrive la finalità di rendering definita dalla specifica ICC v2.</span><span class="sxs-lookup"><span data-stu-id="f5de7-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="f5de7-108">Questo valore deve essere ignorato se un'immagine o un elemento grafico ha un profilo incorporato che specifica la finalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="f5de7-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="f5de7-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5de7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f5de7-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f5de7-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f5de7-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f5de7-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f5de7-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5de7-112">Element Information</span></span>



| <span data-ttu-id="f5de7-113">Nome</span><span class="sxs-lookup"><span data-stu-id="f5de7-113">Name</span></span> | <span data-ttu-id="f5de7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f5de7-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f5de7-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f5de7-115">Element Type</span></span> <br/>   | <span data-ttu-id="f5de7-116">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="f5de7-116">Feature</span></span><br/> |
| <span data-ttu-id="f5de7-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f5de7-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f5de7-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="f5de7-118">Page</span></span><br/>    |
| <span data-ttu-id="f5de7-119">Note</span><span class="sxs-lookup"><span data-stu-id="f5de7-119">Notes</span></span> <br/>          | <span data-ttu-id="f5de7-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="f5de7-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="f5de7-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="f5de7-121">Structural Content</span></span>

<span data-ttu-id="f5de7-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f5de7-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="f5de7-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="f5de7-123">Structure Variables</span></span>

<span data-ttu-id="f5de7-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f5de7-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f5de7-125">Nome</span><span class="sxs-lookup"><span data-stu-id="f5de7-125">Name</span></span>                               | <span data-ttu-id="f5de7-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5de7-126">Data type</span></span>         | <span data-ttu-id="f5de7-127">Unità</span><span class="sxs-lookup"><span data-stu-id="f5de7-127">Unit</span></span>                  | <span data-ttu-id="f5de7-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="f5de7-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f5de7-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f5de7-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f5de7-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f5de7-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f5de7-131">string</span><span class="sxs-lookup"><span data-stu-id="f5de7-131">string</span></span><br/> | <span data-ttu-id="f5de7-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="f5de7-132">characters</span></span><br/> | <span data-ttu-id="f5de7-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f5de7-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f5de7-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="f5de7-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f5de7-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="f5de7-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f5de7-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5de7-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f5de7-137">string</span><span class="sxs-lookup"><span data-stu-id="f5de7-137">string</span></span><br/> | <span data-ttu-id="f5de7-138">n/d</span><span class="sxs-lookup"><span data-stu-id="f5de7-138">n/a</span></span><br/>        | <span data-ttu-id="f5de7-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="f5de7-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f5de7-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f5de7-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f5de7-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f5de7-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f5de7-142">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="f5de7-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f5de7-143">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="f5de7-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f5de7-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5de7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5de7-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f5de7-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




