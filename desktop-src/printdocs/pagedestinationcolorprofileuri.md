---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996098"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="fd3f5-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="fd3f5-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="fd3f5-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-105">This topic is not current.</span></span> <span data-ttu-id="fd3f5-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fd3f5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fd3f5-107">Specifica un riferimento URI relativo a un profilo ICC contenuto in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="fd3f5-108">L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="fd3f5-109">Si presuppone che tutti gli elementi che usano tale profilo siano già nello spazio colori del dispositivo appropriato e non saranno gestiti a colori nel driver o nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="fd3f5-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fd3f5-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fd3f5-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="fd3f5-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fd3f5-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fd3f5-112">Element Information</span></span>



| <span data-ttu-id="fd3f5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="fd3f5-113">Name</span></span> | <span data-ttu-id="fd3f5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fd3f5-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="fd3f5-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="fd3f5-115">Element Type</span></span> <br/>   | <span data-ttu-id="fd3f5-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fd3f5-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="fd3f5-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="fd3f5-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fd3f5-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="fd3f5-118">Page</span></span><br/>                                          |
| <span data-ttu-id="fd3f5-119">Note</span><span class="sxs-lookup"><span data-stu-id="fd3f5-119">Notes</span></span> <br/>          | <span data-ttu-id="fd3f5-120">Collegato all'elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="fd3f5-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fd3f5-121">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="fd3f5-121">Structure Content</span></span>

<span data-ttu-id="fd3f5-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="fd3f5-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fd3f5-123">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="fd3f5-123">Structure Properties</span></span>

<span data-ttu-id="fd3f5-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fd3f5-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd3f5-125">Property</span></span>                | <span data-ttu-id="fd3f5-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fd3f5-126">xsi:type</span></span>           | <span data-ttu-id="fd3f5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fd3f5-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fd3f5-128">DataType</span><span class="sxs-lookup"><span data-stu-id="fd3f5-128">DataType</span></span><br/>     | <span data-ttu-id="fd3f5-129">string</span><span class="sxs-lookup"><span data-stu-id="fd3f5-129">string</span></span><br/>  | <span data-ttu-id="fd3f5-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd3f5-130">xs:string</span></span><br/>       |
| <span data-ttu-id="fd3f5-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fd3f5-131">DefaultValue</span></span><br/> | <span data-ttu-id="fd3f5-132">string</span><span class="sxs-lookup"><span data-stu-id="fd3f5-132">string</span></span><br/>  | <span data-ttu-id="fd3f5-133">Non definito</span><span class="sxs-lookup"><span data-stu-id="fd3f5-133">undefined</span></span><br/>       |
| <span data-ttu-id="fd3f5-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fd3f5-134">MaxLength</span></span><br/>    | <span data-ttu-id="fd3f5-135">numero intero</span><span class="sxs-lookup"><span data-stu-id="fd3f5-135">integer</span></span><br/> | <span data-ttu-id="fd3f5-136">Non definito</span><span class="sxs-lookup"><span data-stu-id="fd3f5-136">undefined</span></span><br/>       |
| <span data-ttu-id="fd3f5-137">Minlength</span><span class="sxs-lookup"><span data-stu-id="fd3f5-137">MinLength</span></span><br/>    | <span data-ttu-id="fd3f5-138">integer</span><span class="sxs-lookup"><span data-stu-id="fd3f5-138">integer</span></span><br/> | <span data-ttu-id="fd3f5-139">1</span><span class="sxs-lookup"><span data-stu-id="fd3f5-139">1</span></span><br/>               |
| <span data-ttu-id="fd3f5-140">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="fd3f5-140">Mandatory</span></span><br/>    | <span data-ttu-id="fd3f5-141">string</span><span class="sxs-lookup"><span data-stu-id="fd3f5-141">string</span></span><br/>  | <span data-ttu-id="fd3f5-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="fd3f5-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fd3f5-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="fd3f5-143">UnitType</span></span><br/>     | <span data-ttu-id="fd3f5-144">string</span><span class="sxs-lookup"><span data-stu-id="fd3f5-144">string</span></span><br/>  | <span data-ttu-id="fd3f5-145">caratteri</span><span class="sxs-lookup"><span data-stu-id="fd3f5-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fd3f5-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd3f5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd3f5-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="fd3f5-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




