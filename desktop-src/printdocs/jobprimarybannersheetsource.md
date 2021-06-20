---
description: Informazioni sull'elemento JobPrimaryBannerSheetSource, che specifica l'origine per un foglio banner personalizzato primario per il processo.
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: JobPrimaryBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366266576fca98762fd7d3dcb7e491a6cc94f529
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408714"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="7b2a9-103">JobPrimaryBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="7b2a9-103">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="7b2a9-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7b2a9-104">This topic is not current.</span></span> <span data-ttu-id="7b2a9-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b2a9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b2a9-106">Specifica l'origine per un foglio banner personalizzato primario per il processo.</span><span class="sxs-lookup"><span data-stu-id="7b2a9-106">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="7b2a9-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7b2a9-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b2a9-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7b2a9-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7b2a9-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7b2a9-109">Element Information</span></span>



| <span data-ttu-id="7b2a9-110">Nome</span><span class="sxs-lookup"><span data-stu-id="7b2a9-110">Name</span></span> | <span data-ttu-id="7b2a9-111">Valore</span><span class="sxs-lookup"><span data-stu-id="7b2a9-111">Value</span></span> |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="7b2a9-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7b2a9-112">Element Type</span></span> <br/>   | <span data-ttu-id="7b2a9-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7b2a9-113">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="7b2a9-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7b2a9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b2a9-115">Processo</span><span class="sxs-lookup"><span data-stu-id="7b2a9-115">Job</span></span><br/>                              |
| <span data-ttu-id="7b2a9-116">Note</span><span class="sxs-lookup"><span data-stu-id="7b2a9-116">Notes</span></span> <br/>          | <span data-ttu-id="7b2a9-117">Collegato all'elemento JobBannerSheet</span><span class="sxs-lookup"><span data-stu-id="7b2a9-117">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7b2a9-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7b2a9-118">Structure Content</span></span>

<span data-ttu-id="7b2a9-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7b2a9-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryBannerSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="7b2a9-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="7b2a9-120">Structure Properties</span></span>

<span data-ttu-id="7b2a9-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7b2a9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b2a9-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b2a9-122">Property</span></span>                | <span data-ttu-id="7b2a9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7b2a9-123">xsi:type</span></span>           | <span data-ttu-id="7b2a9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7b2a9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7b2a9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7b2a9-125">DataType</span></span><br/>     | <span data-ttu-id="7b2a9-126">string</span><span class="sxs-lookup"><span data-stu-id="7b2a9-126">string</span></span><br/>  | <span data-ttu-id="7b2a9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b2a9-127">xs:string</span></span><br/>       |
| <span data-ttu-id="7b2a9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7b2a9-128">DefaultValue</span></span><br/> | <span data-ttu-id="7b2a9-129">string</span><span class="sxs-lookup"><span data-stu-id="7b2a9-129">string</span></span><br/>  | <span data-ttu-id="7b2a9-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="7b2a9-130">undefined</span></span><br/>       |
| <span data-ttu-id="7b2a9-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="7b2a9-131">MaxLength</span></span><br/>    | <span data-ttu-id="7b2a9-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="7b2a9-132">integer</span></span><br/> | <span data-ttu-id="7b2a9-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="7b2a9-133">undefined</span></span><br/>       |
| <span data-ttu-id="7b2a9-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="7b2a9-134">MinLength</span></span><br/>    | <span data-ttu-id="7b2a9-135">integer</span><span class="sxs-lookup"><span data-stu-id="7b2a9-135">integer</span></span><br/> | <span data-ttu-id="7b2a9-136">1</span><span class="sxs-lookup"><span data-stu-id="7b2a9-136">1</span></span><br/>               |
| <span data-ttu-id="7b2a9-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7b2a9-137">Mandatory</span></span><br/>    | <span data-ttu-id="7b2a9-138">string</span><span class="sxs-lookup"><span data-stu-id="7b2a9-138">string</span></span><br/>  | <span data-ttu-id="7b2a9-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7b2a9-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7b2a9-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="7b2a9-140">UnitType</span></span><br/>     | <span data-ttu-id="7b2a9-141">string</span><span class="sxs-lookup"><span data-stu-id="7b2a9-141">string</span></span><br/>  | <span data-ttu-id="7b2a9-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="7b2a9-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="7b2a9-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b2a9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2a9-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7b2a9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




