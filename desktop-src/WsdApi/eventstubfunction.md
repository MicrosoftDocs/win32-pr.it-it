---
description: Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni di notifica.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe353f43d02eec68f29f3075cc445c1314c9762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313666"
---
# <a name="eventstubfunction-element"></a><span data-ttu-id="f96c1-103">elemento eventStubFunction</span><span class="sxs-lookup"><span data-stu-id="f96c1-103">eventStubFunction element</span></span>

<span data-ttu-id="f96c1-104">Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni di notifica.</span><span class="sxs-lookup"><span data-stu-id="f96c1-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="f96c1-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f96c1-105">Usage</span></span>

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="f96c1-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="f96c1-106">Attributes</span></span>

<span data-ttu-id="f96c1-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="f96c1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f96c1-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f96c1-108">Child elements</span></span>

<span data-ttu-id="f96c1-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f96c1-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f96c1-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f96c1-110">Parent elements</span></span>



| <span data-ttu-id="f96c1-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="f96c1-111">Element</span></span>                                                       | <span data-ttu-id="f96c1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f96c1-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f96c1-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f96c1-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="f96c1-114">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="f96c1-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f96c1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f96c1-115">Remarks</span></span>

<span data-ttu-id="f96c1-116">I riferimenti alle funzioni stub si trovano in scenari client per le operazioni di notifica (eventi).</span><span class="sxs-lookup"><span data-stu-id="f96c1-116">Stub function references are in client scenarios for notification operations (events).</span></span>

<span data-ttu-id="f96c1-117">I valori validi per questo elemento sono 1 (i riferimenti alle funzioni TRUE/stub sono inclusi) e 0 (FALSE/nessun riferimento di funzione stub incluso).</span><span class="sxs-lookup"><span data-stu-id="f96c1-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="f96c1-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f96c1-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f96c1-119">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f96c1-119">Minimum supported system</span></span><br/> | <span data-ttu-id="f96c1-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f96c1-120">Windows Vista</span></span> |
| <span data-ttu-id="f96c1-121">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f96c1-121">Can be empty</span></span>                        | <span data-ttu-id="f96c1-122">Sì</span><span class="sxs-lookup"><span data-stu-id="f96c1-122">Yes</span></span>           |



 

 




