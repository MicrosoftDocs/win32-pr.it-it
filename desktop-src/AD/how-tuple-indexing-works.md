---
title: Funzionamento dell'indicizzazione delle tuple
description: Gli indici di tupla vengono usati per ottimizzare le ricerche con 0 o più stringhe di ricerca mediale e 0 o 1 stringhe di ricerca finale. Possono essere usati anche per ottimizzare le ricerche di una stringa di ricerca iniziale se non è disponibile alcun indice comune per tale attributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indicizzazione tupla
- Ricerca di Active Directory Active Directory, ottimizzazione
- Active Directory, ottimizzazione della ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724487"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="8b716-107">Funzionamento dell'indicizzazione delle tuple</span><span class="sxs-lookup"><span data-stu-id="8b716-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="8b716-108">Gli indici di tupla vengono usati per ottimizzare le ricerche con 0 o più [stringhe di ricerca mediale](search-string-types.md) e 0 o 1 stringhe di ricerca finale.</span><span class="sxs-lookup"><span data-stu-id="8b716-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="8b716-109">Possono essere usati anche per ottimizzare le ricerche di una stringa di ricerca iniziale se non è disponibile alcun indice comune per tale attributo.</span><span class="sxs-lookup"><span data-stu-id="8b716-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="8b716-110">È possibile attivare l'indicizzazione tupla per un attributo impostando il bit 5, che corrisponde al valore 32, nell'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .</span><span class="sxs-lookup"><span data-stu-id="8b716-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="8b716-111">Questo attributo viene impostato nell'oggetto dello schema che rappresenta l'attributo che richiede l'indice della tupla.</span><span class="sxs-lookup"><span data-stu-id="8b716-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="8b716-112">L'effetto sulle prestazioni di attivazione dell'indicizzazione delle tuple consiste nel fatto che qualsiasi valore stringa impostato per tale attributo verrà espanso in un numero elevato di frammenti nell'indice della tupla.</span><span class="sxs-lookup"><span data-stu-id="8b716-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="8b716-113">Quando un attributo si espande, viene utilizzata una quantità maggiore di spazio su disco nel file di albero delle informazioni della directory e viene anche aggiornata più lentamente.</span><span class="sxs-lookup"><span data-stu-id="8b716-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="8b716-114">Gli indici di tupla sono progettati per accelerare le ricerche del modulo `*string*` .</span><span class="sxs-lookup"><span data-stu-id="8b716-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="8b716-115">L'accelerazione può essere considerevole perché questa forma di ricerca non può essere ottimizzata in altro modo e, nella forma non ottimizzata, impone al server Active Directory di esaminare ogni oggetto nell'ambito della ricerca per eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="8b716-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="8b716-116">Pertanto, una ricerca di base Cerca solo un oggetto, che usa un minor numero di risorse, una ricerca di elementi figlio immediata Cerca solo gli elementi figlio di un oggetto (che potrebbero usare un minor numero di risorse o più risorse a seconda delle dimensioni del contenitore) e la ricerca di un sottoalbero produrrà l'intero sottoalbero sotto l'oggetto di base, che in genere richiederebbe una grande quantità di</span><span class="sxs-lookup"><span data-stu-id="8b716-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="8b716-117">Gli indici di tupla funzionano suddividendo una stringa in *Tuple*.</span><span class="sxs-lookup"><span data-stu-id="8b716-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="8b716-118">Ad esempio, la stringa "Active Directory" verrebbe suddivisa nelle tuple seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b716-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="8b716-119">La directory si arresterà a 32767 caratteri quando si espande una stringa per l'indicizzazione delle tuple.</span><span class="sxs-lookup"><span data-stu-id="8b716-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="8b716-120">Un indice tupla conterrebbe una voce per ogni tupla.</span><span class="sxs-lookup"><span data-stu-id="8b716-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="8b716-121">Quindi, se un utente cerca `*cto*` , il server di Active Directory cercherà tutte le corrispondenze per "CTO" nell'indice e, in questo caso, rileverà un puntatore al record con un attributo (tupla indicizzata) con un valore "directory".</span><span class="sxs-lookup"><span data-stu-id="8b716-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="8b716-122">Se la stringa di ricerca mediale ( `*cto*` nell'esempio precedente) è sufficientemente specifica, la ricerca sarà abbastanza efficiente perché riduce notevolmente il numero di oggetti che il server di Active Directory deve esaminare per eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="8b716-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 