---
description: Ottenere informazioni sul parametro PageWatermarkTextColor. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396016"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="c87a9-105">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="c87a9-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="c87a9-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c87a9-106">This topic is not current.</span></span> <span data-ttu-id="c87a9-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c87a9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c87a9-108">Definisce il colore sRGB per il testo della filigrana.</span><span class="sxs-lookup"><span data-stu-id="c87a9-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="c87a9-109">Il formato è ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="c87a9-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="c87a9-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c87a9-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c87a9-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c87a9-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c87a9-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c87a9-112">Element Information</span></span>



| <span data-ttu-id="c87a9-113">Nome</span><span class="sxs-lookup"><span data-stu-id="c87a9-113">Name</span></span> | <span data-ttu-id="c87a9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c87a9-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="c87a9-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c87a9-115">Element Type</span></span> <br/>   | <span data-ttu-id="c87a9-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c87a9-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="c87a9-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="c87a9-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c87a9-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="c87a9-118">Page</span></span><br/>                            |
| <span data-ttu-id="c87a9-119">Note</span><span class="sxs-lookup"><span data-stu-id="c87a9-119">Notes</span></span> <br/>          | <span data-ttu-id="c87a9-120">Collegato all'elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="c87a9-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c87a9-121">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="c87a9-121">Structure Content</span></span>

<span data-ttu-id="c87a9-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c87a9-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c87a9-123">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="c87a9-123">Structure Properties</span></span>

<span data-ttu-id="c87a9-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="c87a9-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c87a9-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c87a9-125">Property</span></span>                | <span data-ttu-id="c87a9-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c87a9-126">xsi:type</span></span>           | <span data-ttu-id="c87a9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c87a9-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c87a9-128">DataType</span><span class="sxs-lookup"><span data-stu-id="c87a9-128">DataType</span></span><br/>     | <span data-ttu-id="c87a9-129">string</span><span class="sxs-lookup"><span data-stu-id="c87a9-129">string</span></span><br/>  | <span data-ttu-id="c87a9-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="c87a9-130">xs:string</span></span><br/>       |
| <span data-ttu-id="c87a9-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c87a9-131">DefaultValue</span></span><br/> | <span data-ttu-id="c87a9-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="c87a9-132">integer</span></span><br/> | <span data-ttu-id="c87a9-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="c87a9-133">undefined</span></span><br/>       |
| <span data-ttu-id="c87a9-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c87a9-134">MaxValue</span></span><br/>     | <span data-ttu-id="c87a9-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="c87a9-135">integer</span></span><br/> | <span data-ttu-id="c87a9-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="c87a9-136">undefined</span></span><br/>       |
| <span data-ttu-id="c87a9-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="c87a9-137">MinValue</span></span><br/>     | <span data-ttu-id="c87a9-138">numero intero</span><span class="sxs-lookup"><span data-stu-id="c87a9-138">integer</span></span><br/> | <span data-ttu-id="c87a9-139">Non definito</span><span class="sxs-lookup"><span data-stu-id="c87a9-139">undefined</span></span><br/>       |
| <span data-ttu-id="c87a9-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c87a9-140">Mandatory</span></span><br/>    | <span data-ttu-id="c87a9-141">string</span><span class="sxs-lookup"><span data-stu-id="c87a9-141">string</span></span><br/>  | <span data-ttu-id="c87a9-142">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="c87a9-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c87a9-143">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="c87a9-143">UnitType</span></span><br/>     | <span data-ttu-id="c87a9-144">string</span><span class="sxs-lookup"><span data-stu-id="c87a9-144">string</span></span><br/>  | <span data-ttu-id="c87a9-145">Srgb</span><span class="sxs-lookup"><span data-stu-id="c87a9-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="c87a9-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c87a9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c87a9-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c87a9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




