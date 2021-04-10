---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954f67df5720e19de39d2c1c752c6d9eb860a502
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103969017"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="781ed-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="781ed-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="781ed-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="781ed-105">This topic is not current.</span></span> <span data-ttu-id="781ed-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="781ed-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="781ed-107">Specifica il profilo colori ottimale in base alla configurazione corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="781ed-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="781ed-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="781ed-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="781ed-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="781ed-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="781ed-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="781ed-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="781ed-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="781ed-111">Element Information</span></span>



| <span data-ttu-id="781ed-112">Nome</span><span class="sxs-lookup"><span data-stu-id="781ed-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="781ed-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="781ed-113">Element Type</span></span> <br/>   | <span data-ttu-id="781ed-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="781ed-114">Property</span></span><br/> |
| <span data-ttu-id="781ed-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="781ed-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="781ed-116">Processo</span><span class="sxs-lookup"><span data-stu-id="781ed-116">Job</span></span><br/>      |
| <span data-ttu-id="781ed-117">Note</span><span class="sxs-lookup"><span data-stu-id="781ed-117">Notes</span></span> <br/>          | <span data-ttu-id="781ed-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="781ed-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="781ed-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="781ed-119">Structural Content</span></span>

<span data-ttu-id="781ed-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="781ed-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="781ed-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="781ed-121">Structure Variables</span></span>

<span data-ttu-id="781ed-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="781ed-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="781ed-123">Nome</span><span class="sxs-lookup"><span data-stu-id="781ed-123">Name</span></span>                            | <span data-ttu-id="781ed-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="781ed-124">Data type</span></span>         | <span data-ttu-id="781ed-125">Unità</span><span class="sxs-lookup"><span data-stu-id="781ed-125">Unit</span></span>           | <span data-ttu-id="781ed-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="781ed-126">Supported values</span></span>          | <span data-ttu-id="781ed-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="781ed-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="781ed-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="781ed-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="781ed-129">string</span><span class="sxs-lookup"><span data-stu-id="781ed-129">string</span></span><br/> | <span data-ttu-id="781ed-130">n/d</span><span class="sxs-lookup"><span data-stu-id="781ed-130">n/a</span></span><br/> | <span data-ttu-id="781ed-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="781ed-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="781ed-132">Specifica il profilo colori.</span><span class="sxs-lookup"><span data-stu-id="781ed-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="781ed-133">\_Su pathValue\_</span><span class="sxs-lookup"><span data-stu-id="781ed-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="781ed-134">string</span><span class="sxs-lookup"><span data-stu-id="781ed-134">string</span></span><br/> | <span data-ttu-id="781ed-135">n/d</span><span class="sxs-lookup"><span data-stu-id="781ed-135">n/a</span></span><br/> | <span data-ttu-id="781ed-136">n/d</span><span class="sxs-lookup"><span data-stu-id="781ed-136">n/a</span></span><br/>            | <span data-ttu-id="781ed-137">Specifica il percorso del file del profilo.</span><span class="sxs-lookup"><span data-stu-id="781ed-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="781ed-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="781ed-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="781ed-139">string</span><span class="sxs-lookup"><span data-stu-id="781ed-139">string</span></span><br/> | <span data-ttu-id="781ed-140">n/d</span><span class="sxs-lookup"><span data-stu-id="781ed-140">n/a</span></span><br/> | <span data-ttu-id="781ed-141">n/d</span><span class="sxs-lookup"><span data-stu-id="781ed-141">n/a</span></span><br/>            | <span data-ttu-id="781ed-142">Contiene il contenuto dei dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="781ed-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="781ed-143">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="781ed-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="781ed-144">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="781ed-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="781ed-145">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="781ed-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="781ed-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="781ed-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="781ed-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="781ed-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




