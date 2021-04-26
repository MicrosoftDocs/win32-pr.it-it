---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2372636ea22610e6a209cfad3f1fe6297be34833
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997188"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="72a86-104">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="72a86-104">DocumentBindingGutter</span></span>

<span data-ttu-id="72a86-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="72a86-105">This topic is not current.</span></span> <span data-ttu-id="72a86-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="72a86-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72a86-107">Specifica la larghezza della barra di associazione.</span><span class="sxs-lookup"><span data-stu-id="72a86-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="72a86-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="72a86-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72a86-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="72a86-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="72a86-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="72a86-110">Element Information</span></span>



| <span data-ttu-id="72a86-111">Nome</span><span class="sxs-lookup"><span data-stu-id="72a86-111">Name</span></span> | <span data-ttu-id="72a86-112">Valore</span><span class="sxs-lookup"><span data-stu-id="72a86-112">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="72a86-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="72a86-113">Element Type</span></span> <br/>   | <span data-ttu-id="72a86-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="72a86-114">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="72a86-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="72a86-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72a86-116">Documento</span><span class="sxs-lookup"><span data-stu-id="72a86-116">Document</span></span><br/>                          |
| <span data-ttu-id="72a86-117">Note</span><span class="sxs-lookup"><span data-stu-id="72a86-117">Notes</span></span> <br/>          | <span data-ttu-id="72a86-118">Collegato all'elemento DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="72a86-118">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="72a86-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="72a86-119">Structure Content</span></span>

<span data-ttu-id="72a86-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="72a86-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="72a86-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="72a86-121">Structure Properties</span></span>

<span data-ttu-id="72a86-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="72a86-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72a86-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72a86-123">Property</span></span>                | <span data-ttu-id="72a86-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="72a86-124">xsi:type</span></span>           | <span data-ttu-id="72a86-125">Valore</span><span class="sxs-lookup"><span data-stu-id="72a86-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="72a86-126">DataType</span><span class="sxs-lookup"><span data-stu-id="72a86-126">DataType</span></span><br/>     | <span data-ttu-id="72a86-127">string</span><span class="sxs-lookup"><span data-stu-id="72a86-127">string</span></span><br/>  | <span data-ttu-id="72a86-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="72a86-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="72a86-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="72a86-129">DefaultValue</span></span><br/> | <span data-ttu-id="72a86-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="72a86-130">integer</span></span><br/> | <span data-ttu-id="72a86-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="72a86-131">undefined</span></span><br/>       |
| <span data-ttu-id="72a86-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="72a86-132">MaxValue</span></span><br/>     | <span data-ttu-id="72a86-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="72a86-133">integer</span></span><br/> | <span data-ttu-id="72a86-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="72a86-134">undefined</span></span><br/>       |
| <span data-ttu-id="72a86-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="72a86-135">MinValue</span></span><br/>     | <span data-ttu-id="72a86-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="72a86-136">integer</span></span><br/> | <span data-ttu-id="72a86-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="72a86-137">undefined</span></span><br/>       |
| <span data-ttu-id="72a86-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="72a86-138">Mandatory</span></span><br/>    | <span data-ttu-id="72a86-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="72a86-139">String</span></span><br/>  | <span data-ttu-id="72a86-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="72a86-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="72a86-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="72a86-141">Multiple</span></span><br/>     | <span data-ttu-id="72a86-142">integer</span><span class="sxs-lookup"><span data-stu-id="72a86-142">integer</span></span><br/> | <span data-ttu-id="72a86-143">1</span><span class="sxs-lookup"><span data-stu-id="72a86-143">1</span></span><br/>               |
| <span data-ttu-id="72a86-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="72a86-144">UnitType</span></span><br/>     | <span data-ttu-id="72a86-145">string</span><span class="sxs-lookup"><span data-stu-id="72a86-145">string</span></span><br/>  | <span data-ttu-id="72a86-146">Micron</span><span class="sxs-lookup"><span data-stu-id="72a86-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="72a86-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72a86-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72a86-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="72a86-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




