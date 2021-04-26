---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998288"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="aa979-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="aa979-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="aa979-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="aa979-105">This topic is not current.</span></span> <span data-ttu-id="aa979-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aa979-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aa979-107">Descrive la configurazione dell'elaborazione della firma digitale per l'intero processo.</span><span class="sxs-lookup"><span data-stu-id="aa979-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="aa979-108">Applicabile solo al contenuto che contiene firme digitali.</span><span class="sxs-lookup"><span data-stu-id="aa979-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="aa979-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="aa979-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aa979-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="aa979-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="aa979-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="aa979-111">Element Information</span></span>



| <span data-ttu-id="aa979-112">Nome</span><span class="sxs-lookup"><span data-stu-id="aa979-112">Name</span></span> | <span data-ttu-id="aa979-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aa979-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="aa979-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="aa979-114">Element Type</span></span> <br/>   | <span data-ttu-id="aa979-115">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="aa979-115">Feature</span></span><br/> |
| <span data-ttu-id="aa979-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="aa979-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aa979-117">Processo</span><span class="sxs-lookup"><span data-stu-id="aa979-117">Job</span></span><br/>     |
| <span data-ttu-id="aa979-118">Note</span><span class="sxs-lookup"><span data-stu-id="aa979-118">Notes</span></span> <br/>          | <span data-ttu-id="aa979-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="aa979-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="aa979-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="aa979-120">Structural Content</span></span>

<span data-ttu-id="aa979-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="aa979-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="aa979-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="aa979-122">Structure Variables</span></span>

<span data-ttu-id="aa979-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="aa979-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aa979-124">Nome</span><span class="sxs-lookup"><span data-stu-id="aa979-124">Name</span></span>                               | <span data-ttu-id="aa979-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="aa979-125">Data type</span></span>         | <span data-ttu-id="aa979-126">Unità</span><span class="sxs-lookup"><span data-stu-id="aa979-126">Unit</span></span>                   | <span data-ttu-id="aa979-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="aa979-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="aa979-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="aa979-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aa979-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="aa979-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="aa979-130">string</span><span class="sxs-lookup"><span data-stu-id="aa979-130">string</span></span><br/> | <span data-ttu-id="aa979-131">caratteri</span><span class="sxs-lookup"><span data-stu-id="aa979-131">characters</span></span> <br/> | <span data-ttu-id="aa979-132">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="aa979-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="aa979-133">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="aa979-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aa979-134">Nome dell'opzione</span><span class="sxs-lookup"><span data-stu-id="aa979-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="aa979-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="aa979-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="aa979-136">string</span><span class="sxs-lookup"><span data-stu-id="aa979-136">string</span></span><br/> | <span data-ttu-id="aa979-137">n/d</span><span class="sxs-lookup"><span data-stu-id="aa979-137">n/a</span></span><br/>         | <span data-ttu-id="aa979-138">True, False</span><span class="sxs-lookup"><span data-stu-id="aa979-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="aa979-139">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aa979-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aa979-140">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="aa979-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aa979-141">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="aa979-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aa979-142">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="aa979-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="aa979-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa979-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa979-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="aa979-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




