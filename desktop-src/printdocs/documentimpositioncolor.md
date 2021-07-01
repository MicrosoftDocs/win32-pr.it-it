---
description: Informazioni sul parametro DocumentImpositionColor. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b747487c19160d29778f306a91b62cf43d245f65
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120006"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="5a3dd-105">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="5a3dd-105">DocumentImpositionColor</span></span>

<span data-ttu-id="5a3dd-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5a3dd-106">This topic is not current.</span></span> <span data-ttu-id="5a3dd-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a3dd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a3dd-108">Il contenuto dell'applicazione etichettato con il colore denominato specificato DEVE essere visualizzato in tutte le separazioni dei colori.</span><span class="sxs-lookup"><span data-stu-id="5a3dd-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="5a3dd-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5a3dd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5a3dd-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5a3dd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5a3dd-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5a3dd-111">Element Information</span></span>



| <span data-ttu-id="5a3dd-112">Nome</span><span class="sxs-lookup"><span data-stu-id="5a3dd-112">Name</span></span> | <span data-ttu-id="5a3dd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5a3dd-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="5a3dd-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5a3dd-114">Element Type</span></span> <br/>   | <span data-ttu-id="5a3dd-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5a3dd-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="5a3dd-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5a3dd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a3dd-117">Documento</span><span class="sxs-lookup"><span data-stu-id="5a3dd-117">Document</span></span><br/>     |
| <span data-ttu-id="5a3dd-118">Note</span><span class="sxs-lookup"><span data-stu-id="5a3dd-118">Notes</span></span> <br/>          | <span data-ttu-id="5a3dd-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="5a3dd-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="5a3dd-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5a3dd-120">Structure Content</span></span>

<span data-ttu-id="5a3dd-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5a3dd-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="5a3dd-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="5a3dd-122">Structure Properties</span></span>

<span data-ttu-id="5a3dd-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5a3dd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a3dd-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a3dd-124">Property</span></span>                | <span data-ttu-id="5a3dd-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5a3dd-125">xsi:type</span></span>           | <span data-ttu-id="5a3dd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5a3dd-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5a3dd-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5a3dd-127">DataType</span></span><br/>     | <span data-ttu-id="5a3dd-128">string</span><span class="sxs-lookup"><span data-stu-id="5a3dd-128">string</span></span><br/>  | <span data-ttu-id="5a3dd-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a3dd-129">xs:string</span></span><br/>       |
| <span data-ttu-id="5a3dd-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5a3dd-130">DefaultValue</span></span><br/> | <span data-ttu-id="5a3dd-131">string</span><span class="sxs-lookup"><span data-stu-id="5a3dd-131">string</span></span><br/>  | <span data-ttu-id="5a3dd-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="5a3dd-132">undefined</span></span><br/>       |
| <span data-ttu-id="5a3dd-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="5a3dd-133">MaxLength</span></span><br/>    | <span data-ttu-id="5a3dd-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="5a3dd-134">integer</span></span><br/> | <span data-ttu-id="5a3dd-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="5a3dd-135">undefined</span></span><br/>       |
| <span data-ttu-id="5a3dd-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="5a3dd-136">MinLength</span></span><br/>    | <span data-ttu-id="5a3dd-137">integer</span><span class="sxs-lookup"><span data-stu-id="5a3dd-137">integer</span></span><br/> | <span data-ttu-id="5a3dd-138">1</span><span class="sxs-lookup"><span data-stu-id="5a3dd-138">1</span></span><br/>               |
| <span data-ttu-id="5a3dd-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="5a3dd-139">Mandatory</span></span><br/>    | <span data-ttu-id="5a3dd-140">string</span><span class="sxs-lookup"><span data-stu-id="5a3dd-140">string</span></span><br/>  | <span data-ttu-id="5a3dd-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="5a3dd-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5a3dd-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="5a3dd-142">UnitType</span></span><br/>     | <span data-ttu-id="5a3dd-143">string</span><span class="sxs-lookup"><span data-stu-id="5a3dd-143">string</span></span><br/>  | <span data-ttu-id="5a3dd-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="5a3dd-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="5a3dd-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a3dd-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a3dd-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5a3dd-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




