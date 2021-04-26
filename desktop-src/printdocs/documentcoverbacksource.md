---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6547ac2dc2c3f91ea4d0ebeea87622c790ae7d4d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996278"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="e5b59-104">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="e5b59-104">DocumentCoverBackSource</span></span>

<span data-ttu-id="e5b59-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e5b59-105">This topic is not current.</span></span> <span data-ttu-id="e5b59-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e5b59-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e5b59-107">Specifica l'origine per un foglio di copertura posteriore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e5b59-107">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="e5b59-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e5b59-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e5b59-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="e5b59-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e5b59-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e5b59-110">Element Information</span></span>



| <span data-ttu-id="e5b59-111">Nome</span><span class="sxs-lookup"><span data-stu-id="e5b59-111">Name</span></span> | <span data-ttu-id="e5b59-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b59-112">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="e5b59-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e5b59-113">Element Type</span></span> <br/>   | <span data-ttu-id="e5b59-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e5b59-114">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="e5b59-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e5b59-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e5b59-116">Documento</span><span class="sxs-lookup"><span data-stu-id="e5b59-116">Document</span></span><br/>                            |
| <span data-ttu-id="e5b59-117">Note</span><span class="sxs-lookup"><span data-stu-id="e5b59-117">Notes</span></span> <br/>          | <span data-ttu-id="e5b59-118">Collegato all'elemento DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="e5b59-118">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e5b59-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="e5b59-119">Structure Content</span></span>

<span data-ttu-id="e5b59-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="e5b59-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="e5b59-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="e5b59-121">Structure Properties</span></span>

<span data-ttu-id="e5b59-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e5b59-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e5b59-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5b59-123">Property</span></span>                | <span data-ttu-id="e5b59-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e5b59-124">xsi:type</span></span>           | <span data-ttu-id="e5b59-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b59-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e5b59-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e5b59-126">DataType</span></span><br/>     | <span data-ttu-id="e5b59-127">string</span><span class="sxs-lookup"><span data-stu-id="e5b59-127">string</span></span><br/>  | <span data-ttu-id="e5b59-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e5b59-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e5b59-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e5b59-129">DefaultValue</span></span><br/> | <span data-ttu-id="e5b59-130">string</span><span class="sxs-lookup"><span data-stu-id="e5b59-130">string</span></span><br/>  | <span data-ttu-id="e5b59-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="e5b59-131">undefined</span></span><br/>       |
| <span data-ttu-id="e5b59-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e5b59-132">MaxLength</span></span><br/>    | <span data-ttu-id="e5b59-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="e5b59-133">integer</span></span><br/> | <span data-ttu-id="e5b59-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="e5b59-134">undefined</span></span><br/>       |
| <span data-ttu-id="e5b59-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="e5b59-135">MinLength</span></span><br/>    | <span data-ttu-id="e5b59-136">integer</span><span class="sxs-lookup"><span data-stu-id="e5b59-136">integer</span></span><br/> | <span data-ttu-id="e5b59-137">1</span><span class="sxs-lookup"><span data-stu-id="e5b59-137">1</span></span><br/>               |
| <span data-ttu-id="e5b59-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="e5b59-138">Mandatory</span></span><br/>    | <span data-ttu-id="e5b59-139">string</span><span class="sxs-lookup"><span data-stu-id="e5b59-139">string</span></span><br/>  | <span data-ttu-id="e5b59-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="e5b59-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e5b59-141">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="e5b59-141">UnitType</span></span><br/>     | <span data-ttu-id="e5b59-142">string</span><span class="sxs-lookup"><span data-stu-id="e5b59-142">string</span></span><br/>  | <span data-ttu-id="e5b59-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="e5b59-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e5b59-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5b59-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b59-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e5b59-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




