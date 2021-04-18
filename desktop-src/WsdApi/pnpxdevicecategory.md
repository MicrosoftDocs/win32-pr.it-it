---
description: Specifica la categoria PnP-X a cui appartiene il dispositivo. È possibile specificare più di una categoria.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312679"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="3db9f-104">Elemento PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="3db9f-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="3db9f-105">Specifica la categoria PnP-X a cui appartiene il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3db9f-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="3db9f-106">È possibile specificare più di una categoria.</span><span class="sxs-lookup"><span data-stu-id="3db9f-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="3db9f-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3db9f-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="3db9f-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="3db9f-108">Attributes</span></span>

<span data-ttu-id="3db9f-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="3db9f-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3db9f-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3db9f-110">Child elements</span></span>

<span data-ttu-id="3db9f-111">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="3db9f-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3db9f-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3db9f-112">Parent elements</span></span>



| <span data-ttu-id="3db9f-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="3db9f-113">Element</span></span>                                                   | <span data-ttu-id="3db9f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3db9f-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3db9f-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="3db9f-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="3db9f-116">Definisce il produttore e i metadati del modello per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="3db9f-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3db9f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3db9f-117">Remarks</span></span>

<span data-ttu-id="3db9f-118">I dispositivi possono inoltre specificare una sottocategoria del dispositivo per una categoria di dispositivi più descrittiva.</span><span class="sxs-lookup"><span data-stu-id="3db9f-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="3db9f-119">Ad esempio, "phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica un dispositivo che è un dispositivo Microsoft Windows Mobile con una fotocamera e Music Player.</span><span class="sxs-lookup"><span data-stu-id="3db9f-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="3db9f-120">La categoria del dispositivo primario per questo dispositivo è "phones".</span><span class="sxs-lookup"><span data-stu-id="3db9f-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="3db9f-121">Per specificare più di una categoria di dispositivi, separare le categorie con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="3db9f-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="3db9f-122">Ad esempio, "stampanti archiviazione" identifica un dispositivo con una categoria primaria di "stampanti" e una categoria secondaria di "archiviazione".</span><span class="sxs-lookup"><span data-stu-id="3db9f-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="3db9f-123">Se è presente un elemento **PnPXDeviceCategory** , almeno un elemento [**Hosted**](hosted.md) deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="3db9f-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="3db9f-124">Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **Hosted** , è necessario che sia presente almeno un elemento **PnPXDeviceCategory** all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="3db9f-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="3db9f-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3db9f-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="3db9f-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3db9f-126">Minimum supported system</span></span><br/> | <span data-ttu-id="3db9f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3db9f-127">Windows Vista</span></span> |
| <span data-ttu-id="3db9f-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="3db9f-128">Can be empty</span></span>                        | <span data-ttu-id="3db9f-129">Sì</span><span class="sxs-lookup"><span data-stu-id="3db9f-129">Yes</span></span>           |



 

 




