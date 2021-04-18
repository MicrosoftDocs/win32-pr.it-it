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
# <a name="interprocess-synchronization"></a>Sincronizzazione interprocesso

Più processi possono avere handle per lo stesso evento, mutex, semaforo o oggetto timer, quindi questi oggetti possono essere usati per eseguire la sincronizzazione interprocesso. Il processo che crea un oggetto può usare l'handle restituito dalla funzione di creazione ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Altri processi possono aprire un handle per l'oggetto utilizzandone il nome o l'ereditarietà o la duplicazione. Per altre informazioni, vedere i seguenti argomenti:

-   [Nomi degli oggetti](object-names.md)
-   [Ereditarietà degli oggetti](object-inheritance.md)
-   [Duplicazione di oggetti](object-duplication.md)

 

 
