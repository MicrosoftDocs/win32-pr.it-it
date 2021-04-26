---
description: Definisce i metadati del produttore e del modello per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: Elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995338"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="bac49-104">Elemento thisModelMetadata</span><span class="sxs-lookup"><span data-stu-id="bac49-104">thisModelMetadata element</span></span>

<span data-ttu-id="bac49-105">Definisce i metadati del produttore e del modello per il dispositivo da implementazione.</span><span class="sxs-lookup"><span data-stu-id="bac49-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="bac49-106">Questo elemento viene usato solo per le implementazioni del dispositivo (host).</span><span class="sxs-lookup"><span data-stu-id="bac49-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="bac49-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bac49-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="bac49-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="bac49-108">Attributes</span></span>

<span data-ttu-id="bac49-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="bac49-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bac49-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bac49-110">Child elements</span></span>



| <span data-ttu-id="bac49-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="bac49-111">Element</span></span>                                                     | <span data-ttu-id="bac49-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bac49-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bac49-113">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="bac49-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="bac49-114">Nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="bac49-114">Name of the manufacturer.</span></span> <span data-ttu-id="bac49-115">Almeno uno dei [](manufacturerls.md) [**produttori deve**](manufacturer.md) essere presente nei metadati.</span><span class="sxs-lookup"><span data-stu-id="bac49-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="bac49-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="bac49-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="bac49-117">Versione localizzata del nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="bac49-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="bac49-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="bac49-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="bac49-119">Indirizzo URL del produttore.</span><span class="sxs-lookup"><span data-stu-id="bac49-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="bac49-120">**Modelname**</span><span class="sxs-lookup"><span data-stu-id="bac49-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="bac49-121">Nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-121">Name of the device.</span></span> <span data-ttu-id="bac49-122">Nei metadati deve essere presente almeno uno di [**modelName**](modelname.md) o [**modelNameLS.**](modelnamels.md)</span><span class="sxs-lookup"><span data-stu-id="bac49-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="bac49-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="bac49-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="bac49-124">Versione localizzata del nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="bac49-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="bac49-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="bac49-126">Numero di modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="bac49-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="bac49-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="bac49-128">Indirizzo URL per il modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="bac49-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="bac49-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="bac49-130">Categoria PnP-X a cui appartiene il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="bac49-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="bac49-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="bac49-132">Indirizzo URL dei dati di presentazione del modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="bac49-133">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bac49-133">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="bac49-134">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="bac49-134">Parent elements</span></span>



| <span data-ttu-id="bac49-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="bac49-135">Element</span></span>                                     | <span data-ttu-id="bac49-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bac49-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="bac49-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="bac49-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="bac49-138">Elemento radice di un file script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="bac49-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bac49-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="bac49-139">Remarks</span></span>

<span data-ttu-id="bac49-140">I metadati del produttore corrispondono alla sezione dei metadati del produttore descritta nel profilo del dispositivo . Per informazioni dettagliate, vedere il profilo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bac49-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="bac49-141">È necessario specificare il nome del produttore o almeno una versione localizzata del nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="bac49-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="bac49-142">È necessario specificare il nome del modello o almeno una versione localizzata del nome del modello.</span><span class="sxs-lookup"><span data-stu-id="bac49-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="bac49-143">[**L'elemento thisModelMetadataDefinition**](thismodelmetadatadefinition.md) viene successivamente usato per generare una costante C contenente queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="bac49-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="bac49-144">Se è presente un elemento [**PnPXDeviceCategory,**](pnpxdevicecategory.md) almeno un elemento ospitato deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) [**e PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md)</span><span class="sxs-lookup"><span data-stu-id="bac49-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="bac49-145">Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento ospitato, un elemento **PnPXDeviceCategory** deve essere presente all'interno dell'elemento **thisModelMetadata.** </span><span class="sxs-lookup"><span data-stu-id="bac49-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="bac49-146">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bac49-146">Element information</span></span>



| <span data-ttu-id="bac49-147">Label</span><span class="sxs-lookup"><span data-stu-id="bac49-147">Label</span></span> | <span data-ttu-id="bac49-148">Valore</span><span class="sxs-lookup"><span data-stu-id="bac49-148">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="bac49-149">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bac49-149">Minimum supported system</span></span><br/> | <span data-ttu-id="bac49-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bac49-150">Windows Vista</span></span> |
| <span data-ttu-id="bac49-151">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="bac49-151">Can be empty</span></span>                        | <span data-ttu-id="bac49-152">No</span><span class="sxs-lookup"><span data-stu-id="bac49-152">No</span></span>            |



 

 




