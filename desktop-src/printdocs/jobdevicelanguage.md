---
description: Informazioni sull'elemento JobDeviceLanguage, che descrive le lingue dei dispositivi supportate per l'invio di dati dal driver al dispositivo fisico.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7bf56018a2b395ec5aa182336a89d8872057e7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408995"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="8f307-103">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="8f307-103">JobDeviceLanguage</span></span>

<span data-ttu-id="8f307-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="8f307-104">This topic is not current.</span></span> <span data-ttu-id="8f307-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f307-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f307-106">Descrive le lingue dei dispositivi supportate per l'invio di dati dal driver al dispositivo fisico.</span><span class="sxs-lookup"><span data-stu-id="8f307-106">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="8f307-107">Questo linguaggio è spesso denominato "Page Description Language".</span><span class="sxs-lookup"><span data-stu-id="8f307-107">This is often called "Page Description Language".</span></span> <span data-ttu-id="8f307-108">Questa parola chiave definisce il linguaggio di descrizione della pagina supportato dal driver e dal dispositivo fisico.</span><span class="sxs-lookup"><span data-stu-id="8f307-108">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="8f307-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8f307-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8f307-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="8f307-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8f307-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8f307-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8f307-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8f307-112">Element Information</span></span>



| <span data-ttu-id="8f307-113">Nome</span><span class="sxs-lookup"><span data-stu-id="8f307-113">Name</span></span> | <span data-ttu-id="8f307-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8f307-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8f307-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="8f307-115">Element Type</span></span> <br/>   | <span data-ttu-id="8f307-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="8f307-116">Feature</span></span><br/> |
| <span data-ttu-id="8f307-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="8f307-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8f307-118">Processo</span><span class="sxs-lookup"><span data-stu-id="8f307-118">Job</span></span><br/>     |
| <span data-ttu-id="8f307-119">Note</span><span class="sxs-lookup"><span data-stu-id="8f307-119">Notes</span></span> <br/>          | <span data-ttu-id="8f307-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="8f307-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="8f307-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="8f307-121">Structural Content</span></span>

<span data-ttu-id="8f307-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="8f307-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="8f307-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="8f307-123">Structure Variables</span></span>

<span data-ttu-id="8f307-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="8f307-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8f307-125">Nome</span><span class="sxs-lookup"><span data-stu-id="8f307-125">Name</span></span>                                 | <span data-ttu-id="8f307-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8f307-126">Data type</span></span>         | <span data-ttu-id="8f307-127">Unità</span><span class="sxs-lookup"><span data-stu-id="8f307-127">Unit</span></span>                  | <span data-ttu-id="8f307-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="8f307-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8f307-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="8f307-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8f307-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8f307-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="8f307-131">string</span><span class="sxs-lookup"><span data-stu-id="8f307-131">string</span></span><br/> | <span data-ttu-id="8f307-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="8f307-132">characters</span></span><br/> | <span data-ttu-id="8f307-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="8f307-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8f307-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8f307-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8f307-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="8f307-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8f307-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8f307-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="8f307-137">string</span><span class="sxs-lookup"><span data-stu-id="8f307-137">string</span></span><br/> | <span data-ttu-id="8f307-138">n/d</span><span class="sxs-lookup"><span data-stu-id="8f307-138">n/a</span></span><br/>        | <span data-ttu-id="8f307-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="8f307-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8f307-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8f307-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="8f307-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="8f307-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="8f307-142">string</span><span class="sxs-lookup"><span data-stu-id="8f307-142">string</span></span><br/> | <span data-ttu-id="8f307-143">n/d</span><span class="sxs-lookup"><span data-stu-id="8f307-143">n/a</span></span><br/>        | <span data-ttu-id="8f307-144">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8f307-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="8f307-145">Specifica il livello di lingua ,ad esempio PS Level 2.</span><span class="sxs-lookup"><span data-stu-id="8f307-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="8f307-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="8f307-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="8f307-147">string</span><span class="sxs-lookup"><span data-stu-id="8f307-147">string</span></span><br/> | <span data-ttu-id="8f307-148">n/d</span><span class="sxs-lookup"><span data-stu-id="8f307-148">n/a</span></span><br/>        | <span data-ttu-id="8f307-149">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8f307-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="8f307-150">Specifica la codifica della lingua, ad esempio ISOLatin1.</span><span class="sxs-lookup"><span data-stu-id="8f307-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="8f307-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="8f307-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="8f307-152">string</span><span class="sxs-lookup"><span data-stu-id="8f307-152">string</span></span><br/> | <span data-ttu-id="8f307-153">n/d</span><span class="sxs-lookup"><span data-stu-id="8f307-153">n/a</span></span><br/>        | <span data-ttu-id="8f307-154">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8f307-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="8f307-155">Specifica la versione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="8f307-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8f307-156">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="8f307-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8f307-157">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="8f307-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8f307-158">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="8f307-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="8f307-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f307-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f307-160">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="8f307-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




