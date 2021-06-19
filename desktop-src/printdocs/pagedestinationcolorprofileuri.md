---
description: Informazioni sul parametro PageDestinationColorProfileURI. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396676"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="2b152-105">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="2b152-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="2b152-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="2b152-106">This topic is not current.</span></span> <span data-ttu-id="2b152-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2b152-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2b152-108">Specifica un riferimento URI relativo a un profilo ICC contenuto in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2b152-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="2b152-109">L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="2b152-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="2b152-110">Si presuppone che tutti gli elementi che usano tale profilo siano già nello spazio colore del dispositivo appropriato e non verranno gestiti dal colore nel driver o nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b152-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="2b152-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2b152-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2b152-112">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="2b152-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2b152-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="2b152-113">Element Information</span></span>



| <span data-ttu-id="2b152-114">Nome</span><span class="sxs-lookup"><span data-stu-id="2b152-114">Name</span></span> | <span data-ttu-id="2b152-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2b152-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="2b152-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="2b152-116">Element Type</span></span> <br/>   | <span data-ttu-id="2b152-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2b152-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="2b152-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="2b152-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2b152-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="2b152-119">Page</span></span><br/>                                          |
| <span data-ttu-id="2b152-120">Note</span><span class="sxs-lookup"><span data-stu-id="2b152-120">Notes</span></span> <br/>          | <span data-ttu-id="2b152-121">Collegato all'elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="2b152-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2b152-122">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="2b152-122">Structure Content</span></span>

<span data-ttu-id="2b152-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="2b152-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2b152-124">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="2b152-124">Structure Properties</span></span>

<span data-ttu-id="2b152-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="2b152-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2b152-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b152-126">Property</span></span>                | <span data-ttu-id="2b152-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2b152-127">xsi:type</span></span>           | <span data-ttu-id="2b152-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2b152-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2b152-129">DataType</span><span class="sxs-lookup"><span data-stu-id="2b152-129">DataType</span></span><br/>     | <span data-ttu-id="2b152-130">string</span><span class="sxs-lookup"><span data-stu-id="2b152-130">string</span></span><br/>  | <span data-ttu-id="2b152-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b152-131">xs:string</span></span><br/>       |
| <span data-ttu-id="2b152-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2b152-132">DefaultValue</span></span><br/> | <span data-ttu-id="2b152-133">string</span><span class="sxs-lookup"><span data-stu-id="2b152-133">string</span></span><br/>  | <span data-ttu-id="2b152-134">Non definito</span><span class="sxs-lookup"><span data-stu-id="2b152-134">undefined</span></span><br/>       |
| <span data-ttu-id="2b152-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="2b152-135">MaxLength</span></span><br/>    | <span data-ttu-id="2b152-136">numero intero</span><span class="sxs-lookup"><span data-stu-id="2b152-136">integer</span></span><br/> | <span data-ttu-id="2b152-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="2b152-137">undefined</span></span><br/>       |
| <span data-ttu-id="2b152-138">Minlength</span><span class="sxs-lookup"><span data-stu-id="2b152-138">MinLength</span></span><br/>    | <span data-ttu-id="2b152-139">integer</span><span class="sxs-lookup"><span data-stu-id="2b152-139">integer</span></span><br/> | <span data-ttu-id="2b152-140">1</span><span class="sxs-lookup"><span data-stu-id="2b152-140">1</span></span><br/>               |
| <span data-ttu-id="2b152-141">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="2b152-141">Mandatory</span></span><br/>    | <span data-ttu-id="2b152-142">string</span><span class="sxs-lookup"><span data-stu-id="2b152-142">string</span></span><br/>  | <span data-ttu-id="2b152-143">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="2b152-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2b152-144">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="2b152-144">UnitType</span></span><br/>     | <span data-ttu-id="2b152-145">string</span><span class="sxs-lookup"><span data-stu-id="2b152-145">string</span></span><br/>  | <span data-ttu-id="2b152-146">caratteri</span><span class="sxs-lookup"><span data-stu-id="2b152-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="2b152-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b152-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b152-148">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="2b152-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




