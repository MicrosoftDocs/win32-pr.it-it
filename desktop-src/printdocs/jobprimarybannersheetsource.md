---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: JobPrimaryBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556390d58df3073263a6a6b666d98c48ceed6469
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997738"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="6afe5-104">JobPrimaryBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="6afe5-104">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="6afe5-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6afe5-105">This topic is not current.</span></span> <span data-ttu-id="6afe5-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6afe5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6afe5-107">Specifica l'origine per un foglio banner personalizzato primario per il processo.</span><span class="sxs-lookup"><span data-stu-id="6afe5-107">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="6afe5-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6afe5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6afe5-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="6afe5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6afe5-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6afe5-110">Element Information</span></span>



| <span data-ttu-id="6afe5-111">Nome</span><span class="sxs-lookup"><span data-stu-id="6afe5-111">Name</span></span> | <span data-ttu-id="6afe5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6afe5-112">Value</span></span> |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="6afe5-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6afe5-113">Element Type</span></span> <br/>   | <span data-ttu-id="6afe5-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6afe5-114">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="6afe5-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6afe5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6afe5-116">Processo</span><span class="sxs-lookup"><span data-stu-id="6afe5-116">Job</span></span><br/>                              |
| <span data-ttu-id="6afe5-117">Note</span><span class="sxs-lookup"><span data-stu-id="6afe5-117">Notes</span></span> <br/>          | <span data-ttu-id="6afe5-118">Collegato all'elemento JobBannerSheet</span><span class="sxs-lookup"><span data-stu-id="6afe5-118">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6afe5-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="6afe5-119">Structure Content</span></span>

<span data-ttu-id="6afe5-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6afe5-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="6afe5-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="6afe5-121">Structure Properties</span></span>

<span data-ttu-id="6afe5-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6afe5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6afe5-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6afe5-123">Property</span></span>                | <span data-ttu-id="6afe5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6afe5-124">xsi:type</span></span>           | <span data-ttu-id="6afe5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6afe5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6afe5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="6afe5-126">DataType</span></span><br/>     | <span data-ttu-id="6afe5-127">string</span><span class="sxs-lookup"><span data-stu-id="6afe5-127">string</span></span><br/>  | <span data-ttu-id="6afe5-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="6afe5-128">xs:string</span></span><br/>       |
| <span data-ttu-id="6afe5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6afe5-129">DefaultValue</span></span><br/> | <span data-ttu-id="6afe5-130">string</span><span class="sxs-lookup"><span data-stu-id="6afe5-130">string</span></span><br/>  | <span data-ttu-id="6afe5-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="6afe5-131">undefined</span></span><br/>       |
| <span data-ttu-id="6afe5-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="6afe5-132">MaxLength</span></span><br/>    | <span data-ttu-id="6afe5-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="6afe5-133">integer</span></span><br/> | <span data-ttu-id="6afe5-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="6afe5-134">undefined</span></span><br/>       |
| <span data-ttu-id="6afe5-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="6afe5-135">MinLength</span></span><br/>    | <span data-ttu-id="6afe5-136">integer</span><span class="sxs-lookup"><span data-stu-id="6afe5-136">integer</span></span><br/> | <span data-ttu-id="6afe5-137">1</span><span class="sxs-lookup"><span data-stu-id="6afe5-137">1</span></span><br/>               |
| <span data-ttu-id="6afe5-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6afe5-138">Mandatory</span></span><br/>    | <span data-ttu-id="6afe5-139">string</span><span class="sxs-lookup"><span data-stu-id="6afe5-139">string</span></span><br/>  | <span data-ttu-id="6afe5-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="6afe5-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6afe5-141">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="6afe5-141">UnitType</span></span><br/>     | <span data-ttu-id="6afe5-142">string</span><span class="sxs-lookup"><span data-stu-id="6afe5-142">string</span></span><br/>  | <span data-ttu-id="6afe5-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="6afe5-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="6afe5-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6afe5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6afe5-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6afe5-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




