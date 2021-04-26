---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c9a314bf435664d121fd35e588b62903da323e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994508"
---
# <a name="pagemediacolor"></a><span data-ttu-id="6fed3-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="6fed3-104">PageMediaColor</span></span>

<span data-ttu-id="6fed3-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6fed3-105">This topic is not current.</span></span> <span data-ttu-id="6fed3-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6fed3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6fed3-107">Vengono descritte le opzioni Colore supporto e le caratteristiche di ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="6fed3-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="6fed3-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fed3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6fed3-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6fed3-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6fed3-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fed3-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6fed3-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fed3-111">Element Information</span></span>



| <span data-ttu-id="6fed3-112">Nome</span><span class="sxs-lookup"><span data-stu-id="6fed3-112">Name</span></span> | <span data-ttu-id="6fed3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6fed3-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6fed3-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6fed3-114">Element Type</span></span> <br/>   | <span data-ttu-id="6fed3-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="6fed3-115">Feature</span></span><br/> |
| <span data-ttu-id="6fed3-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6fed3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6fed3-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="6fed3-117">Page</span></span><br/>    |
| <span data-ttu-id="6fed3-118">Note</span><span class="sxs-lookup"><span data-stu-id="6fed3-118">Notes</span></span> <br/>          | <span data-ttu-id="6fed3-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="6fed3-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6fed3-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6fed3-120">Structural Content</span></span>

<span data-ttu-id="6fed3-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6fed3-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="6fed3-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6fed3-122">Structure Variables</span></span>

<span data-ttu-id="6fed3-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6fed3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6fed3-124">Nome</span><span class="sxs-lookup"><span data-stu-id="6fed3-124">Name</span></span>                               | <span data-ttu-id="6fed3-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6fed3-125">Data type</span></span>         | <span data-ttu-id="6fed3-126">Unità</span><span class="sxs-lookup"><span data-stu-id="6fed3-126">Unit</span></span>                  | <span data-ttu-id="6fed3-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6fed3-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6fed3-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6fed3-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6fed3-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6fed3-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6fed3-130">string</span><span class="sxs-lookup"><span data-stu-id="6fed3-130">string</span></span><br/> | <span data-ttu-id="6fed3-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="6fed3-131">characters</span></span><br/> | <span data-ttu-id="6fed3-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6fed3-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6fed3-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6fed3-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6fed3-134">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6fed3-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6fed3-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6fed3-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6fed3-136">string</span><span class="sxs-lookup"><span data-stu-id="6fed3-136">string</span></span><br/> | <span data-ttu-id="6fed3-137">n/d</span><span class="sxs-lookup"><span data-stu-id="6fed3-137">n/a</span></span><br/>        | <span data-ttu-id="6fed3-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="6fed3-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6fed3-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6fed3-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="6fed3-140">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="6fed3-140">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="6fed3-141">string</span><span class="sxs-lookup"><span data-stu-id="6fed3-141">string</span></span><br/> | <span data-ttu-id="6fed3-142">Colore sRGB</span><span class="sxs-lookup"><span data-stu-id="6fed3-142">sRGB Color</span></span><br/> | <span data-ttu-id="6fed3-143">\#AARRGGBB dove A, R, G, B rappresentano cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="6fed3-143">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="6fed3-144">Definisce il colore sRGB per il foglio multimediale fisico.</span><span class="sxs-lookup"><span data-stu-id="6fed3-144">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6fed3-145">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fed3-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6fed3-146">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` nomi .</span><span class="sxs-lookup"><span data-stu-id="6fed3-146">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="6fed3-147">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6fed3-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6fed3-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fed3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fed3-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6fed3-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
