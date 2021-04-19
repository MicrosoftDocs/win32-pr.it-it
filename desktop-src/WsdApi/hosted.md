---
description: Definisce gli elementi ServiceID, types, PnPXHardwareId e PnPXCompatibleId per i servizi definiti dall'host del servizio.
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: elemento Hosted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316979"
---
# <a name="hosted-element"></a><span data-ttu-id="1f87b-103">elemento Hosted</span><span class="sxs-lookup"><span data-stu-id="1f87b-103">hosted element</span></span>

<span data-ttu-id="1f87b-104">Definisce gli elementi [**ServiceID**](serviceid.md), [**types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](pnpxcompatibleid.md) per i servizi definiti dall'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="1f87b-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="1f87b-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1f87b-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="1f87b-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="1f87b-106">Attributes</span></span>

<span data-ttu-id="1f87b-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="1f87b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1f87b-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1f87b-108">Child elements</span></span>



| <span data-ttu-id="1f87b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f87b-109">Element</span></span>                                                 | <span data-ttu-id="1f87b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f87b-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="1f87b-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="1f87b-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="1f87b-112">Specifica l'identificatore compatibile PnP-X del servizio.</span><span class="sxs-lookup"><span data-stu-id="1f87b-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="1f87b-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="1f87b-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="1f87b-114">Specifica l'identificatore hardware PnP-X del servizio.</span><span class="sxs-lookup"><span data-stu-id="1f87b-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="1f87b-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="1f87b-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="1f87b-116">Definisce un identificatore del servizio per l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="1f87b-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="1f87b-117">**Tipi**</span><span class="sxs-lookup"><span data-stu-id="1f87b-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="1f87b-118">Definisce un elenco di nomi completi XSD.</span><span class="sxs-lookup"><span data-stu-id="1f87b-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="1f87b-119">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1f87b-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="1f87b-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="1f87b-120">Parent elements</span></span>



| <span data-ttu-id="1f87b-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f87b-121">Element</span></span>                                         | <span data-ttu-id="1f87b-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f87b-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="1f87b-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="1f87b-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="1f87b-124">Metadati di hosting per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="1f87b-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1f87b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f87b-125">Remarks</span></span>

<span data-ttu-id="1f87b-126">Ogni servizio fornito da un host del servizio deve disporre di informazioni relative all'elemento **ospitato** per garantire che il servizio venga pubblicato correttamente nelle risposte alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="1f87b-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="1f87b-127">Gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) sono facoltativi, ma se usati devono essere usati insieme.</span><span class="sxs-lookup"><span data-stu-id="1f87b-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="1f87b-128">Se è presente un oggetto, deve essere presente anche l'altro.</span><span class="sxs-lookup"><span data-stu-id="1f87b-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="1f87b-129">Se è presente un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , almeno un elemento **Hosted** deve contenere entrambi gli elementi [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="1f87b-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="1f87b-130">Analogamente, se gli elementi **PnPXHardwareId** e **PnPXCompatibleId** sono presenti in un elemento **Hosted** , è necessario che sia presente almeno un elemento **PnPXDeviceCategory** all'interno dell'elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="1f87b-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="1f87b-131">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1f87b-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1f87b-132">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f87b-132">Minimum supported system</span></span><br/> | <span data-ttu-id="1f87b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f87b-133">Windows Vista</span></span> |
| <span data-ttu-id="1f87b-134">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="1f87b-134">Can be empty</span></span>                        | <span data-ttu-id="1f87b-135">No</span><span class="sxs-lookup"><span data-stu-id="1f87b-135">No</span></span>            |



 

 




