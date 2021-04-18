---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246f77c5878b74e1b149c6d4020230030fb3c5b0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320993"
---
# <a name="pagescalingscale"></a><span data-ttu-id="b9238-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="b9238-104">PageScalingScale</span></span>

<span data-ttu-id="b9238-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b9238-105">This topic is not current.</span></span> <span data-ttu-id="b9238-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b9238-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b9238-107">Specifica il fattore di scala per la scala quadrata personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b9238-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="b9238-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b9238-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b9238-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b9238-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b9238-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b9238-110">Element Information</span></span>



| <span data-ttu-id="b9238-111">Nome</span><span class="sxs-lookup"><span data-stu-id="b9238-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="b9238-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b9238-112">Element Type</span></span> <br/>   | <span data-ttu-id="b9238-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b9238-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="b9238-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="b9238-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b9238-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="b9238-115">Page</span></span><br/>                                         |
| <span data-ttu-id="b9238-116">Note</span><span class="sxs-lookup"><span data-stu-id="b9238-116">Notes</span></span> <br/>          | <span data-ttu-id="b9238-117">Collegato a elemento PageScaling, opzione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b9238-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b9238-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b9238-118">Structure Content</span></span>

<span data-ttu-id="b9238-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b9238-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="b9238-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="b9238-120">Structure Properties</span></span>

<span data-ttu-id="b9238-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b9238-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b9238-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9238-122">Property</span></span>                | <span data-ttu-id="b9238-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b9238-123">xsi:type</span></span>           | <span data-ttu-id="b9238-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b9238-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b9238-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b9238-125">DataType</span></span><br/>     | <span data-ttu-id="b9238-126">string</span><span class="sxs-lookup"><span data-stu-id="b9238-126">string</span></span><br/>  | <span data-ttu-id="b9238-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b9238-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="b9238-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b9238-128">DefaultValue</span></span><br/> | <span data-ttu-id="b9238-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="b9238-129">integer</span></span><br/> | <span data-ttu-id="b9238-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="b9238-130">undefined</span></span><br/>       |
| <span data-ttu-id="b9238-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b9238-131">MaxValue</span></span><br/>     | <span data-ttu-id="b9238-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="b9238-132">integer</span></span><br/> | <span data-ttu-id="b9238-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="b9238-133">undefined</span></span><br/>       |
| <span data-ttu-id="b9238-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b9238-134">MinValue</span></span><br/>     | <span data-ttu-id="b9238-135">integer</span><span class="sxs-lookup"><span data-stu-id="b9238-135">integer</span></span><br/> | <span data-ttu-id="b9238-136">1</span><span class="sxs-lookup"><span data-stu-id="b9238-136">1</span></span><br/>               |
| <span data-ttu-id="b9238-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b9238-137">Mandatory</span></span><br/>    | <span data-ttu-id="b9238-138">string</span><span class="sxs-lookup"><span data-stu-id="b9238-138">string</span></span><br/>  | <span data-ttu-id="b9238-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="b9238-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b9238-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="b9238-140">Multiple</span></span><br/>     | <span data-ttu-id="b9238-141">integer</span><span class="sxs-lookup"><span data-stu-id="b9238-141">integer</span></span><br/> | <span data-ttu-id="b9238-142">1</span><span class="sxs-lookup"><span data-stu-id="b9238-142">1</span></span><br/>               |
| <span data-ttu-id="b9238-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="b9238-143">UnitType</span></span><br/>     | <span data-ttu-id="b9238-144">string</span><span class="sxs-lookup"><span data-stu-id="b9238-144">string</span></span><br/>  | <span data-ttu-id="b9238-145">percent</span><span class="sxs-lookup"><span data-stu-id="b9238-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b9238-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9238-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9238-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b9238-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




