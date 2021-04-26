---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305f67179343fa4acb2fa784113d63d5d2333b0b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993708"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="df0a8-104">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="df0a8-104">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="df0a8-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="df0a8-105">This topic is not current.</span></span> <span data-ttu-id="df0a8-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="df0a8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="df0a8-107">Specifica la direzione mediasizeheight della dimensione per l'opzione MediaSize personalizzata.</span><span class="sxs-lookup"><span data-stu-id="df0a8-107">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="df0a8-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="df0a8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="df0a8-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="df0a8-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="df0a8-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="df0a8-110">Element Information</span></span>



| <span data-ttu-id="df0a8-111">Nome</span><span class="sxs-lookup"><span data-stu-id="df0a8-111">Name</span></span> | <span data-ttu-id="df0a8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="df0a8-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df0a8-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="df0a8-113">Element Type</span></span> <br/>   | <span data-ttu-id="df0a8-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="df0a8-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="df0a8-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="df0a8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="df0a8-116">Pagina</span><span class="sxs-lookup"><span data-stu-id="df0a8-116">Page</span></span><br/>                                           |
| <span data-ttu-id="df0a8-117">Note</span><span class="sxs-lookup"><span data-stu-id="df0a8-117">Notes</span></span> <br/>          | <span data-ttu-id="df0a8-118">Collegato all'elemento PageMediaSize, opzione Custom</span><span class="sxs-lookup"><span data-stu-id="df0a8-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="df0a8-119">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="df0a8-119">Structure Content</span></span>

<span data-ttu-id="df0a8-120">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="df0a8-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="df0a8-121">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="df0a8-121">Structure Properties</span></span>

<span data-ttu-id="df0a8-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="df0a8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="df0a8-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df0a8-123">Property</span></span>                | <span data-ttu-id="df0a8-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="df0a8-124">xsi:type</span></span>           | <span data-ttu-id="df0a8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="df0a8-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="df0a8-126">DataType</span><span class="sxs-lookup"><span data-stu-id="df0a8-126">DataType</span></span><br/>     | <span data-ttu-id="df0a8-127">string</span><span class="sxs-lookup"><span data-stu-id="df0a8-127">string</span></span><br/>  | <span data-ttu-id="df0a8-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="df0a8-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="df0a8-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="df0a8-129">DefaultValue</span></span><br/> | <span data-ttu-id="df0a8-130">numero intero</span><span class="sxs-lookup"><span data-stu-id="df0a8-130">integer</span></span><br/> | <span data-ttu-id="df0a8-131">Non definito</span><span class="sxs-lookup"><span data-stu-id="df0a8-131">undefined</span></span><br/>       |
| <span data-ttu-id="df0a8-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="df0a8-132">MaxValue</span></span><br/>     | <span data-ttu-id="df0a8-133">numero intero</span><span class="sxs-lookup"><span data-stu-id="df0a8-133">integer</span></span><br/> | <span data-ttu-id="df0a8-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="df0a8-134">undefined</span></span><br/>       |
| <span data-ttu-id="df0a8-135">Minvalue</span><span class="sxs-lookup"><span data-stu-id="df0a8-135">MinValue</span></span><br/>     | <span data-ttu-id="df0a8-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="df0a8-136">integer</span></span><br/> | <span data-ttu-id="df0a8-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="df0a8-137">undefined</span></span><br/>       |
| <span data-ttu-id="df0a8-138">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="df0a8-138">Mandatory</span></span><br/>    | <span data-ttu-id="df0a8-139">string</span><span class="sxs-lookup"><span data-stu-id="df0a8-139">string</span></span><br/>  | <span data-ttu-id="df0a8-140">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="df0a8-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="df0a8-141">Più elementi</span><span class="sxs-lookup"><span data-stu-id="df0a8-141">Multiple</span></span><br/>     | <span data-ttu-id="df0a8-142">integer</span><span class="sxs-lookup"><span data-stu-id="df0a8-142">integer</span></span><br/> | <span data-ttu-id="df0a8-143">1</span><span class="sxs-lookup"><span data-stu-id="df0a8-143">1</span></span><br/>               |
| <span data-ttu-id="df0a8-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="df0a8-144">UnitType</span></span><br/>     | <span data-ttu-id="df0a8-145">string</span><span class="sxs-lookup"><span data-stu-id="df0a8-145">string</span></span><br/>  | <span data-ttu-id="df0a8-146">Micron</span><span class="sxs-lookup"><span data-stu-id="df0a8-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="df0a8-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df0a8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df0a8-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="df0a8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




