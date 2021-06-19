---
description: Informazioni sul parametro PageDeviceColorSpaceProfileURI. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396646"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="31498-105">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="31498-105">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="31498-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="31498-106">This topic is not current.</span></span> <span data-ttu-id="31498-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="31498-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="31498-108">Specifica un URI relativo alla radice del pacchetto a un profilo ICC contenuto in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="31498-108">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="31498-109">L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="31498-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="31498-110">Si presuppone che tutti gli elementi che usano tale profilo siano già nello spazio colori del dispositivo appropriato e non saranno gestiti a colori nel driver o nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31498-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="31498-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="31498-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="31498-112">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="31498-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="31498-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="31498-113">Element Information</span></span>



| <span data-ttu-id="31498-114">Nome</span><span class="sxs-lookup"><span data-stu-id="31498-114">Name</span></span> | <span data-ttu-id="31498-115">Valore</span><span class="sxs-lookup"><span data-stu-id="31498-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31498-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="31498-116">Element Type</span></span> <br/>   | <span data-ttu-id="31498-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="31498-117">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="31498-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="31498-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="31498-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="31498-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="31498-120">Note</span><span class="sxs-lookup"><span data-stu-id="31498-120">Notes</span></span> <br/>          | <span data-ttu-id="31498-121">Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="31498-121">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="31498-122">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="31498-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="31498-123">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="31498-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="31498-124">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="31498-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="31498-125">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="31498-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="31498-126">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31498-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="31498-127">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="31498-127">Structure Content</span></span>

<span data-ttu-id="31498-128">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="31498-128">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="31498-129">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="31498-129">Structure Properties</span></span>

<span data-ttu-id="31498-130">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="31498-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="31498-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31498-131">Property</span></span>                | <span data-ttu-id="31498-132">xsi:type</span><span class="sxs-lookup"><span data-stu-id="31498-132">xsi:type</span></span>           | <span data-ttu-id="31498-133">Valore</span><span class="sxs-lookup"><span data-stu-id="31498-133">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="31498-134">DataType</span><span class="sxs-lookup"><span data-stu-id="31498-134">DataType</span></span><br/>     | <span data-ttu-id="31498-135">string</span><span class="sxs-lookup"><span data-stu-id="31498-135">string</span></span><br/>  | <span data-ttu-id="31498-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="31498-136">xs:string</span></span><br/>       |
| <span data-ttu-id="31498-137">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="31498-137">DefaultValue</span></span><br/> | <span data-ttu-id="31498-138">string</span><span class="sxs-lookup"><span data-stu-id="31498-138">string</span></span><br/>  | <span data-ttu-id="31498-139">Non definito</span><span class="sxs-lookup"><span data-stu-id="31498-139">undefined</span></span><br/>       |
| <span data-ttu-id="31498-140">MaxLength</span><span class="sxs-lookup"><span data-stu-id="31498-140">MaxLength</span></span><br/>    | <span data-ttu-id="31498-141">numero intero</span><span class="sxs-lookup"><span data-stu-id="31498-141">integer</span></span><br/> | <span data-ttu-id="31498-142">Non definito</span><span class="sxs-lookup"><span data-stu-id="31498-142">undefined</span></span><br/>       |
| <span data-ttu-id="31498-143">Minlength</span><span class="sxs-lookup"><span data-stu-id="31498-143">MinLength</span></span><br/>    | <span data-ttu-id="31498-144">integer</span><span class="sxs-lookup"><span data-stu-id="31498-144">integer</span></span><br/> | <span data-ttu-id="31498-145">1</span><span class="sxs-lookup"><span data-stu-id="31498-145">1</span></span><br/>               |
| <span data-ttu-id="31498-146">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="31498-146">Mandatory</span></span><br/>    | <span data-ttu-id="31498-147">string</span><span class="sxs-lookup"><span data-stu-id="31498-147">string</span></span><br/>  | <span data-ttu-id="31498-148">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="31498-148">psk:Conditional</span></span><br/> |
| <span data-ttu-id="31498-149">UnitType</span><span class="sxs-lookup"><span data-stu-id="31498-149">UnitType</span></span><br/>     | <span data-ttu-id="31498-150">string</span><span class="sxs-lookup"><span data-stu-id="31498-150">string</span></span><br/>  | <span data-ttu-id="31498-151">caratteri</span><span class="sxs-lookup"><span data-stu-id="31498-151">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="31498-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31498-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31498-153">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="31498-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




