---
description: Un processo figlio può ereditare diverse proprietà e risorse dal processo padre.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Ereditarietà (processi e thread)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713fe398360b510fab3c66f5cf74dc07b642dac
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300659"
---
# <a name="inheritance"></a>Ereditarietà

Un processo figlio può ereditare diverse proprietà e risorse dal processo padre. È anche possibile impedire a un processo figlio di ereditare le proprietà dal processo padre. È possibile ereditare quanto segue:

-   Handle aperti restituiti dalla funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Sono inclusi gli handle per i file, i buffer di input della console, i buffer dello schermo della console, le named pipe, i dispositivi di comunicazione seriale e mailslot.
-   Apre gli handle per elaborare, thread, mutex, Event, Semaphore, named pipe, Anonymous-pipe e oggetti di mapping di file. Tali funzioni vengono restituite rispettivamente dalle funzioni [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa), [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea), [**non**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)e [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) .
-   Variabili di ambiente.
-   La directory corrente.
-   La console, a meno che il processo non venga scollegato o venga creata una nuova console. Un processo della console figlio può anche ereditare gli handle standard del padre, nonché l'accesso al buffer di input e al buffer dello schermo attivo.
-   Modalità di errore, impostata dalla funzione [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) .
-   Maschera di affinità del processore.
-   Associazione a un processo.

Il processo figlio non eredita quanto segue:

-   Classe priority.
-   Handle restituiti da [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)e [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc).
-   Pseudo-handle, come negli handle restituiti dalla funzione [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) . Questi handle sono validi solo per il processo chiamante.
-   Handle del modulo DLL restituiti dalla funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .
-   Handle GDI o utente, ad esempio **HBITMAP** o **HMENU**.

## <a name="inheriting-handles"></a>Handle di ereditarietà

Un processo figlio può ereditare alcuni degli handle del padre, ma non ereditarne altri. Per far sì che un handle venga ereditato, è necessario eseguire due operazioni:

-   Consente di specificare che l'handle deve essere ereditato quando si crea, si apre o si duplica l'handle. Per questo scopo, le funzioni di creazione usano in genere il membro **bInheritHandle** di una struttura di [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) usa il parametro *bInheritHandles* .
-   Consente di specificare che gli handle ereditabili devono essere ereditati impostando il parametro *bInheritHandles* su true quando si chiama la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Inoltre, per ereditare l'input standard, l'output standard e gli handle di errore standard, il membro **dwFlags** della struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) deve includere STARTF \_ USESTDHANDLES.

Per specificare un elenco degli handle che devono essere ereditati da un processo figlio specifico, chiamare la funzione [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) con il flag *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* .

Un handle ereditato fa riferimento allo stesso oggetto nel processo figlio come nel processo padre. Ha anche lo stesso valore e i privilegi di accesso. Pertanto, quando un processo modifica lo stato dell'oggetto, la modifica ha effetto su entrambi i processi. Per utilizzare un handle, è necessario che il processo figlio recuperi il valore dell'handle e "conosca" l'oggetto a cui fa riferimento. In genere, il processo padre comunica queste informazioni al processo figlio tramite la riga di comando, il blocco dell'ambiente o una forma di [comunicazione interprocesso](/windows/desktop/ipc/interprocess-communications).

Utilizzare la funzione [**SetHandleInformation**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) per controllare se un handle esistente è ereditabile o meno.

## <a name="inheriting-environment-variables"></a>Ereditarietà delle variabili di ambiente

Per impostazione predefinita, un processo figlio eredita le variabili di ambiente del processo padre. Tuttavia, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente al processo padre di specificare un blocco diverso di variabili di ambiente. Per altre informazioni, vedere [variabili di ambiente](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Eredità della directory corrente

La funzione [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) recupera la directory corrente del processo chiamante. Per impostazione predefinita, un processo figlio eredita la directory corrente del processo padre. Tuttavia, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente al processo padre di specificare una directory corrente diversa per il processo figlio. Per modificare la directory corrente del processo chiamante, usare la funzione [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) .
