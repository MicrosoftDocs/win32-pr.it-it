---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2c60fd005f42bd3f9861e86156a7da9164a81e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321106"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="1a8b2-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="1a8b2-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="1a8b2-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-105">This topic is not current.</span></span> <span data-ttu-id="1a8b2-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1a8b2-107">Viene descritta la configurazione dell'elaborazione della firma digitale per l'intero processo.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="1a8b2-108">Applicabile solo ai contenuti che contengono firme digitali.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="1a8b2-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a8b2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a8b2-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1a8b2-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="1a8b2-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a8b2-111">Element Information</span></span>



| <span data-ttu-id="1a8b2-112">Nome</span><span class="sxs-lookup"><span data-stu-id="1a8b2-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="1a8b2-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1a8b2-113">Element Type</span></span> <br/>   | <span data-ttu-id="1a8b2-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="1a8b2-114">Feature</span></span><br/> |
| <span data-ttu-id="1a8b2-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="1a8b2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1a8b2-116">Processo</span><span class="sxs-lookup"><span data-stu-id="1a8b2-116">Job</span></span><br/>     |
| <span data-ttu-id="1a8b2-117">Note</span><span class="sxs-lookup"><span data-stu-id="1a8b2-117">Notes</span></span> <br/>          | <span data-ttu-id="1a8b2-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="1a8b2-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1a8b2-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1a8b2-119">Structural Content</span></span>

<span data-ttu-id="1a8b2-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="1a8b2-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="1a8b2-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="1a8b2-121">Structure Variables</span></span>

<span data-ttu-id="1a8b2-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1a8b2-123">Nome</span><span class="sxs-lookup"><span data-stu-id="1a8b2-123">Name</span></span>                               | <span data-ttu-id="1a8b2-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1a8b2-124">Data type</span></span>         | <span data-ttu-id="1a8b2-125">Unità</span><span class="sxs-lookup"><span data-stu-id="1a8b2-125">Unit</span></span>                   | <span data-ttu-id="1a8b2-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="1a8b2-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1a8b2-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="1a8b2-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1a8b2-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1a8b2-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1a8b2-129">string</span><span class="sxs-lookup"><span data-stu-id="1a8b2-129">string</span></span><br/> | <span data-ttu-id="1a8b2-130">caratteri</span><span class="sxs-lookup"><span data-stu-id="1a8b2-130">characters</span></span> <br/> | <span data-ttu-id="1a8b2-131">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1a8b2-132">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1a8b2-133">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="1a8b2-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="1a8b2-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1a8b2-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1a8b2-135">string</span><span class="sxs-lookup"><span data-stu-id="1a8b2-135">string</span></span><br/> | <span data-ttu-id="1a8b2-136">n/d</span><span class="sxs-lookup"><span data-stu-id="1a8b2-136">n/a</span></span><br/>         | <span data-ttu-id="1a8b2-137">True, False</span><span class="sxs-lookup"><span data-stu-id="1a8b2-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="1a8b2-138">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1a8b2-139">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="1a8b2-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1a8b2-140">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1a8b2-141">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="1a8b2-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="1a8b2-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a8b2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a8b2-143">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1a8b2-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




