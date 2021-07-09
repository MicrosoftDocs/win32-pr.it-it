---
description: Ottiene informazioni sul parametro JobErrorSheetSource. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656d71422c46800d6155c1dea1e221f9c6dfe021
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549389"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="9e1c9-105">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="9e1c9-105">JobErrorSheetSource</span></span>

<span data-ttu-id="9e1c9-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="9e1c9-106">This topic is not current.</span></span> <span data-ttu-id="9e1c9-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9e1c9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9e1c9-108">Specifica l'origine per un foglio errori personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9e1c9-108">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="9e1c9-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9e1c9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9e1c9-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="9e1c9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9e1c9-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9e1c9-111">Element Information</span></span>



| <span data-ttu-id="9e1c9-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9e1c9-112">Name</span></span> | <span data-ttu-id="9e1c9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9e1c9-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="9e1c9-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="9e1c9-114">Element Type</span></span> <br/>   | <span data-ttu-id="9e1c9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9e1c9-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="9e1c9-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="9e1c9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9e1c9-117">Documento</span><span class="sxs-lookup"><span data-stu-id="9e1c9-117">Document</span></span><br/>                        |
| <span data-ttu-id="9e1c9-118">Note</span><span class="sxs-lookup"><span data-stu-id="9e1c9-118">Notes</span></span> <br/>          | <span data-ttu-id="9e1c9-119">Collegato all'elemento JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="9e1c9-119">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9e1c9-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="9e1c9-120">Structure Content</span></span>

<span data-ttu-id="9e1c9-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="9e1c9-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9e1c9-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="9e1c9-122">Structure Properties</span></span>

<span data-ttu-id="9e1c9-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="9e1c9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9e1c9-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e1c9-124">Property</span></span>                | <span data-ttu-id="9e1c9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9e1c9-125">xsi:type</span></span>           | <span data-ttu-id="9e1c9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9e1c9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9e1c9-127">DataType</span><span class="sxs-lookup"><span data-stu-id="9e1c9-127">DataType</span></span><br/>     | <span data-ttu-id="9e1c9-128">string</span><span class="sxs-lookup"><span data-stu-id="9e1c9-128">string</span></span><br/>  | <span data-ttu-id="9e1c9-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="9e1c9-129">xs:string</span></span><br/>       |
| <span data-ttu-id="9e1c9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9e1c9-130">DefaultValue</span></span><br/> | <span data-ttu-id="9e1c9-131">string</span><span class="sxs-lookup"><span data-stu-id="9e1c9-131">string</span></span><br/>  | <span data-ttu-id="9e1c9-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="9e1c9-132">undefined</span></span><br/>       |
| <span data-ttu-id="9e1c9-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="9e1c9-133">MaxLength</span></span><br/>    | <span data-ttu-id="9e1c9-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="9e1c9-134">integer</span></span><br/> | <span data-ttu-id="9e1c9-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="9e1c9-135">undefined</span></span><br/>       |
| <span data-ttu-id="9e1c9-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="9e1c9-136">MinLength</span></span><br/>    | <span data-ttu-id="9e1c9-137">integer</span><span class="sxs-lookup"><span data-stu-id="9e1c9-137">integer</span></span><br/> | <span data-ttu-id="9e1c9-138">1</span><span class="sxs-lookup"><span data-stu-id="9e1c9-138">1</span></span><br/>               |
| <span data-ttu-id="9e1c9-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9e1c9-139">Mandatory</span></span><br/>    | <span data-ttu-id="9e1c9-140">string</span><span class="sxs-lookup"><span data-stu-id="9e1c9-140">string</span></span><br/>  | <span data-ttu-id="9e1c9-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="9e1c9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9e1c9-142">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="9e1c9-142">UnitType</span></span><br/>     | <span data-ttu-id="9e1c9-143">string</span><span class="sxs-lookup"><span data-stu-id="9e1c9-143">string</span></span><br/>  | <span data-ttu-id="9e1c9-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="9e1c9-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="9e1c9-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e1c9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e1c9-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9e1c9-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




