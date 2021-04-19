---
description: Definisce i metadati di hosting per il dispositivo da implementare. Questo elemento viene usato solo per le implementazioni dei dispositivi (host).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318152"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="6689a-104">elemento hostMetadata</span><span class="sxs-lookup"><span data-stu-id="6689a-104">hostMetadata element</span></span>

<span data-ttu-id="6689a-105">Definisce i metadati di hosting per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="6689a-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="6689a-106">Questo elemento viene usato solo per le implementazioni dei dispositivi (host).</span><span class="sxs-lookup"><span data-stu-id="6689a-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="6689a-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="6689a-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="6689a-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="6689a-108">Attributes</span></span>

<span data-ttu-id="6689a-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="6689a-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6689a-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6689a-110">Child elements</span></span>



| <span data-ttu-id="6689a-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="6689a-111">Element</span></span>                             | <span data-ttu-id="6689a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6689a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6689a-113">**host**</span><span class="sxs-lookup"><span data-stu-id="6689a-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="6689a-114">Definisce gli elementi ServiceID e [**types**](types.md) per l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="6689a-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="6689a-115">Se non viene specificato in modo esplicito, WSDAPI non fornirà dati predefiniti in risposta alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="6689a-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="6689a-116">**ospitato**</span><span class="sxs-lookup"><span data-stu-id="6689a-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="6689a-117">Definisce gli elementi [**ServiceID**](serviceid.md) e [**types**](types.md) per i servizi forniti da questo host del servizio.</span><span class="sxs-lookup"><span data-stu-id="6689a-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="6689a-118">Ogni servizio fornito da questo host del servizio deve disporre di informazioni relative all'elemento [**ospitato**](hosted.md) per garantire che il servizio venga pubblicato correttamente nelle risposte alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="6689a-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6689a-119">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6689a-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="6689a-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6689a-120">Parent elements</span></span>



| <span data-ttu-id="6689a-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="6689a-121">Element</span></span>                                                         | <span data-ttu-id="6689a-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6689a-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="6689a-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="6689a-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="6689a-124">Descrive l'host e i metadati ospitati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6689a-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6689a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6689a-125">Remarks</span></span>

<span data-ttu-id="6689a-126">I metadati di hosting vengono visualizzati in questo elemento in un formato simile a quello specificato nel profilo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6689a-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="6689a-127">**hostMetadata** è leggermente diverso dal formato descritto nel profilo del dispositivo perché l'unica proprietà di riferimento supportata è l'ID del servizio.</span><span class="sxs-lookup"><span data-stu-id="6689a-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="6689a-128">L'elemento [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) viene usato in seguito per generare una costante C che contiene queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="6689a-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="6689a-129">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6689a-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="6689a-130">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6689a-130">Minimum supported system</span></span><br/> | <span data-ttu-id="6689a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6689a-131">Windows Vista</span></span> |
| <span data-ttu-id="6689a-132">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="6689a-132">Can be empty</span></span>                        | <span data-ttu-id="6689a-133">No</span><span class="sxs-lookup"><span data-stu-id="6689a-133">No</span></span>            |



 

 




