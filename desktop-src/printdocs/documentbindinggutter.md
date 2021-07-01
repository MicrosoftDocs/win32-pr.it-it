---
description: Trovare informazioni sul parametro DocumentBindingGutter. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118466"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="e337c-105">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="e337c-105">DocumentBindingGutter</span></span>

<span data-ttu-id="e337c-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e337c-106">This topic is not current.</span></span> <span data-ttu-id="e337c-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e337c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e337c-108">Specifica la larghezza della barra di associazione.</span><span class="sxs-lookup"><span data-stu-id="e337c-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="e337c-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e337c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e337c-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="e337c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e337c-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e337c-111">Element Information</span></span>



| <span data-ttu-id="e337c-112">Nome</span><span class="sxs-lookup"><span data-stu-id="e337c-112">Name</span></span> | <span data-ttu-id="e337c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e337c-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="e337c-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e337c-114">Element Type</span></span> <br/>   | <span data-ttu-id="e337c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e337c-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="e337c-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e337c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e337c-117">Documento</span><span class="sxs-lookup"><span data-stu-id="e337c-117">Document</span></span><br/>                          |
| <span data-ttu-id="e337c-118">Note</span><span class="sxs-lookup"><span data-stu-id="e337c-118">Notes</span></span> <br/>          | <span data-ttu-id="e337c-119">Collegato all'elemento DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="e337c-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e337c-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="e337c-120">Structure Content</span></span>

<span data-ttu-id="e337c-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e337c-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e337c-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="e337c-122">Structure Properties</span></span>

<span data-ttu-id="e337c-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e337c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e337c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e337c-124">Property</span></span>                | <span data-ttu-id="e337c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e337c-125">xsi:type</span></span>           | <span data-ttu-id="e337c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e337c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e337c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e337c-127">DataType</span></span><br/>     | <span data-ttu-id="e337c-128">string</span><span class="sxs-lookup"><span data-stu-id="e337c-128">string</span></span><br/>  | <span data-ttu-id="e337c-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e337c-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="e337c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e337c-130">DefaultValue</span></span><br/> | <span data-ttu-id="e337c-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="e337c-131">integer</span></span><br/> | <span data-ttu-id="e337c-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="e337c-132">undefined</span></span><br/>       |
| <span data-ttu-id="e337c-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e337c-133">MaxValue</span></span><br/>     | <span data-ttu-id="e337c-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="e337c-134">integer</span></span><br/> | <span data-ttu-id="e337c-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="e337c-135">undefined</span></span><br/>       |
| <span data-ttu-id="e337c-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="e337c-136">MinValue</span></span><br/>     | <span data-ttu-id="e337c-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="e337c-137">integer</span></span><br/> | <span data-ttu-id="e337c-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="e337c-138">undefined</span></span><br/>       |
| <span data-ttu-id="e337c-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="e337c-139">Mandatory</span></span><br/>    | <span data-ttu-id="e337c-140">Stringa</span><span class="sxs-lookup"><span data-stu-id="e337c-140">String</span></span><br/>  | <span data-ttu-id="e337c-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="e337c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e337c-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="e337c-142">Multiple</span></span><br/>     | <span data-ttu-id="e337c-143">integer</span><span class="sxs-lookup"><span data-stu-id="e337c-143">integer</span></span><br/> | <span data-ttu-id="e337c-144">1</span><span class="sxs-lookup"><span data-stu-id="e337c-144">1</span></span><br/>               |
| <span data-ttu-id="e337c-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="e337c-145">UnitType</span></span><br/>     | <span data-ttu-id="e337c-146">string</span><span class="sxs-lookup"><span data-stu-id="e337c-146">string</span></span><br/>  | <span data-ttu-id="e337c-147">Micron</span><span class="sxs-lookup"><span data-stu-id="e337c-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e337c-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e337c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e337c-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e337c-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




