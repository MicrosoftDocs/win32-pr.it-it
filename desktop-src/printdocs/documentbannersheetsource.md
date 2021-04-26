---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a2802094a0d20cf1b8b0a177a5b774489bb37
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996318"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="0cd10-104">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="0cd10-104">DocumentBannerSheetSource</span></span>

<span data-ttu-id="0cd10-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0cd10-105">This topic is not current.</span></span> <span data-ttu-id="0cd10-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0cd10-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0cd10-107">Specifica l'origine per un foglio banner personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0cd10-107">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="0cd10-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0cd10-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0cd10-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0cd10-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0cd10-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0cd10-110">Element Information</span></span>



| <span data-ttu-id="0cd10-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0cd10-111">Name</span></span> | <span data-ttu-id="0cd10-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0cd10-112">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="0cd10-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0cd10-113">Element Type</span></span> <br/>   | <span data-ttu-id="0cd10-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0cd10-114">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="0cd10-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0cd10-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0cd10-116">Documento</span><span class="sxs-lookup"><span data-stu-id="0cd10-116">Document</span></span><br/>                              |
| <span data-ttu-id="0cd10-117">Note</span><span class="sxs-lookup"><span data-stu-id="0cd10-117">Notes</span></span> <br/>          | <span data-ttu-id="0cd10-118">Collegato all'elemento DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="0cd10-118">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0cd10-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0cd10-119">Structure Content</span></span>

<span data-ttu-id="0cd10-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0cd10-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0cd10-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="0cd10-121">Structure Properties</span></span>

<span data-ttu-id="0cd10-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0cd10-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0cd10-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0cd10-123">Property</span></span>                | <span data-ttu-id="0cd10-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0cd10-124">xsi:type</span></span>           | <span data-ttu-id="0cd10-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0cd10-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0cd10-126">DataType</span><span class="sxs-lookup"><span data-stu-id="0cd10-126">DataType</span></span><br/>     | <span data-ttu-id="0cd10-127">string</span><span class="sxs-lookup"><span data-stu-id="0cd10-127">string</span></span><br/>  | <span data-ttu-id="0cd10-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="0cd10-128">xs:string</span></span><br/>       |
| <span data-ttu-id="0cd10-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0cd10-129">DefaultValue</span></span><br/> | <span data-ttu-id="0cd10-130">string</span><span class="sxs-lookup"><span data-stu-id="0cd10-130">string</span></span><br/>  | <span data-ttu-id="0cd10-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="0cd10-131">undefined</span></span><br/>       |
| <span data-ttu-id="0cd10-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0cd10-132">MaxLength</span></span><br/>    | <span data-ttu-id="0cd10-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="0cd10-133">integer</span></span><br/> | <span data-ttu-id="0cd10-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="0cd10-134">undefined</span></span><br/>       |
| <span data-ttu-id="0cd10-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="0cd10-135">MinLength</span></span><br/>    | <span data-ttu-id="0cd10-136">integer</span><span class="sxs-lookup"><span data-stu-id="0cd10-136">integer</span></span><br/> | <span data-ttu-id="0cd10-137">1</span><span class="sxs-lookup"><span data-stu-id="0cd10-137">1</span></span><br/>               |
| <span data-ttu-id="0cd10-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0cd10-138">Mandatory</span></span><br/>    | <span data-ttu-id="0cd10-139">string</span><span class="sxs-lookup"><span data-stu-id="0cd10-139">string</span></span><br/>  | <span data-ttu-id="0cd10-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="0cd10-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0cd10-141">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="0cd10-141">UnitType</span></span><br/>     | <span data-ttu-id="0cd10-142">string</span><span class="sxs-lookup"><span data-stu-id="0cd10-142">string</span></span><br/>  | <span data-ttu-id="0cd10-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="0cd10-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0cd10-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cd10-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cd10-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0cd10-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




