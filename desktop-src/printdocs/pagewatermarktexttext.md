---
description: Ottenere altre informazioni sul parametro PageWatermarkTextText. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395966"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="11040-105">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="11040-105">PageWatermarkTextText</span></span>

<span data-ttu-id="11040-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="11040-106">This topic is not current.</span></span> <span data-ttu-id="11040-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11040-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11040-108">Specifica il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="11040-108">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="11040-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="11040-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="11040-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="11040-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="11040-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="11040-111">Element Information</span></span>



| <span data-ttu-id="11040-112">Nome</span><span class="sxs-lookup"><span data-stu-id="11040-112">Name</span></span> | <span data-ttu-id="11040-113">Valore</span><span class="sxs-lookup"><span data-stu-id="11040-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="11040-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="11040-114">Element Type</span></span> <br/>   | <span data-ttu-id="11040-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="11040-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="11040-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="11040-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="11040-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="11040-117">Page</span></span><br/>                            |
| <span data-ttu-id="11040-118">Note</span><span class="sxs-lookup"><span data-stu-id="11040-118">Notes</span></span> <br/>          | <span data-ttu-id="11040-119">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="11040-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="11040-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="11040-120">Structure Content</span></span>

<span data-ttu-id="11040-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="11040-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="11040-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="11040-122">Structure Properties</span></span>

<span data-ttu-id="11040-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="11040-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="11040-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="11040-124">Property</span></span>                | <span data-ttu-id="11040-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="11040-125">xsi:type</span></span>           | <span data-ttu-id="11040-126">Valore</span><span class="sxs-lookup"><span data-stu-id="11040-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="11040-127">DataType</span><span class="sxs-lookup"><span data-stu-id="11040-127">DataType</span></span><br/>     | <span data-ttu-id="11040-128">Stringa</span><span class="sxs-lookup"><span data-stu-id="11040-128">String</span></span><br/>  | <span data-ttu-id="11040-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="11040-129">xs:string</span></span><br/>       |
| <span data-ttu-id="11040-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="11040-130">DefaultValue</span></span><br/> | <span data-ttu-id="11040-131">Intero</span><span class="sxs-lookup"><span data-stu-id="11040-131">Integer</span></span><br/> | <span data-ttu-id="11040-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="11040-132">undefined</span></span><br/>       |
| <span data-ttu-id="11040-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="11040-133">MaxLength</span></span><br/>    | <span data-ttu-id="11040-134">Intero</span><span class="sxs-lookup"><span data-stu-id="11040-134">Integer</span></span><br/> | <span data-ttu-id="11040-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="11040-135">undefined</span></span><br/>       |
| <span data-ttu-id="11040-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="11040-136">MinLength</span></span><br/>    | <span data-ttu-id="11040-137">Integer</span><span class="sxs-lookup"><span data-stu-id="11040-137">Integer</span></span><br/> | <span data-ttu-id="11040-138">1</span><span class="sxs-lookup"><span data-stu-id="11040-138">1</span></span><br/>               |
| <span data-ttu-id="11040-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="11040-139">Mandatory</span></span><br/>    | <span data-ttu-id="11040-140">Stringa</span><span class="sxs-lookup"><span data-stu-id="11040-140">String</span></span><br/>  | <span data-ttu-id="11040-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="11040-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="11040-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="11040-142">UnitType</span></span><br/>     | <span data-ttu-id="11040-143">Stringa</span><span class="sxs-lookup"><span data-stu-id="11040-143">String</span></span><br/>  | <span data-ttu-id="11040-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="11040-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="11040-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11040-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11040-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="11040-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




