---
description: Informazioni sul parametro PageSourceColorProfileEmbedded. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0633fa061601c1d575f174ab5572582efdf9a89e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395636"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="b112a-105">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="b112a-105">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="b112a-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b112a-106">This topic is not current.</span></span> <span data-ttu-id="b112a-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b112a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b112a-108">Specifica il profilo colori di origine incorporato.</span><span class="sxs-lookup"><span data-stu-id="b112a-108">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="b112a-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b112a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b112a-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b112a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b112a-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b112a-111">Element Information</span></span>



| <span data-ttu-id="b112a-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b112a-112">Name</span></span> | <span data-ttu-id="b112a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b112a-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="b112a-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b112a-114">Element Type</span></span> <br/>   | <span data-ttu-id="b112a-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b112a-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="b112a-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="b112a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b112a-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="b112a-117">Page</span></span><br/>                                     |
| <span data-ttu-id="b112a-118">Note</span><span class="sxs-lookup"><span data-stu-id="b112a-118">Notes</span></span> <br/>          | <span data-ttu-id="b112a-119">Collegato all'elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="b112a-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b112a-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="b112a-120">Structure Content</span></span>

<span data-ttu-id="b112a-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="b112a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="b112a-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="b112a-122">Structure Properties</span></span>

<span data-ttu-id="b112a-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="b112a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b112a-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b112a-124">Property</span></span>                | <span data-ttu-id="b112a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b112a-125">xsi:type</span></span>           | <span data-ttu-id="b112a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b112a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b112a-127">DataType</span><span class="sxs-lookup"><span data-stu-id="b112a-127">DataType</span></span><br/>     | <span data-ttu-id="b112a-128">string</span><span class="sxs-lookup"><span data-stu-id="b112a-128">string</span></span><br/>  | <span data-ttu-id="b112a-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="b112a-129">xs:string</span></span><br/>       |
| <span data-ttu-id="b112a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b112a-130">DefaultValue</span></span><br/> | <span data-ttu-id="b112a-131">string</span><span class="sxs-lookup"><span data-stu-id="b112a-131">string</span></span><br/>  | <span data-ttu-id="b112a-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="b112a-132">undefined</span></span><br/>       |
| <span data-ttu-id="b112a-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b112a-133">MaxLength</span></span><br/>    | <span data-ttu-id="b112a-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="b112a-134">integer</span></span><br/> | <span data-ttu-id="b112a-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="b112a-135">undefined</span></span><br/>       |
| <span data-ttu-id="b112a-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="b112a-136">MinLength</span></span><br/>    | <span data-ttu-id="b112a-137">integer</span><span class="sxs-lookup"><span data-stu-id="b112a-137">integer</span></span><br/> | <span data-ttu-id="b112a-138">1</span><span class="sxs-lookup"><span data-stu-id="b112a-138">1</span></span><br/>               |
| <span data-ttu-id="b112a-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="b112a-139">Mandatory</span></span><br/>    | <span data-ttu-id="b112a-140">string</span><span class="sxs-lookup"><span data-stu-id="b112a-140">string</span></span><br/>  | <span data-ttu-id="b112a-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="b112a-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b112a-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="b112a-142">UnitType</span></span><br/>     | <span data-ttu-id="b112a-143">string</span><span class="sxs-lookup"><span data-stu-id="b112a-143">string</span></span><br/>  | <span data-ttu-id="b112a-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="b112a-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b112a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b112a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b112a-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b112a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




