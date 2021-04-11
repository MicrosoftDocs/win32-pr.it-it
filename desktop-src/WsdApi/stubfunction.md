---
description: Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni unidirezionali e bidirezionali.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233107"
---
# <a name="stubfunction-element"></a><span data-ttu-id="7e454-103">elemento stubFunction</span><span class="sxs-lookup"><span data-stu-id="7e454-103">stubFunction element</span></span>

<span data-ttu-id="7e454-104">Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni unidirezionali e bidirezionali.</span><span class="sxs-lookup"><span data-stu-id="7e454-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="7e454-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7e454-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="7e454-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="7e454-106">Attributes</span></span>

<span data-ttu-id="7e454-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="7e454-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7e454-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7e454-108">Child elements</span></span>

<span data-ttu-id="7e454-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="7e454-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7e454-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="7e454-110">Parent elements</span></span>



| <span data-ttu-id="7e454-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e454-111">Element</span></span>                                                       | <span data-ttu-id="7e454-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e454-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="7e454-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="7e454-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="7e454-114">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="7e454-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7e454-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e454-115">Remarks</span></span>

<span data-ttu-id="7e454-116">I riferimenti alle funzioni stub vengono utilizzati negli scenari di hosting per operazioni unidirezionali e bidirezionali.</span><span class="sxs-lookup"><span data-stu-id="7e454-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="7e454-117">I valori validi per questo elemento sono 1 (i riferimenti alle funzioni TRUE/stub sono inclusi) e 0 (FALSE/nessun riferimento di funzione stub incluso).</span><span class="sxs-lookup"><span data-stu-id="7e454-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="7e454-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7e454-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7e454-119">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e454-119">Minimum supported system</span></span><br/> | <span data-ttu-id="7e454-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e454-120">Windows Vista</span></span> |
| <span data-ttu-id="7e454-121">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="7e454-121">Can be empty</span></span>                        | <span data-ttu-id="7e454-122">Sì</span><span class="sxs-lookup"><span data-stu-id="7e454-122">Yes</span></span>           |



 

 




