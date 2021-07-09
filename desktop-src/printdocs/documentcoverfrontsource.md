---
description: Ottenere informazioni sul parametro DocumentCoverFrontSource. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb6ecb089eb271e0b8fff136e73a20194f0c8f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548759"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="1cae7-105">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="1cae7-105">DocumentCoverFrontSource</span></span>

<span data-ttu-id="1cae7-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1cae7-106">This topic is not current.</span></span> <span data-ttu-id="1cae7-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1cae7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1cae7-108">Specifica l'origine per un foglio front-cover personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1cae7-108">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="1cae7-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1cae7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1cae7-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1cae7-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1cae7-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1cae7-111">Element Information</span></span>



| <span data-ttu-id="1cae7-112">Nome</span><span class="sxs-lookup"><span data-stu-id="1cae7-112">Name</span></span> | <span data-ttu-id="1cae7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1cae7-113">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="1cae7-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1cae7-114">Element Type</span></span> <br/>   | <span data-ttu-id="1cae7-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1cae7-115">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="1cae7-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1cae7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1cae7-117">Documento</span><span class="sxs-lookup"><span data-stu-id="1cae7-117">Document</span></span><br/>                             |
| <span data-ttu-id="1cae7-118">Note</span><span class="sxs-lookup"><span data-stu-id="1cae7-118">Notes</span></span> <br/>          | <span data-ttu-id="1cae7-119">Collegato all'elemento DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="1cae7-119">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1cae7-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="1cae7-120">Structure Content</span></span>

<span data-ttu-id="1cae7-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="1cae7-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
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
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="1cae7-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="1cae7-122">Structure Properties</span></span>

<span data-ttu-id="1cae7-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1cae7-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1cae7-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1cae7-124">Property</span></span>                | <span data-ttu-id="1cae7-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1cae7-125">xsi:type</span></span>           | <span data-ttu-id="1cae7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1cae7-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1cae7-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1cae7-127">DataType</span></span><br/>     | <span data-ttu-id="1cae7-128">string</span><span class="sxs-lookup"><span data-stu-id="1cae7-128">string</span></span><br/>  | <span data-ttu-id="1cae7-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="1cae7-129">xs:string</span></span><br/>       |
| <span data-ttu-id="1cae7-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1cae7-130">DefaultValue</span></span><br/> | <span data-ttu-id="1cae7-131">string</span><span class="sxs-lookup"><span data-stu-id="1cae7-131">string</span></span><br/>  | <span data-ttu-id="1cae7-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="1cae7-132">undefined</span></span><br/>       |
| <span data-ttu-id="1cae7-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1cae7-133">MaxLength</span></span><br/>    | <span data-ttu-id="1cae7-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="1cae7-134">integer</span></span><br/> | <span data-ttu-id="1cae7-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="1cae7-135">undefined</span></span><br/>       |
| <span data-ttu-id="1cae7-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="1cae7-136">MinLength</span></span><br/>    | <span data-ttu-id="1cae7-137">integer</span><span class="sxs-lookup"><span data-stu-id="1cae7-137">integer</span></span><br/> | <span data-ttu-id="1cae7-138">1</span><span class="sxs-lookup"><span data-stu-id="1cae7-138">1</span></span><br/>               |
| <span data-ttu-id="1cae7-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="1cae7-139">Mandatory</span></span><br/>    | <span data-ttu-id="1cae7-140">string</span><span class="sxs-lookup"><span data-stu-id="1cae7-140">string</span></span><br/>  | <span data-ttu-id="1cae7-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1cae7-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1cae7-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="1cae7-142">UnitType</span></span><br/>     | <span data-ttu-id="1cae7-143">string</span><span class="sxs-lookup"><span data-stu-id="1cae7-143">string</span></span><br/>  | <span data-ttu-id="1cae7-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="1cae7-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1cae7-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1cae7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cae7-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1cae7-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




