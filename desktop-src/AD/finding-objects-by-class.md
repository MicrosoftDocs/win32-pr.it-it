---
title: Ricerca di oggetti per classe
description: Query di ricerca tipiche per una classe di oggetti specifica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Ricerca di oggetti per classe AD
- Active Directory, utilizzo, ricerca, per classe
- oggetto AD, ricerca per classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297735"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="cd6f9-106">Ricerca di oggetti per classe</span><span class="sxs-lookup"><span data-stu-id="cd6f9-106">Finding Objects by Class</span></span>

<span data-ttu-id="cd6f9-107">Query di ricerca tipiche per una classe di oggetti specifica.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="cd6f9-108">Nell'esempio di codice seguente viene eseguita la ricerca di computer con percorso nella compilazione di 7N.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="cd6f9-109">Considerare il motivo per cui **objectClass** non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="cd6f9-110">Non utilizzare **objectClass** senza un altro confronto che contenga un attributo indicizzato.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="cd6f9-111">Gli attributi di indice possono aumentare l'efficienza di una query.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="cd6f9-112">L'attributo **objectClass** è multivalore e non indicizzato.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="cd6f9-113">Per specificare il tipo o la classe di un oggetto, usare **objectCategory**.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="cd6f9-114">Meno efficiente:</span><span class="sxs-lookup"><span data-stu-id="cd6f9-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="cd6f9-115">Maggiore efficienza:</span><span class="sxs-lookup"><span data-stu-id="cd6f9-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="cd6f9-116">Tenere presente che in alcuni casi è necessario usare una combinazione di **objectClass** e **objectCategory** .</span><span class="sxs-lookup"><span data-stu-id="cd6f9-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="cd6f9-117">È necessario specificare la classe utente e la classe Contact come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="cd6f9-118">Tenere presente che è possibile cercare gli utenti e i contatti con il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="cd6f9-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




