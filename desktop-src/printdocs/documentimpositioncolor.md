---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228d1efded114c9471a55c4f88ca6e51ed6337ca
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997868"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="00f75-104">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="00f75-104">DocumentImpositionColor</span></span>

<span data-ttu-id="00f75-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="00f75-105">This topic is not current.</span></span> <span data-ttu-id="00f75-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="00f75-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="00f75-107">Il contenuto dell'applicazione etichettato con il colore denominato specificato DEVE essere visualizzato in tutte le separazioni dei colori.</span><span class="sxs-lookup"><span data-stu-id="00f75-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="00f75-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="00f75-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="00f75-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="00f75-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="00f75-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="00f75-110">Element Information</span></span>



| <span data-ttu-id="00f75-111">Nome</span><span class="sxs-lookup"><span data-stu-id="00f75-111">Name</span></span> | <span data-ttu-id="00f75-112">Valore</span><span class="sxs-lookup"><span data-stu-id="00f75-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="00f75-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="00f75-113">Element Type</span></span> <br/>   | <span data-ttu-id="00f75-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="00f75-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="00f75-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="00f75-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="00f75-116">Documento</span><span class="sxs-lookup"><span data-stu-id="00f75-116">Document</span></span><br/>     |
| <span data-ttu-id="00f75-117">Note</span><span class="sxs-lookup"><span data-stu-id="00f75-117">Notes</span></span> <br/>          | <span data-ttu-id="00f75-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="00f75-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="00f75-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="00f75-119">Structure Content</span></span>

<span data-ttu-id="00f75-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="00f75-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="00f75-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="00f75-121">Structure Properties</span></span>

<span data-ttu-id="00f75-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="00f75-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="00f75-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00f75-123">Property</span></span>                | <span data-ttu-id="00f75-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="00f75-124">xsi:type</span></span>           | <span data-ttu-id="00f75-125">Valore</span><span class="sxs-lookup"><span data-stu-id="00f75-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="00f75-126">DataType</span><span class="sxs-lookup"><span data-stu-id="00f75-126">DataType</span></span><br/>     | <span data-ttu-id="00f75-127">string</span><span class="sxs-lookup"><span data-stu-id="00f75-127">string</span></span><br/>  | <span data-ttu-id="00f75-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="00f75-128">xs:string</span></span><br/>       |
| <span data-ttu-id="00f75-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="00f75-129">DefaultValue</span></span><br/> | <span data-ttu-id="00f75-130">string</span><span class="sxs-lookup"><span data-stu-id="00f75-130">string</span></span><br/>  | <span data-ttu-id="00f75-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="00f75-131">undefined</span></span><br/>       |
| <span data-ttu-id="00f75-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="00f75-132">MaxLength</span></span><br/>    | <span data-ttu-id="00f75-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="00f75-133">integer</span></span><br/> | <span data-ttu-id="00f75-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="00f75-134">undefined</span></span><br/>       |
| <span data-ttu-id="00f75-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="00f75-135">MinLength</span></span><br/>    | <span data-ttu-id="00f75-136">integer</span><span class="sxs-lookup"><span data-stu-id="00f75-136">integer</span></span><br/> | <span data-ttu-id="00f75-137">1</span><span class="sxs-lookup"><span data-stu-id="00f75-137">1</span></span><br/>               |
| <span data-ttu-id="00f75-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="00f75-138">Mandatory</span></span><br/>    | <span data-ttu-id="00f75-139">string</span><span class="sxs-lookup"><span data-stu-id="00f75-139">string</span></span><br/>  | <span data-ttu-id="00f75-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="00f75-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="00f75-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="00f75-141">UnitType</span></span><br/>     | <span data-ttu-id="00f75-142">string</span><span class="sxs-lookup"><span data-stu-id="00f75-142">string</span></span><br/>  | <span data-ttu-id="00f75-143">caratteri</span><span class="sxs-lookup"><span data-stu-id="00f75-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="00f75-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00f75-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00f75-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="00f75-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




