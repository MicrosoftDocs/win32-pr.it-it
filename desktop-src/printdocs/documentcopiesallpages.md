---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723242ddd127113b573f167e6902b27fcca9665a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993988"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="89219-104">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="89219-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="89219-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="89219-105">This topic is not current.</span></span> <span data-ttu-id="89219-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="89219-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="89219-107">Specifica il numero di copie di un documento.</span><span class="sxs-lookup"><span data-stu-id="89219-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="89219-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="89219-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="89219-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="89219-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="89219-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="89219-110">Element Information</span></span>



| <span data-ttu-id="89219-111">Nome</span><span class="sxs-lookup"><span data-stu-id="89219-111">Name</span></span> | <span data-ttu-id="89219-112">Valore</span><span class="sxs-lookup"><span data-stu-id="89219-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="89219-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="89219-113">Element Type</span></span> <br/>   | <span data-ttu-id="89219-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="89219-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="89219-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="89219-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="89219-116">Documento</span><span class="sxs-lookup"><span data-stu-id="89219-116">Document</span></span><br/>     |
| <span data-ttu-id="89219-117">Note</span><span class="sxs-lookup"><span data-stu-id="89219-117">Notes</span></span> <br/>          | <span data-ttu-id="89219-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="89219-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="89219-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="89219-119">Structure Content</span></span>

<span data-ttu-id="89219-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="89219-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="89219-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="89219-121">Structure Properties</span></span>

<span data-ttu-id="89219-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="89219-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="89219-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89219-123">Property</span></span>                | <span data-ttu-id="89219-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="89219-124">xsi:type</span></span>           | <span data-ttu-id="89219-125">Valore</span><span class="sxs-lookup"><span data-stu-id="89219-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="89219-126">DataType</span><span class="sxs-lookup"><span data-stu-id="89219-126">DataType</span></span><br/>     | <span data-ttu-id="89219-127">string</span><span class="sxs-lookup"><span data-stu-id="89219-127">string</span></span><br/>  | <span data-ttu-id="89219-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="89219-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="89219-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="89219-129">DefaultValue</span></span><br/> | <span data-ttu-id="89219-130">integer</span><span class="sxs-lookup"><span data-stu-id="89219-130">integer</span></span><br/> | <span data-ttu-id="89219-131">1</span><span class="sxs-lookup"><span data-stu-id="89219-131">1</span></span><br/>                 |
| <span data-ttu-id="89219-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="89219-132">MaxValue</span></span><br/>     | <span data-ttu-id="89219-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="89219-133">integer</span></span><br/> | <span data-ttu-id="89219-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="89219-134">undefined</span></span><br/>         |
| <span data-ttu-id="89219-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="89219-135">MinValue</span></span><br/>     | <span data-ttu-id="89219-136">integer</span><span class="sxs-lookup"><span data-stu-id="89219-136">integer</span></span><br/> | <span data-ttu-id="89219-137">1</span><span class="sxs-lookup"><span data-stu-id="89219-137">1</span></span><br/>                 |
| <span data-ttu-id="89219-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="89219-138">Mandatory</span></span><br/>    | <span data-ttu-id="89219-139">string</span><span class="sxs-lookup"><span data-stu-id="89219-139">string</span></span><br/>  | <span data-ttu-id="89219-140">psk:unconditional</span><span class="sxs-lookup"><span data-stu-id="89219-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="89219-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="89219-141">Multiple</span></span><br/>     | <span data-ttu-id="89219-142">integer</span><span class="sxs-lookup"><span data-stu-id="89219-142">integer</span></span><br/> | <span data-ttu-id="89219-143">1</span><span class="sxs-lookup"><span data-stu-id="89219-143">1</span></span><br/>                 |
| <span data-ttu-id="89219-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="89219-144">UnitType</span></span><br/>     | <span data-ttu-id="89219-145">string</span><span class="sxs-lookup"><span data-stu-id="89219-145">string</span></span><br/>  | <span data-ttu-id="89219-146">Copie</span><span class="sxs-lookup"><span data-stu-id="89219-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="89219-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89219-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89219-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="89219-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




