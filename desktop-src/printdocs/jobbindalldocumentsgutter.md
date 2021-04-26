---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998378"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="7b80d-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="7b80d-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="7b80d-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="7b80d-105">This topic is not current.</span></span> <span data-ttu-id="7b80d-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b80d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b80d-107">Specifica la larghezza della barra di associazione.</span><span class="sxs-lookup"><span data-stu-id="7b80d-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="7b80d-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7b80d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b80d-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7b80d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7b80d-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7b80d-110">Element Information</span></span>



| <span data-ttu-id="7b80d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7b80d-111">Name</span></span> | <span data-ttu-id="7b80d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7b80d-112">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="7b80d-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7b80d-113">Element Type</span></span> <br/>   | <span data-ttu-id="7b80d-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7b80d-114">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="7b80d-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="7b80d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b80d-116">Processo</span><span class="sxs-lookup"><span data-stu-id="7b80d-116">Job</span></span> <br/>                         |
| <span data-ttu-id="7b80d-117">Note</span><span class="sxs-lookup"><span data-stu-id="7b80d-117">Notes</span></span> <br/>          | <span data-ttu-id="7b80d-118">Collegato all'elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="7b80d-118">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7b80d-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7b80d-119">Structure Content</span></span>

<span data-ttu-id="7b80d-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="7b80d-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="7b80d-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="7b80d-121">Structure Properties</span></span>

<span data-ttu-id="7b80d-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7b80d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b80d-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b80d-123">Property</span></span>                | <span data-ttu-id="7b80d-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7b80d-124">xsi:type</span></span>           | <span data-ttu-id="7b80d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7b80d-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7b80d-126">DataType</span><span class="sxs-lookup"><span data-stu-id="7b80d-126">DataType</span></span><br/>     | <span data-ttu-id="7b80d-127">string</span><span class="sxs-lookup"><span data-stu-id="7b80d-127">string</span></span><br/>  | <span data-ttu-id="7b80d-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7b80d-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="7b80d-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7b80d-129">DefaultValue</span></span><br/> | <span data-ttu-id="7b80d-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="7b80d-130">integer</span></span><br/> | <span data-ttu-id="7b80d-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="7b80d-131">undefined</span></span><br/>       |
| <span data-ttu-id="7b80d-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7b80d-132">MaxValue</span></span><br/>     | <span data-ttu-id="7b80d-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="7b80d-133">integer</span></span><br/> | <span data-ttu-id="7b80d-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="7b80d-134">undefined</span></span><br/>       |
| <span data-ttu-id="7b80d-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="7b80d-135">MinValue</span></span><br/>     | <span data-ttu-id="7b80d-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="7b80d-136">integer</span></span><br/> | <span data-ttu-id="7b80d-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="7b80d-137">undefined</span></span><br/>       |
| <span data-ttu-id="7b80d-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7b80d-138">Mandatory</span></span><br/>    | <span data-ttu-id="7b80d-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="7b80d-139">String</span></span><br/>  | <span data-ttu-id="7b80d-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="7b80d-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7b80d-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="7b80d-141">Multiple</span></span><br/>     | <span data-ttu-id="7b80d-142">integer</span><span class="sxs-lookup"><span data-stu-id="7b80d-142">integer</span></span><br/> | <span data-ttu-id="7b80d-143">1</span><span class="sxs-lookup"><span data-stu-id="7b80d-143">1</span></span><br/>               |
| <span data-ttu-id="7b80d-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="7b80d-144">UnitType</span></span><br/>     | <span data-ttu-id="7b80d-145">string</span><span class="sxs-lookup"><span data-stu-id="7b80d-145">string</span></span><br/>  | <span data-ttu-id="7b80d-146">Micron</span><span class="sxs-lookup"><span data-stu-id="7b80d-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7b80d-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b80d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b80d-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7b80d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




