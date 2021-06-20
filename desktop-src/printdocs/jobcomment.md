---
description: Informazioni sull'elemento JobComment, che specifica un commento associato al processo, ad esempio, Recapitare alla stanza 1234 al termine.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409044"
---
# <a name="jobcomment"></a><span data-ttu-id="a86e6-103">JobComment</span><span class="sxs-lookup"><span data-stu-id="a86e6-103">JobComment</span></span>

<span data-ttu-id="a86e6-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a86e6-104">This topic is not current.</span></span> <span data-ttu-id="a86e6-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a86e6-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a86e6-106">Specifica un commento associato al processo.</span><span class="sxs-lookup"><span data-stu-id="a86e6-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="a86e6-107">Esempio: "Recapitare alla stanza 1234 al termine".</span><span class="sxs-lookup"><span data-stu-id="a86e6-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="a86e6-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a86e6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a86e6-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="a86e6-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a86e6-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a86e6-110">Element Information</span></span>



| <span data-ttu-id="a86e6-111">Nome</span><span class="sxs-lookup"><span data-stu-id="a86e6-111">Name</span></span> | <span data-ttu-id="a86e6-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a86e6-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="a86e6-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a86e6-113">Element Type</span></span> <br/>   | <span data-ttu-id="a86e6-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a86e6-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="a86e6-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a86e6-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a86e6-116">Processo</span><span class="sxs-lookup"><span data-stu-id="a86e6-116">Job</span></span><br/>          |
| <span data-ttu-id="a86e6-117">Note</span><span class="sxs-lookup"><span data-stu-id="a86e6-117">Notes</span></span> <br/>          | <span data-ttu-id="a86e6-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="a86e6-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="a86e6-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="a86e6-119">Structure Content</span></span>

<span data-ttu-id="a86e6-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="a86e6-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a86e6-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="a86e6-121">Structure Properties</span></span>

<span data-ttu-id="a86e6-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a86e6-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a86e6-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a86e6-123">Property</span></span>                | <span data-ttu-id="a86e6-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a86e6-124">xsi:type</span></span>           | <span data-ttu-id="a86e6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a86e6-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a86e6-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a86e6-126">DataType</span></span><br/>     | <span data-ttu-id="a86e6-127">string</span><span class="sxs-lookup"><span data-stu-id="a86e6-127">string</span></span><br/>  | <span data-ttu-id="a86e6-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a86e6-128">xs:string</span></span><br/>       |
| <span data-ttu-id="a86e6-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a86e6-129">DefaultValue</span></span><br/> | <span data-ttu-id="a86e6-130">string</span><span class="sxs-lookup"><span data-stu-id="a86e6-130">string</span></span><br/>  | <span data-ttu-id="a86e6-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="a86e6-131">undefined</span></span><br/>       |
| <span data-ttu-id="a86e6-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a86e6-132">MaxLength</span></span><br/>    | <span data-ttu-id="a86e6-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="a86e6-133">integer</span></span><br/> | <span data-ttu-id="a86e6-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="a86e6-134">undefined</span></span><br/>       |
| <span data-ttu-id="a86e6-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="a86e6-135">MinLength</span></span><br/>    | <span data-ttu-id="a86e6-136">integer</span><span class="sxs-lookup"><span data-stu-id="a86e6-136">integer</span></span><br/> | <span data-ttu-id="a86e6-137">1</span><span class="sxs-lookup"><span data-stu-id="a86e6-137">1</span></span><br/>               |
| <span data-ttu-id="a86e6-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="a86e6-138">Mandatory</span></span><br/>    | <span data-ttu-id="a86e6-139">string</span><span class="sxs-lookup"><span data-stu-id="a86e6-139">string</span></span><br/>  | <span data-ttu-id="a86e6-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a86e6-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a86e6-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="a86e6-141">UnitType</span></span><br/>     | <span data-ttu-id="a86e6-142">string</span><span class="sxs-lookup"><span data-stu-id="a86e6-142">string</span></span><br/>  | <span data-ttu-id="a86e6-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="a86e6-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a86e6-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a86e6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a86e6-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a86e6-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




