---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320860"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="87572-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="87572-104">PageWatermarkTextText</span></span>

<span data-ttu-id="87572-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="87572-105">This topic is not current.</span></span> <span data-ttu-id="87572-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87572-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87572-107">Specifica il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="87572-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="87572-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="87572-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87572-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="87572-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="87572-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="87572-110">Element Information</span></span>



| <span data-ttu-id="87572-111">Nome</span><span class="sxs-lookup"><span data-stu-id="87572-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="87572-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="87572-112">Element Type</span></span> <br/>   | <span data-ttu-id="87572-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="87572-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="87572-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="87572-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87572-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="87572-115">Page</span></span><br/>                            |
| <span data-ttu-id="87572-116">Note</span><span class="sxs-lookup"><span data-stu-id="87572-116">Notes</span></span> <br/>          | <span data-ttu-id="87572-117">Collegato a elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="87572-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="87572-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="87572-118">Structure Content</span></span>

<span data-ttu-id="87572-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="87572-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="87572-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="87572-120">Structure Properties</span></span>

<span data-ttu-id="87572-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="87572-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87572-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87572-122">Property</span></span>                | <span data-ttu-id="87572-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="87572-123">xsi:type</span></span>           | <span data-ttu-id="87572-124">Valore</span><span class="sxs-lookup"><span data-stu-id="87572-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="87572-125">DataType</span><span class="sxs-lookup"><span data-stu-id="87572-125">DataType</span></span><br/>     | <span data-ttu-id="87572-126">string</span><span class="sxs-lookup"><span data-stu-id="87572-126">String</span></span><br/>  | <span data-ttu-id="87572-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="87572-127">xs:string</span></span><br/>       |
| <span data-ttu-id="87572-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="87572-128">DefaultValue</span></span><br/> | <span data-ttu-id="87572-129">Integer</span><span class="sxs-lookup"><span data-stu-id="87572-129">Integer</span></span><br/> | <span data-ttu-id="87572-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="87572-130">undefined</span></span><br/>       |
| <span data-ttu-id="87572-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="87572-131">MaxLength</span></span><br/>    | <span data-ttu-id="87572-132">Integer</span><span class="sxs-lookup"><span data-stu-id="87572-132">Integer</span></span><br/> | <span data-ttu-id="87572-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="87572-133">undefined</span></span><br/>       |
| <span data-ttu-id="87572-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="87572-134">MinLength</span></span><br/>    | <span data-ttu-id="87572-135">Integer</span><span class="sxs-lookup"><span data-stu-id="87572-135">Integer</span></span><br/> | <span data-ttu-id="87572-136">1</span><span class="sxs-lookup"><span data-stu-id="87572-136">1</span></span><br/>               |
| <span data-ttu-id="87572-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="87572-137">Mandatory</span></span><br/>    | <span data-ttu-id="87572-138">string</span><span class="sxs-lookup"><span data-stu-id="87572-138">String</span></span><br/>  | <span data-ttu-id="87572-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="87572-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="87572-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="87572-140">UnitType</span></span><br/>     | <span data-ttu-id="87572-141">string</span><span class="sxs-lookup"><span data-stu-id="87572-141">String</span></span><br/>  | <span data-ttu-id="87572-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="87572-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="87572-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87572-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87572-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="87572-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




