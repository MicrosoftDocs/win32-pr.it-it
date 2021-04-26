---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e97e768561fd13d5033b12f69a9bc481448e0e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999119"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="f23f2-104">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="f23f2-104">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="f23f2-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="f23f2-105">This topic is not current.</span></span> <span data-ttu-id="f23f2-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f23f2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f23f2-107">Specifica il profilo colori di origine incorporato.</span><span class="sxs-lookup"><span data-stu-id="f23f2-107">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="f23f2-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f23f2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f23f2-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f23f2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f23f2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f23f2-110">Element Information</span></span>



| <span data-ttu-id="f23f2-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f23f2-111">Name</span></span> | <span data-ttu-id="f23f2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f23f2-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="f23f2-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f23f2-113">Element Type</span></span> <br/>   | <span data-ttu-id="f23f2-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f23f2-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="f23f2-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="f23f2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f23f2-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="f23f2-116">Page</span></span><br/>                                     |
| <span data-ttu-id="f23f2-117">Note</span><span class="sxs-lookup"><span data-stu-id="f23f2-117">Notes</span></span> <br/>          | <span data-ttu-id="f23f2-118">Collegato all'elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="f23f2-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f23f2-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="f23f2-119">Structure Content</span></span>

<span data-ttu-id="f23f2-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="f23f2-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f23f2-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="f23f2-121">Structure Properties</span></span>

<span data-ttu-id="f23f2-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="f23f2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f23f2-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f23f2-123">Property</span></span>                | <span data-ttu-id="f23f2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f23f2-124">xsi:type</span></span>           | <span data-ttu-id="f23f2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f23f2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f23f2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="f23f2-126">DataType</span></span><br/>     | <span data-ttu-id="f23f2-127">string</span><span class="sxs-lookup"><span data-stu-id="f23f2-127">string</span></span><br/>  | <span data-ttu-id="f23f2-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="f23f2-128">xs:string</span></span><br/>       |
| <span data-ttu-id="f23f2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f23f2-129">DefaultValue</span></span><br/> | <span data-ttu-id="f23f2-130">string</span><span class="sxs-lookup"><span data-stu-id="f23f2-130">string</span></span><br/>  | <span data-ttu-id="f23f2-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="f23f2-131">undefined</span></span><br/>       |
| <span data-ttu-id="f23f2-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f23f2-132">MaxLength</span></span><br/>    | <span data-ttu-id="f23f2-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="f23f2-133">integer</span></span><br/> | <span data-ttu-id="f23f2-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="f23f2-134">undefined</span></span><br/>       |
| <span data-ttu-id="f23f2-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="f23f2-135">MinLength</span></span><br/>    | <span data-ttu-id="f23f2-136">integer</span><span class="sxs-lookup"><span data-stu-id="f23f2-136">integer</span></span><br/> | <span data-ttu-id="f23f2-137">1</span><span class="sxs-lookup"><span data-stu-id="f23f2-137">1</span></span><br/>               |
| <span data-ttu-id="f23f2-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f23f2-138">Mandatory</span></span><br/>    | <span data-ttu-id="f23f2-139">string</span><span class="sxs-lookup"><span data-stu-id="f23f2-139">string</span></span><br/>  | <span data-ttu-id="f23f2-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="f23f2-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f23f2-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="f23f2-141">UnitType</span></span><br/>     | <span data-ttu-id="f23f2-142">string</span><span class="sxs-lookup"><span data-stu-id="f23f2-142">string</span></span><br/>  | <span data-ttu-id="f23f2-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="f23f2-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f23f2-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f23f2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f23f2-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f23f2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




