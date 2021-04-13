---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351786"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="9fc71-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="9fc71-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="9fc71-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9fc71-105">This topic is not current.</span></span> <span data-ttu-id="9fc71-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9fc71-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9fc71-107">Specifica la direzione MediaSizeWidth della dimensione per l'opzione MediaSize personalizzata.</span><span class="sxs-lookup"><span data-stu-id="9fc71-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="9fc71-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9fc71-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9fc71-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="9fc71-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9fc71-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9fc71-110">Element Information</span></span>



| <span data-ttu-id="9fc71-111">Nome</span><span class="sxs-lookup"><span data-stu-id="9fc71-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9fc71-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="9fc71-112">Element Type</span></span> <br/>   | <span data-ttu-id="9fc71-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9fc71-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="9fc71-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="9fc71-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9fc71-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="9fc71-115">Page</span></span><br/>                                           |
| <span data-ttu-id="9fc71-116">Note</span><span class="sxs-lookup"><span data-stu-id="9fc71-116">Notes</span></span> <br/>          | <span data-ttu-id="9fc71-117">Collegato a elemento PageMediaSize, opzione personalizzata</span><span class="sxs-lookup"><span data-stu-id="9fc71-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9fc71-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="9fc71-118">Structure Content</span></span>

<span data-ttu-id="9fc71-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="9fc71-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9fc71-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="9fc71-120">Structure Properties</span></span>

<span data-ttu-id="9fc71-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="9fc71-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9fc71-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fc71-122">Property</span></span>                | <span data-ttu-id="9fc71-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9fc71-123">xsi:type</span></span>           | <span data-ttu-id="9fc71-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9fc71-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9fc71-125">DataType</span><span class="sxs-lookup"><span data-stu-id="9fc71-125">DataType</span></span><br/>     | <span data-ttu-id="9fc71-126">string</span><span class="sxs-lookup"><span data-stu-id="9fc71-126">string</span></span><br/>  | <span data-ttu-id="9fc71-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9fc71-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="9fc71-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9fc71-128">DefaultValue</span></span><br/> | <span data-ttu-id="9fc71-129">numero intero</span><span class="sxs-lookup"><span data-stu-id="9fc71-129">integer</span></span><br/> | <span data-ttu-id="9fc71-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="9fc71-130">undefined</span></span><br/>       |
| <span data-ttu-id="9fc71-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9fc71-131">MaxValue</span></span><br/>     | <span data-ttu-id="9fc71-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="9fc71-132">integer</span></span><br/> | <span data-ttu-id="9fc71-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="9fc71-133">undefined</span></span><br/>       |
| <span data-ttu-id="9fc71-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="9fc71-134">MinValue</span></span><br/>     | <span data-ttu-id="9fc71-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="9fc71-135">integer</span></span><br/> | <span data-ttu-id="9fc71-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="9fc71-136">undefined</span></span><br/>       |
| <span data-ttu-id="9fc71-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9fc71-137">Mandatory</span></span><br/>    | <span data-ttu-id="9fc71-138">string</span><span class="sxs-lookup"><span data-stu-id="9fc71-138">string</span></span><br/>  | <span data-ttu-id="9fc71-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="9fc71-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9fc71-140">Più elementi</span><span class="sxs-lookup"><span data-stu-id="9fc71-140">Multiple</span></span><br/>     | <span data-ttu-id="9fc71-141">integer</span><span class="sxs-lookup"><span data-stu-id="9fc71-141">integer</span></span><br/> | <span data-ttu-id="9fc71-142">1</span><span class="sxs-lookup"><span data-stu-id="9fc71-142">1</span></span><br/>               |
| <span data-ttu-id="9fc71-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="9fc71-143">UnitType</span></span><br/>     | <span data-ttu-id="9fc71-144">string</span><span class="sxs-lookup"><span data-stu-id="9fc71-144">string</span></span><br/>  | <span data-ttu-id="9fc71-145">micron</span><span class="sxs-lookup"><span data-stu-id="9fc71-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="9fc71-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9fc71-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fc71-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9fc71-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




