---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d56a0b46c73bb3afdcefe96dc2131c861d5419
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997978"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="7f877-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="7f877-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="7f877-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7f877-105">This topic is not current.</span></span> <span data-ttu-id="7f877-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7f877-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7f877-107">Indica una finalità di alto livello per il driver per il popolamento delle impostazioni di stampa foto.</span><span class="sxs-lookup"><span data-stu-id="7f877-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="7f877-108">Queste impostazioni si occupano della qualità di output prevista che un utente può specificare durante la stampa di foto.</span><span class="sxs-lookup"><span data-stu-id="7f877-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="7f877-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7f877-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="7f877-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7f877-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="7f877-111">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="7f877-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7f877-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7f877-112">Element Information</span></span>



| <span data-ttu-id="7f877-113">Nome</span><span class="sxs-lookup"><span data-stu-id="7f877-113">Name</span></span> | <span data-ttu-id="7f877-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7f877-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7f877-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7f877-115">Element Type</span></span> <br/>   | <span data-ttu-id="7f877-116">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="7f877-116">Feature</span></span><br/> |
| <span data-ttu-id="7f877-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7f877-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7f877-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="7f877-118">Page</span></span><br/>    |
| <span data-ttu-id="7f877-119">Note</span><span class="sxs-lookup"><span data-stu-id="7f877-119">Notes</span></span> <br/>          | <span data-ttu-id="7f877-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f877-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7f877-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7f877-121">Structural Content</span></span>

<span data-ttu-id="7f877-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7f877-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7f877-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="7f877-123">Structure Variables</span></span>

<span data-ttu-id="7f877-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7f877-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7f877-125">Nome</span><span class="sxs-lookup"><span data-stu-id="7f877-125">Name</span></span>                               | <span data-ttu-id="7f877-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f877-126">Data type</span></span>         | <span data-ttu-id="7f877-127">Unità</span><span class="sxs-lookup"><span data-stu-id="7f877-127">Unit</span></span>                  | <span data-ttu-id="7f877-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="7f877-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7f877-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7f877-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7f877-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7f877-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7f877-131">string</span><span class="sxs-lookup"><span data-stu-id="7f877-131">string</span></span><br/> | <span data-ttu-id="7f877-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="7f877-132">characters</span></span><br/> | <span data-ttu-id="7f877-133">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7f877-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7f877-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7f877-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7f877-135">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="7f877-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="7f877-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7f877-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7f877-137">string</span><span class="sxs-lookup"><span data-stu-id="7f877-137">string</span></span><br/> | <span data-ttu-id="7f877-138">n/d</span><span class="sxs-lookup"><span data-stu-id="7f877-138">n/a</span></span><br/>        | <span data-ttu-id="7f877-139">True, False</span><span class="sxs-lookup"><span data-stu-id="7f877-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="7f877-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7f877-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7f877-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7f877-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7f877-142">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="7f877-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7f877-143">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="7f877-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7f877-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f877-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f877-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7f877-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




