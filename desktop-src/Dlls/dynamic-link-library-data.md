---
description: Una Dynamic-Link (DLL) può contenere dati globali o dati locali.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link dati della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8902eb6388624d958c7176a14b8893f8e2245ddd9370f6ba2ac71605b2379cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048441"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link dati della libreria

Una Dynamic-Link (DLL) può contenere dati globali o dati locali.

## <a name="variable-scope"></a>Ambito della variabile

Le variabili dichiarate come globali in un file di codice sorgente dll vengono considerate variabili globali dal compilatore e dal linker, ma ogni processo che carica una determinata DLL ottiene la propria copia delle variabili globali di tale DLL. L'ambito delle variabili statiche è limitato al blocco in cui vengono dichiarate le variabili statiche. Di conseguenza, per impostazione predefinita, ogni processo dispone di una propria istanza delle variabili statiche e globali della DLL.

> [!Note]  
> Gli strumenti di sviluppo possono consentire di eseguire l'override del comportamento predefinito. Ad esempio, il compilatore Visual C++ supporta la **\# sezione pragma** e il linker supporta l'opzione /SECTION. Per altre informazioni, vedere la documentazione inclusa con gli strumenti di sviluppo.

 

## <a name="dynamic-memory-allocation"></a>memoria dinamica allocazione

Quando una DLL alloca memoria usando una delle funzioni di allocazione di memoria ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)), la memoria viene allocata nello spazio degli indirizzi virtuali del processo chiamante ed è accessibile solo ai thread del processo.

Una DLL può usare il mapping dei file per allocare memoria che può essere condivisa tra i processi. Per una descrizione generale dell'uso del mapping dei file per creare una memoria condivisa denominata, vedere [Mapping dei file.](/windows/desktop/Memory/file-mapping) Per un esempio in cui viene utilizzata la funzione [**DllMain**](dllmain.md) per configurare la memoria condivisa usando il mapping dei file, vedere [Using Shared Memory in a Dynamic-Link Library](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>archiviazione thread-local

Le funzioni di archiviazione thread-local (TLS) consentono a una DLL di allocare un indice per l'archiviazione e il recupero di un valore diverso per ogni thread di un processo multithreading. Ad esempio, un'applicazione foglio di calcolo può creare una nuova istanza dello stesso thread ogni volta che l'utente apre un nuovo foglio di calcolo. Una DLL che fornisce le funzioni per varie operazioni del foglio di calcolo può usare TLS per salvare le informazioni sullo stato corrente di ogni foglio di calcolo (riga, colonna e così via). Per una descrizione generale dell'archiviazione thread-local, vedere [Thread Local Archiviazione](/windows/desktop/ProcThread/thread-local-storage). Per un esempio in cui viene utilizzata la funzione [**DllMain**](dllmain.md) per configurare l'archiviazione [thread-local,](using-thread-local-storage-in-a-dynamic-link-library.md)vedere Using Thread Local Archiviazione in a Dynamic-Link Library .

**Windows Server 2003 e Windows XP:** Il Visual C++ supporta una sintassi che consente di dichiarare variabili locali del thread: **\_ declspec(thread)**. Se si usa questa sintassi in una DLL, non sarà possibile caricare la DLL in modo esplicito usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) nelle versioni di Windows precedenti a Windows Vista. Se la DLL verrà caricata in modo esplicito, è necessario usare le funzioni di archiviazione thread-local anziché **\_ declspec(thread)**.

 

 
