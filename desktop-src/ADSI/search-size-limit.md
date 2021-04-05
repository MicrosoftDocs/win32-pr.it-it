---
title: Limite dimensioni ricerca
description: Per ridurre i requisiti di memoria, un client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati.
ms.assetid: 675a4931-dfa4-4948-936b-dee27add530c
ms.tgt_platform: multiple
keywords:
- Limite dimensioni ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd11148f9e887df1e15e221e8188f9e9e3b10d33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955084"
---
# <a name="search-size-limit"></a><span data-ttu-id="14027-104">Limite dimensioni ricerca</span><span class="sxs-lookup"><span data-stu-id="14027-104">Search Size Limit</span></span>

<span data-ttu-id="14027-105">Per ridurre i requisiti di memoria, un client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="14027-105">To reduce memory requirements, a client can focus on a small number of objects returned from the server and ignore the rest of the result set.</span></span> <span data-ttu-id="14027-106">A tale scopo, il client specifica un limite di dimensioni di ricerca e altri criteri di ricerca appropriati.</span><span class="sxs-lookup"><span data-stu-id="14027-106">To accomplish this, the client specifies a search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="14027-107">Se, ad esempio, una directory archivia i punteggi dei test di un quartiere School, è possibile eseguire una query sui primi dieci studenti con i punteggi di test più elevati specificando un limite di dimensioni pari a dieci e un ordinamento decrescente.</span><span class="sxs-lookup"><span data-stu-id="14027-107">For example, if a directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten and a descending sort order.</span></span>

<span data-ttu-id="14027-108">Per ulteriori informazioni sull'utilizzo dell'opzione limite dimensioni ricerca con un'interfaccia di ricerca specifica, vedere:</span><span class="sxs-lookup"><span data-stu-id="14027-108">For more information about using the search size limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="14027-109">Limite dimensioni con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="14027-109">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="14027-110">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="14027-110">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="14027-111">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="14027-111">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




