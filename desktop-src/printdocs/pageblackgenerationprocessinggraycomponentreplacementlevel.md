---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553919bf9fab43cb1281f625eb518937b5c8b805
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994528"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="1c53a-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="1c53a-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="1c53a-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1c53a-105">This topic is not current.</span></span> <span data-ttu-id="1c53a-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1c53a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1c53a-107">Specifica la percentuale di sostituzione del componente grigio da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1c53a-107">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="1c53a-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1c53a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1c53a-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1c53a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1c53a-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1c53a-110">Element Information</span></span>



| <span data-ttu-id="1c53a-111">Nome</span><span class="sxs-lookup"><span data-stu-id="1c53a-111">Name</span></span> | <span data-ttu-id="1c53a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1c53a-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c53a-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1c53a-113">Element Type</span></span> <br/>   | <span data-ttu-id="1c53a-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1c53a-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1c53a-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1c53a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1c53a-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="1c53a-116">Page</span></span><br/>                                            |
| <span data-ttu-id="1c53a-117">Note</span><span class="sxs-lookup"><span data-stu-id="1c53a-117">Notes</span></span> <br/>          | <span data-ttu-id="1c53a-118">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="1c53a-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1c53a-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1c53a-119">Structure Content</span></span>

<span data-ttu-id="1c53a-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="1c53a-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="1c53a-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="1c53a-121">Structure Properties</span></span>

<span data-ttu-id="1c53a-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1c53a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1c53a-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c53a-123">Property</span></span>                | <span data-ttu-id="1c53a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1c53a-124">xsi:type</span></span>           | <span data-ttu-id="1c53a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1c53a-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1c53a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="1c53a-126">DataType</span></span><br/>     | <span data-ttu-id="1c53a-127">string</span><span class="sxs-lookup"><span data-stu-id="1c53a-127">string</span></span><br/>  | <span data-ttu-id="1c53a-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1c53a-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="1c53a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1c53a-129">DefaultValue</span></span><br/> | <span data-ttu-id="1c53a-130">string</span><span class="sxs-lookup"><span data-stu-id="1c53a-130">string</span></span><br/>  | <span data-ttu-id="1c53a-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="1c53a-131">undefined</span></span><br/>       |
| <span data-ttu-id="1c53a-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1c53a-132">MaxValue</span></span><br/>     | <span data-ttu-id="1c53a-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="1c53a-133">integer</span></span><br/> | <span data-ttu-id="1c53a-134">100</span><span class="sxs-lookup"><span data-stu-id="1c53a-134">100</span></span><br/>             |
| <span data-ttu-id="1c53a-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="1c53a-135">MinValue</span></span><br/>     | <span data-ttu-id="1c53a-136">integer</span><span class="sxs-lookup"><span data-stu-id="1c53a-136">integer</span></span><br/> | <span data-ttu-id="1c53a-137">0</span><span class="sxs-lookup"><span data-stu-id="1c53a-137">0</span></span><br/>               |
| <span data-ttu-id="1c53a-138">Più elementi</span><span class="sxs-lookup"><span data-stu-id="1c53a-138">Multiple</span></span><br/>     | <span data-ttu-id="1c53a-139">integer</span><span class="sxs-lookup"><span data-stu-id="1c53a-139">integer</span></span><br/> | <span data-ttu-id="1c53a-140">1</span><span class="sxs-lookup"><span data-stu-id="1c53a-140">1</span></span><br/>               |
| <span data-ttu-id="1c53a-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="1c53a-141">Mandatory</span></span><br/>    | <span data-ttu-id="1c53a-142">string</span><span class="sxs-lookup"><span data-stu-id="1c53a-142">string</span></span><br/>  | <span data-ttu-id="1c53a-143">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="1c53a-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1c53a-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="1c53a-144">UnitType</span></span><br/>     | <span data-ttu-id="1c53a-145">string</span><span class="sxs-lookup"><span data-stu-id="1c53a-145">string</span></span><br/>  | <span data-ttu-id="1c53a-146">percent</span><span class="sxs-lookup"><span data-stu-id="1c53a-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1c53a-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c53a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c53a-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1c53a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




