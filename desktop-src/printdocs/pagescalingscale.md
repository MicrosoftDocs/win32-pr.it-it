---
description: Ottenere informazioni sul parametro PageScalingScale. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c6cee5fc46568e3cf7f15ecd43c07c6584c856
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548829"
---
# <a name="pagescalingscale"></a><span data-ttu-id="363ce-105">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="363ce-105">PageScalingScale</span></span>

<span data-ttu-id="363ce-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="363ce-106">This topic is not current.</span></span> <span data-ttu-id="363ce-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="363ce-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="363ce-108">Specifica il fattore di scala per il ridimensionamento quadrato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="363ce-108">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="363ce-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="363ce-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="363ce-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="363ce-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="363ce-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="363ce-111">Element Information</span></span>



| <span data-ttu-id="363ce-112">Nome</span><span class="sxs-lookup"><span data-stu-id="363ce-112">Name</span></span> | <span data-ttu-id="363ce-113">Valore</span><span class="sxs-lookup"><span data-stu-id="363ce-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="363ce-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="363ce-114">Element Type</span></span> <br/>   | <span data-ttu-id="363ce-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="363ce-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="363ce-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="363ce-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="363ce-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="363ce-117">Page</span></span><br/>                                         |
| <span data-ttu-id="363ce-118">Note</span><span class="sxs-lookup"><span data-stu-id="363ce-118">Notes</span></span> <br/>          | <span data-ttu-id="363ce-119">Collegato all'elemento PageScaling, opzione Personalizzata</span><span class="sxs-lookup"><span data-stu-id="363ce-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="363ce-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="363ce-120">Structure Content</span></span>

<span data-ttu-id="363ce-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="363ce-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="363ce-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="363ce-122">Structure Properties</span></span>

<span data-ttu-id="363ce-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="363ce-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="363ce-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="363ce-124">Property</span></span>                | <span data-ttu-id="363ce-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="363ce-125">xsi:type</span></span>           | <span data-ttu-id="363ce-126">Valore</span><span class="sxs-lookup"><span data-stu-id="363ce-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="363ce-127">DataType</span><span class="sxs-lookup"><span data-stu-id="363ce-127">DataType</span></span><br/>     | <span data-ttu-id="363ce-128">string</span><span class="sxs-lookup"><span data-stu-id="363ce-128">string</span></span><br/>  | <span data-ttu-id="363ce-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="363ce-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="363ce-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="363ce-130">DefaultValue</span></span><br/> | <span data-ttu-id="363ce-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="363ce-131">integer</span></span><br/> | <span data-ttu-id="363ce-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="363ce-132">undefined</span></span><br/>       |
| <span data-ttu-id="363ce-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="363ce-133">MaxValue</span></span><br/>     | <span data-ttu-id="363ce-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="363ce-134">integer</span></span><br/> | <span data-ttu-id="363ce-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="363ce-135">undefined</span></span><br/>       |
| <span data-ttu-id="363ce-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="363ce-136">MinValue</span></span><br/>     | <span data-ttu-id="363ce-137">integer</span><span class="sxs-lookup"><span data-stu-id="363ce-137">integer</span></span><br/> | <span data-ttu-id="363ce-138">1</span><span class="sxs-lookup"><span data-stu-id="363ce-138">1</span></span><br/>               |
| <span data-ttu-id="363ce-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="363ce-139">Mandatory</span></span><br/>    | <span data-ttu-id="363ce-140">string</span><span class="sxs-lookup"><span data-stu-id="363ce-140">string</span></span><br/>  | <span data-ttu-id="363ce-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="363ce-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="363ce-142">Multipli</span><span class="sxs-lookup"><span data-stu-id="363ce-142">Multiple</span></span><br/>     | <span data-ttu-id="363ce-143">integer</span><span class="sxs-lookup"><span data-stu-id="363ce-143">integer</span></span><br/> | <span data-ttu-id="363ce-144">1</span><span class="sxs-lookup"><span data-stu-id="363ce-144">1</span></span><br/>               |
| <span data-ttu-id="363ce-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="363ce-145">UnitType</span></span><br/>     | <span data-ttu-id="363ce-146">string</span><span class="sxs-lookup"><span data-stu-id="363ce-146">string</span></span><br/>  | <span data-ttu-id="363ce-147">percent</span><span class="sxs-lookup"><span data-stu-id="363ce-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="363ce-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="363ce-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="363ce-149">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="363ce-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




