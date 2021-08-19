---
description: Il collegamento dinamico consente a un modulo di includere solo le informazioni necessarie per individuare una funzione DLL esportata in fase di caricamento o di esecuzione.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: Informazioni Dynamic-Link librerie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62e6a6a23315e915bd4a5a7fe6e2dcb54a9a2ebfbd66bf5d4ba7a2519a04576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815910"
---
# <a name="about-dynamic-link-libraries"></a>Informazioni Dynamic-Link librerie

Il collegamento dinamico consente a un modulo di includere solo le informazioni necessarie per individuare una funzione DLL esportata in fase di caricamento o di esecuzione. Il collegamento dinamico differisce dal collegamento statico più noto, in cui il linker copia il codice di una funzione di libreria in ogni modulo che la chiama.

## <a name="types-of-dynamic-linking"></a>Tipi di collegamento dinamico

Esistono due metodi per chiamare una funzione in una DLL:

-   Nel *collegamento dinamico in fase di* caricamento, un modulo effettua chiamate esplicite alle funzioni DLL esportate come se fossero funzioni locali. A questo scopo è necessario collegare il modulo alla libreria di importazione per la DLL che contiene le funzioni. Una libreria di importazione fornisce al sistema le informazioni necessarie per caricare la DLL e individuare le funzioni dll esportate quando l'applicazione viene caricata.
-   Nel *collegamento dinamico in fase* di esecuzione, un modulo usa la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) per caricare la DLL in fase di esecuzione. Dopo il caricamento della DLL, il modulo chiama la [**funzione GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere gli indirizzi delle funzioni DLL esportate. Il modulo chiama le funzioni DLL esportate usando i puntatori a funzione restituiti da **GetProcAddress**. In questo modo si elimina la necessità di una libreria di importazione.

## <a name="dlls-and-memory-management"></a>DLL e gestione della memoria

Ogni processo che carica la DLL ne esegue il mapping nello spazio indirizzi virtuale. Dopo aver caricato la DLL nel relativo indirizzo virtuale, il processo può chiamare le funzioni DLL esportate.

Il sistema mantiene un conteggio dei riferimenti per processo per ogni DLL. Quando un thread carica la DLL, il conteggio dei riferimenti viene incrementato di uno. Quando il processo termina o quando il conteggio dei riferimenti diventa zero (solo collegamento dinamico in fase di esecuzione), la DLL viene scaricata dallo spazio degli indirizzi virtuali del processo.

Come qualsiasi altra funzione, una funzione DLL esportata viene eseguita nel contesto del thread che la chiama. Di conseguenza, si applicano le condizioni seguenti:

-   I thread del processo che ha chiamato la DLL possono usare gli handle aperti da una funzione DLL. Analogamente, gli handle aperti da qualsiasi thread del processo chiamante possono essere usati nella funzione DLL.
-   La DLL usa lo stack del thread chiamante e lo spazio degli indirizzi virtuali del processo chiamante.
-   La DLL alloca memoria dallo spazio degli indirizzi virtuali del processo chiamante.

Per altre informazioni sulle DLL, vedere gli argomenti seguenti:

-   [Vantaggi del collegamento dinamico](advantages-of-dynamic-linking.md)
-   [Creazione di librerie a collegamento dinamico](dynamic-link-library-creation.md)
-   [Funzione dynamic-link library Entry-Point](dynamic-link-library-entry-point-function.md)
-   [Collegamento dinamico in fase di caricamento](load-time-dynamic-linking.md)
-   [Collegamento dinamico in fase di esecuzione](run-time-dynamic-linking.md)
-   [Ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md)
-   [Dati della libreria a collegamento dinamico](dynamic-link-library-data.md)
-   [Reindirizzamento della libreria a collegamento dinamico](dynamic-link-library-redirection.md)
-   [Aggiornamenti della libreria a collegamento dinamico](dynamic-link-library-updates.md)
-   [Sicurezza delle librerie a collegamento dinamico](dynamic-link-library-security.md)
-   [DLL AppInit e avvio protetto](secure-boot-and-appinit-dlls.md)

 

 
