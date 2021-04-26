---
description: Definisce i metadati di hosting per il dispositivo da implementazione. Questo elemento viene usato solo per le implementazioni del dispositivo (host).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994798"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="f3b28-104">elemento hostMetadata</span><span class="sxs-lookup"><span data-stu-id="f3b28-104">hostMetadata element</span></span>

<span data-ttu-id="f3b28-105">Definisce i metadati di hosting per il dispositivo da implementazione.</span><span class="sxs-lookup"><span data-stu-id="f3b28-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="f3b28-106">Questo elemento viene usato solo per le implementazioni del dispositivo (host).</span><span class="sxs-lookup"><span data-stu-id="f3b28-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="f3b28-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f3b28-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="f3b28-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="f3b28-108">Attributes</span></span>

<span data-ttu-id="f3b28-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="f3b28-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f3b28-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f3b28-110">Child elements</span></span>



| <span data-ttu-id="f3b28-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3b28-111">Element</span></span>                             | <span data-ttu-id="f3b28-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3b28-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3b28-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="f3b28-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="f3b28-114">Definisce gli elementi ServiceID e [**Types per**](types.md) l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="f3b28-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="f3b28-115">Se non viene specificato in modo esplicito, WSDAPI non fornisce dati predefiniti in risposta alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3b28-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="f3b28-116">**Ospitato da**</span><span class="sxs-lookup"><span data-stu-id="f3b28-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="f3b28-117">Definisce gli elementi [**ServiceID**](serviceid.md) e [**Types**](types.md) per i servizi forniti da questo host del servizio.</span><span class="sxs-lookup"><span data-stu-id="f3b28-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="f3b28-118">Ogni servizio fornito da questo host [](hosted.md) del servizio deve avere le proprie informazioni sugli elementi ospitati per garantire che il servizio venga pubblicato correttamente in risposta alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3b28-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="f3b28-119">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f3b28-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="f3b28-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f3b28-120">Parent elements</span></span>



| <span data-ttu-id="f3b28-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3b28-121">Element</span></span>                                                         | <span data-ttu-id="f3b28-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3b28-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="f3b28-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="f3b28-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="f3b28-124">Descrive l'host e i metadati ospitati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3b28-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f3b28-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3b28-125">Remarks</span></span>

<span data-ttu-id="f3b28-126">I metadati di hosting vengono visualizzati in questo elemento in un formato simile a quello specificato nel profilo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3b28-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="f3b28-127">**hostMetadata** è leggermente diverso dal formato descritto nel profilo del dispositivo in quanto l'unica proprietà di riferimento che supporta è l'ID servizio.</span><span class="sxs-lookup"><span data-stu-id="f3b28-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="f3b28-128">[**L'elemento relationshipMetadataDefinition**](relationshipmetadatadefinition.md) viene usato successivamente per generare una costante C contenente queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="f3b28-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="f3b28-129">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3b28-129">Element information</span></span>



| <span data-ttu-id="f3b28-130">Label</span><span class="sxs-lookup"><span data-stu-id="f3b28-130">Label</span></span> | <span data-ttu-id="f3b28-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f3b28-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f3b28-132">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3b28-132">Minimum supported system</span></span><br/> | <span data-ttu-id="f3b28-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3b28-133">Windows Vista</span></span> |
| <span data-ttu-id="f3b28-134">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f3b28-134">Can be empty</span></span>                        | <span data-ttu-id="f3b28-135">No</span><span class="sxs-lookup"><span data-stu-id="f3b28-135">No</span></span>            |



 

 




