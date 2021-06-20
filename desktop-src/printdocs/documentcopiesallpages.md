---
description: Informazioni sull'elemento DocumentCopiesAllPages, che specifica il numero di copie di un documento.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf82c23b764f3fe1f8257f4cdb2e7fa03374bd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409444"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="49313-103">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="49313-103">DocumentCopiesAllPages</span></span>

<span data-ttu-id="49313-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="49313-104">This topic is not current.</span></span> <span data-ttu-id="49313-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49313-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49313-106">Specifica il numero di copie di un documento.</span><span class="sxs-lookup"><span data-stu-id="49313-106">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="49313-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="49313-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="49313-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="49313-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="49313-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="49313-109">Element Information</span></span>



| <span data-ttu-id="49313-110">Nome</span><span class="sxs-lookup"><span data-stu-id="49313-110">Name</span></span> | <span data-ttu-id="49313-111">Valore</span><span class="sxs-lookup"><span data-stu-id="49313-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="49313-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="49313-112">Element Type</span></span> <br/>   | <span data-ttu-id="49313-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="49313-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="49313-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="49313-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="49313-115">Documento</span><span class="sxs-lookup"><span data-stu-id="49313-115">Document</span></span><br/>     |
| <span data-ttu-id="49313-116">Note</span><span class="sxs-lookup"><span data-stu-id="49313-116">Notes</span></span> <br/>          | <span data-ttu-id="49313-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="49313-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="49313-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="49313-118">Structure Content</span></span>

<span data-ttu-id="49313-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="49313-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="49313-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="49313-120">Structure Properties</span></span>

<span data-ttu-id="49313-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="49313-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="49313-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49313-122">Property</span></span>                | <span data-ttu-id="49313-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="49313-123">xsi:type</span></span>           | <span data-ttu-id="49313-124">Valore</span><span class="sxs-lookup"><span data-stu-id="49313-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="49313-125">DataType</span><span class="sxs-lookup"><span data-stu-id="49313-125">DataType</span></span><br/>     | <span data-ttu-id="49313-126">string</span><span class="sxs-lookup"><span data-stu-id="49313-126">string</span></span><br/>  | <span data-ttu-id="49313-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="49313-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="49313-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="49313-128">DefaultValue</span></span><br/> | <span data-ttu-id="49313-129">integer</span><span class="sxs-lookup"><span data-stu-id="49313-129">integer</span></span><br/> | <span data-ttu-id="49313-130">1</span><span class="sxs-lookup"><span data-stu-id="49313-130">1</span></span><br/>                 |
| <span data-ttu-id="49313-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="49313-131">MaxValue</span></span><br/>     | <span data-ttu-id="49313-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="49313-132">integer</span></span><br/> | <span data-ttu-id="49313-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="49313-133">undefined</span></span><br/>         |
| <span data-ttu-id="49313-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="49313-134">MinValue</span></span><br/>     | <span data-ttu-id="49313-135">integer</span><span class="sxs-lookup"><span data-stu-id="49313-135">integer</span></span><br/> | <span data-ttu-id="49313-136">1</span><span class="sxs-lookup"><span data-stu-id="49313-136">1</span></span><br/>                 |
| <span data-ttu-id="49313-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="49313-137">Mandatory</span></span><br/>    | <span data-ttu-id="49313-138">string</span><span class="sxs-lookup"><span data-stu-id="49313-138">string</span></span><br/>  | <span data-ttu-id="49313-139">psk:Unconditional</span><span class="sxs-lookup"><span data-stu-id="49313-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="49313-140">Multipli</span><span class="sxs-lookup"><span data-stu-id="49313-140">Multiple</span></span><br/>     | <span data-ttu-id="49313-141">integer</span><span class="sxs-lookup"><span data-stu-id="49313-141">integer</span></span><br/> | <span data-ttu-id="49313-142">1</span><span class="sxs-lookup"><span data-stu-id="49313-142">1</span></span><br/>                 |
| <span data-ttu-id="49313-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="49313-143">UnitType</span></span><br/>     | <span data-ttu-id="49313-144">string</span><span class="sxs-lookup"><span data-stu-id="49313-144">string</span></span><br/>  | <span data-ttu-id="49313-145">Copie</span><span class="sxs-lookup"><span data-stu-id="49313-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="49313-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49313-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49313-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="49313-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




