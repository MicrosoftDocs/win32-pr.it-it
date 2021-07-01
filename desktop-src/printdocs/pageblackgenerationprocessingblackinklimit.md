---
description: Informazioni sul parametro PageBlackGenerationProcessingBlackInkLimit. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118426"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="6eb41-105">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="6eb41-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="6eb41-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6eb41-106">This topic is not current.</span></span> <span data-ttu-id="6eb41-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6eb41-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6eb41-108">Il contenuto dell'applicazione etichettato con il colore denominato specificato DEVE essere visualizzato in tutte le separazioni dei colori.</span><span class="sxs-lookup"><span data-stu-id="6eb41-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="6eb41-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6eb41-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6eb41-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="6eb41-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6eb41-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6eb41-111">Element Information</span></span>



| <span data-ttu-id="6eb41-112">Nome</span><span class="sxs-lookup"><span data-stu-id="6eb41-112">Name</span></span> | <span data-ttu-id="6eb41-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6eb41-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="6eb41-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6eb41-114">Element Type</span></span> <br/>   | <span data-ttu-id="6eb41-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6eb41-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="6eb41-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6eb41-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6eb41-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="6eb41-117">Page</span></span><br/>                                            |
| <span data-ttu-id="6eb41-118">Note</span><span class="sxs-lookup"><span data-stu-id="6eb41-118">Notes</span></span> <br/>          | <span data-ttu-id="6eb41-119">Collegato all'elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="6eb41-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6eb41-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="6eb41-120">Structure Content</span></span>

<span data-ttu-id="6eb41-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6eb41-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="6eb41-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="6eb41-122">Structure Properties</span></span>

<span data-ttu-id="6eb41-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6eb41-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6eb41-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6eb41-124">Property</span></span>                | <span data-ttu-id="6eb41-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6eb41-125">xsi:type</span></span>           | <span data-ttu-id="6eb41-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6eb41-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6eb41-127">DataType</span><span class="sxs-lookup"><span data-stu-id="6eb41-127">DataType</span></span><br/>     | <span data-ttu-id="6eb41-128">string</span><span class="sxs-lookup"><span data-stu-id="6eb41-128">string</span></span><br/>  | <span data-ttu-id="6eb41-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6eb41-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="6eb41-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6eb41-130">DefaultValue</span></span><br/> | <span data-ttu-id="6eb41-131">string</span><span class="sxs-lookup"><span data-stu-id="6eb41-131">string</span></span><br/>  | <span data-ttu-id="6eb41-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="6eb41-132">undefined</span></span><br/>       |
| <span data-ttu-id="6eb41-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6eb41-133">MaxValue</span></span><br/>     | <span data-ttu-id="6eb41-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="6eb41-134">integer</span></span><br/> | <span data-ttu-id="6eb41-135">100</span><span class="sxs-lookup"><span data-stu-id="6eb41-135">100</span></span><br/>             |
| <span data-ttu-id="6eb41-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="6eb41-136">MinValue</span></span><br/>     | <span data-ttu-id="6eb41-137">integer</span><span class="sxs-lookup"><span data-stu-id="6eb41-137">integer</span></span><br/> | <span data-ttu-id="6eb41-138">0</span><span class="sxs-lookup"><span data-stu-id="6eb41-138">0</span></span><br/>               |
| <span data-ttu-id="6eb41-139">Multipli</span><span class="sxs-lookup"><span data-stu-id="6eb41-139">Multiple</span></span><br/>     | <span data-ttu-id="6eb41-140">integer</span><span class="sxs-lookup"><span data-stu-id="6eb41-140">integer</span></span><br/> | <span data-ttu-id="6eb41-141">1</span><span class="sxs-lookup"><span data-stu-id="6eb41-141">1</span></span><br/>               |
| <span data-ttu-id="6eb41-142">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6eb41-142">Mandatory</span></span><br/>    | <span data-ttu-id="6eb41-143">string</span><span class="sxs-lookup"><span data-stu-id="6eb41-143">string</span></span><br/>  | <span data-ttu-id="6eb41-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="6eb41-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6eb41-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="6eb41-145">UnitType</span></span><br/>     | <span data-ttu-id="6eb41-146">string</span><span class="sxs-lookup"><span data-stu-id="6eb41-146">string</span></span><br/>  | <span data-ttu-id="6eb41-147">percent</span><span class="sxs-lookup"><span data-stu-id="6eb41-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6eb41-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6eb41-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eb41-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6eb41-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




