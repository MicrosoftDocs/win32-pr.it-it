---
description: Informazioni sull'elemento JobBindAllDocumentsGutter, che specifica la larghezza della barra di associazione.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42180ff9a00d1502d844b270fe5da7324825ca3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409074"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="4e6a4-103">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="4e6a4-103">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="4e6a4-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="4e6a4-104">This topic is not current.</span></span> <span data-ttu-id="4e6a4-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4e6a4-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4e6a4-106">Specifica la larghezza della barra di associazione.</span><span class="sxs-lookup"><span data-stu-id="4e6a4-106">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="4e6a4-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4e6a4-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4e6a4-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="4e6a4-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4e6a4-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4e6a4-109">Element Information</span></span>



| <span data-ttu-id="4e6a4-110">Nome</span><span class="sxs-lookup"><span data-stu-id="4e6a4-110">Name</span></span> | <span data-ttu-id="4e6a4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="4e6a4-111">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="4e6a4-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="4e6a4-112">Element Type</span></span> <br/>   | <span data-ttu-id="4e6a4-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4e6a4-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="4e6a4-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="4e6a4-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4e6a4-115">Processo</span><span class="sxs-lookup"><span data-stu-id="4e6a4-115">Job</span></span> <br/>                         |
| <span data-ttu-id="4e6a4-116">Note</span><span class="sxs-lookup"><span data-stu-id="4e6a4-116">Notes</span></span> <br/>          | <span data-ttu-id="4e6a4-117">Collegato all'elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="4e6a4-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4e6a4-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="4e6a4-118">Structure Content</span></span>

<span data-ttu-id="4e6a4-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="4e6a4-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4e6a4-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="4e6a4-120">Structure Properties</span></span>

<span data-ttu-id="4e6a4-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="4e6a4-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4e6a4-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e6a4-122">Property</span></span>                | <span data-ttu-id="4e6a4-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4e6a4-123">xsi:type</span></span>           | <span data-ttu-id="4e6a4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4e6a4-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4e6a4-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4e6a4-125">DataType</span></span><br/>     | <span data-ttu-id="4e6a4-126">string</span><span class="sxs-lookup"><span data-stu-id="4e6a4-126">string</span></span><br/>  | <span data-ttu-id="4e6a4-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4e6a4-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="4e6a4-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4e6a4-128">DefaultValue</span></span><br/> | <span data-ttu-id="4e6a4-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="4e6a4-129">integer</span></span><br/> | <span data-ttu-id="4e6a4-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="4e6a4-130">undefined</span></span><br/>       |
| <span data-ttu-id="4e6a4-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4e6a4-131">MaxValue</span></span><br/>     | <span data-ttu-id="4e6a4-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="4e6a4-132">integer</span></span><br/> | <span data-ttu-id="4e6a4-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="4e6a4-133">undefined</span></span><br/>       |
| <span data-ttu-id="4e6a4-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="4e6a4-134">MinValue</span></span><br/>     | <span data-ttu-id="4e6a4-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="4e6a4-135">integer</span></span><br/> | <span data-ttu-id="4e6a4-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="4e6a4-136">undefined</span></span><br/>       |
| <span data-ttu-id="4e6a4-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="4e6a4-137">Mandatory</span></span><br/>    | <span data-ttu-id="4e6a4-138">Stringa</span><span class="sxs-lookup"><span data-stu-id="4e6a4-138">String</span></span><br/>  | <span data-ttu-id="4e6a4-139">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="4e6a4-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4e6a4-140">Multipli</span><span class="sxs-lookup"><span data-stu-id="4e6a4-140">Multiple</span></span><br/>     | <span data-ttu-id="4e6a4-141">integer</span><span class="sxs-lookup"><span data-stu-id="4e6a4-141">integer</span></span><br/> | <span data-ttu-id="4e6a4-142">1</span><span class="sxs-lookup"><span data-stu-id="4e6a4-142">1</span></span><br/>               |
| <span data-ttu-id="4e6a4-143">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="4e6a4-143">UnitType</span></span><br/>     | <span data-ttu-id="4e6a4-144">string</span><span class="sxs-lookup"><span data-stu-id="4e6a4-144">string</span></span><br/>  | <span data-ttu-id="4e6a4-145">Micron</span><span class="sxs-lookup"><span data-stu-id="4e6a4-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4e6a4-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e6a4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e6a4-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4e6a4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




