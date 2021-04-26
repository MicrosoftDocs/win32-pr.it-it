---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb19f5965347e79732aa116e5be51f90e4ef6943
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996078"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="3b733-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="3b733-104">PageWatermarkTextText</span></span>

<span data-ttu-id="3b733-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="3b733-105">This topic is not current.</span></span> <span data-ttu-id="3b733-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3b733-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3b733-107">Specifica il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="3b733-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="3b733-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3b733-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3b733-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="3b733-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3b733-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3b733-110">Element Information</span></span>



| <span data-ttu-id="3b733-111">Nome</span><span class="sxs-lookup"><span data-stu-id="3b733-111">Name</span></span> | <span data-ttu-id="3b733-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3b733-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="3b733-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="3b733-113">Element Type</span></span> <br/>   | <span data-ttu-id="3b733-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3b733-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="3b733-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="3b733-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3b733-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="3b733-116">Page</span></span><br/>                            |
| <span data-ttu-id="3b733-117">Note</span><span class="sxs-lookup"><span data-stu-id="3b733-117">Notes</span></span> <br/>          | <span data-ttu-id="3b733-118">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="3b733-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3b733-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="3b733-119">Structure Content</span></span>

<span data-ttu-id="3b733-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="3b733-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3b733-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="3b733-121">Structure Properties</span></span>

<span data-ttu-id="3b733-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="3b733-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3b733-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b733-123">Property</span></span>                | <span data-ttu-id="3b733-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3b733-124">xsi:type</span></span>           | <span data-ttu-id="3b733-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3b733-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3b733-126">DataType</span><span class="sxs-lookup"><span data-stu-id="3b733-126">DataType</span></span><br/>     | <span data-ttu-id="3b733-127">Stringa</span><span class="sxs-lookup"><span data-stu-id="3b733-127">String</span></span><br/>  | <span data-ttu-id="3b733-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3b733-128">xs:string</span></span><br/>       |
| <span data-ttu-id="3b733-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3b733-129">DefaultValue</span></span><br/> | <span data-ttu-id="3b733-130">Intero</span><span class="sxs-lookup"><span data-stu-id="3b733-130">Integer</span></span><br/> | <span data-ttu-id="3b733-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="3b733-131">undefined</span></span><br/>       |
| <span data-ttu-id="3b733-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3b733-132">MaxLength</span></span><br/>    | <span data-ttu-id="3b733-133">Intero</span><span class="sxs-lookup"><span data-stu-id="3b733-133">Integer</span></span><br/> | <span data-ttu-id="3b733-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="3b733-134">undefined</span></span><br/>       |
| <span data-ttu-id="3b733-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="3b733-135">MinLength</span></span><br/>    | <span data-ttu-id="3b733-136">Integer</span><span class="sxs-lookup"><span data-stu-id="3b733-136">Integer</span></span><br/> | <span data-ttu-id="3b733-137">1</span><span class="sxs-lookup"><span data-stu-id="3b733-137">1</span></span><br/>               |
| <span data-ttu-id="3b733-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="3b733-138">Mandatory</span></span><br/>    | <span data-ttu-id="3b733-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="3b733-139">String</span></span><br/>  | <span data-ttu-id="3b733-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="3b733-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3b733-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="3b733-141">UnitType</span></span><br/>     | <span data-ttu-id="3b733-142">Stringa</span><span class="sxs-lookup"><span data-stu-id="3b733-142">String</span></span><br/>  | <span data-ttu-id="3b733-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="3b733-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3b733-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b733-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b733-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3b733-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




