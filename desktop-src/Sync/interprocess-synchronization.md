---
description: Più processi possono avere handle per lo stesso evento, mutex, semaforo o oggetto timer, quindi questi oggetti possono essere usati per eseguire la sincronizzazione interprocesso.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronizzazione interprocesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886351"
---
# <a name="interprocess-synchronization"></a>Sincronizzazione interprocesso

Più processi possono avere handle per lo stesso evento, mutex, semaforo o oggetto timer, quindi questi oggetti possono essere usati per eseguire la sincronizzazione interprocesso. Il processo che crea un oggetto può usare l'handle restituito dalla funzione di creazione ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Altri processi possono aprire un handle per l'oggetto usando il relativo nome o tramite ereditarietà o duplicazione. Per altre informazioni, vedere i seguenti argomenti:

-   [Nomi degli oggetti](object-names.md)
-   [Ereditarietà degli oggetti](object-inheritance.md)
-   [Duplicazione di oggetti](object-duplication.md)

 

 
