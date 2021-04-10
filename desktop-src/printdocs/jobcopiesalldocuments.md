---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f8be33f98b540cab56b88df49cfb1e3c067988
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761548"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="7f72a-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="7f72a-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="7f72a-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7f72a-105">This topic is not current.</span></span> <span data-ttu-id="7f72a-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7f72a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7f72a-107">Specifica il numero di copie di un processo.</span><span class="sxs-lookup"><span data-stu-id="7f72a-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="7f72a-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7f72a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7f72a-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7f72a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7f72a-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7f72a-110">Element Information</span></span>



| <span data-ttu-id="7f72a-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7f72a-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="7f72a-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7f72a-112">Element Type</span></span> <br/>   | <span data-ttu-id="7f72a-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7f72a-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="7f72a-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="7f72a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7f72a-115">Processo</span><span class="sxs-lookup"><span data-stu-id="7f72a-115">Job</span></span><br/>          |
| <span data-ttu-id="7f72a-116">Note</span><span class="sxs-lookup"><span data-stu-id="7f72a-116">Notes</span></span> <br/>          | <span data-ttu-id="7f72a-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="7f72a-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="7f72a-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="7f72a-118">Structure Content</span></span>

<span data-ttu-id="7f72a-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="7f72a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
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

## <a name="structure-properties"></a><span data-ttu-id="7f72a-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="7f72a-120">Structure Properties</span></span>

<span data-ttu-id="7f72a-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="7f72a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7f72a-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f72a-122">Property</span></span>                | <span data-ttu-id="7f72a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7f72a-123">xsi:type</span></span>           | <span data-ttu-id="7f72a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7f72a-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="7f72a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7f72a-125">DataType</span></span><br/>     | <span data-ttu-id="7f72a-126">string</span><span class="sxs-lookup"><span data-stu-id="7f72a-126">string</span></span><br/>  | <span data-ttu-id="7f72a-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7f72a-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="7f72a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7f72a-128">DefaultValue</span></span><br/> | <span data-ttu-id="7f72a-129">integer</span><span class="sxs-lookup"><span data-stu-id="7f72a-129">integer</span></span><br/> | <span data-ttu-id="7f72a-130">1</span><span class="sxs-lookup"><span data-stu-id="7f72a-130">1</span></span><br/>                 |
| <span data-ttu-id="7f72a-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7f72a-131">MaxValue</span></span><br/>     | <span data-ttu-id="7f72a-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="7f72a-132">integer</span></span><br/> | <span data-ttu-id="7f72a-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="7f72a-133">undefined</span></span><br/>         |
| <span data-ttu-id="7f72a-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7f72a-134">MinValue</span></span><br/>     | <span data-ttu-id="7f72a-135">integer</span><span class="sxs-lookup"><span data-stu-id="7f72a-135">integer</span></span><br/> | <span data-ttu-id="7f72a-136">1</span><span class="sxs-lookup"><span data-stu-id="7f72a-136">1</span></span><br/>                 |
| <span data-ttu-id="7f72a-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7f72a-137">Mandatory</span></span><br/>    | <span data-ttu-id="7f72a-138">string</span><span class="sxs-lookup"><span data-stu-id="7f72a-138">string</span></span><br/>  | <span data-ttu-id="7f72a-139">PSK: non condizionale</span><span class="sxs-lookup"><span data-stu-id="7f72a-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="7f72a-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="7f72a-140">Multiple</span></span><br/>     | <span data-ttu-id="7f72a-141">integer</span><span class="sxs-lookup"><span data-stu-id="7f72a-141">integer</span></span><br/> | <span data-ttu-id="7f72a-142">1</span><span class="sxs-lookup"><span data-stu-id="7f72a-142">1</span></span><br/>                 |
| <span data-ttu-id="7f72a-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="7f72a-143">UnitType</span></span><br/>     | <span data-ttu-id="7f72a-144">string</span><span class="sxs-lookup"><span data-stu-id="7f72a-144">string</span></span><br/>  | <span data-ttu-id="7f72a-145">copie</span><span class="sxs-lookup"><span data-stu-id="7f72a-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="7f72a-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f72a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f72a-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7f72a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




