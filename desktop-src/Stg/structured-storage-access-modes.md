---
title: Modalità di accesso all'archiviazione strutturata
description: I meccanismi di controllo dell'accesso simultaneo a un oggetto, da parte di più processi e utenti, sono essenziali.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Archiviazione strutturata Strctd STG, nozioni fondamentali, funzioni API, flag per l'accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297843"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="b61bf-104">Modalità di accesso all'archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="b61bf-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="b61bf-105">I meccanismi di controllo dell'accesso simultaneo a un oggetto, da parte di più processi e utenti, sono essenziali.</span><span class="sxs-lookup"><span data-stu-id="b61bf-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="b61bf-106">COM fornisce questi meccanismi definendo le modalità di accesso per gli oggetti di archiviazione e di flusso.</span><span class="sxs-lookup"><span data-stu-id="b61bf-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="b61bf-107">La modalità di accesso specificata per un oggetto di archiviazione padre viene ereditata dai relativi elementi figlio, sebbene sia possibile inserire restrizioni aggiuntive sul flusso o sull'archiviazione figlio.</span><span class="sxs-lookup"><span data-stu-id="b61bf-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="b61bf-108">Un oggetto di archiviazione o flusso annidato può essere aperto nella stessa modalità o in una modalità più limitata rispetto a quello del relativo elemento padre, ma non può essere aperto in modalità meno limitata rispetto a quello del relativo padre.</span><span class="sxs-lookup"><span data-stu-id="b61bf-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="b61bf-109">Per specificare le modalità di accesso, è possibile usare i valori elencati in [**costanti STGM**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b61bf-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="b61bf-110">Questi valori vengono usati come flag per essere passati come argomenti ai metodi nell'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e alle funzioni API associate.</span><span class="sxs-lookup"><span data-stu-id="b61bf-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="b61bf-111">In genere, diversi flag vengono combinati nel parametro *grfMode*, usando un'operazione **o** un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="b61bf-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="b61bf-112">I flag rientrano in sei gruppi.</span><span class="sxs-lookup"><span data-stu-id="b61bf-112">The flags fall into six groups.</span></span> <span data-ttu-id="b61bf-113">È possibile specificare solo un flag di ogni gruppo alla volta:</span><span class="sxs-lookup"><span data-stu-id="b61bf-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="b61bf-114">Flag di transazione</span><span class="sxs-lookup"><span data-stu-id="b61bf-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="b61bf-115">Flag di creazione archiviazione</span><span class="sxs-lookup"><span data-stu-id="b61bf-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="b61bf-116">Flag di creazione temporanei</span><span class="sxs-lookup"><span data-stu-id="b61bf-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="b61bf-117">Flag di priorità</span><span class="sxs-lookup"><span data-stu-id="b61bf-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="b61bf-118">Flag di autorizzazione di accesso</span><span class="sxs-lookup"><span data-stu-id="b61bf-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="b61bf-119">Flag di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="b61bf-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




