---
description: Leggere le informazioni di riferimento sul parametro PageCopies. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396686"
---
# <a name="pagecopies"></a><span data-ttu-id="0a4e2-105">PageCopies</span><span class="sxs-lookup"><span data-stu-id="0a4e2-105">PageCopies</span></span>

<span data-ttu-id="0a4e2-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="0a4e2-106">This topic is not current.</span></span> <span data-ttu-id="0a4e2-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a4e2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a4e2-108">Specifica il numero di copie di una pagina.</span><span class="sxs-lookup"><span data-stu-id="0a4e2-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="0a4e2-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a4e2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0a4e2-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0a4e2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0a4e2-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a4e2-111">Element Information</span></span>



| <span data-ttu-id="0a4e2-112">Nome</span><span class="sxs-lookup"><span data-stu-id="0a4e2-112">Name</span></span> | <span data-ttu-id="0a4e2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0a4e2-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="0a4e2-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0a4e2-114">Element Type</span></span> <br/>   | <span data-ttu-id="0a4e2-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0a4e2-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="0a4e2-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="0a4e2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a4e2-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="0a4e2-117">Page</span></span><br/>         |
| <span data-ttu-id="0a4e2-118">Note</span><span class="sxs-lookup"><span data-stu-id="0a4e2-118">Notes</span></span> <br/>          | <span data-ttu-id="0a4e2-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4e2-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="0a4e2-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0a4e2-120">Structure Content</span></span>

<span data-ttu-id="0a4e2-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="0a4e2-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
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

## <a name="structure-properties"></a><span data-ttu-id="0a4e2-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="0a4e2-122">Structure Properties</span></span>

<span data-ttu-id="0a4e2-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0a4e2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a4e2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a4e2-124">Property</span></span>                | <span data-ttu-id="0a4e2-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0a4e2-125">xsi:type</span></span>           | <span data-ttu-id="0a4e2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0a4e2-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="0a4e2-127">DataType</span><span class="sxs-lookup"><span data-stu-id="0a4e2-127">DataType</span></span><br/>     | <span data-ttu-id="0a4e2-128">string</span><span class="sxs-lookup"><span data-stu-id="0a4e2-128">string</span></span><br/>  | <span data-ttu-id="0a4e2-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0a4e2-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="0a4e2-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0a4e2-130">DefaultValue</span></span><br/> | <span data-ttu-id="0a4e2-131">integer</span><span class="sxs-lookup"><span data-stu-id="0a4e2-131">integer</span></span><br/> | <span data-ttu-id="0a4e2-132">1</span><span class="sxs-lookup"><span data-stu-id="0a4e2-132">1</span></span><br/>                 |
| <span data-ttu-id="0a4e2-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0a4e2-133">MaxValue</span></span><br/>     | <span data-ttu-id="0a4e2-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="0a4e2-134">integer</span></span><br/> | <span data-ttu-id="0a4e2-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="0a4e2-135">undefined</span></span><br/>         |
| <span data-ttu-id="0a4e2-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="0a4e2-136">MinValue</span></span><br/>     | <span data-ttu-id="0a4e2-137">integer</span><span class="sxs-lookup"><span data-stu-id="0a4e2-137">integer</span></span><br/> | <span data-ttu-id="0a4e2-138">1</span><span class="sxs-lookup"><span data-stu-id="0a4e2-138">1</span></span><br/>                 |
| <span data-ttu-id="0a4e2-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0a4e2-139">Mandatory</span></span><br/>    | <span data-ttu-id="0a4e2-140">string</span><span class="sxs-lookup"><span data-stu-id="0a4e2-140">string</span></span><br/>  | <span data-ttu-id="0a4e2-141">psk:unconditional</span><span class="sxs-lookup"><span data-stu-id="0a4e2-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="0a4e2-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="0a4e2-142">Multiple</span></span><br/>     | <span data-ttu-id="0a4e2-143">integer</span><span class="sxs-lookup"><span data-stu-id="0a4e2-143">integer</span></span><br/> | <span data-ttu-id="0a4e2-144">1</span><span class="sxs-lookup"><span data-stu-id="0a4e2-144">1</span></span><br/>                 |
| <span data-ttu-id="0a4e2-145">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="0a4e2-145">UnitType</span></span><br/>     | <span data-ttu-id="0a4e2-146">string</span><span class="sxs-lookup"><span data-stu-id="0a4e2-146">string</span></span><br/>  | <span data-ttu-id="0a4e2-147">Copie</span><span class="sxs-lookup"><span data-stu-id="0a4e2-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="0a4e2-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a4e2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a4e2-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0a4e2-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




