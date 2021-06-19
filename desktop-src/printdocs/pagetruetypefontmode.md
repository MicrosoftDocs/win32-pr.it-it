---
description: Informazioni sull'elemento pageTrueTypeFontMode configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf30af3684693f594f497dbad95d4f9a7743d624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395616"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="beb1a-105">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="beb1a-105">PageTrueTypeFontMode</span></span>

<span data-ttu-id="beb1a-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="beb1a-106">This topic is not current.</span></span> <span data-ttu-id="beb1a-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="beb1a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="beb1a-108">Descrive il metodo di gestione dei tipi di carattere TrueType da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="beb1a-108">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="beb1a-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="beb1a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="beb1a-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="beb1a-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="beb1a-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="beb1a-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="beb1a-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="beb1a-112">Element Information</span></span>



| <span data-ttu-id="beb1a-113">Nome</span><span class="sxs-lookup"><span data-stu-id="beb1a-113">Name</span></span> | <span data-ttu-id="beb1a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="beb1a-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="beb1a-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="beb1a-115">Element Type</span></span> <br/>   | <span data-ttu-id="beb1a-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="beb1a-116">Feature</span></span><br/> |
| <span data-ttu-id="beb1a-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="beb1a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="beb1a-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="beb1a-118">Page</span></span><br/>    |
| <span data-ttu-id="beb1a-119">Note</span><span class="sxs-lookup"><span data-stu-id="beb1a-119">Notes</span></span> <br/>          | <span data-ttu-id="beb1a-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="beb1a-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="beb1a-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="beb1a-121">Structural Content</span></span>

<span data-ttu-id="beb1a-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="beb1a-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
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

## <a name="structure-variables"></a><span data-ttu-id="beb1a-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="beb1a-123">Structure Variables</span></span>

<span data-ttu-id="beb1a-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="beb1a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="beb1a-125">Nome</span><span class="sxs-lookup"><span data-stu-id="beb1a-125">Name</span></span>                               | <span data-ttu-id="beb1a-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="beb1a-126">Data type</span></span>         | <span data-ttu-id="beb1a-127">Unità</span><span class="sxs-lookup"><span data-stu-id="beb1a-127">Unit</span></span>                  | <span data-ttu-id="beb1a-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="beb1a-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="beb1a-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="beb1a-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="beb1a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="beb1a-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="beb1a-131">string</span><span class="sxs-lookup"><span data-stu-id="beb1a-131">string</span></span><br/> | <span data-ttu-id="beb1a-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="beb1a-132">characters</span></span><br/> | <span data-ttu-id="beb1a-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="beb1a-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="beb1a-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="beb1a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="beb1a-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="beb1a-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="beb1a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="beb1a-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="beb1a-137">string</span><span class="sxs-lookup"><span data-stu-id="beb1a-137">string</span></span><br/> | <span data-ttu-id="beb1a-138">n/d</span><span class="sxs-lookup"><span data-stu-id="beb1a-138">n/a</span></span><br/>        | <span data-ttu-id="beb1a-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="beb1a-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="beb1a-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="beb1a-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="beb1a-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="beb1a-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="beb1a-142">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="beb1a-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="beb1a-143">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="beb1a-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="beb1a-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="beb1a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beb1a-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="beb1a-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




