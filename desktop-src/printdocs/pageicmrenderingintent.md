---
description: Informazioni sull'elemento PageICMRenderingIntent configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549179"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="5cf95-105">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="5cf95-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="5cf95-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5cf95-106">This topic is not current.</span></span> <span data-ttu-id="5cf95-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5cf95-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5cf95-108">Descrive la finalità di rendering definita dalla specifica ICC v2.</span><span class="sxs-lookup"><span data-stu-id="5cf95-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="5cf95-109">Questo valore deve essere ignorato se un'immagine o un elemento grafico ha un profilo incorporato che specifica la finalità rendering.</span><span class="sxs-lookup"><span data-stu-id="5cf95-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="5cf95-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5cf95-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5cf95-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5cf95-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5cf95-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5cf95-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5cf95-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5cf95-113">Element Information</span></span>



| <span data-ttu-id="5cf95-114">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf95-114">Name</span></span> | <span data-ttu-id="5cf95-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5cf95-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5cf95-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5cf95-116">Element Type</span></span> <br/>   | <span data-ttu-id="5cf95-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="5cf95-117">Feature</span></span><br/> |
| <span data-ttu-id="5cf95-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5cf95-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5cf95-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="5cf95-119">Page</span></span><br/>    |
| <span data-ttu-id="5cf95-120">Note</span><span class="sxs-lookup"><span data-stu-id="5cf95-120">Notes</span></span> <br/>          | <span data-ttu-id="5cf95-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="5cf95-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="5cf95-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="5cf95-122">Structural Content</span></span>

<span data-ttu-id="5cf95-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5cf95-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5cf95-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="5cf95-124">Structure Variables</span></span>

<span data-ttu-id="5cf95-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5cf95-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5cf95-126">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf95-126">Name</span></span>                               | <span data-ttu-id="5cf95-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5cf95-127">Data type</span></span>         | <span data-ttu-id="5cf95-128">Unità</span><span class="sxs-lookup"><span data-stu-id="5cf95-128">Unit</span></span>                  | <span data-ttu-id="5cf95-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="5cf95-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5cf95-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5cf95-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5cf95-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5cf95-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5cf95-132">string</span><span class="sxs-lookup"><span data-stu-id="5cf95-132">string</span></span><br/> | <span data-ttu-id="5cf95-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="5cf95-133">characters</span></span><br/> | <span data-ttu-id="5cf95-134">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5cf95-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5cf95-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="5cf95-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5cf95-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="5cf95-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5cf95-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5cf95-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5cf95-138">string</span><span class="sxs-lookup"><span data-stu-id="5cf95-138">string</span></span><br/> | <span data-ttu-id="5cf95-139">n/d</span><span class="sxs-lookup"><span data-stu-id="5cf95-139">n/a</span></span><br/>        | <span data-ttu-id="5cf95-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="5cf95-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5cf95-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5cf95-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5cf95-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="5cf95-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5cf95-143">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="5cf95-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5cf95-144">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="5cf95-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5cf95-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cf95-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cf95-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5cf95-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




