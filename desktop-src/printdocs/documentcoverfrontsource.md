---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f67ab3f3dc3515a494dad2ab72f1413de88cd00
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234573"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="4ae85-104">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="4ae85-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="4ae85-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="4ae85-105">This topic is not current.</span></span> <span data-ttu-id="4ae85-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4ae85-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ae85-107">Specifica l'origine per un foglio di copertina personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4ae85-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="4ae85-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4ae85-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4ae85-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="4ae85-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4ae85-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4ae85-110">Element Information</span></span>



| <span data-ttu-id="4ae85-111">Nome</span><span class="sxs-lookup"><span data-stu-id="4ae85-111">Name</span></span>                       |                                                 |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="4ae85-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="4ae85-112">Element Type</span></span> <br/>   | <span data-ttu-id="4ae85-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4ae85-113">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="4ae85-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="4ae85-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4ae85-115">Documento</span><span class="sxs-lookup"><span data-stu-id="4ae85-115">Document</span></span><br/>                             |
| <span data-ttu-id="4ae85-116">Note</span><span class="sxs-lookup"><span data-stu-id="4ae85-116">Notes</span></span> <br/>          | <span data-ttu-id="4ae85-117">Collegato a elemento DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="4ae85-117">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4ae85-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="4ae85-118">Structure Content</span></span>

<span data-ttu-id="4ae85-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="4ae85-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4ae85-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="4ae85-120">Structure Properties</span></span>

<span data-ttu-id="4ae85-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="4ae85-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4ae85-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ae85-122">Property</span></span>                | <span data-ttu-id="4ae85-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4ae85-123">xsi:type</span></span>           | <span data-ttu-id="4ae85-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4ae85-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4ae85-125">DataType</span><span class="sxs-lookup"><span data-stu-id="4ae85-125">DataType</span></span><br/>     | <span data-ttu-id="4ae85-126">string</span><span class="sxs-lookup"><span data-stu-id="4ae85-126">string</span></span><br/>  | <span data-ttu-id="4ae85-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="4ae85-127">xs:string</span></span><br/>       |
| <span data-ttu-id="4ae85-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4ae85-128">DefaultValue</span></span><br/> | <span data-ttu-id="4ae85-129">string</span><span class="sxs-lookup"><span data-stu-id="4ae85-129">string</span></span><br/>  | <span data-ttu-id="4ae85-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="4ae85-130">undefined</span></span><br/>       |
| <span data-ttu-id="4ae85-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4ae85-131">MaxLength</span></span><br/>    | <span data-ttu-id="4ae85-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="4ae85-132">integer</span></span><br/> | <span data-ttu-id="4ae85-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="4ae85-133">undefined</span></span><br/>       |
| <span data-ttu-id="4ae85-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="4ae85-134">MinLength</span></span><br/>    | <span data-ttu-id="4ae85-135">integer</span><span class="sxs-lookup"><span data-stu-id="4ae85-135">integer</span></span><br/> | <span data-ttu-id="4ae85-136">1</span><span class="sxs-lookup"><span data-stu-id="4ae85-136">1</span></span><br/>               |
| <span data-ttu-id="4ae85-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="4ae85-137">Mandatory</span></span><br/>    | <span data-ttu-id="4ae85-138">string</span><span class="sxs-lookup"><span data-stu-id="4ae85-138">string</span></span><br/>  | <span data-ttu-id="4ae85-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="4ae85-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4ae85-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="4ae85-140">UnitType</span></span><br/>     | <span data-ttu-id="4ae85-141">string</span><span class="sxs-lookup"><span data-stu-id="4ae85-141">string</span></span><br/>  | <span data-ttu-id="4ae85-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="4ae85-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4ae85-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ae85-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ae85-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4ae85-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




