---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a1b4cf607ddf880311659e562647ba583a2951
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995678"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="965b7-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="965b7-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="965b7-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="965b7-105">This topic is not current.</span></span> <span data-ttu-id="965b7-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="965b7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="965b7-107">Specifica un URI relativo alla radice del pacchetto a un profilo ICC contenuto in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="965b7-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="965b7-108">L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="965b7-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="965b7-109">Si presuppone che tutti gli elementi che usano tale profilo siano già nello spazio colori del dispositivo appropriato e non saranno gestiti a colori nel driver o nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="965b7-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="965b7-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="965b7-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="965b7-111">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="965b7-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="965b7-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="965b7-112">Element Information</span></span>



| <span data-ttu-id="965b7-113">Nome</span><span class="sxs-lookup"><span data-stu-id="965b7-113">Name</span></span> | <span data-ttu-id="965b7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="965b7-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965b7-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="965b7-115">Element Type</span></span> <br/>   | <span data-ttu-id="965b7-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="965b7-116">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="965b7-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="965b7-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="965b7-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="965b7-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="965b7-119">Note</span><span class="sxs-lookup"><span data-stu-id="965b7-119">Notes</span></span> <br/>          | <span data-ttu-id="965b7-120">Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.</span><span class="sxs-lookup"><span data-stu-id="965b7-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="965b7-121">I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante.</span><span class="sxs-lookup"><span data-stu-id="965b7-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="965b7-122">Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte.</span><span class="sxs-lookup"><span data-stu-id="965b7-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="965b7-123">Queste impostazioni sono specifiche di XPS.</span><span class="sxs-lookup"><span data-stu-id="965b7-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="965b7-124">Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL.</span><span class="sxs-lookup"><span data-stu-id="965b7-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="965b7-125">Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="965b7-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="965b7-126">Contenuto della struttura</span><span class="sxs-lookup"><span data-stu-id="965b7-126">Structure Content</span></span>

<span data-ttu-id="965b7-127">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="965b7-127">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="965b7-128">Proprietà della struttura</span><span class="sxs-lookup"><span data-stu-id="965b7-128">Structure Properties</span></span>

<span data-ttu-id="965b7-129">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="965b7-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="965b7-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="965b7-130">Property</span></span>                | <span data-ttu-id="965b7-131">xsi:type</span><span class="sxs-lookup"><span data-stu-id="965b7-131">xsi:type</span></span>           | <span data-ttu-id="965b7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="965b7-132">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="965b7-133">DataType</span><span class="sxs-lookup"><span data-stu-id="965b7-133">DataType</span></span><br/>     | <span data-ttu-id="965b7-134">string</span><span class="sxs-lookup"><span data-stu-id="965b7-134">string</span></span><br/>  | <span data-ttu-id="965b7-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="965b7-135">xs:string</span></span><br/>       |
| <span data-ttu-id="965b7-136">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="965b7-136">DefaultValue</span></span><br/> | <span data-ttu-id="965b7-137">string</span><span class="sxs-lookup"><span data-stu-id="965b7-137">string</span></span><br/>  | <span data-ttu-id="965b7-138">Non definito</span><span class="sxs-lookup"><span data-stu-id="965b7-138">undefined</span></span><br/>       |
| <span data-ttu-id="965b7-139">MaxLength</span><span class="sxs-lookup"><span data-stu-id="965b7-139">MaxLength</span></span><br/>    | <span data-ttu-id="965b7-140">numero intero</span><span class="sxs-lookup"><span data-stu-id="965b7-140">integer</span></span><br/> | <span data-ttu-id="965b7-141">Non definito</span><span class="sxs-lookup"><span data-stu-id="965b7-141">undefined</span></span><br/>       |
| <span data-ttu-id="965b7-142">Minlength</span><span class="sxs-lookup"><span data-stu-id="965b7-142">MinLength</span></span><br/>    | <span data-ttu-id="965b7-143">integer</span><span class="sxs-lookup"><span data-stu-id="965b7-143">integer</span></span><br/> | <span data-ttu-id="965b7-144">1</span><span class="sxs-lookup"><span data-stu-id="965b7-144">1</span></span><br/>               |
| <span data-ttu-id="965b7-145">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="965b7-145">Mandatory</span></span><br/>    | <span data-ttu-id="965b7-146">string</span><span class="sxs-lookup"><span data-stu-id="965b7-146">string</span></span><br/>  | <span data-ttu-id="965b7-147">psk:Condizionale</span><span class="sxs-lookup"><span data-stu-id="965b7-147">psk:Conditional</span></span><br/> |
| <span data-ttu-id="965b7-148">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="965b7-148">UnitType</span></span><br/>     | <span data-ttu-id="965b7-149">string</span><span class="sxs-lookup"><span data-stu-id="965b7-149">string</span></span><br/>  | <span data-ttu-id="965b7-150">caratteri</span><span class="sxs-lookup"><span data-stu-id="965b7-150">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="965b7-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="965b7-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="965b7-152">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="965b7-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




