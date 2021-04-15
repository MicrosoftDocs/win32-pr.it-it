---
title: Attributi di struttura e di Unione
description: Utilizzare l'opzione \_ \ attributi per specificare la caratteristica di un'Unione in una chiamata di procedura remota. Usare l'attributo Ignore per definire determinati membri di struttura o di Unione come locali per l'applicazione client.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- MIDL, attributi, struttura e unione IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471142"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="a0b8d-105">Attributi di struttura e di Unione</span><span class="sxs-lookup"><span data-stu-id="a0b8d-105">Structure and Union Attributes</span></span>

<span data-ttu-id="a0b8d-106">Utilizzare gli **attributi \_ Switch** \* per specificare la caratteristica di un'Unione in una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="a0b8d-107">Usare l'attributo [**Ignore**](ignore.md) per definire determinati membri di struttura o di Unione come locali per l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="a0b8d-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="a0b8d-108">Attribute</span></span>                           | <span data-ttu-id="a0b8d-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a0b8d-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0b8d-110">**commutatore**</span><span class="sxs-lookup"><span data-stu-id="a0b8d-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="a0b8d-111">Seleziona discriminante per un'Unione incapsulata.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="a0b8d-112">**opzione \_**</span><span class="sxs-lookup"><span data-stu-id="a0b8d-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="a0b8d-113">Identifica discriminante per un'Unione non incapsulata.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="a0b8d-114">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="a0b8d-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="a0b8d-115">Identifica il tipo di discriminante per un'Unione non incapsulata.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="a0b8d-116">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="a0b8d-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="a0b8d-117">Indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dal puntatore non devono essere trasmessi.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="a0b8d-118">Per specificare le caratteristiche dei membri di struttura o di Unione, è inoltre possibile utilizzare la [matrice e gli attributi del puntatore ridimensionati](array-and-sized-pointer-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b8d-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




