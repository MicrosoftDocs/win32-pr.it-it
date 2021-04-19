---
description: URI che rappresenta l'identificatore del servizio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318486"
---
# <a name="serviceid-element"></a><span data-ttu-id="159a0-103">Elemento ServiceID</span><span class="sxs-lookup"><span data-stu-id="159a0-103">ServiceID element</span></span>

<span data-ttu-id="159a0-104">URI che rappresenta l'identificatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="159a0-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="159a0-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="159a0-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="159a0-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="159a0-106">Attributes</span></span>

<span data-ttu-id="159a0-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="159a0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="159a0-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="159a0-108">Child elements</span></span>

<span data-ttu-id="159a0-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="159a0-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="159a0-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="159a0-110">Parent elements</span></span>



| <span data-ttu-id="159a0-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="159a0-111">Element</span></span>                             | <span data-ttu-id="159a0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="159a0-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="159a0-113">**host**</span><span class="sxs-lookup"><span data-stu-id="159a0-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="159a0-114">Definisce gli elementi **ServiceID** e [**types**](types.md) per l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="159a0-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="159a0-115">Se non viene specificato in modo esplicito, WSDAPI non fornirà dati predefiniti in risposta alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="159a0-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="159a0-116">**ospitato**</span><span class="sxs-lookup"><span data-stu-id="159a0-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="159a0-117">Definisce gli elementi **ServiceID** e [**types**](types.md) per i servizi forniti da questo host del servizio.</span><span class="sxs-lookup"><span data-stu-id="159a0-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="159a0-118">Ogni servizio fornito da questo host del servizio deve disporre di informazioni relative all'elemento [**ospitato**](hosted.md) per garantire che il servizio venga pubblicato correttamente nelle risposte alle richieste di metadati.</span><span class="sxs-lookup"><span data-stu-id="159a0-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="159a0-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="159a0-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="159a0-120">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159a0-120">Minimum supported system</span></span><br/> | <span data-ttu-id="159a0-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="159a0-121">Windows Vista</span></span> |
| <span data-ttu-id="159a0-122">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="159a0-122">Can be empty</span></span>                        | <span data-ttu-id="159a0-123">Sì</span><span class="sxs-lookup"><span data-stu-id="159a0-123">Yes</span></span>           |



 

 




