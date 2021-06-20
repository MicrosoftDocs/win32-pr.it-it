---
description: Informazioni sull'elemento DocumentCoverBackSource, che specifica l'origine per un foglio di copertura posteriore personalizzato.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be16ab26a4aa3dd7109fee7d630ed354b9b686d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409354"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="b7384-103">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="b7384-103">DocumentCoverBackSource</span></span>

<span data-ttu-id="b7384-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b7384-104">This topic is not current.</span></span> <span data-ttu-id="b7384-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b7384-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7384-106">Specifica l'origine per un foglio di copertura posteriore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b7384-106">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="b7384-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b7384-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7384-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b7384-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b7384-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b7384-109">Element Information</span></span>



| <span data-ttu-id="b7384-110">Nome</span><span class="sxs-lookup"><span data-stu-id="b7384-110">Name</span></span> | <span data-ttu-id="b7384-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b7384-111">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="b7384-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b7384-112">Element Type</span></span> <br/>   | <span data-ttu-id="b7384-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b7384-113">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="b7384-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b7384-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7384-115">Documento</span><span class="sxs-lookup"><span data-stu-id="b7384-115">Document</span></span><br/>                            |
| <span data-ttu-id="b7384-116">Note</span><span class="sxs-lookup"><span data-stu-id="b7384-116">Notes</span></span> <br/>          | <span data-ttu-id="b7384-117">Collegato all'elemento DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="b7384-117">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b7384-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b7384-118">Structure Content</span></span>

<span data-ttu-id="b7384-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b7384-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b7384-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="b7384-120">Structure Properties</span></span>

<span data-ttu-id="b7384-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b7384-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7384-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7384-122">Property</span></span>                | <span data-ttu-id="b7384-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b7384-123">xsi:type</span></span>           | <span data-ttu-id="b7384-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b7384-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b7384-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b7384-125">DataType</span></span><br/>     | <span data-ttu-id="b7384-126">string</span><span class="sxs-lookup"><span data-stu-id="b7384-126">string</span></span><br/>  | <span data-ttu-id="b7384-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="b7384-127">xs:string</span></span><br/>       |
| <span data-ttu-id="b7384-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b7384-128">DefaultValue</span></span><br/> | <span data-ttu-id="b7384-129">string</span><span class="sxs-lookup"><span data-stu-id="b7384-129">string</span></span><br/>  | <span data-ttu-id="b7384-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="b7384-130">undefined</span></span><br/>       |
| <span data-ttu-id="b7384-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b7384-131">MaxLength</span></span><br/>    | <span data-ttu-id="b7384-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="b7384-132">integer</span></span><br/> | <span data-ttu-id="b7384-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="b7384-133">undefined</span></span><br/>       |
| <span data-ttu-id="b7384-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="b7384-134">MinLength</span></span><br/>    | <span data-ttu-id="b7384-135">integer</span><span class="sxs-lookup"><span data-stu-id="b7384-135">integer</span></span><br/> | <span data-ttu-id="b7384-136">1</span><span class="sxs-lookup"><span data-stu-id="b7384-136">1</span></span><br/>               |
| <span data-ttu-id="b7384-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b7384-137">Mandatory</span></span><br/>    | <span data-ttu-id="b7384-138">string</span><span class="sxs-lookup"><span data-stu-id="b7384-138">string</span></span><br/>  | <span data-ttu-id="b7384-139">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="b7384-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b7384-140">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="b7384-140">UnitType</span></span><br/>     | <span data-ttu-id="b7384-141">string</span><span class="sxs-lookup"><span data-stu-id="b7384-141">string</span></span><br/>  | <span data-ttu-id="b7384-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="b7384-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b7384-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7384-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7384-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b7384-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




