---
title: Ricerca nel catalogo globale
description: Active Directory Domain Services dispone anche di un catalogo globale (GC), che contiene una replica parziale di tutti gli oggetti nella directory.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- ricerca nel catalogo globale Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707558"
---
# <a name="searching-the-global-catalog"></a><span data-ttu-id="9692a-104">Ricerca nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9692a-104">Searching the Global Catalog</span></span>

<span data-ttu-id="9692a-105">Active Directory Domain Services dispone anche di un catalogo globale (GC), che contiene una replica parziale di tutti gli oggetti nella directory.</span><span class="sxs-lookup"><span data-stu-id="9692a-105">Active Directory Domain Services also have a global catalog (GC), which contains a partial replica of all objects in the directory.</span></span> <span data-ttu-id="9692a-106">Contiene anche le repliche parziali dei contenitori dello schema e della configurazione.</span><span class="sxs-lookup"><span data-stu-id="9692a-106">It also contains partial replicas of the schema and configuration containers.</span></span> <span data-ttu-id="9692a-107">Uno o più controller di dominio in un dominio possono conservare una copia del catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="9692a-107">One or more domain controllers in a domain can hold a copy of the global catalog.</span></span> <span data-ttu-id="9692a-108">Per ulteriori informazioni sull'associazione a un catalogo globale, vedere [associazione al catalogo globale](binding-to-the-global-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="9692a-108">For more information about binding to a global catalog, see [Binding to the Global Catalog](binding-to-the-global-catalog.md).</span></span>

<span data-ttu-id="9692a-109">Il catalogo globale include una replica di ogni oggetto in Active Directory Domain Services, ma con un numero ridotto di attributi.</span><span class="sxs-lookup"><span data-stu-id="9692a-109">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="9692a-110">Gli attributi nel catalogo globale sono quelli usati più di frequente nelle operazioni di ricerca, ad esempio il nome e il cognome di un utente, i nomi di accesso e così via.</span><span class="sxs-lookup"><span data-stu-id="9692a-110">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="9692a-111">Gli attributi del catalogo globale includono anche quelli necessari per individuare una replica completa dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9692a-111">The global catalog attributes also include those required to locate a full replica of the object.</span></span> <span data-ttu-id="9692a-112">Il catalogo globale consente agli utenti di trovare rapidamente oggetti di interesse senza conoscere il dominio che li contiene e senza richiedere uno spazio dei nomi esteso contiguo nell'organizzazione. ovvero, è possibile eseguire ricerche nell'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="9692a-112">The global catalog allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise; that is, you can search the entire forest.</span></span>

<span data-ttu-id="9692a-113">Se quindi si esegue l'associazione a un oggetto nel catalogo globale, si eseguirà la ricerca dell'oggetto e dell'intera gerarchia sottostante, senza dover passare a un altro server.</span><span class="sxs-lookup"><span data-stu-id="9692a-113">So, if you bind to an object in the global catalog, you will search that object and the entire hierarchy below it — without having to go to any other server.</span></span> <span data-ttu-id="9692a-114">Tuttavia, la ricerca può utilizzare solo un filtro di query che contiene le proprietà nel catalogo globale e può recuperare solo le proprietà nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="9692a-114">However, the search can only use a query filter containing properties in the global catalog and can retrieve only properties in the global catalog.</span></span>

<span data-ttu-id="9692a-115">La ricerca nel catalogo globale presenta i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9692a-115">Searching the global catalog has the following benefits:</span></span>

-   <span data-ttu-id="9692a-116">Il catalogo globale consente di eseguire ricerche nell'intera foresta o in qualsiasi parte della foresta, nonché nei contenitori dello schema e della configurazione.</span><span class="sxs-lookup"><span data-stu-id="9692a-116">Global catalog enables you to search the entire forest or any part of the forest as well as the schema and configuration containers.</span></span>
-   <span data-ttu-id="9692a-117">Il catalogo globale consente di eseguire una ricerca completa su un singolo server.</span><span class="sxs-lookup"><span data-stu-id="9692a-117">Global catalog enables you to perform a complete search on a single server.</span></span> <span data-ttu-id="9692a-118">Non è richiesto alcun riferimento o inseguimento del riferimento.</span><span class="sxs-lookup"><span data-stu-id="9692a-118">No referrals or referral chasing is required.</span></span>

<span data-ttu-id="9692a-119">La ricerca nel catalogo globale presenta gli svantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9692a-119">Searching the global catalog has the following disadvantages:</span></span>

-   <span data-ttu-id="9692a-120">Il catalogo globale contiene un piccolo subset delle proprietà per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="9692a-120">Global catalog contains a small subset of the properties on each object.</span></span> <span data-ttu-id="9692a-121">Se il filtro di query include proprietà non presenti nel catalogo globale, la query valuterà le espressioni che contengono tali proprietà come false.</span><span class="sxs-lookup"><span data-stu-id="9692a-121">If your query filter includes properties that are not in the global catalog, the query will evaluate the expressions containing those properties as false.</span></span> <span data-ttu-id="9692a-122">Se si specificano proprietà del catalogo non globali nell'elenco di proprietà da restituire, tali proprietà non vengono recuperate.</span><span class="sxs-lookup"><span data-stu-id="9692a-122">If you specify non-global catalog properties in the list of properties to return, those properties are not retrieved.</span></span>
-   <span data-ttu-id="9692a-123">Per eseguire una ricerca nel catalogo globale, è necessario che sia disponibile un controller di dominio che contiene un catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="9692a-123">To search the global catalog, a domain controller that contains a global catalog must be available.</span></span> <span data-ttu-id="9692a-124">Se non è disponibile, non è possibile eseguire una ricerca nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="9692a-124">If one is not available, you cannot perform a global catalog search.</span></span>
-   <span data-ttu-id="9692a-125">Il catalogo globale è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9692a-125">The global catalog is read-only.</span></span> <span data-ttu-id="9692a-126">Ciò significa che non è possibile eseguire l'associazione a un oggetto nel catalogo globale per creare, modificare o eliminare oggetti.</span><span class="sxs-lookup"><span data-stu-id="9692a-126">This means you cannot bind to an object in the global catalog to create, modify, or delete objects.</span></span>

 

 




