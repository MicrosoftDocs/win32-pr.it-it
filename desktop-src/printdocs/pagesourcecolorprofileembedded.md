---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409b101d944152fa28c8972da4d8515e8cdfb05b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321046"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="f922f-104">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="f922f-104">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="f922f-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f922f-105">This topic is not current.</span></span> <span data-ttu-id="f922f-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f922f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f922f-107">Specifica il profilo del colore di origine incorporato.</span><span class="sxs-lookup"><span data-stu-id="f922f-107">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="f922f-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f922f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f922f-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f922f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f922f-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f922f-110">Element Information</span></span>



| <span data-ttu-id="f922f-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f922f-111">Name</span></span>                       |                                                     |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="f922f-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f922f-112">Element Type</span></span> <br/>   | <span data-ttu-id="f922f-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f922f-113">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="f922f-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="f922f-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f922f-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="f922f-115">Page</span></span><br/>                                     |
| <span data-ttu-id="f922f-116">Note</span><span class="sxs-lookup"><span data-stu-id="f922f-116">Notes</span></span> <br/>          | <span data-ttu-id="f922f-117">Collegato a elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="f922f-117">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f922f-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f922f-118">Structure Content</span></span>

<span data-ttu-id="f922f-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f922f-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="f922f-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="f922f-120">Structure Properties</span></span>

<span data-ttu-id="f922f-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f922f-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f922f-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f922f-122">Property</span></span>                | <span data-ttu-id="f922f-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f922f-123">xsi:type</span></span>           | <span data-ttu-id="f922f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f922f-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f922f-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f922f-125">DataType</span></span><br/>     | <span data-ttu-id="f922f-126">string</span><span class="sxs-lookup"><span data-stu-id="f922f-126">string</span></span><br/>  | <span data-ttu-id="f922f-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f922f-127">xs:string</span></span><br/>       |
| <span data-ttu-id="f922f-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f922f-128">DefaultValue</span></span><br/> | <span data-ttu-id="f922f-129">string</span><span class="sxs-lookup"><span data-stu-id="f922f-129">string</span></span><br/>  | <span data-ttu-id="f922f-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="f922f-130">undefined</span></span><br/>       |
| <span data-ttu-id="f922f-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f922f-131">MaxLength</span></span><br/>    | <span data-ttu-id="f922f-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="f922f-132">integer</span></span><br/> | <span data-ttu-id="f922f-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="f922f-133">undefined</span></span><br/>       |
| <span data-ttu-id="f922f-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="f922f-134">MinLength</span></span><br/>    | <span data-ttu-id="f922f-135">integer</span><span class="sxs-lookup"><span data-stu-id="f922f-135">integer</span></span><br/> | <span data-ttu-id="f922f-136">1</span><span class="sxs-lookup"><span data-stu-id="f922f-136">1</span></span><br/>               |
| <span data-ttu-id="f922f-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f922f-137">Mandatory</span></span><br/>    | <span data-ttu-id="f922f-138">string</span><span class="sxs-lookup"><span data-stu-id="f922f-138">string</span></span><br/>  | <span data-ttu-id="f922f-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="f922f-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f922f-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="f922f-140">UnitType</span></span><br/>     | <span data-ttu-id="f922f-141">string</span><span class="sxs-lookup"><span data-stu-id="f922f-141">string</span></span><br/>  | <span data-ttu-id="f922f-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="f922f-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f922f-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f922f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f922f-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f922f-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




