---
description: Le funzioni seguenti vengono utilizzate nel collegamento dinamico.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Funzioni della libreria Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884902"
---
# <a name="dynamic-link-library-functions"></a>Funzioni della libreria Dynamic-Link

Le funzioni seguenti vengono utilizzate nel collegamento dinamico.



| Funzione                                                       | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Aggiunge una directory al percorso di ricerca della DLL del processo.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Disabilita le notifiche di connessione thread e scollegamento thread per la DLL specificata.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Un punto di ingresso facoltativo in una DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Decrementa il conteggio dei riferimenti della DLL caricata. Quando il conteggio dei riferimenti raggiunge zero, viene annullato il mapping del modulo dallo spazio degli indirizzi del processo chiamante. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Decrementa di uno il conteggio dei riferimenti di una DLL caricata, quindi chiama [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) per terminare il thread chiamante.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Recupera la parte specifica dell'applicazione del percorso di ricerca utilizzato per individuare le dll per l'applicazione.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Recupera il percorso completo del file contenente il modulo specificato.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Recupera il percorso completo del file contenente il modulo specificato.                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Recupera un handle di modulo per il modulo specificato.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Recupera un handle di modulo per il modulo specificato.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Recupera l'indirizzo di una funzione o una variabile esportata dalla DLL specificata.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Esegue il mapping del modulo eseguibile specificato nello spazio degli indirizzi del processo chiamante.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Esegue il mapping del modulo eseguibile specificato nello spazio degli indirizzi del processo chiamante.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Esegue il mapping del modulo incluso nel pacchetto specificato e delle relative dipendenze nello spazio degli indirizzi del processo chiamante. Questa funzione può essere chiamata solo dalle app di Windows Store.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Rimuove una directory aggiunta al percorso di ricerca della DLL di processo tramite [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Specifica un set predefinito di directory in cui eseguire la ricerca durante il caricamento di una DLL da parte del processo chiamante.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifica il percorso di ricerca utilizzato per individuare le dll per l'applicazione.                                                                                              |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Queste funzioni vengono fornite solo per la compatibilità con le versioni di Windows a 16 bit.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
