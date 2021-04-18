---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320971"
---
# <a name="jobcomment"></a><span data-ttu-id="cc8aa-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="cc8aa-104">JobComment</span></span>

<span data-ttu-id="cc8aa-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="cc8aa-105">This topic is not current.</span></span> <span data-ttu-id="cc8aa-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cc8aa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cc8aa-107">Specifica un commento associato al processo.</span><span class="sxs-lookup"><span data-stu-id="cc8aa-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="cc8aa-108">Esempio: "recapitare alla chat room 1234 al termine dell'operazione".</span><span class="sxs-lookup"><span data-stu-id="cc8aa-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="cc8aa-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cc8aa-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cc8aa-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="cc8aa-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cc8aa-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cc8aa-111">Element Information</span></span>



| <span data-ttu-id="cc8aa-112">Nome</span><span class="sxs-lookup"><span data-stu-id="cc8aa-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="cc8aa-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="cc8aa-113">Element Type</span></span> <br/>   | <span data-ttu-id="cc8aa-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cc8aa-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="cc8aa-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="cc8aa-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cc8aa-116">Processo</span><span class="sxs-lookup"><span data-stu-id="cc8aa-116">Job</span></span><br/>          |
| <span data-ttu-id="cc8aa-117">Note</span><span class="sxs-lookup"><span data-stu-id="cc8aa-117">Notes</span></span> <br/>          | <span data-ttu-id="cc8aa-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="cc8aa-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="cc8aa-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="cc8aa-119">Structure Content</span></span>

<span data-ttu-id="cc8aa-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="cc8aa-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cc8aa-121">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="cc8aa-121">Structure Properties</span></span>

<span data-ttu-id="cc8aa-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="cc8aa-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cc8aa-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cc8aa-123">Property</span></span>                | <span data-ttu-id="cc8aa-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cc8aa-124">xsi:type</span></span>           | <span data-ttu-id="cc8aa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cc8aa-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cc8aa-126">DataType</span><span class="sxs-lookup"><span data-stu-id="cc8aa-126">DataType</span></span><br/>     | <span data-ttu-id="cc8aa-127">string</span><span class="sxs-lookup"><span data-stu-id="cc8aa-127">string</span></span><br/>  | <span data-ttu-id="cc8aa-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc8aa-128">xs:string</span></span><br/>       |
| <span data-ttu-id="cc8aa-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cc8aa-129">DefaultValue</span></span><br/> | <span data-ttu-id="cc8aa-130">string</span><span class="sxs-lookup"><span data-stu-id="cc8aa-130">string</span></span><br/>  | <span data-ttu-id="cc8aa-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="cc8aa-131">undefined</span></span><br/>       |
| <span data-ttu-id="cc8aa-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="cc8aa-132">MaxLength</span></span><br/>    | <span data-ttu-id="cc8aa-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="cc8aa-133">integer</span></span><br/> | <span data-ttu-id="cc8aa-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="cc8aa-134">undefined</span></span><br/>       |
| <span data-ttu-id="cc8aa-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="cc8aa-135">MinLength</span></span><br/>    | <span data-ttu-id="cc8aa-136">integer</span><span class="sxs-lookup"><span data-stu-id="cc8aa-136">integer</span></span><br/> | <span data-ttu-id="cc8aa-137">1</span><span class="sxs-lookup"><span data-stu-id="cc8aa-137">1</span></span><br/>               |
| <span data-ttu-id="cc8aa-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="cc8aa-138">Mandatory</span></span><br/>    | <span data-ttu-id="cc8aa-139">string</span><span class="sxs-lookup"><span data-stu-id="cc8aa-139">string</span></span><br/>  | <span data-ttu-id="cc8aa-140">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="cc8aa-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cc8aa-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="cc8aa-141">UnitType</span></span><br/>     | <span data-ttu-id="cc8aa-142">string</span><span class="sxs-lookup"><span data-stu-id="cc8aa-142">string</span></span><br/>  | <span data-ttu-id="cc8aa-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="cc8aa-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="cc8aa-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc8aa-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc8aa-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="cc8aa-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




