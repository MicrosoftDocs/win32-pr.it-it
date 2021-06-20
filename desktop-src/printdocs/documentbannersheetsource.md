---
description: Informazioni sull'elemento DocumentBannerSheetSource, che specifica l'origine per un foglio banner personalizzato.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33aa949982e98781c42cbf6aa770dbd4e3d1707
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409474"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="c8c54-103">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="c8c54-103">DocumentBannerSheetSource</span></span>

<span data-ttu-id="c8c54-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c8c54-104">This topic is not current.</span></span> <span data-ttu-id="c8c54-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c8c54-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c8c54-106">Specifica l'origine per un foglio banner personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c8c54-106">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="c8c54-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c8c54-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c8c54-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c8c54-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c8c54-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c8c54-109">Element Information</span></span>



| <span data-ttu-id="c8c54-110">Nome</span><span class="sxs-lookup"><span data-stu-id="c8c54-110">Name</span></span> | <span data-ttu-id="c8c54-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c8c54-111">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="c8c54-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c8c54-112">Element Type</span></span> <br/>   | <span data-ttu-id="c8c54-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c8c54-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="c8c54-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="c8c54-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c8c54-115">Documento</span><span class="sxs-lookup"><span data-stu-id="c8c54-115">Document</span></span><br/>                              |
| <span data-ttu-id="c8c54-116">Note</span><span class="sxs-lookup"><span data-stu-id="c8c54-116">Notes</span></span> <br/>          | <span data-ttu-id="c8c54-117">Collegato all'elemento DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="c8c54-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c8c54-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c8c54-118">Structure Content</span></span>

<span data-ttu-id="c8c54-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="c8c54-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="c8c54-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="c8c54-120">Structure Properties</span></span>

<span data-ttu-id="c8c54-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c8c54-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c8c54-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8c54-122">Property</span></span>                | <span data-ttu-id="c8c54-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c8c54-123">xsi:type</span></span>           | <span data-ttu-id="c8c54-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c8c54-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c8c54-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c8c54-125">DataType</span></span><br/>     | <span data-ttu-id="c8c54-126">string</span><span class="sxs-lookup"><span data-stu-id="c8c54-126">string</span></span><br/>  | <span data-ttu-id="c8c54-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="c8c54-127">xs:string</span></span><br/>       |
| <span data-ttu-id="c8c54-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c8c54-128">DefaultValue</span></span><br/> | <span data-ttu-id="c8c54-129">string</span><span class="sxs-lookup"><span data-stu-id="c8c54-129">string</span></span><br/>  | <span data-ttu-id="c8c54-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="c8c54-130">undefined</span></span><br/>       |
| <span data-ttu-id="c8c54-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c8c54-131">MaxLength</span></span><br/>    | <span data-ttu-id="c8c54-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="c8c54-132">integer</span></span><br/> | <span data-ttu-id="c8c54-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="c8c54-133">undefined</span></span><br/>       |
| <span data-ttu-id="c8c54-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="c8c54-134">MinLength</span></span><br/>    | <span data-ttu-id="c8c54-135">integer</span><span class="sxs-lookup"><span data-stu-id="c8c54-135">integer</span></span><br/> | <span data-ttu-id="c8c54-136">1</span><span class="sxs-lookup"><span data-stu-id="c8c54-136">1</span></span><br/>               |
| <span data-ttu-id="c8c54-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c8c54-137">Mandatory</span></span><br/>    | <span data-ttu-id="c8c54-138">string</span><span class="sxs-lookup"><span data-stu-id="c8c54-138">string</span></span><br/>  | <span data-ttu-id="c8c54-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="c8c54-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c8c54-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="c8c54-140">UnitType</span></span><br/>     | <span data-ttu-id="c8c54-141">string</span><span class="sxs-lookup"><span data-stu-id="c8c54-141">string</span></span><br/>  | <span data-ttu-id="c8c54-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="c8c54-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c8c54-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8c54-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8c54-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c8c54-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




