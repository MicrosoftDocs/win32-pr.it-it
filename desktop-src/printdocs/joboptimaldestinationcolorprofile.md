---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999253"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="73b0a-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="73b0a-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="73b0a-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="73b0a-105">This topic is not current.</span></span> <span data-ttu-id="73b0a-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="73b0a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="73b0a-107">Specifica il profilo colori ottimale in base alla configurazione del dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="73b0a-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="73b0a-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="73b0a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="73b0a-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="73b0a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="73b0a-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="73b0a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="73b0a-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="73b0a-111">Element Information</span></span>



| <span data-ttu-id="73b0a-112">Nome</span><span class="sxs-lookup"><span data-stu-id="73b0a-112">Name</span></span> | <span data-ttu-id="73b0a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="73b0a-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="73b0a-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="73b0a-114">Element Type</span></span> <br/>   | <span data-ttu-id="73b0a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73b0a-115">Property</span></span><br/> |
| <span data-ttu-id="73b0a-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="73b0a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="73b0a-117">Processo</span><span class="sxs-lookup"><span data-stu-id="73b0a-117">Job</span></span><br/>      |
| <span data-ttu-id="73b0a-118">Note</span><span class="sxs-lookup"><span data-stu-id="73b0a-118">Notes</span></span> <br/>          | <span data-ttu-id="73b0a-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="73b0a-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="73b0a-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="73b0a-120">Structural Content</span></span>

<span data-ttu-id="73b0a-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="73b0a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="73b0a-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="73b0a-122">Structure Variables</span></span>

<span data-ttu-id="73b0a-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="73b0a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="73b0a-124">Nome</span><span class="sxs-lookup"><span data-stu-id="73b0a-124">Name</span></span>                            | <span data-ttu-id="73b0a-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="73b0a-125">Data type</span></span>         | <span data-ttu-id="73b0a-126">Unità</span><span class="sxs-lookup"><span data-stu-id="73b0a-126">Unit</span></span>           | <span data-ttu-id="73b0a-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="73b0a-127">Supported values</span></span>          | <span data-ttu-id="73b0a-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="73b0a-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="73b0a-129">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="73b0a-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="73b0a-130">string</span><span class="sxs-lookup"><span data-stu-id="73b0a-130">string</span></span><br/> | <span data-ttu-id="73b0a-131">n/d</span><span class="sxs-lookup"><span data-stu-id="73b0a-131">n/a</span></span><br/> | <span data-ttu-id="73b0a-132">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="73b0a-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="73b0a-133">Specifica il profilo colori.</span><span class="sxs-lookup"><span data-stu-id="73b0a-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="73b0a-134">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="73b0a-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="73b0a-135">string</span><span class="sxs-lookup"><span data-stu-id="73b0a-135">string</span></span><br/> | <span data-ttu-id="73b0a-136">n/d</span><span class="sxs-lookup"><span data-stu-id="73b0a-136">n/a</span></span><br/> | <span data-ttu-id="73b0a-137">n/d</span><span class="sxs-lookup"><span data-stu-id="73b0a-137">n/a</span></span><br/>            | <span data-ttu-id="73b0a-138">Specifica il percorso del file del profilo.</span><span class="sxs-lookup"><span data-stu-id="73b0a-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="73b0a-139">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="73b0a-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="73b0a-140">string</span><span class="sxs-lookup"><span data-stu-id="73b0a-140">string</span></span><br/> | <span data-ttu-id="73b0a-141">n/d</span><span class="sxs-lookup"><span data-stu-id="73b0a-141">n/a</span></span><br/> | <span data-ttu-id="73b0a-142">n/d</span><span class="sxs-lookup"><span data-stu-id="73b0a-142">n/a</span></span><br/>            | <span data-ttu-id="73b0a-143">Contiene il contenuto dei dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="73b0a-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="73b0a-144">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="73b0a-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="73b0a-145">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="73b0a-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="73b0a-146">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="73b0a-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="73b0a-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73b0a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73b0a-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="73b0a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




