---
description: Ottenere informazioni sul parametro JobPrimaryCoverFrontSource. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: JobPrimaryCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4698d826e59e513d5eb171381cd1b18ea4a751
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549399"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="dd53c-105">JobPrimaryCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="dd53c-105">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="dd53c-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="dd53c-106">This topic is not current.</span></span> <span data-ttu-id="dd53c-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dd53c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd53c-108">Specifica l'origine per un foglio principale di copertura anteriore personalizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="dd53c-108">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="dd53c-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="dd53c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dd53c-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="dd53c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dd53c-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="dd53c-111">Element Information</span></span>



| <span data-ttu-id="dd53c-112">Nome</span><span class="sxs-lookup"><span data-stu-id="dd53c-112">Name</span></span> | <span data-ttu-id="dd53c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="dd53c-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="dd53c-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="dd53c-114">Element Type</span></span> <br/>   | <span data-ttu-id="dd53c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dd53c-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="dd53c-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="dd53c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dd53c-117">Processo</span><span class="sxs-lookup"><span data-stu-id="dd53c-117">Job</span></span><br/>                             |
| <span data-ttu-id="dd53c-118">Note</span><span class="sxs-lookup"><span data-stu-id="dd53c-118">Notes</span></span> <br/>          | <span data-ttu-id="dd53c-119">Collegato all'elemento JobCoverFront</span><span class="sxs-lookup"><span data-stu-id="dd53c-119">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dd53c-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="dd53c-120">Structure Content</span></span>

<span data-ttu-id="dd53c-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="dd53c-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="dd53c-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="dd53c-122">Structure Properties</span></span>

<span data-ttu-id="dd53c-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="dd53c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dd53c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd53c-124">Property</span></span>                | <span data-ttu-id="dd53c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dd53c-125">xsi:type</span></span>           | <span data-ttu-id="dd53c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="dd53c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dd53c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="dd53c-127">DataType</span></span><br/>     | <span data-ttu-id="dd53c-128">string</span><span class="sxs-lookup"><span data-stu-id="dd53c-128">string</span></span><br/>  | <span data-ttu-id="dd53c-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="dd53c-129">xs:string</span></span><br/>       |
| <span data-ttu-id="dd53c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dd53c-130">DefaultValue</span></span><br/> | <span data-ttu-id="dd53c-131">string</span><span class="sxs-lookup"><span data-stu-id="dd53c-131">string</span></span><br/>  | <span data-ttu-id="dd53c-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="dd53c-132">undefined</span></span><br/>       |
| <span data-ttu-id="dd53c-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="dd53c-133">MaxLength</span></span><br/>    | <span data-ttu-id="dd53c-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="dd53c-134">integer</span></span><br/> | <span data-ttu-id="dd53c-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="dd53c-135">undefined</span></span><br/>       |
| <span data-ttu-id="dd53c-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="dd53c-136">MinLength</span></span><br/>    | <span data-ttu-id="dd53c-137">integer</span><span class="sxs-lookup"><span data-stu-id="dd53c-137">integer</span></span><br/> | <span data-ttu-id="dd53c-138">1</span><span class="sxs-lookup"><span data-stu-id="dd53c-138">1</span></span><br/>               |
| <span data-ttu-id="dd53c-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="dd53c-139">Mandatory</span></span><br/>    | <span data-ttu-id="dd53c-140">string</span><span class="sxs-lookup"><span data-stu-id="dd53c-140">string</span></span><br/>  | <span data-ttu-id="dd53c-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="dd53c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dd53c-142">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="dd53c-142">UnitType</span></span><br/>     | <span data-ttu-id="dd53c-143">string</span><span class="sxs-lookup"><span data-stu-id="dd53c-143">string</span></span><br/>  | <span data-ttu-id="dd53c-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="dd53c-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="dd53c-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd53c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd53c-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="dd53c-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




