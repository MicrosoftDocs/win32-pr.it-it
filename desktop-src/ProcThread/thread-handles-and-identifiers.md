---
description: Quando un nuovo thread viene creato dalla funzione CreateThread o CreateRemoteThread, viene restituito un handle per il thread.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Handle e identificatori di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6058388f450b4b44c371fc26b132ea785b22c29bc0a2fd86875f563371608512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031631"
---
# <a name="thread-handles-and-identifiers"></a>Handle e identificatori di thread

Quando un nuovo thread viene creato dalla [**funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) viene restituito un handle per il thread. Per impostazione predefinita, questo handle dispone di diritti di accesso completi e, soggetto al controllo di accesso di sicurezza, può essere usato in qualsiasi funzione che accetta un handle di thread. Questo handle può essere ereditato dai processi figlio, a seconda del flag di ereditarietà specificato al momento della creazione. L'handle può essere duplicato [**da DuplicateHandle,**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)che consente di creare un handle di thread con un subset dei diritti di accesso. L'handle è valido fino alla chiusura, anche dopo che il thread che rappresenta è stato terminato.

Le [**funzioni CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**e CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) restituiscono anche un identificatore che identifica in modo univoco il thread in tutto il sistema. Un thread può usare la [**funzione GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) per ottenere il proprio identificatore di thread. Gli identificatori sono validi dal momento in cui viene creato il thread fino al termine del thread. Si noti che nessun identificatore di thread sarà mai 0.

Se si dispone di un identificatore di thread, è possibile ottenere l'handle del thread chiamando la [**funzione OpenThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) **OpenThread** consente di specificare i diritti di accesso dell'handle e se può essere ereditato.

Un thread può usare la [**funzione GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) per recuperare uno *pseudo handle* per il proprio oggetto thread. Questo pseudo handle è valido solo per il processo chiamante. non può essere ereditato o duplicato per l'uso da parte di altri processi. Per ottenere l'handle reale per il thread, dato uno pseudo handle, usare la [**funzione DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

Per enumerare i thread di un processo, usare le [**funzioni Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) [**e Thread32Next.**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next)

 

 
