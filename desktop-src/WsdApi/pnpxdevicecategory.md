---
description: Specifica la categoria PnP-X a cui appartiene il dispositivo. È possibile specificare più di una categoria.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996588"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="a45b2-104">Elemento PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="a45b2-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="a45b2-105">Specifica la categoria PnP-X a cui appartiene il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45b2-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="a45b2-106">È possibile specificare più di una categoria.</span><span class="sxs-lookup"><span data-stu-id="a45b2-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="a45b2-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a45b2-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="a45b2-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="a45b2-108">Attributes</span></span>

<span data-ttu-id="a45b2-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a45b2-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a45b2-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a45b2-110">Child elements</span></span>

<span data-ttu-id="a45b2-111">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="a45b2-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a45b2-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a45b2-112">Parent elements</span></span>



| <span data-ttu-id="a45b2-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="a45b2-113">Element</span></span>                                                   | <span data-ttu-id="a45b2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a45b2-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a45b2-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="a45b2-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="a45b2-116">Definisce i metadati del produttore e del modello per il dispositivo da implementazione.</span><span class="sxs-lookup"><span data-stu-id="a45b2-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a45b2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a45b2-117">Remarks</span></span>

<span data-ttu-id="a45b2-118">I dispositivi possono anche specificare una sottocategoria di dispositivo per una categoria di dispositivi più descrittiva.</span><span class="sxs-lookup"><span data-stu-id="a45b2-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="a45b2-119">Ad esempio, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifica un dispositivo Microsoft Windows Mobile con una fotocamera e un lettore musicale.</span><span class="sxs-lookup"><span data-stu-id="a45b2-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="a45b2-120">La categoria di dispositivi principale per questo dispositivo sarà "Telefoni".</span><span class="sxs-lookup"><span data-stu-id="a45b2-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="a45b2-121">Per specificare più di una categoria di dispositivi, separare le categorie con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="a45b2-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="a45b2-122">Ad esempio, "Archiviazione stampanti" identifica un dispositivo con una categoria primaria "Stampanti" e una categoria secondaria "Archiviazione".</span><span class="sxs-lookup"><span data-stu-id="a45b2-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="a45b2-123">Se è presente un elemento **PnPXDeviceCategory,** almeno un elemento ospitato deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md)</span><span class="sxs-lookup"><span data-stu-id="a45b2-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="a45b2-124">Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento ospitato, all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) deve essere presente almeno un elemento **PnPXDeviceCategory.** </span><span class="sxs-lookup"><span data-stu-id="a45b2-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="a45b2-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a45b2-125">Element information</span></span>



| <span data-ttu-id="a45b2-126">Label</span><span class="sxs-lookup"><span data-stu-id="a45b2-126">Label</span></span> | <span data-ttu-id="a45b2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a45b2-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="a45b2-128">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45b2-128">Minimum supported system</span></span><br/> | <span data-ttu-id="a45b2-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a45b2-129">Windows Vista</span></span> |
| <span data-ttu-id="a45b2-130">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="a45b2-130">Can be empty</span></span>                        | <span data-ttu-id="a45b2-131">Sì</span><span class="sxs-lookup"><span data-stu-id="a45b2-131">Yes</span></span>           |



 

 




