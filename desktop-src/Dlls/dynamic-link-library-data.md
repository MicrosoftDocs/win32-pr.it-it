---
description: Una libreria di Dynamic-Link (DLL) può contenere dati globali o dati locali.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dati della libreria Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83280d3bfc449061c44f9e8bfd9b47833e7eca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317822"
---
# <a name="dynamic-link-library-data"></a>Dati della libreria Dynamic-Link

Una libreria di Dynamic-Link (DLL) può contenere dati globali o dati locali.

## <a name="variable-scope"></a>Ambito della variabile

Le variabili dichiarate come globali in un file di codice sorgente DLL vengono considerate come variabili globali dal compilatore e dal linker, ma ogni processo che carica una determinata DLL ottiene la propria copia delle variabili globali di tale DLL. L'ambito delle variabili statiche è limitato al blocco in cui vengono dichiarate le variabili statiche. Di conseguenza, ogni processo ha una propria istanza delle variabili globali e statiche della DLL per impostazione predefinita.

> [!Note]  
> È possibile che gli strumenti di sviluppo consentano di eseguire l'override del comportamento predefinito. Ad esempio, il compilatore Visual C++ supporta la **\# sezione pragma** e il linker supporta l'opzione/section. Per ulteriori informazioni, vedere la documentazione inclusa con gli strumenti di sviluppo.

 

## <a name="dynamic-memory-allocation"></a>Allocazione memoria dinamica

Quando una DLL alloca memoria utilizzando una delle funzioni di allocazione della memoria ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)), la memoria viene allocata nello spazio degli indirizzi virtuali del processo chiamante ed è accessibile solo ai thread di tale processo.

Una DLL può usare il mapping dei file per allocare memoria che può essere condivisa tra i processi. Per informazioni generali su come usare il mapping dei file per creare una memoria condivisa denominata, vedere [mapping di file](/windows/desktop/Memory/file-mapping). Per un esempio in cui viene utilizzata la funzione [**DllMain**](dllmain.md) per configurare la memoria condivisa utilizzando il mapping dei file, vedere [utilizzo della memoria condivisa in una libreria di Dynamic-Link](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>archiviazione thread-local

Le funzioni di archiviazione locale di thread (TLS) consentono a una DLL di allocare un indice per l'archiviazione e il recupero di un valore diverso per ogni thread di un processo multithread. Ad esempio, un'applicazione del foglio di calcolo può creare una nuova istanza dello stesso thread ogni volta che l'utente apre un nuovo foglio di calcolo. Una DLL che fornisce le funzioni per varie operazioni di fogli di calcolo può utilizzare TLS per salvare informazioni sullo stato corrente di ogni foglio di calcolo (riga, colonna e così via). Per informazioni generali sull'archiviazione thread-local, vedere [archiviazione locale di thread](/windows/desktop/ProcThread/thread-local-storage). Per un esempio in cui viene utilizzata la funzione [**DllMain**](dllmain.md) per configurare l'archiviazione thread-local, vedere [utilizzo dell'archiviazione locale di thread in una libreria di Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 e Windows XP:** Il compilatore Visual C++ supporta una sintassi che consente di dichiarare variabili locali del thread: **\_ declspec (thread)**. Se si utilizza questa sintassi in una DLL, non sarà possibile caricare la DLL in modo esplicito utilizzando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) nelle versioni di Windows precedenti a Windows Vista. Se la DLL viene caricata in modo esplicito, è necessario usare le funzioni di archiviazione locale di thread invece di **\_ declspec (thread)**.

 

 
