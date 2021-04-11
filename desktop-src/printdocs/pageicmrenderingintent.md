---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014213bdd2e11cc2587cef580a0b48fe03172ef0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234595"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="30cf9-104">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="30cf9-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="30cf9-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="30cf9-105">This topic is not current.</span></span> <span data-ttu-id="30cf9-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="30cf9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="30cf9-107">Descrive lo scopo del rendering come definito dalla specifica ICC v2.</span><span class="sxs-lookup"><span data-stu-id="30cf9-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="30cf9-108">Questo valore deve essere ignorato se un'immagine o un elemento grafico ha un profilo incorporato che specifica la finalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="30cf9-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="30cf9-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="30cf9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="30cf9-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="30cf9-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="30cf9-111">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="30cf9-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="30cf9-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="30cf9-112">Element Information</span></span>



| <span data-ttu-id="30cf9-113">Nome</span><span class="sxs-lookup"><span data-stu-id="30cf9-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="30cf9-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="30cf9-114">Element Type</span></span> <br/>   | <span data-ttu-id="30cf9-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="30cf9-115">Feature</span></span><br/> |
| <span data-ttu-id="30cf9-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="30cf9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="30cf9-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="30cf9-117">Page</span></span><br/>    |
| <span data-ttu-id="30cf9-118">Note</span><span class="sxs-lookup"><span data-stu-id="30cf9-118">Notes</span></span> <br/>          | <span data-ttu-id="30cf9-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="30cf9-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="30cf9-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="30cf9-120">Structural Content</span></span>

<span data-ttu-id="30cf9-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="30cf9-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="30cf9-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="30cf9-122">Structure Variables</span></span>

<span data-ttu-id="30cf9-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="30cf9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="30cf9-124">Nome</span><span class="sxs-lookup"><span data-stu-id="30cf9-124">Name</span></span>                               | <span data-ttu-id="30cf9-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="30cf9-125">Data type</span></span>         | <span data-ttu-id="30cf9-126">Unità</span><span class="sxs-lookup"><span data-stu-id="30cf9-126">Unit</span></span>                  | <span data-ttu-id="30cf9-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="30cf9-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="30cf9-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="30cf9-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="30cf9-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="30cf9-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="30cf9-130">string</span><span class="sxs-lookup"><span data-stu-id="30cf9-130">string</span></span><br/> | <span data-ttu-id="30cf9-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="30cf9-131">characters</span></span><br/> | <span data-ttu-id="30cf9-132">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="30cf9-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="30cf9-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="30cf9-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="30cf9-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="30cf9-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="30cf9-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="30cf9-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="30cf9-136">string</span><span class="sxs-lookup"><span data-stu-id="30cf9-136">string</span></span><br/> | <span data-ttu-id="30cf9-137">n/d</span><span class="sxs-lookup"><span data-stu-id="30cf9-137">n/a</span></span><br/>        | <span data-ttu-id="30cf9-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="30cf9-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="30cf9-139">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="30cf9-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="30cf9-140">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="30cf9-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="30cf9-141">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="30cf9-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="30cf9-142">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="30cf9-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="30cf9-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30cf9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30cf9-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="30cf9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




