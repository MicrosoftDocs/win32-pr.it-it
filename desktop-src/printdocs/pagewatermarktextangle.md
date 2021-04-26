---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995548"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="beb5a-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="beb5a-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="beb5a-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="beb5a-105">This topic is not current.</span></span> <span data-ttu-id="beb5a-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="beb5a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="beb5a-107">Specifica l'angolo del testo della filigrana rispetto alla direzione PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="beb5a-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="beb5a-108">L'angolo viene misurato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="beb5a-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="beb5a-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="beb5a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="beb5a-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="beb5a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="beb5a-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="beb5a-111">Element Information</span></span>



| <span data-ttu-id="beb5a-112">Nome</span><span class="sxs-lookup"><span data-stu-id="beb5a-112">Name</span></span> | <span data-ttu-id="beb5a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="beb5a-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="beb5a-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="beb5a-114">Element Type</span></span> <br/>   | <span data-ttu-id="beb5a-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="beb5a-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="beb5a-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="beb5a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="beb5a-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="beb5a-117">Page</span></span><br/>                            |
| <span data-ttu-id="beb5a-118">Note</span><span class="sxs-lookup"><span data-stu-id="beb5a-118">Notes</span></span> <br/>          | <span data-ttu-id="beb5a-119">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="beb5a-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="beb5a-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="beb5a-120">Structure Content</span></span>

<span data-ttu-id="beb5a-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="beb5a-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="beb5a-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="beb5a-122">Structure Properties</span></span>

<span data-ttu-id="beb5a-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="beb5a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="beb5a-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="beb5a-124">Property</span></span>                | <span data-ttu-id="beb5a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="beb5a-125">xsi:type</span></span>           | <span data-ttu-id="beb5a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="beb5a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="beb5a-127">DataType</span><span class="sxs-lookup"><span data-stu-id="beb5a-127">DataType</span></span><br/>     | <span data-ttu-id="beb5a-128">string</span><span class="sxs-lookup"><span data-stu-id="beb5a-128">string</span></span><br/>  | <span data-ttu-id="beb5a-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="beb5a-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="beb5a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="beb5a-130">DefaultValue</span></span><br/> | <span data-ttu-id="beb5a-131">integer</span><span class="sxs-lookup"><span data-stu-id="beb5a-131">integer</span></span><br/> | <span data-ttu-id="beb5a-132">0</span><span class="sxs-lookup"><span data-stu-id="beb5a-132">0</span></span><br/>               |
| <span data-ttu-id="beb5a-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="beb5a-133">MaxValue</span></span><br/>     | <span data-ttu-id="beb5a-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="beb5a-134">integer</span></span><br/> | <span data-ttu-id="beb5a-135">359</span><span class="sxs-lookup"><span data-stu-id="beb5a-135">359</span></span><br/>             |
| <span data-ttu-id="beb5a-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="beb5a-136">MinValue</span></span><br/>     | <span data-ttu-id="beb5a-137">integer</span><span class="sxs-lookup"><span data-stu-id="beb5a-137">integer</span></span><br/> | <span data-ttu-id="beb5a-138">0</span><span class="sxs-lookup"><span data-stu-id="beb5a-138">0</span></span><br/>               |
| <span data-ttu-id="beb5a-139">Più elementi</span><span class="sxs-lookup"><span data-stu-id="beb5a-139">Multiple</span></span><br/>     | <span data-ttu-id="beb5a-140">integer</span><span class="sxs-lookup"><span data-stu-id="beb5a-140">integer</span></span><br/> | <span data-ttu-id="beb5a-141">1</span><span class="sxs-lookup"><span data-stu-id="beb5a-141">1</span></span><br/>               |
| <span data-ttu-id="beb5a-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="beb5a-142">Mandatory</span></span><br/>    | <span data-ttu-id="beb5a-143">string</span><span class="sxs-lookup"><span data-stu-id="beb5a-143">string</span></span><br/>  | <span data-ttu-id="beb5a-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="beb5a-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="beb5a-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="beb5a-145">UnitType</span></span><br/>     | <span data-ttu-id="beb5a-146">string</span><span class="sxs-lookup"><span data-stu-id="beb5a-146">string</span></span><br/>  | <span data-ttu-id="beb5a-147">gradi</span><span class="sxs-lookup"><span data-stu-id="beb5a-147">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="beb5a-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="beb5a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beb5a-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="beb5a-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




