---
description: Informazioni sull'elemento JobPrimaryCoverBackSource, che specifica l'origine per un foglio primario di copertura posteriore personalizzato per il processo.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408694"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="43a9e-103">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="43a9e-103">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="43a9e-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="43a9e-104">This topic is not current.</span></span> <span data-ttu-id="43a9e-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="43a9e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="43a9e-106">Specifica l'origine per un foglio primario di copertura posteriore personalizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="43a9e-106">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="43a9e-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="43a9e-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="43a9e-108">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="43a9e-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="43a9e-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="43a9e-109">Element Information</span></span>



| <span data-ttu-id="43a9e-110">Nome</span><span class="sxs-lookup"><span data-stu-id="43a9e-110">Name</span></span> | <span data-ttu-id="43a9e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="43a9e-111">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="43a9e-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="43a9e-112">Element Type</span></span> <br/>   | <span data-ttu-id="43a9e-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="43a9e-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="43a9e-114">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="43a9e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="43a9e-115">Processo</span><span class="sxs-lookup"><span data-stu-id="43a9e-115">Job</span></span><br/>                            |
| <span data-ttu-id="43a9e-116">Note</span><span class="sxs-lookup"><span data-stu-id="43a9e-116">Notes</span></span> <br/>          | <span data-ttu-id="43a9e-117">Collegato all'elemento JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="43a9e-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="43a9e-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="43a9e-118">Structure Content</span></span>

<span data-ttu-id="43a9e-119">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="43a9e-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="43a9e-120">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="43a9e-120">Structure Properties</span></span>

<span data-ttu-id="43a9e-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="43a9e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="43a9e-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="43a9e-122">Property</span></span>                | <span data-ttu-id="43a9e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="43a9e-123">xsi:type</span></span>           | <span data-ttu-id="43a9e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="43a9e-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="43a9e-125">DataType</span><span class="sxs-lookup"><span data-stu-id="43a9e-125">DataType</span></span><br/>     | <span data-ttu-id="43a9e-126">string</span><span class="sxs-lookup"><span data-stu-id="43a9e-126">string</span></span><br/>  | <span data-ttu-id="43a9e-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="43a9e-127">xs:string</span></span><br/>       |
| <span data-ttu-id="43a9e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="43a9e-128">DefaultValue</span></span><br/> | <span data-ttu-id="43a9e-129">string</span><span class="sxs-lookup"><span data-stu-id="43a9e-129">string</span></span><br/>  | <span data-ttu-id="43a9e-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="43a9e-130">undefined</span></span><br/>       |
| <span data-ttu-id="43a9e-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="43a9e-131">MaxLength</span></span><br/>    | <span data-ttu-id="43a9e-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="43a9e-132">integer</span></span><br/> | <span data-ttu-id="43a9e-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="43a9e-133">undefined</span></span><br/>       |
| <span data-ttu-id="43a9e-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="43a9e-134">MinLength</span></span><br/>    | <span data-ttu-id="43a9e-135">integer</span><span class="sxs-lookup"><span data-stu-id="43a9e-135">integer</span></span><br/> | <span data-ttu-id="43a9e-136">1</span><span class="sxs-lookup"><span data-stu-id="43a9e-136">1</span></span><br/>               |
| <span data-ttu-id="43a9e-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="43a9e-137">Mandatory</span></span><br/>    | <span data-ttu-id="43a9e-138">string</span><span class="sxs-lookup"><span data-stu-id="43a9e-138">string</span></span><br/>  | <span data-ttu-id="43a9e-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="43a9e-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="43a9e-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="43a9e-140">UnitType</span></span><br/>     | <span data-ttu-id="43a9e-141">string</span><span class="sxs-lookup"><span data-stu-id="43a9e-141">string</span></span><br/>  | <span data-ttu-id="43a9e-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="43a9e-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="43a9e-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43a9e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a9e-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="43a9e-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




