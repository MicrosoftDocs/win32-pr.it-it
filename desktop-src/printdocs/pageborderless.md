---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: PageBorderless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd73e2808380bf73a7df7156c10c40cfa339765
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321113"
---
# <a name="pageborderless"></a><span data-ttu-id="75d02-104">PageBorderless</span><span class="sxs-lookup"><span data-stu-id="75d02-104">PageBorderless</span></span>

<span data-ttu-id="75d02-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="75d02-105">This topic is not current.</span></span> <span data-ttu-id="75d02-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="75d02-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75d02-107">Descrive quando il contenuto dell'immagine deve essere stampato sui bordi fisici del supporto.</span><span class="sxs-lookup"><span data-stu-id="75d02-107">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="75d02-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="75d02-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75d02-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="75d02-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="75d02-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="75d02-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="75d02-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="75d02-111">Element Information</span></span>



| <span data-ttu-id="75d02-112">Nome</span><span class="sxs-lookup"><span data-stu-id="75d02-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="75d02-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="75d02-113">Element Type</span></span> <br/>   | <span data-ttu-id="75d02-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="75d02-114">Feature</span></span><br/> |
| <span data-ttu-id="75d02-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="75d02-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75d02-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="75d02-116">Page</span></span><br/>    |
| <span data-ttu-id="75d02-117">Note</span><span class="sxs-lookup"><span data-stu-id="75d02-117">Notes</span></span> <br/>          | <span data-ttu-id="75d02-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="75d02-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="75d02-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="75d02-119">Structural Content</span></span>

<span data-ttu-id="75d02-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="75d02-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
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

## <a name="structure-variables"></a><span data-ttu-id="75d02-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="75d02-121">Structure Variables</span></span>

<span data-ttu-id="75d02-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="75d02-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75d02-123">Nome</span><span class="sxs-lookup"><span data-stu-id="75d02-123">Name</span></span>                               | <span data-ttu-id="75d02-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="75d02-124">Data type</span></span>         | <span data-ttu-id="75d02-125">Unità</span><span class="sxs-lookup"><span data-stu-id="75d02-125">Unit</span></span>                  | <span data-ttu-id="75d02-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="75d02-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="75d02-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="75d02-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="75d02-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="75d02-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="75d02-129">string</span><span class="sxs-lookup"><span data-stu-id="75d02-129">string</span></span><br/> | <span data-ttu-id="75d02-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="75d02-130">characters</span></span><br/> | <span data-ttu-id="75d02-131">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="75d02-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="75d02-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="75d02-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="75d02-133">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="75d02-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="75d02-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75d02-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="75d02-135">string</span><span class="sxs-lookup"><span data-stu-id="75d02-135">string</span></span><br/> | <span data-ttu-id="75d02-136">n/d</span><span class="sxs-lookup"><span data-stu-id="75d02-136">n/a</span></span><br/>        | <span data-ttu-id="75d02-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="75d02-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75d02-138">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="75d02-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="75d02-139">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="75d02-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="75d02-140">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="75d02-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="75d02-141">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="75d02-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies borderless printing. -->
  <psf:Option name="psk:Borderless" />
  <!-- Specifies no borderless printing. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="75d02-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75d02-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d02-143">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="75d02-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




