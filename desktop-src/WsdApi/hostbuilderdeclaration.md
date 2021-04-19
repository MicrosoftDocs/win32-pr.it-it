---
description: Genera una dichiarazione per una funzione che crea un host tipizzato.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316980"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="0f9fb-103">elemento hostBuilderDeclaration</span><span class="sxs-lookup"><span data-stu-id="0f9fb-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="0f9fb-104">Genera una dichiarazione per una funzione che crea un host tipizzato.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="0f9fb-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0f9fb-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="0f9fb-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0f9fb-106">Attributes</span></span>

<span data-ttu-id="0f9fb-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0f9fb-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0f9fb-108">Child elements</span></span>



| <span data-ttu-id="0f9fb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f9fb-109">Element</span></span>                                   | <span data-ttu-id="0f9fb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f9fb-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f9fb-111">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="0f9fb-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="0f9fb-112">Nome dell'interfaccia del servizio da includere per l'host.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="0f9fb-113">Il valore di questo elemento deve corrispondere al valore dell'elemento figlio dell' [**interfaccia**](interface.md) di [**servizio ospitato**](hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="0f9fb-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0f9fb-114">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0f9fb-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="0f9fb-115">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0f9fb-115">Parent elements</span></span>



| <span data-ttu-id="0f9fb-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f9fb-116">Element</span></span>                         | <span data-ttu-id="0f9fb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f9fb-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0f9fb-118">**file**</span><span class="sxs-lookup"><span data-stu-id="0f9fb-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0f9fb-119">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0f9fb-120">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0f9fb-120">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0f9fb-121">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f9fb-121">Minimum supported system</span></span><br/> | <span data-ttu-id="0f9fb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f9fb-122">Windows Vista</span></span> |
| <span data-ttu-id="0f9fb-123">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0f9fb-123">Can be empty</span></span>                        | <span data-ttu-id="0f9fb-124">No</span><span class="sxs-lookup"><span data-stu-id="0f9fb-124">No</span></span>            |



 

 




