---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50df088fd25a69ee566e1406d3f1b833aa6131f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997568"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="5f8f7-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="5f8f7-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="5f8f7-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="5f8f7-105">This topic is not current.</span></span> <span data-ttu-id="5f8f7-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5f8f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f8f7-107">Specifica la direzione mediasizewidth della dimensione per l'opzione MediaSize personalizzata.</span><span class="sxs-lookup"><span data-stu-id="5f8f7-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="5f8f7-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5f8f7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f8f7-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5f8f7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5f8f7-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5f8f7-110">Element Information</span></span>



| <span data-ttu-id="5f8f7-111">Nome</span><span class="sxs-lookup"><span data-stu-id="5f8f7-111">Name</span></span> | <span data-ttu-id="5f8f7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5f8f7-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5f8f7-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="5f8f7-113">Element Type</span></span> <br/>   | <span data-ttu-id="5f8f7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5f8f7-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="5f8f7-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="5f8f7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f8f7-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="5f8f7-116">Page</span></span><br/>                                           |
| <span data-ttu-id="5f8f7-117">Note</span><span class="sxs-lookup"><span data-stu-id="5f8f7-117">Notes</span></span> <br/>          | <span data-ttu-id="5f8f7-118">Collegato all'elemento PageMediaSize, opzione Custom</span><span class="sxs-lookup"><span data-stu-id="5f8f7-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5f8f7-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="5f8f7-119">Structure Content</span></span>

<span data-ttu-id="5f8f7-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="5f8f7-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="5f8f7-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="5f8f7-121">Structure Properties</span></span>

<span data-ttu-id="5f8f7-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="5f8f7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f8f7-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5f8f7-123">Property</span></span>                | <span data-ttu-id="5f8f7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5f8f7-124">xsi:type</span></span>           | <span data-ttu-id="5f8f7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5f8f7-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5f8f7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5f8f7-126">DataType</span></span><br/>     | <span data-ttu-id="5f8f7-127">string</span><span class="sxs-lookup"><span data-stu-id="5f8f7-127">string</span></span><br/>  | <span data-ttu-id="5f8f7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f8f7-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5f8f7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5f8f7-129">DefaultValue</span></span><br/> | <span data-ttu-id="5f8f7-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="5f8f7-130">integer</span></span><br/> | <span data-ttu-id="5f8f7-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="5f8f7-131">undefined</span></span><br/>       |
| <span data-ttu-id="5f8f7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5f8f7-132">MaxValue</span></span><br/>     | <span data-ttu-id="5f8f7-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="5f8f7-133">integer</span></span><br/> | <span data-ttu-id="5f8f7-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="5f8f7-134">undefined</span></span><br/>       |
| <span data-ttu-id="5f8f7-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="5f8f7-135">MinValue</span></span><br/>     | <span data-ttu-id="5f8f7-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="5f8f7-136">integer</span></span><br/> | <span data-ttu-id="5f8f7-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="5f8f7-137">undefined</span></span><br/>       |
| <span data-ttu-id="5f8f7-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="5f8f7-138">Mandatory</span></span><br/>    | <span data-ttu-id="5f8f7-139">string</span><span class="sxs-lookup"><span data-stu-id="5f8f7-139">string</span></span><br/>  | <span data-ttu-id="5f8f7-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="5f8f7-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5f8f7-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="5f8f7-141">Multiple</span></span><br/>     | <span data-ttu-id="5f8f7-142">integer</span><span class="sxs-lookup"><span data-stu-id="5f8f7-142">integer</span></span><br/> | <span data-ttu-id="5f8f7-143">1</span><span class="sxs-lookup"><span data-stu-id="5f8f7-143">1</span></span><br/>               |
| <span data-ttu-id="5f8f7-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="5f8f7-144">UnitType</span></span><br/>     | <span data-ttu-id="5f8f7-145">string</span><span class="sxs-lookup"><span data-stu-id="5f8f7-145">string</span></span><br/>  | <span data-ttu-id="5f8f7-146">Micron</span><span class="sxs-lookup"><span data-stu-id="5f8f7-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5f8f7-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f8f7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f8f7-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="5f8f7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




