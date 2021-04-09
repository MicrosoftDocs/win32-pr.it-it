---
description: Quando un nuovo thread viene creato dalla funzione CreateThread o CreateRemoteThread, viene restituito un handle per il thread.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Handle di thread e identificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501d449bdb34d158ad14e52409967d4ef17f62f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881698"
---
# <a name="thread-handles-and-identifiers"></a>Handle di thread e identificatori

Quando un nuovo thread viene creato dalla funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) , viene restituito un handle per il thread. Per impostazione predefinita, questo handle dispone di diritti di accesso completi e, in base al controllo di accesso di sicurezza, può essere usato in qualsiasi funzione che accetta un handle di thread. Questo handle può essere ereditato dai processi figlio, a seconda del flag di ereditarietà specificato quando viene creato. L'handle può essere duplicato da [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle), che consente di creare un handle del thread con un subset dei diritti di accesso. L'handle è valido fino alla chiusura, anche dopo che il thread che rappresenta è stato terminato.

Anche le funzioni [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) e [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) restituiscono un identificatore che identifica in modo univoco il thread in tutto il sistema. Un thread può usare la funzione [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) per ottenere il proprio identificatore del thread. Gli identificatori sono validi dal momento in cui il thread viene creato fino a quando il thread non è stato terminato. Si noti che nessun identificatore del thread sarà mai 0.

Se si dispone di un identificatore di thread, è possibile ottenere l'handle del thread chiamando la funzione [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) . **OpenThread** consente di specificare i diritti di accesso dell'handle e se può essere ereditato.

Un thread può usare la funzione [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) per recuperare un *handle pseudo* per il proprio oggetto thread. Questo pseudo handle è valido solo per il processo chiamante. non può essere ereditato o duplicato per l'uso da altri processi. Per ottenere l'handle reale al thread, in base a uno pseudo handle, usare la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Per enumerare i thread di un processo, usare le funzioni [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) .

 

 
