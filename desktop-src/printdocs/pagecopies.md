---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234569"
---
# <a name="pagecopies"></a><span data-ttu-id="0aba4-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="0aba4-104">PageCopies</span></span>

<span data-ttu-id="0aba4-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0aba4-105">This topic is not current.</span></span> <span data-ttu-id="0aba4-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0aba4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0aba4-107">Specifica il numero di copie di una pagina.</span><span class="sxs-lookup"><span data-stu-id="0aba4-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="0aba4-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0aba4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0aba4-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0aba4-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0aba4-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0aba4-110">Element Information</span></span>



| <span data-ttu-id="0aba4-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0aba4-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="0aba4-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0aba4-112">Element Type</span></span> <br/>   | <span data-ttu-id="0aba4-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0aba4-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="0aba4-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="0aba4-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0aba4-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="0aba4-115">Page</span></span><br/>         |
| <span data-ttu-id="0aba4-116">Note</span><span class="sxs-lookup"><span data-stu-id="0aba4-116">Notes</span></span> <br/>          | <span data-ttu-id="0aba4-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="0aba4-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="0aba4-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="0aba4-118">Structure Content</span></span>

<span data-ttu-id="0aba4-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="0aba4-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0aba4-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="0aba4-120">Structure Properties</span></span>

<span data-ttu-id="0aba4-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="0aba4-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0aba4-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0aba4-122">Property</span></span>                | <span data-ttu-id="0aba4-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0aba4-123">xsi:type</span></span>           | <span data-ttu-id="0aba4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0aba4-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="0aba4-125">DataType</span><span class="sxs-lookup"><span data-stu-id="0aba4-125">DataType</span></span><br/>     | <span data-ttu-id="0aba4-126">string</span><span class="sxs-lookup"><span data-stu-id="0aba4-126">string</span></span><br/>  | <span data-ttu-id="0aba4-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0aba4-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="0aba4-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0aba4-128">DefaultValue</span></span><br/> | <span data-ttu-id="0aba4-129">integer</span><span class="sxs-lookup"><span data-stu-id="0aba4-129">integer</span></span><br/> | <span data-ttu-id="0aba4-130">1</span><span class="sxs-lookup"><span data-stu-id="0aba4-130">1</span></span><br/>                 |
| <span data-ttu-id="0aba4-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0aba4-131">MaxValue</span></span><br/>     | <span data-ttu-id="0aba4-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="0aba4-132">integer</span></span><br/> | <span data-ttu-id="0aba4-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="0aba4-133">undefined</span></span><br/>         |
| <span data-ttu-id="0aba4-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="0aba4-134">MinValue</span></span><br/>     | <span data-ttu-id="0aba4-135">integer</span><span class="sxs-lookup"><span data-stu-id="0aba4-135">integer</span></span><br/> | <span data-ttu-id="0aba4-136">1</span><span class="sxs-lookup"><span data-stu-id="0aba4-136">1</span></span><br/>                 |
| <span data-ttu-id="0aba4-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0aba4-137">Mandatory</span></span><br/>    | <span data-ttu-id="0aba4-138">string</span><span class="sxs-lookup"><span data-stu-id="0aba4-138">string</span></span><br/>  | <span data-ttu-id="0aba4-139">PSK: non condizionale</span><span class="sxs-lookup"><span data-stu-id="0aba4-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="0aba4-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="0aba4-140">Multiple</span></span><br/>     | <span data-ttu-id="0aba4-141">integer</span><span class="sxs-lookup"><span data-stu-id="0aba4-141">integer</span></span><br/> | <span data-ttu-id="0aba4-142">1</span><span class="sxs-lookup"><span data-stu-id="0aba4-142">1</span></span><br/>                 |
| <span data-ttu-id="0aba4-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="0aba4-143">UnitType</span></span><br/>     | <span data-ttu-id="0aba4-144">string</span><span class="sxs-lookup"><span data-stu-id="0aba4-144">string</span></span><br/>  | <span data-ttu-id="0aba4-145">copie</span><span class="sxs-lookup"><span data-stu-id="0aba4-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="0aba4-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0aba4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aba4-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="0aba4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




