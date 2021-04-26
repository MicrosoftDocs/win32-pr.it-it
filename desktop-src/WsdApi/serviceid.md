---
description: URI che rappresenta l'identificatore del servizio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995108"
---
# <a name="serviceid-element"></a><span data-ttu-id="84d0f-103">Elemento ServiceID</span><span class="sxs-lookup"><span data-stu-id="84d0f-103">ServiceID element</span></span>

<span data-ttu-id="84d0f-104">URI che rappresenta l'identificatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="84d0f-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="84d0f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="84d0f-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="84d0f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="84d0f-106">Attributes</span></span>

<span data-ttu-id="84d0f-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="84d0f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="84d0f-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="84d0f-108">Child elements</span></span>

<span data-ttu-id="84d0f-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="84d0f-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="84d0f-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="84d0f-110">Parent elements</span></span>



| <span data-ttu-id="84d0f-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="84d0f-111">Element</span></span>                             | <span data-ttu-id="84d0f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d0f-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84d0f-113">**Host**</span><span class="sxs-lookup"><span data-stu-id="84d0f-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="84d0f-114">Definisce gli elementi **ServiceID** e [**Types per**](types.md) l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="84d0f-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="84d0f-115">Se non viene specificato in modo esplicito, WSDAPI non fornisce dati predefiniti in risposta alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="84d0f-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="84d0f-116">**Ospitato da**</span><span class="sxs-lookup"><span data-stu-id="84d0f-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="84d0f-117">Definisce gli elementi **ServiceID** e [**Types**](types.md) per i servizi forniti da questo host del servizio.</span><span class="sxs-lookup"><span data-stu-id="84d0f-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="84d0f-118">Ogni servizio fornito da questo host [](hosted.md) del servizio deve avere le proprie informazioni sugli elementi ospitati per garantire che il servizio venga pubblicato correttamente in risposta alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="84d0f-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="84d0f-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="84d0f-119">Element information</span></span>



| <span data-ttu-id="84d0f-120">Label</span><span class="sxs-lookup"><span data-stu-id="84d0f-120">Label</span></span> | <span data-ttu-id="84d0f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="84d0f-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="84d0f-122">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84d0f-122">Minimum supported system</span></span><br/> | <span data-ttu-id="84d0f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84d0f-123">Windows Vista</span></span> |
| <span data-ttu-id="84d0f-124">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="84d0f-124">Can be empty</span></span>                        | <span data-ttu-id="84d0f-125">Sì</span><span class="sxs-lookup"><span data-stu-id="84d0f-125">Yes</span></span>           |



 

 




