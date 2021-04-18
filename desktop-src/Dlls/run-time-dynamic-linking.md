---
description: Quando l'applicazione chiama le funzioni LoadLibrary o LoadLibraryEx, il sistema tenta di individuare la DLL. per informazioni dettagliate, vedere Dynamic-Link ordine di ricerca della libreria.
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Collegamento dinamico Run-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308380"
---
# <a name="run-time-dynamic-linking"></a>Collegamento dinamico Run-Time

Quando l'applicazione chiama le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , il sistema tenta di individuare la dll. per informazioni dettagliate, vedere l'ordine di ricerca della [libreria a collegamento dinamico](dynamic-link-library-search-order.md). Se la ricerca ha esito positivo, il sistema esegue il mapping del modulo DLL allo spazio degli indirizzi virtuali del processo e incrementa il conteggio dei riferimenti. Se la chiamata a **LoadLibrary** o **LOADLIBRARYEX** specifica una dll il cui codice è già stato mappato nello spazio degli indirizzi virtuali del processo chiamante, la funzione restituisce semplicemente un handle per la dll e incrementa il conteggio dei riferimenti alla dll. Si noti che due DLL con lo stesso nome e l'estensione di file di base, ma che si trovano in directory diverse, non sono considerate uguali.

Il sistema chiama la funzione del punto di ingresso nel contesto del thread che ha chiamato [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). La funzione del punto di ingresso non viene chiamata se la DLL è già stata caricata dal processo tramite una chiamata a **LoadLibrary** o **LoadLibraryEx** senza una chiamata corrispondente alla funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

Se il sistema non riesce a trovare la DLL o se la funzione del punto di ingresso restituisce FALSE, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) restituisce null. Se **LoadLibrary** o **LoadLibraryEx** ha esito positivo, restituisce un handle per il modulo dll. Il processo può utilizzare questo handle per identificare la DLL in una chiamata alla funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)o [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) .

La funzione [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) restituisce un handle utilizzato in [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)o [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). La funzione **GetModuleHandle** ha esito positivo solo se è già stato eseguito il mapping del modulo dll nello spazio degli indirizzi del processo tramite il collegamento della fase di caricamento o una chiamata precedente a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Diversamente da **LoadLibrary** o **LoadLibraryEx**, **GetModuleHandle** non incrementa il conteggio dei riferimenti del modulo. La funzione [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) Recupera il percorso completo del modulo associato a un handle restituito da **GetModuleHandle**, **LoadLibrary** o **LoadLibraryEx**.

Il processo può usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere l'indirizzo di una funzione esportata nella dll usando un handle di modulo DLL restituito da [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

Quando il modulo DLL non è più necessario, il processo può chiamare [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) o [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Queste funzioni decrementano il conteggio dei riferimenti al modulo e annullare il codice DLL dallo spazio degli indirizzi virtuali del processo se il conteggio dei riferimenti è pari a zero.

Il collegamento dinamico in fase di esecuzione consente di continuare l'esecuzione del processo anche se non è disponibile una DLL. Il processo può quindi utilizzare un metodo alternativo per completare l'obiettivo. Se, ad esempio, un processo non è in grado di individuare una DLL, può provare a utilizzarne un'altra o può inviare una notifica all'utente di un errore. Se l'utente è in grado di fornire il percorso completo della DLL mancante, il processo può utilizzare queste informazioni per caricare la DLL anche se non si trova nel percorso di ricerca normale. Questa situazione si differenzia dal collegamento del tempo di caricamento, in cui il sistema termina semplicemente il processo se non riesce a trovare la DLL.

Il collegamento dinamico in fase di esecuzione può causare problemi se la DLL usa la funzione [**DllMain**](dllmain.md) per eseguire l'inizializzazione per ogni thread di un processo, perché il punto di ingresso non viene chiamato per i thread esistenti prima della chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o a [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Per un esempio che illustra come gestire questo problema, vedere [uso dell'archiviazione locale di thread in una libreria di Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del collegamento dinamico in fase di esecuzione](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
