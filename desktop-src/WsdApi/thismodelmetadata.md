---
description: Definisce il produttore e i metadati del modello per il dispositivo da implementare. Questo elemento viene usato solo per le implementazioni dei dispositivi (host).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884245"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="0a89e-104">elemento thisModelMetadata</span><span class="sxs-lookup"><span data-stu-id="0a89e-104">thisModelMetadata element</span></span>

<span data-ttu-id="0a89e-105">Definisce il produttore e i metadati del modello per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="0a89e-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="0a89e-106">Questo elemento viene usato solo per le implementazioni dei dispositivi (host).</span><span class="sxs-lookup"><span data-stu-id="0a89e-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="0a89e-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0a89e-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="0a89e-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="0a89e-108">Attributes</span></span>

<span data-ttu-id="0a89e-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0a89e-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0a89e-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0a89e-110">Child elements</span></span>



| <span data-ttu-id="0a89e-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a89e-111">Element</span></span>                                                     | <span data-ttu-id="0a89e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a89e-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a89e-113">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="0a89e-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="0a89e-114">Nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="0a89e-114">Name of the manufacturer.</span></span> <span data-ttu-id="0a89e-115">Almeno un [**produttore**](manufacturer.md) o [**manufacturerLS**](manufacturerls.md) deve essere presente nei metadati.</span><span class="sxs-lookup"><span data-stu-id="0a89e-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="0a89e-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="0a89e-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="0a89e-117">Versione localizzata del nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="0a89e-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="0a89e-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="0a89e-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="0a89e-119">Indirizzo URL produttore.</span><span class="sxs-lookup"><span data-stu-id="0a89e-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="0a89e-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="0a89e-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="0a89e-121">Nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-121">Name of the device.</span></span> <span data-ttu-id="0a89e-122">È necessario che nei metadati sia presente almeno un oggetto [**ModelName**](modelname.md) o [**modelNameLS**](modelnamels.md) .</span><span class="sxs-lookup"><span data-stu-id="0a89e-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="0a89e-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="0a89e-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="0a89e-124">Versione localizzata del nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="0a89e-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="0a89e-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="0a89e-126">Numero del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="0a89e-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="0a89e-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="0a89e-128">Indirizzo URL per il modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="0a89e-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="0a89e-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="0a89e-130">Categoria PnP-X a cui appartiene il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="0a89e-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="0a89e-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="0a89e-132">Indirizzo URL dei dati di presentazione del modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="0a89e-133">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0a89e-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="0a89e-134">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0a89e-134">Parent elements</span></span>



| <span data-ttu-id="0a89e-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a89e-135">Element</span></span>                                     | <span data-ttu-id="0a89e-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a89e-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a89e-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="0a89e-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0a89e-138">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0a89e-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0a89e-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a89e-139">Remarks</span></span>

<span data-ttu-id="0a89e-140">I metadati del produttore corrispondono alla sezione dei metadati del produttore descritta nel profilo del dispositivo. per informazioni dettagliate, vedere il profilo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a89e-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="0a89e-141">È necessario fornire il nome del produttore o almeno una versione localizzata del nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="0a89e-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="0a89e-142">È necessario fornire il nome del modello o almeno una versione localizzata del nome del modello.</span><span class="sxs-lookup"><span data-stu-id="0a89e-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="0a89e-143">L'elemento [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) viene successivamente usato per generare una costante C che contiene queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="0a89e-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="0a89e-144">Se è presente un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , almeno un elemento [**Hosted**](hosted.md) deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="0a89e-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="0a89e-145">Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **Hosted** , è necessario che sia presente un elemento **PnPXDeviceCategory** all'interno dell'elemento **thisModelMetadata** .</span><span class="sxs-lookup"><span data-stu-id="0a89e-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="0a89e-146">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a89e-146">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0a89e-147">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a89e-147">Minimum supported system</span></span><br/> | <span data-ttu-id="0a89e-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a89e-148">Windows Vista</span></span> |
| <span data-ttu-id="0a89e-149">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0a89e-149">Can be empty</span></span>                        | <span data-ttu-id="0a89e-150">No</span><span class="sxs-lookup"><span data-stu-id="0a89e-150">No</span></span>            |



 

 




