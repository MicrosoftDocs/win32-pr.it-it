---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321071"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="2460c-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="2460c-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="2460c-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2460c-105">This topic is not current.</span></span> <span data-ttu-id="2460c-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2460c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2460c-107">Specifica un riferimento URI relativo a un profilo ICC contenuto in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2460c-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="2460c-108">L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="2460c-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="2460c-109">Si presuppone che tutti gli elementi che usano tale profilo si trovino già nello spazio dei colori del dispositivo appropriato e non verranno gestiti nel dispositivo o nel driver.</span><span class="sxs-lookup"><span data-stu-id="2460c-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="2460c-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2460c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2460c-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="2460c-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2460c-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2460c-112">Element Information</span></span>



| <span data-ttu-id="2460c-113">Nome</span><span class="sxs-lookup"><span data-stu-id="2460c-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="2460c-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="2460c-114">Element Type</span></span> <br/>   | <span data-ttu-id="2460c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2460c-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="2460c-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="2460c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2460c-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="2460c-117">Page</span></span><br/>                                          |
| <span data-ttu-id="2460c-118">Note</span><span class="sxs-lookup"><span data-stu-id="2460c-118">Notes</span></span> <br/>          | <span data-ttu-id="2460c-119">Collegato a elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="2460c-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2460c-120">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="2460c-120">Structure Content</span></span>

<span data-ttu-id="2460c-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="2460c-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="2460c-122">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="2460c-122">Structure Properties</span></span>

<span data-ttu-id="2460c-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="2460c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2460c-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2460c-124">Property</span></span>                | <span data-ttu-id="2460c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2460c-125">xsi:type</span></span>           | <span data-ttu-id="2460c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2460c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2460c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="2460c-127">DataType</span></span><br/>     | <span data-ttu-id="2460c-128">string</span><span class="sxs-lookup"><span data-stu-id="2460c-128">string</span></span><br/>  | <span data-ttu-id="2460c-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="2460c-129">xs:string</span></span><br/>       |
| <span data-ttu-id="2460c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2460c-130">DefaultValue</span></span><br/> | <span data-ttu-id="2460c-131">string</span><span class="sxs-lookup"><span data-stu-id="2460c-131">string</span></span><br/>  | <span data-ttu-id="2460c-132">Non definito</span><span class="sxs-lookup"><span data-stu-id="2460c-132">undefined</span></span><br/>       |
| <span data-ttu-id="2460c-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="2460c-133">MaxLength</span></span><br/>    | <span data-ttu-id="2460c-134">numero intero</span><span class="sxs-lookup"><span data-stu-id="2460c-134">integer</span></span><br/> | <span data-ttu-id="2460c-135">Non definito</span><span class="sxs-lookup"><span data-stu-id="2460c-135">undefined</span></span><br/>       |
| <span data-ttu-id="2460c-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="2460c-136">MinLength</span></span><br/>    | <span data-ttu-id="2460c-137">integer</span><span class="sxs-lookup"><span data-stu-id="2460c-137">integer</span></span><br/> | <span data-ttu-id="2460c-138">1</span><span class="sxs-lookup"><span data-stu-id="2460c-138">1</span></span><br/>               |
| <span data-ttu-id="2460c-139">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="2460c-139">Mandatory</span></span><br/>    | <span data-ttu-id="2460c-140">string</span><span class="sxs-lookup"><span data-stu-id="2460c-140">string</span></span><br/>  | <span data-ttu-id="2460c-141">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="2460c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2460c-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="2460c-142">UnitType</span></span><br/>     | <span data-ttu-id="2460c-143">string</span><span class="sxs-lookup"><span data-stu-id="2460c-143">string</span></span><br/>  | <span data-ttu-id="2460c-144">caratteri</span><span class="sxs-lookup"><span data-stu-id="2460c-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="2460c-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2460c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2460c-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="2460c-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




