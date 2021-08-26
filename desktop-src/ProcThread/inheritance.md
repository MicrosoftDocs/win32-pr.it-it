---
description: Un processo figlio può ereditare diverse proprietà e risorse dal processo padre.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Ereditarietà (processi e thread)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f50b191ee24783f7213ac15f61c435ebd696175a3042d79e2f359ef61097fe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032591"
---
# <a name="inheritance"></a>Ereditarietà

Un processo figlio può ereditare diverse proprietà e risorse dal processo padre. È anche possibile impedire a un processo figlio di ereditare le proprietà dal processo padre. È possibile ereditare quanto segue:

-   Handle aperti restituiti dalla [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Sono inclusi handle per file, buffer di input della console, buffer dello schermo della console, named pipe, dispositivi di comunicazione seriale e mailslot.
-   Handle aperti per oggetti di elaborazione, thread, mutex, evento, semaforo, named pipe, pipe anonima e mapping di file. Vengono restituiti rispettivamente dalle funzioni [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa), [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea), [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)e [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) .
-   Variabili di ambiente.
-   La directory corrente.
-   La console, a meno che il processo non venga scollegato o non venga creata una nuova console. Un processo console figlio può anche ereditare gli handle standard dell'elemento padre, nonché l'accesso al buffer di input e al buffer dello schermo attivo.
-   Modalità di errore, come impostato dalla [**funzione SetErrorMode.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode)
-   Maschera di affinità del processore.
-   Associazione a un processo.

Il processo figlio non eredita quanto segue:

-   Classe di priorità.
-   Handle restituiti [**da LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)e [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc).
-   Pseudo handle, come negli handle restituiti dalla [**funzione GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) [**o GetCurrentThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) Questi handle sono validi solo per il processo chiamante.
-   Handle del modulo DLL restituiti [**dalla funzione LoadLibrary.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
-   Handle GDI o USER, ad esempio **HBITMAP** o **HMENU.**

## <a name="inheriting-handles"></a>Ereditarietà degli handle

Un processo figlio può ereditare alcuni degli handle del relativo elemento padre, ma non ereditarne altri. Per fare in modo che un handle sia ereditato, è necessario eseguire due operazioni:

-   Specificare che l'handle deve essere ereditato quando si crea, apre o duplica l'handle. Le funzioni di creazione usano **in genere il membro bInheritHandle** di una struttura SECURITY [**\_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) a questo scopo. [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) usa il *parametro bInheritHandles.*
-   Specificare che gli handle ereditabili devono essere ereditati impostando il *parametro bInheritHandles* su TRUE quando si chiama la [**funzione CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Inoltre, per ereditare l'input standard, l'output standard e gli handle di errore standard, il membro **dwFlags** della struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) deve includere STARTF \_ USESTDHANDLES.

Per specificare un elenco degli handle che devono essere ereditati da un processo figlio specifico, chiamare la [**funzione UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) con il *flag* PROC_THREAD_ATTRIBUTE_HANDLE_LIST.

Un handle ereditato fa riferimento allo stesso oggetto nel processo figlio come nel processo padre. Ha anche lo stesso valore e gli stessi privilegi di accesso. Pertanto, quando un processo modifica lo stato dell'oggetto , la modifica influisce su entrambi i processi. Per usare un handle, il processo figlio deve recuperare il valore dell'handle e "conoscere" l'oggetto a cui fa riferimento. In genere, il processo padre comunica queste informazioni al processo figlio tramite la riga di comando, il blocco di ambiente o una qualche forma di [comunicazione interprocesso.](/windows/desktop/ipc/interprocess-communications)

Usare la [**funzione SetHandleInformation**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) per controllare se un handle esistente è ereditabile o meno.

## <a name="inheriting-environment-variables"></a>Ereditarietà delle variabili di ambiente

Un processo figlio eredita le variabili di ambiente del processo padre per impostazione predefinita. Tuttavia, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente al processo padre di specificare un blocco diverso di variabili di ambiente. Per altre informazioni, vedere [Variabili di ambiente](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Ereditarietà della directory corrente

La [**funzione GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) recupera la directory corrente del processo chiamante. Un processo figlio eredita la directory corrente del processo padre per impostazione predefinita. Tuttavia, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente al processo padre di specificare una directory corrente diversa per il processo figlio. Per modificare la directory corrente del processo chiamante, usare la [**funzione SetCurrentDirectory.**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory)
