---
description: Le funzioni seguenti vengono usate nel collegamento dinamico.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Dynamic-Link di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521c9200b3fa6585ec2804d76ac385845dcd6fb56ef4e7b70a7a3d9bd59150c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070581"
---
# <a name="dynamic-link-library-functions"></a>Dynamic-Link di libreria

Le funzioni seguenti vengono usate nel collegamento dinamico.



| Funzione                                                       | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Aggiunge una directory al percorso di ricerca della DLL del processo.                                                                                                               |
| [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Disabilita le notifiche di collegamento e disconnessione thread per la DLL specificata.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Punto di ingresso facoltativo in una DLL.                                                                                                                            |
| [**Freelibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Decrementa il conteggio dei riferimenti della DLL caricata. Quando il conteggio dei riferimenti raggiunge lo zero, il modulo viene rimosso dallo spazio indirizzi del processo chiamante. |
| [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Decrementa il conteggio dei riferimenti di una DLL caricata di una e quindi chiama [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) per terminare il thread chiamante.                       |
| [**GetDllDirectory**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Recupera la parte specifica dell'applicazione del percorso di ricerca usato per individuare le DLL per l'applicazione.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Recupera il percorso completo del file contenente il modulo specificato.                                                                               |
| [**GetModuleFileNameEx**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Recupera il percorso completo del file contenente il modulo specificato.                                                                               |
| [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Recupera un handle di modulo per il modulo specificato.                                                                                                            |
| [**GetModuleHandleEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Recupera un handle di modulo per il modulo specificato.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Recupera l'indirizzo di una funzione o di una variabile esportata dalla DLL specificata.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Mappe il modulo eseguibile specificato nello spazio degli indirizzi del processo chiamante.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Mappe il modulo eseguibile specificato nello spazio degli indirizzi del processo chiamante.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Mappe il modulo in pacchetto specificato e le relative dipendenze nello spazio degli indirizzi del processo chiamante. Solo Windows app di Store possono chiamare questa funzione.         |
| [**RemoveDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Rimuove una directory aggiunta al percorso di ricerca della DLL del processo usando [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Specifica un set predefinito di directory in cui eseguire la ricerca quando il processo chiamante carica una DLL.                                                                         |
| [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Modifica il percorso di ricerca usato per individuare le DLL per l'applicazione.                                                                                              |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Queste funzioni vengono fornite solo per la compatibilità con le versioni a 16 bit Windows.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
