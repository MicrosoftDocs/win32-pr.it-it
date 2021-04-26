---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998348"
---
# <a name="jobcomment"></a><span data-ttu-id="67e90-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="67e90-104">JobComment</span></span>

<span data-ttu-id="67e90-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="67e90-105">This topic is not current.</span></span> <span data-ttu-id="67e90-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="67e90-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="67e90-107">Specifica un commento associato al processo.</span><span class="sxs-lookup"><span data-stu-id="67e90-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="67e90-108">Esempio: "Recapitare alla stanza 1234 al termine".</span><span class="sxs-lookup"><span data-stu-id="67e90-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="67e90-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="67e90-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="67e90-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="67e90-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="67e90-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="67e90-111">Element Information</span></span>



| <span data-ttu-id="67e90-112">Nome</span><span class="sxs-lookup"><span data-stu-id="67e90-112">Name</span></span> | <span data-ttu-id="67e90-113">Valore</span><span class="sxs-lookup"><span data-stu-id="67e90-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="67e90-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="67e90-114">Element Type</span></span> <br/>   | <span data-ttu-id="67e90-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="67e90-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="67e90-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="67e90-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="67e90-117">Processo</span><span class="sxs-lookup"><span data-stu-id="67e90-117">Job</span></span><br/>          |
| <span data-ttu-id="67e90-118">Note</span><span class="sxs-lookup"><span data-stu-id="67e90-118">Notes</span></span> <br/>          | <span data-ttu-id="67e90-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="67e90-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="67e90-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="67e90-120">Structure Content</span></span>

<span data-ttu-id="67e90-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="67e90-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="67e90-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="67e90-122">Structure Properties</span></span>

<span data-ttu-id="67e90-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="67e90-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="67e90-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="67e90-124">Property</span></span>                | <span data-ttu-id="67e90-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="67e90-125">xsi:type</span></span>           | <span data-ttu-id="67e90-126">Valore</span><span class="sxs-lookup"><span data-stu-id="67e90-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="67e90-127">DataType</span><span class="sxs-lookup"><span data-stu-id="67e90-127">DataType</span></span><br/>     | <span data-ttu-id="67e90-128">string</span><span class="sxs-lookup"><span data-stu-id="67e90-128">string</span></span><br/>  | <span data-ttu-id="67e90-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="67e90-129">xs:string</span></span><br/>       |
| <span data-ttu-id="67e90-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="67e90-130">DefaultValue</span></span><br/> | <span data-ttu-id="67e90-131">string</span><span class="sxs-lookup"><span data-stu-id="67e90-131">string</span></span><br/>  | <span data-ttu-id="67e90-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="67e90-132">undefined</span></span><br/>       |
| <span data-ttu-id="67e90-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="67e90-133">MaxLength</span></span><br/>    | <span data-ttu-id="67e90-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="67e90-134">integer</span></span><br/> | <span data-ttu-id="67e90-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="67e90-135">undefined</span></span><br/>       |
| <span data-ttu-id="67e90-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="67e90-136">MinLength</span></span><br/>    | <span data-ttu-id="67e90-137">integer</span><span class="sxs-lookup"><span data-stu-id="67e90-137">integer</span></span><br/> | <span data-ttu-id="67e90-138">1</span><span class="sxs-lookup"><span data-stu-id="67e90-138">1</span></span><br/>               |
| <span data-ttu-id="67e90-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="67e90-139">Mandatory</span></span><br/>    | <span data-ttu-id="67e90-140">string</span><span class="sxs-lookup"><span data-stu-id="67e90-140">string</span></span><br/>  | <span data-ttu-id="67e90-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="67e90-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="67e90-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="67e90-142">UnitType</span></span><br/>     | <span data-ttu-id="67e90-143">string</span><span class="sxs-lookup"><span data-stu-id="67e90-143">string</span></span><br/>  | <span data-ttu-id="67e90-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="67e90-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="67e90-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67e90-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67e90-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="67e90-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




