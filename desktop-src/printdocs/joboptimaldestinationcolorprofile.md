---
description: Informazioni sull'elemento JobOptimalDestinationColorProfile che specifica il profilo colori ottimale in base alla configurazione del dispositivo corrente.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408844"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="303b5-103">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="303b5-103">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="303b5-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="303b5-104">This topic is not current.</span></span> <span data-ttu-id="303b5-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="303b5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="303b5-106">Specifica il profilo colori ottimale in base alla configurazione del dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="303b5-106">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="303b5-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="303b5-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="303b5-108">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="303b5-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="303b5-109">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="303b5-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="303b5-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="303b5-110">Element Information</span></span>



| <span data-ttu-id="303b5-111">Nome</span><span class="sxs-lookup"><span data-stu-id="303b5-111">Name</span></span> | <span data-ttu-id="303b5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="303b5-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="303b5-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="303b5-113">Element Type</span></span> <br/>   | <span data-ttu-id="303b5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="303b5-114">Property</span></span><br/> |
| <span data-ttu-id="303b5-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="303b5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="303b5-116">Processo</span><span class="sxs-lookup"><span data-stu-id="303b5-116">Job</span></span><br/>      |
| <span data-ttu-id="303b5-117">Note</span><span class="sxs-lookup"><span data-stu-id="303b5-117">Notes</span></span> <br/>          | <span data-ttu-id="303b5-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="303b5-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="303b5-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="303b5-119">Structural Content</span></span>

<span data-ttu-id="303b5-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="303b5-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="303b5-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="303b5-121">Structure Variables</span></span>

<span data-ttu-id="303b5-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="303b5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="303b5-123">Nome</span><span class="sxs-lookup"><span data-stu-id="303b5-123">Name</span></span>                            | <span data-ttu-id="303b5-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="303b5-124">Data type</span></span>         | <span data-ttu-id="303b5-125">Unità</span><span class="sxs-lookup"><span data-stu-id="303b5-125">Unit</span></span>           | <span data-ttu-id="303b5-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="303b5-126">Supported values</span></span>          | <span data-ttu-id="303b5-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="303b5-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="303b5-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="303b5-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="303b5-129">string</span><span class="sxs-lookup"><span data-stu-id="303b5-129">string</span></span><br/> | <span data-ttu-id="303b5-130">n/d</span><span class="sxs-lookup"><span data-stu-id="303b5-130">n/a</span></span><br/> | <span data-ttu-id="303b5-131">RGB, ICC, CMYK</span><span class="sxs-lookup"><span data-stu-id="303b5-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="303b5-132">Specifica il profilo colori.</span><span class="sxs-lookup"><span data-stu-id="303b5-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="303b5-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="303b5-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="303b5-134">string</span><span class="sxs-lookup"><span data-stu-id="303b5-134">string</span></span><br/> | <span data-ttu-id="303b5-135">n/d</span><span class="sxs-lookup"><span data-stu-id="303b5-135">n/a</span></span><br/> | <span data-ttu-id="303b5-136">n/d</span><span class="sxs-lookup"><span data-stu-id="303b5-136">n/a</span></span><br/>            | <span data-ttu-id="303b5-137">Specifica il percorso del file del profilo.</span><span class="sxs-lookup"><span data-stu-id="303b5-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="303b5-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="303b5-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="303b5-139">string</span><span class="sxs-lookup"><span data-stu-id="303b5-139">string</span></span><br/> | <span data-ttu-id="303b5-140">n/d</span><span class="sxs-lookup"><span data-stu-id="303b5-140">n/a</span></span><br/> | <span data-ttu-id="303b5-141">n/d</span><span class="sxs-lookup"><span data-stu-id="303b5-141">n/a</span></span><br/>            | <span data-ttu-id="303b5-142">Contiene il contenuto dei dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="303b5-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="303b5-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="303b5-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="303b5-144">Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi .</span><span class="sxs-lookup"><span data-stu-id="303b5-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="303b5-145">Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="303b5-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="303b5-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="303b5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="303b5-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="303b5-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




