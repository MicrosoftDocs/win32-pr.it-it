---
description: Genera una dichiarazione per una funzione che crea un host tipidato.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994908"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="d892e-103">elemento hostBuilderDeclaration</span><span class="sxs-lookup"><span data-stu-id="d892e-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="d892e-104">Genera una dichiarazione per una funzione che crea un host tipidato.</span><span class="sxs-lookup"><span data-stu-id="d892e-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="d892e-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d892e-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="d892e-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="d892e-106">Attributes</span></span>

<span data-ttu-id="d892e-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="d892e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d892e-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d892e-108">Child elements</span></span>



| <span data-ttu-id="d892e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d892e-109">Element</span></span>                                   | <span data-ttu-id="d892e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d892e-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d892e-111">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="d892e-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="d892e-112">Nome dell'interfaccia del servizio da includere per l'host.</span><span class="sxs-lookup"><span data-stu-id="d892e-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="d892e-113">Il valore di questo elemento deve corrispondere al valore [**dell'elemento**](interface.md) figlio dell'interfaccia di [**hostedService.**](hostedservice.md)</span><span class="sxs-lookup"><span data-stu-id="d892e-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="d892e-114">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d892e-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="d892e-115">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d892e-115">Parent elements</span></span>



| <span data-ttu-id="d892e-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="d892e-116">Element</span></span>                         | <span data-ttu-id="d892e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d892e-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d892e-118">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="d892e-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d892e-119">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="d892e-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="d892e-120">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d892e-120">Element information</span></span>



| <span data-ttu-id="d892e-121">Label</span><span class="sxs-lookup"><span data-stu-id="d892e-121">Label</span></span> | <span data-ttu-id="d892e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d892e-122">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d892e-123">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d892e-123">Minimum supported system</span></span><br/> | <span data-ttu-id="d892e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d892e-124">Windows Vista</span></span> |
| <span data-ttu-id="d892e-125">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="d892e-125">Can be empty</span></span>                        | <span data-ttu-id="d892e-126">No</span><span class="sxs-lookup"><span data-stu-id="d892e-126">No</span></span>            |



 

 




