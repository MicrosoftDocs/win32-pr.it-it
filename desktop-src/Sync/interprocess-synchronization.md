---
description: Più processi possono avere handle per lo stesso evento, mutex, semaforo o oggetto timer, quindi questi oggetti possono essere usati per eseguire la sincronizzazione interprocesso.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronizzazione interprocesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315303"
---
# <a name="interprocess-synchronization"></a><span data-ttu-id="611c3-103">Sincronizzazione interprocesso</span><span class="sxs-lookup"><span data-stu-id="611c3-103">Interprocess Synchronization</span></span>

<span data-ttu-id="611c3-104">Più processi possono avere handle per lo stesso evento, mutex, semaforo o oggetto timer, quindi questi oggetti possono essere usati per eseguire la sincronizzazione interprocesso.</span><span class="sxs-lookup"><span data-stu-id="611c3-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="611c3-105">Il processo che crea un oggetto può usare l'handle restituito dalla funzione di creazione ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span><span class="sxs-lookup"><span data-stu-id="611c3-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="611c3-106">Altri processi possono aprire un handle per l'oggetto utilizzandone il nome o l'ereditarietà o la duplicazione.</span><span class="sxs-lookup"><span data-stu-id="611c3-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="611c3-107">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="611c3-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="611c3-108">Nomi degli oggetti</span><span class="sxs-lookup"><span data-stu-id="611c3-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="611c3-109">Ereditarietà degli oggetti</span><span class="sxs-lookup"><span data-stu-id="611c3-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="611c3-110">Duplicazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="611c3-110">Object Duplication</span></span>](object-duplication.md)

 

 
