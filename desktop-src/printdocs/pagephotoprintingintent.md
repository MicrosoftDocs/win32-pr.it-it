---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3985d6f21d0d7731d1c08d080d64a4948b58196d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104530601"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="6f9a8-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="6f9a8-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="6f9a8-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-105">This topic is not current.</span></span> <span data-ttu-id="6f9a8-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6f9a8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6f9a8-107">Indica una finalità di alto livello per il driver per la popolazione delle impostazioni di stampa foto.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="6f9a8-108">Queste impostazioni gestiscono la qualità di output prevista che un utente può specificare durante la stampa di foto.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="6f9a8-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6f9a8-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="6f9a8-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6f9a8-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="6f9a8-111">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="6f9a8-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6f9a8-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6f9a8-112">Element Information</span></span>



| <span data-ttu-id="6f9a8-113">Nome</span><span class="sxs-lookup"><span data-stu-id="6f9a8-113">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="6f9a8-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6f9a8-114">Element Type</span></span> <br/>   | <span data-ttu-id="6f9a8-115">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="6f9a8-115">Feature</span></span><br/> |
| <span data-ttu-id="6f9a8-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="6f9a8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6f9a8-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="6f9a8-117">Page</span></span><br/>    |
| <span data-ttu-id="6f9a8-118">Note</span><span class="sxs-lookup"><span data-stu-id="6f9a8-118">Notes</span></span> <br/>          | <span data-ttu-id="6f9a8-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="6f9a8-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6f9a8-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6f9a8-120">Structural Content</span></span>

<span data-ttu-id="6f9a8-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="6f9a8-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="6f9a8-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6f9a8-122">Structure Variables</span></span>

<span data-ttu-id="6f9a8-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6f9a8-124">Nome</span><span class="sxs-lookup"><span data-stu-id="6f9a8-124">Name</span></span>                               | <span data-ttu-id="6f9a8-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6f9a8-125">Data type</span></span>         | <span data-ttu-id="6f9a8-126">Unità</span><span class="sxs-lookup"><span data-stu-id="6f9a8-126">Unit</span></span>                  | <span data-ttu-id="6f9a8-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6f9a8-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6f9a8-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6f9a8-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6f9a8-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6f9a8-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6f9a8-130">string</span><span class="sxs-lookup"><span data-stu-id="6f9a8-130">string</span></span><br/> | <span data-ttu-id="6f9a8-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="6f9a8-131">characters</span></span><br/> | <span data-ttu-id="6f9a8-132">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6f9a8-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6f9a8-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6f9a8-134">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="6f9a8-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="6f9a8-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6f9a8-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6f9a8-136">string</span><span class="sxs-lookup"><span data-stu-id="6f9a8-136">string</span></span><br/> | <span data-ttu-id="6f9a8-137">n/d</span><span class="sxs-lookup"><span data-stu-id="6f9a8-137">n/a</span></span><br/>        | <span data-ttu-id="6f9a8-138">True, False</span><span class="sxs-lookup"><span data-stu-id="6f9a8-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="6f9a8-139">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6f9a8-140">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6f9a8-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6f9a8-141">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6f9a8-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6f9a8-142">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f9a8-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="6f9a8-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f9a8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f9a8-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6f9a8-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




