---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b9f85b44ae9fdc6efb66ce5b72bb68c5187790
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998298"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="663b6-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="663b6-104">JobDeviceLanguage</span></span>

<span data-ttu-id="663b6-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="663b6-105">This topic is not current.</span></span> <span data-ttu-id="663b6-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="663b6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="663b6-107">Descrive le lingue dei dispositivi supportate per l'invio di dati dal driver al dispositivo fisico.</span><span class="sxs-lookup"><span data-stu-id="663b6-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="663b6-108">Questo linguaggio è spesso denominato "Page Description Language".</span><span class="sxs-lookup"><span data-stu-id="663b6-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="663b6-109">Questa parola chiave definisce il linguaggio di descrizione della pagina supportato dal driver e dal dispositivo fisico.</span><span class="sxs-lookup"><span data-stu-id="663b6-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="663b6-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="663b6-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="663b6-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="663b6-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="663b6-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="663b6-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="663b6-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="663b6-113">Element Information</span></span>



| <span data-ttu-id="663b6-114">Nome</span><span class="sxs-lookup"><span data-stu-id="663b6-114">Name</span></span> | <span data-ttu-id="663b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="663b6-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="663b6-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="663b6-116">Element Type</span></span> <br/>   | <span data-ttu-id="663b6-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="663b6-117">Feature</span></span><br/> |
| <span data-ttu-id="663b6-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="663b6-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="663b6-119">Processo</span><span class="sxs-lookup"><span data-stu-id="663b6-119">Job</span></span><br/>     |
| <span data-ttu-id="663b6-120">Note</span><span class="sxs-lookup"><span data-stu-id="663b6-120">Notes</span></span> <br/>          | <span data-ttu-id="663b6-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="663b6-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="663b6-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="663b6-122">Structural Content</span></span>

<span data-ttu-id="663b6-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="663b6-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="663b6-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="663b6-124">Structure Variables</span></span>

<span data-ttu-id="663b6-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="663b6-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="663b6-126">Nome</span><span class="sxs-lookup"><span data-stu-id="663b6-126">Name</span></span>                                 | <span data-ttu-id="663b6-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="663b6-127">Data type</span></span>         | <span data-ttu-id="663b6-128">Unità</span><span class="sxs-lookup"><span data-stu-id="663b6-128">Unit</span></span>                  | <span data-ttu-id="663b6-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="663b6-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="663b6-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="663b6-130">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="663b6-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="663b6-131">\_OptionName\_</span></span><br/>            | <span data-ttu-id="663b6-132">string</span><span class="sxs-lookup"><span data-stu-id="663b6-132">string</span></span><br/> | <span data-ttu-id="663b6-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="663b6-133">characters</span></span><br/> | <span data-ttu-id="663b6-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="663b6-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="663b6-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="663b6-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="663b6-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="663b6-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="663b6-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="663b6-137">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="663b6-138">string</span><span class="sxs-lookup"><span data-stu-id="663b6-138">string</span></span><br/> | <span data-ttu-id="663b6-139">n/d</span><span class="sxs-lookup"><span data-stu-id="663b6-139">n/a</span></span><br/>        | <span data-ttu-id="663b6-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="663b6-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="663b6-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="663b6-141">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="663b6-142">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="663b6-142">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="663b6-143">string</span><span class="sxs-lookup"><span data-stu-id="663b6-143">string</span></span><br/> | <span data-ttu-id="663b6-144">n/d</span><span class="sxs-lookup"><span data-stu-id="663b6-144">n/a</span></span><br/>        | <span data-ttu-id="663b6-145">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="663b6-145">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="663b6-146">Specifica il livello del linguaggio,ad esempio PS Level 2.</span><span class="sxs-lookup"><span data-stu-id="663b6-146">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="663b6-147">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="663b6-147">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="663b6-148">string</span><span class="sxs-lookup"><span data-stu-id="663b6-148">string</span></span><br/> | <span data-ttu-id="663b6-149">n/d</span><span class="sxs-lookup"><span data-stu-id="663b6-149">n/a</span></span><br/>        | <span data-ttu-id="663b6-150">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="663b6-150">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="663b6-151">Specifica la codifica della lingua, ad esempio ISOLatin1.</span><span class="sxs-lookup"><span data-stu-id="663b6-151">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="663b6-152">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="663b6-152">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="663b6-153">string</span><span class="sxs-lookup"><span data-stu-id="663b6-153">string</span></span><br/> | <span data-ttu-id="663b6-154">n/d</span><span class="sxs-lookup"><span data-stu-id="663b6-154">n/a</span></span><br/>        | <span data-ttu-id="663b6-155">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="663b6-155">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="663b6-156">Specifica la versione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="663b6-156">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="663b6-157">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="663b6-157">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="663b6-158">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="663b6-158">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="663b6-159">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="663b6-159">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="663b6-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="663b6-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="663b6-161">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="663b6-161">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




