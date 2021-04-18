---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc6d39d3b189edbd2bd51803f1bb517fedd3edf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321141"
---
# <a name="pagemediacolor"></a><span data-ttu-id="ba284-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="ba284-104">PageMediaColor</span></span>

<span data-ttu-id="ba284-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ba284-105">This topic is not current.</span></span> <span data-ttu-id="ba284-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ba284-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ba284-107">Descrive le opzioni relative ai colori dei supporti e le caratteristiche di ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="ba284-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="ba284-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ba284-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ba284-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ba284-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ba284-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ba284-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ba284-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ba284-111">Element Information</span></span>



| <span data-ttu-id="ba284-112">Nome</span><span class="sxs-lookup"><span data-stu-id="ba284-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ba284-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ba284-113">Element Type</span></span> <br/>   | <span data-ttu-id="ba284-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="ba284-114">Feature</span></span><br/> |
| <span data-ttu-id="ba284-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="ba284-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ba284-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="ba284-116">Page</span></span><br/>    |
| <span data-ttu-id="ba284-117">Note</span><span class="sxs-lookup"><span data-stu-id="ba284-117">Notes</span></span> <br/>          | <span data-ttu-id="ba284-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="ba284-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ba284-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ba284-119">Structural Content</span></span>

<span data-ttu-id="ba284-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ba284-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ba284-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ba284-121">Structure Variables</span></span>

<span data-ttu-id="ba284-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ba284-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ba284-123">Nome</span><span class="sxs-lookup"><span data-stu-id="ba284-123">Name</span></span>                               | <span data-ttu-id="ba284-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ba284-124">Data type</span></span>         | <span data-ttu-id="ba284-125">Unità</span><span class="sxs-lookup"><span data-stu-id="ba284-125">Unit</span></span>                  | <span data-ttu-id="ba284-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ba284-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ba284-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ba284-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ba284-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ba284-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ba284-129">string</span><span class="sxs-lookup"><span data-stu-id="ba284-129">string</span></span><br/> | <span data-ttu-id="ba284-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="ba284-130">characters</span></span><br/> | <span data-ttu-id="ba284-131">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ba284-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ba284-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ba284-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ba284-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="ba284-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ba284-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ba284-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ba284-135">string</span><span class="sxs-lookup"><span data-stu-id="ba284-135">string</span></span><br/> | <span data-ttu-id="ba284-136">n/d</span><span class="sxs-lookup"><span data-stu-id="ba284-136">n/a</span></span><br/>        | <span data-ttu-id="ba284-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="ba284-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ba284-138">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ba284-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="ba284-139">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="ba284-139">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="ba284-140">string</span><span class="sxs-lookup"><span data-stu-id="ba284-140">string</span></span><br/> | <span data-ttu-id="ba284-141">Colore sRGB</span><span class="sxs-lookup"><span data-stu-id="ba284-141">sRGB Color</span></span><br/> | <span data-ttu-id="ba284-142">\#AARRGGBB in cui A, R, G, B rappresentano cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="ba284-142">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="ba284-143">Definisce il colore sRGB per il foglio multimediale fisico.</span><span class="sxs-lookup"><span data-stu-id="ba284-143">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ba284-144">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="ba284-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ba284-145">Le parole chiave dello schema di stampa pubbliche sono definite nello `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ba284-145">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="ba284-146">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="ba284-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ba284-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba284-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba284-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ba284-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
