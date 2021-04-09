---
description: Definisce gli elementi ServiceID e types per l'host del servizio.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880637"
---
# <a name="host-element"></a><span data-ttu-id="0e1fe-103">elemento host</span><span class="sxs-lookup"><span data-stu-id="0e1fe-103">host element</span></span>

<span data-ttu-id="0e1fe-104">Definisce gli elementi [**ServiceID**](serviceid.md) e [**types**](types.md) per l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="0e1fe-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="0e1fe-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0e1fe-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="0e1fe-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0e1fe-106">Attributes</span></span>

<span data-ttu-id="0e1fe-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0e1fe-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0e1fe-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0e1fe-108">Child elements</span></span>



| <span data-ttu-id="0e1fe-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e1fe-109">Element</span></span>                                   | <span data-ttu-id="0e1fe-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e1fe-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="0e1fe-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="0e1fe-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="0e1fe-112">Definisce l'identificatore del servizio per l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="0e1fe-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="0e1fe-113">**Tipi**</span><span class="sxs-lookup"><span data-stu-id="0e1fe-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="0e1fe-114">Definisce un elenco di nomi completi XSD.</span><span class="sxs-lookup"><span data-stu-id="0e1fe-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="0e1fe-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0e1fe-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="0e1fe-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0e1fe-116">Parent elements</span></span>



| <span data-ttu-id="0e1fe-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e1fe-117">Element</span></span>                                         | <span data-ttu-id="0e1fe-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e1fe-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="0e1fe-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="0e1fe-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="0e1fe-120">Metadati di hosting per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="0e1fe-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0e1fe-121">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0e1fe-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0e1fe-122">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e1fe-122">Minimum supported system</span></span><br/> | <span data-ttu-id="0e1fe-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e1fe-123">Windows Vista</span></span> |
| <span data-ttu-id="0e1fe-124">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0e1fe-124">Can be empty</span></span>                        | <span data-ttu-id="0e1fe-125">No</span><span class="sxs-lookup"><span data-stu-id="0e1fe-125">No</span></span>            |



 

 




