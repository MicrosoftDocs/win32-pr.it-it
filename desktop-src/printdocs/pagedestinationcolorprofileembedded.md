---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47eaa810cd23462433c52292506999f90797d659
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321072"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="8c314-104">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="8c314-104">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="8c314-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8c314-105">This topic is not current.</span></span> <span data-ttu-id="8c314-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8c314-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8c314-107">Specifica il profilo colori di destinazione incorporato.</span><span class="sxs-lookup"><span data-stu-id="8c314-107">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="8c314-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8c314-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8c314-109">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="8c314-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8c314-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8c314-110">Element Information</span></span>



| <span data-ttu-id="8c314-111">Nome</span><span class="sxs-lookup"><span data-stu-id="8c314-111">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="8c314-112">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="8c314-112">Element Type</span></span> <br/>   | <span data-ttu-id="8c314-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8c314-113">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="8c314-114">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="8c314-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8c314-115">Pagina</span><span class="sxs-lookup"><span data-stu-id="8c314-115">Page</span></span><br/>                                          |
| <span data-ttu-id="8c314-116">Note</span><span class="sxs-lookup"><span data-stu-id="8c314-116">Notes</span></span> <br/>          | <span data-ttu-id="8c314-117">Collegato a elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="8c314-117">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8c314-118">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="8c314-118">Structure Content</span></span>

<span data-ttu-id="8c314-119">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="8c314-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="8c314-120">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="8c314-120">Structure Properties</span></span>

<span data-ttu-id="8c314-121">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="8c314-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8c314-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c314-122">Property</span></span>                | <span data-ttu-id="8c314-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8c314-123">xsi:type</span></span>           | <span data-ttu-id="8c314-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8c314-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8c314-125">DataType</span><span class="sxs-lookup"><span data-stu-id="8c314-125">DataType</span></span><br/>     | <span data-ttu-id="8c314-126">string</span><span class="sxs-lookup"><span data-stu-id="8c314-126">string</span></span><br/>  | <span data-ttu-id="8c314-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="8c314-127">xs:string</span></span><br/>       |
| <span data-ttu-id="8c314-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8c314-128">DefaultValue</span></span><br/> | <span data-ttu-id="8c314-129">string</span><span class="sxs-lookup"><span data-stu-id="8c314-129">string</span></span><br/>  | <span data-ttu-id="8c314-130">Non definito</span><span class="sxs-lookup"><span data-stu-id="8c314-130">undefined</span></span><br/>       |
| <span data-ttu-id="8c314-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="8c314-131">MaxLength</span></span><br/>    | <span data-ttu-id="8c314-132">numero intero</span><span class="sxs-lookup"><span data-stu-id="8c314-132">integer</span></span><br/> | <span data-ttu-id="8c314-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="8c314-133">undefined</span></span><br/>       |
| <span data-ttu-id="8c314-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="8c314-134">MinLength</span></span><br/>    | <span data-ttu-id="8c314-135">integer</span><span class="sxs-lookup"><span data-stu-id="8c314-135">integer</span></span><br/> | <span data-ttu-id="8c314-136">1</span><span class="sxs-lookup"><span data-stu-id="8c314-136">1</span></span><br/>               |
| <span data-ttu-id="8c314-137">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="8c314-137">Mandatory</span></span><br/>    | <span data-ttu-id="8c314-138">string</span><span class="sxs-lookup"><span data-stu-id="8c314-138">string</span></span><br/>  | <span data-ttu-id="8c314-139">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="8c314-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8c314-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="8c314-140">UnitType</span></span><br/>     | <span data-ttu-id="8c314-141">string</span><span class="sxs-lookup"><span data-stu-id="8c314-141">string</span></span><br/>  | <span data-ttu-id="8c314-142">caratteri</span><span class="sxs-lookup"><span data-stu-id="8c314-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="8c314-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c314-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c314-144">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="8c314-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




