---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2145bae0843323928d8a7d016fc61f10c0e388ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993978"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="22689-104">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="22689-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="22689-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="22689-105">This topic is not current.</span></span> <span data-ttu-id="22689-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="22689-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22689-107">Specifica l'origine per un foglio principale di copertura posteriore personalizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="22689-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="22689-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22689-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22689-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="22689-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="22689-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22689-110">Element Information</span></span>



| <span data-ttu-id="22689-111">Nome</span><span class="sxs-lookup"><span data-stu-id="22689-111">Name</span></span> | <span data-ttu-id="22689-112">Valore</span><span class="sxs-lookup"><span data-stu-id="22689-112">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="22689-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="22689-113">Element Type</span></span> <br/>   | <span data-ttu-id="22689-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="22689-114">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="22689-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="22689-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22689-116">Processo</span><span class="sxs-lookup"><span data-stu-id="22689-116">Job</span></span><br/>                            |
| <span data-ttu-id="22689-117">Note</span><span class="sxs-lookup"><span data-stu-id="22689-117">Notes</span></span> <br/>          | <span data-ttu-id="22689-118">Collegato all'elemento JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="22689-118">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="22689-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="22689-119">Structure Content</span></span>

<span data-ttu-id="22689-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="22689-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="22689-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="22689-121">Structure Properties</span></span>

<span data-ttu-id="22689-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="22689-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22689-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22689-123">Property</span></span>                | <span data-ttu-id="22689-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="22689-124">xsi:type</span></span>           | <span data-ttu-id="22689-125">Valore</span><span class="sxs-lookup"><span data-stu-id="22689-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="22689-126">DataType</span><span class="sxs-lookup"><span data-stu-id="22689-126">DataType</span></span><br/>     | <span data-ttu-id="22689-127">string</span><span class="sxs-lookup"><span data-stu-id="22689-127">string</span></span><br/>  | <span data-ttu-id="22689-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="22689-128">xs:string</span></span><br/>       |
| <span data-ttu-id="22689-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="22689-129">DefaultValue</span></span><br/> | <span data-ttu-id="22689-130">string</span><span class="sxs-lookup"><span data-stu-id="22689-130">string</span></span><br/>  | <span data-ttu-id="22689-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="22689-131">undefined</span></span><br/>       |
| <span data-ttu-id="22689-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="22689-132">MaxLength</span></span><br/>    | <span data-ttu-id="22689-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="22689-133">integer</span></span><br/> | <span data-ttu-id="22689-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="22689-134">undefined</span></span><br/>       |
| <span data-ttu-id="22689-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="22689-135">MinLength</span></span><br/>    | <span data-ttu-id="22689-136">integer</span><span class="sxs-lookup"><span data-stu-id="22689-136">integer</span></span><br/> | <span data-ttu-id="22689-137">1</span><span class="sxs-lookup"><span data-stu-id="22689-137">1</span></span><br/>               |
| <span data-ttu-id="22689-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="22689-138">Mandatory</span></span><br/>    | <span data-ttu-id="22689-139">string</span><span class="sxs-lookup"><span data-stu-id="22689-139">string</span></span><br/>  | <span data-ttu-id="22689-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="22689-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="22689-141">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="22689-141">UnitType</span></span><br/>     | <span data-ttu-id="22689-142">string</span><span class="sxs-lookup"><span data-stu-id="22689-142">string</span></span><br/>  | <span data-ttu-id="22689-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="22689-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="22689-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22689-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22689-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="22689-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




