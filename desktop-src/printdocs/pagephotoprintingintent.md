---
description: Esaminare l'elemento PagePhotoPrintingIntent configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1cf9ae587062efc68b953f5931b55147940b1b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548979"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="7a7fc-105">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="7a7fc-105">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="7a7fc-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-106">This topic is not current.</span></span> <span data-ttu-id="7a7fc-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a7fc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a7fc-108">Indica una finalità di alto livello al driver per il popolamento delle impostazioni di stampa foto.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-108">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="7a7fc-109">Queste impostazioni si occupano della qualità di output prevista che un utente può specificare durante la stampa di foto.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-109">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="7a7fc-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7a7fc-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="7a7fc-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7a7fc-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="7a7fc-112">Contenuto XML</span><span class="sxs-lookup"><span data-stu-id="7a7fc-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7a7fc-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7a7fc-113">Element Information</span></span>



| <span data-ttu-id="7a7fc-114">Nome</span><span class="sxs-lookup"><span data-stu-id="7a7fc-114">Name</span></span> | <span data-ttu-id="7a7fc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7a7fc-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7a7fc-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7a7fc-116">Element Type</span></span> <br/>   | <span data-ttu-id="7a7fc-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="7a7fc-117">Feature</span></span><br/> |
| <span data-ttu-id="7a7fc-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7a7fc-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a7fc-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="7a7fc-119">Page</span></span><br/>    |
| <span data-ttu-id="7a7fc-120">Note</span><span class="sxs-lookup"><span data-stu-id="7a7fc-120">Notes</span></span> <br/>          | <span data-ttu-id="7a7fc-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="7a7fc-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7a7fc-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="7a7fc-122">Structural Content</span></span>

<span data-ttu-id="7a7fc-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7a7fc-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7a7fc-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="7a7fc-124">Structure Variables</span></span>

<span data-ttu-id="7a7fc-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a7fc-126">Nome</span><span class="sxs-lookup"><span data-stu-id="7a7fc-126">Name</span></span>                               | <span data-ttu-id="7a7fc-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7a7fc-127">Data type</span></span>         | <span data-ttu-id="7a7fc-128">Unità</span><span class="sxs-lookup"><span data-stu-id="7a7fc-128">Unit</span></span>                  | <span data-ttu-id="7a7fc-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="7a7fc-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7a7fc-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7a7fc-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7a7fc-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7a7fc-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7a7fc-132">string</span><span class="sxs-lookup"><span data-stu-id="7a7fc-132">string</span></span><br/> | <span data-ttu-id="7a7fc-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="7a7fc-133">characters</span></span><br/> | <span data-ttu-id="7a7fc-134">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7a7fc-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7a7fc-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7a7fc-136">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="7a7fc-136">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="7a7fc-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7a7fc-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7a7fc-138">string</span><span class="sxs-lookup"><span data-stu-id="7a7fc-138">string</span></span><br/> | <span data-ttu-id="7a7fc-139">n/d</span><span class="sxs-lookup"><span data-stu-id="7a7fc-139">n/a</span></span><br/>        | <span data-ttu-id="7a7fc-140">True, False</span><span class="sxs-lookup"><span data-stu-id="7a7fc-140">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="7a7fc-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7a7fc-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7a7fc-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="7a7fc-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7a7fc-143">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="7a7fc-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7a7fc-144">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="7a7fc-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7a7fc-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a7fc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a7fc-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7a7fc-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




