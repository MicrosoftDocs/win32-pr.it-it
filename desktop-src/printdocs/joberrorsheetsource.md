---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c87a31e645b9ea5eedb22b48000991a99bc7e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998158"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="385e1-104">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="385e1-104">JobErrorSheetSource</span></span>

<span data-ttu-id="385e1-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="385e1-105">This topic is not current.</span></span> <span data-ttu-id="385e1-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="385e1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="385e1-107">Specifica l'origine per un foglio errori personalizzato.</span><span class="sxs-lookup"><span data-stu-id="385e1-107">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="385e1-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="385e1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="385e1-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="385e1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="385e1-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="385e1-110">Element Information</span></span>



| <span data-ttu-id="385e1-111">Nome</span><span class="sxs-lookup"><span data-stu-id="385e1-111">Name</span></span> | <span data-ttu-id="385e1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="385e1-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="385e1-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="385e1-113">Element Type</span></span> <br/>   | <span data-ttu-id="385e1-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="385e1-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="385e1-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="385e1-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="385e1-116">Documento</span><span class="sxs-lookup"><span data-stu-id="385e1-116">Document</span></span><br/>                        |
| <span data-ttu-id="385e1-117">Note</span><span class="sxs-lookup"><span data-stu-id="385e1-117">Notes</span></span> <br/>          | <span data-ttu-id="385e1-118">Collegato all'elemento JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="385e1-118">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="385e1-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="385e1-119">Structure Content</span></span>

<span data-ttu-id="385e1-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="385e1-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobErrorSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="385e1-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="385e1-121">Structure Properties</span></span>

<span data-ttu-id="385e1-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="385e1-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="385e1-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="385e1-123">Property</span></span>                | <span data-ttu-id="385e1-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="385e1-124">xsi:type</span></span>           | <span data-ttu-id="385e1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="385e1-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="385e1-126">DataType</span><span class="sxs-lookup"><span data-stu-id="385e1-126">DataType</span></span><br/>     | <span data-ttu-id="385e1-127">string</span><span class="sxs-lookup"><span data-stu-id="385e1-127">string</span></span><br/>  | <span data-ttu-id="385e1-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="385e1-128">xs:string</span></span><br/>       |
| <span data-ttu-id="385e1-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="385e1-129">DefaultValue</span></span><br/> | <span data-ttu-id="385e1-130">string</span><span class="sxs-lookup"><span data-stu-id="385e1-130">string</span></span><br/>  | <span data-ttu-id="385e1-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="385e1-131">undefined</span></span><br/>       |
| <span data-ttu-id="385e1-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="385e1-132">MaxLength</span></span><br/>    | <span data-ttu-id="385e1-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="385e1-133">integer</span></span><br/> | <span data-ttu-id="385e1-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="385e1-134">undefined</span></span><br/>       |
| <span data-ttu-id="385e1-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="385e1-135">MinLength</span></span><br/>    | <span data-ttu-id="385e1-136">integer</span><span class="sxs-lookup"><span data-stu-id="385e1-136">integer</span></span><br/> | <span data-ttu-id="385e1-137">1</span><span class="sxs-lookup"><span data-stu-id="385e1-137">1</span></span><br/>               |
| <span data-ttu-id="385e1-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="385e1-138">Mandatory</span></span><br/>    | <span data-ttu-id="385e1-139">string</span><span class="sxs-lookup"><span data-stu-id="385e1-139">string</span></span><br/>  | <span data-ttu-id="385e1-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="385e1-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="385e1-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="385e1-141">UnitType</span></span><br/>     | <span data-ttu-id="385e1-142">string</span><span class="sxs-lookup"><span data-stu-id="385e1-142">string</span></span><br/>  | <span data-ttu-id="385e1-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="385e1-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="385e1-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="385e1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="385e1-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="385e1-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




