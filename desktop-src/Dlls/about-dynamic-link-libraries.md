---
description: Il collegamento dinamico consente a un modulo di includere solo le informazioni necessarie per individuare una funzione DLL esportata in fase di caricamento o di esecuzione.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: Informazioni sulle librerie Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdb24048e17e9164aaf39d0ab337aea33576c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880018"
---
# <a name="about-dynamic-link-libraries"></a>Informazioni sulle librerie Dynamic-Link

Il collegamento dinamico consente a un modulo di includere solo le informazioni necessarie per individuare una funzione DLL esportata in fase di caricamento o di esecuzione. Il collegamento dinamico differisce dal collegamento statico più familiare, in cui il linker copia il codice di una funzione di libreria in ogni modulo che lo chiama.

## <a name="types-of-dynamic-linking"></a>Tipi di collegamento dinamico

Esistono due metodi per chiamare una funzione in una DLL:

-   Nel *collegamento dinamico in fase di caricamento*, un modulo effettua chiamate esplicite alle funzioni DLL esportate come se fossero funzioni locali. A tale scopo, è necessario collegare il modulo alla libreria di importazione per la DLL che contiene le funzioni. Una libreria di importazione fornisce al sistema le informazioni necessarie per caricare la DLL e individuare le funzioni DLL esportate quando viene caricata l'applicazione.
-   Nel *collegamento dinamico* in fase di esecuzione, un modulo usa la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) per caricare la dll in fase di esecuzione. Al termine del caricamento della DLL, il modulo chiama la funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere gli indirizzi delle funzioni DLL esportate. Il modulo chiama le funzioni DLL esportate usando i puntatori a funzione restituiti da **GetProcAddress**. In questo modo si elimina la necessità di una libreria di importazione.

## <a name="dlls-and-memory-management"></a>Dll e gestione della memoria

Ogni processo che carica la DLL ne esegue il mapping allo spazio degli indirizzi virtuali. Dopo che il processo ha caricato il file DLL nel relativo indirizzo virtuale, può chiamare le funzioni DLL esportate.

Il sistema mantiene un conteggio dei riferimenti per processo per ogni DLL. Quando un thread carica la DLL, il conteggio dei riferimenti viene incrementato di uno. Al termine del processo o quando il conteggio dei riferimenti diventa zero (solo collegamento dinamico in fase di esecuzione), la DLL viene scaricata dallo spazio degli indirizzi virtuali del processo.

Analogamente a qualsiasi altra funzione, una funzione DLL esportata viene eseguita nel contesto del thread che lo chiama. Pertanto, si applicano le condizioni seguenti:

-   I thread del processo che hanno chiamato la DLL possono usare gli handle aperti da una funzione di DLL. Analogamente, nella funzione DLL è possibile utilizzare gli handle aperti da qualsiasi thread del processo chiamante.
-   La DLL usa lo stack del thread chiamante e lo spazio degli indirizzi virtuali del processo chiamante.
-   La DLL alloca memoria dallo spazio degli indirizzi virtuali del processo chiamante.

Per ulteriori informazioni sulle dll, vedere gli argomenti seguenti:

-   [Vantaggi del collegamento dinamico](advantages-of-dynamic-linking.md)
-   [Creazione della libreria a collegamento dinamico](dynamic-link-library-creation.md)
-   [Funzione Entry-Point libreria a collegamento dinamico](dynamic-link-library-entry-point-function.md)
-   [Collegamento dinamico in fase di caricamento](load-time-dynamic-linking.md)
-   [Collegamento dinamico in fase di esecuzione](run-time-dynamic-linking.md)
-   [Ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md)
-   [Dati della libreria a collegamento dinamico](dynamic-link-library-data.md)
-   [Reindirizzamento libreria a collegamento dinamico](dynamic-link-library-redirection.md)
-   [Aggiornamenti della libreria a collegamento dinamico](dynamic-link-library-updates.md)
-   [Sicurezza della libreria a collegamento dinamico](dynamic-link-library-security.md)
-   [AppInit dll e avvio protetto](secure-boot-and-appinit-dlls.md)

 

 
