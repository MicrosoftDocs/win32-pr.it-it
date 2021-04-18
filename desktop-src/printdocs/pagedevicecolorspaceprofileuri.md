---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4536251150851ad02abf41ca26ffaa36699281db
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321017"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="217eb-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="217eb-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="217eb-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="217eb-105">This topic is not current.</span></span> <span data-ttu-id="217eb-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="217eb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="217eb-107">Specifica un URI relativo alla radice del pacchetto in un profilo ICC contenuto in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="217eb-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="217eb-108">L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="217eb-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="217eb-109">Si presuppone che tutti gli elementi che usano tale profilo si trovino già nello spazio dei colori del dispositivo appropriato e non verranno gestiti nel dispositivo o nel driver.</span><span class="sxs-lookup"><span data-stu-id="217eb-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="217eb-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="217eb-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="217eb-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="217eb-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="217eb-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="217eb-112">Element Information</span></span>



| <span data-ttu-id="217eb-113">Nome</span><span class="sxs-lookup"><span data-stu-id="217eb-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217eb-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="217eb-114">Element Type</span></span> <br/>   | <span data-ttu-id="217eb-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="217eb-115">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="217eb-116">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="217eb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="217eb-117">Pagina</span><span class="sxs-lookup"><span data-stu-id="217eb-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="217eb-118">Note</span><span class="sxs-lookup"><span data-stu-id="217eb-118">Notes</span></span> <br/>          | <span data-ttu-id="217eb-119">Questo vale solo per i documenti XPS e non deve essere utilizzato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="217eb-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="217eb-120">I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="217eb-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="217eb-121">Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte.</span><span class="sxs-lookup"><span data-stu-id="217eb-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="217eb-122">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="217eb-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="217eb-123">Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="217eb-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="217eb-124">Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="217eb-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="217eb-125">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="217eb-125">Structure Content</span></span>

<span data-ttu-id="217eb-126">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="217eb-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="217eb-127">Proprietà struttura</span><span class="sxs-lookup"><span data-stu-id="217eb-127">Structure Properties</span></span>

<span data-ttu-id="217eb-128">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="217eb-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="217eb-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="217eb-129">Property</span></span>                | <span data-ttu-id="217eb-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="217eb-130">xsi:type</span></span>           | <span data-ttu-id="217eb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="217eb-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="217eb-132">DataType</span><span class="sxs-lookup"><span data-stu-id="217eb-132">DataType</span></span><br/>     | <span data-ttu-id="217eb-133">string</span><span class="sxs-lookup"><span data-stu-id="217eb-133">string</span></span><br/>  | <span data-ttu-id="217eb-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="217eb-134">xs:string</span></span><br/>       |
| <span data-ttu-id="217eb-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="217eb-135">DefaultValue</span></span><br/> | <span data-ttu-id="217eb-136">string</span><span class="sxs-lookup"><span data-stu-id="217eb-136">string</span></span><br/>  | <span data-ttu-id="217eb-137">Non definito</span><span class="sxs-lookup"><span data-stu-id="217eb-137">undefined</span></span><br/>       |
| <span data-ttu-id="217eb-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="217eb-138">MaxLength</span></span><br/>    | <span data-ttu-id="217eb-139">numero intero</span><span class="sxs-lookup"><span data-stu-id="217eb-139">integer</span></span><br/> | <span data-ttu-id="217eb-140">Non definito</span><span class="sxs-lookup"><span data-stu-id="217eb-140">undefined</span></span><br/>       |
| <span data-ttu-id="217eb-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="217eb-141">MinLength</span></span><br/>    | <span data-ttu-id="217eb-142">integer</span><span class="sxs-lookup"><span data-stu-id="217eb-142">integer</span></span><br/> | <span data-ttu-id="217eb-143">1</span><span class="sxs-lookup"><span data-stu-id="217eb-143">1</span></span><br/>               |
| <span data-ttu-id="217eb-144">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="217eb-144">Mandatory</span></span><br/>    | <span data-ttu-id="217eb-145">string</span><span class="sxs-lookup"><span data-stu-id="217eb-145">string</span></span><br/>  | <span data-ttu-id="217eb-146">PSK: condizionale</span><span class="sxs-lookup"><span data-stu-id="217eb-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="217eb-147">UnitType</span><span class="sxs-lookup"><span data-stu-id="217eb-147">UnitType</span></span><br/>     | <span data-ttu-id="217eb-148">string</span><span class="sxs-lookup"><span data-stu-id="217eb-148">string</span></span><br/>  | <span data-ttu-id="217eb-149">caratteri</span><span class="sxs-lookup"><span data-stu-id="217eb-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="217eb-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="217eb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217eb-151">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="217eb-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




