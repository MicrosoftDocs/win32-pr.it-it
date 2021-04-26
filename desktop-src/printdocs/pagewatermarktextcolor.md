---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996888"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="22f8a-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="22f8a-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="22f8a-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="22f8a-105">This topic is not current.</span></span> <span data-ttu-id="22f8a-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="22f8a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22f8a-107">Definisce il colore sRGB per il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="22f8a-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="22f8a-108">Il formato è ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="22f8a-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="22f8a-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22f8a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="22f8a-110">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="22f8a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="22f8a-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22f8a-111">Element Information</span></span>



| <span data-ttu-id="22f8a-112">Nome</span><span class="sxs-lookup"><span data-stu-id="22f8a-112">Name</span></span> | <span data-ttu-id="22f8a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="22f8a-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="22f8a-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="22f8a-114">Element Type</span></span> <br/>   | <span data-ttu-id="22f8a-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="22f8a-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="22f8a-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="22f8a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="22f8a-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="22f8a-117">Page</span></span><br/>                            |
| <span data-ttu-id="22f8a-118">Note</span><span class="sxs-lookup"><span data-stu-id="22f8a-118">Notes</span></span> <br/>          | <span data-ttu-id="22f8a-119">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="22f8a-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="22f8a-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="22f8a-120">Structure Content</span></span>

<span data-ttu-id="22f8a-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="22f8a-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="22f8a-122">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="22f8a-122">Structure Properties</span></span>

<span data-ttu-id="22f8a-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="22f8a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="22f8a-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22f8a-124">Property</span></span>                | <span data-ttu-id="22f8a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="22f8a-125">xsi:type</span></span>           | <span data-ttu-id="22f8a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="22f8a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="22f8a-127">DataType</span><span class="sxs-lookup"><span data-stu-id="22f8a-127">DataType</span></span><br/>     | <span data-ttu-id="22f8a-128">string</span><span class="sxs-lookup"><span data-stu-id="22f8a-128">string</span></span><br/>  | <span data-ttu-id="22f8a-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="22f8a-129">xs:string</span></span><br/>       |
| <span data-ttu-id="22f8a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="22f8a-130">DefaultValue</span></span><br/> | <span data-ttu-id="22f8a-131">numero intero</span><span class="sxs-lookup"><span data-stu-id="22f8a-131">integer</span></span><br/> | <span data-ttu-id="22f8a-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="22f8a-132">undefined</span></span><br/>       |
| <span data-ttu-id="22f8a-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="22f8a-133">MaxValue</span></span><br/>     | <span data-ttu-id="22f8a-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="22f8a-134">integer</span></span><br/> | <span data-ttu-id="22f8a-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="22f8a-135">undefined</span></span><br/>       |
| <span data-ttu-id="22f8a-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="22f8a-136">MinValue</span></span><br/>     | <span data-ttu-id="22f8a-137">numero intero</span><span class="sxs-lookup"><span data-stu-id="22f8a-137">integer</span></span><br/> | <span data-ttu-id="22f8a-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="22f8a-138">undefined</span></span><br/>       |
| <span data-ttu-id="22f8a-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="22f8a-139">Mandatory</span></span><br/>    | <span data-ttu-id="22f8a-140">string</span><span class="sxs-lookup"><span data-stu-id="22f8a-140">string</span></span><br/>  | <span data-ttu-id="22f8a-141">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="22f8a-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="22f8a-142">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="22f8a-142">UnitType</span></span><br/>     | <span data-ttu-id="22f8a-143">string</span><span class="sxs-lookup"><span data-stu-id="22f8a-143">string</span></span><br/>  | <span data-ttu-id="22f8a-144">Srgb</span><span class="sxs-lookup"><span data-stu-id="22f8a-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="22f8a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22f8a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22f8a-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="22f8a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




