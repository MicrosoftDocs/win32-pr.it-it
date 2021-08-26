---
description: Sono disponibili diverse funzioni per ottenere informazioni sui processi.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Recupero di informazioni aggiuntive sui processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98b4ed87fca02dfcee4cbcd36621fffb9920a3f320cfeac771507748a151cf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032121"
---
# <a name="obtaining-additional-process-information"></a>Recupero di informazioni aggiuntive sui processi

Sono disponibili diverse funzioni per ottenere informazioni sui processi. Alcune di queste funzioni possono essere usate solo per il processo chiamante, perché non accettano un handle di processo come parametro. È possibile usare funzioni che accettano un handle di processo per ottenere informazioni su altri processi.

-   Per ottenere la stringa della riga di comando per il processo corrente, usare la [**funzione GetCommandLine.**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)
-   Per recuperare la [**struttura STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) specificata al momento della creazione del processo corrente, usare la [**funzione GetStartupInfo.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)
-   Per ottenere le informazioni sulla versione dall'intestazione eseguibile, usare la [**funzione GetProcessVersion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)
-   Per ottenere il percorso completo e il nome del file eseguibile contenente il codice del processo, usare la [**funzione GetModuleFileName.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
-   Per ottenere il numero di handle per gli oggetti dell'interfaccia utente grafica (GUI) in uso, usare la [**funzione GetGuiResources.**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)
-   Per determinare se è in corso il debug di un processo, usa la [**funzione IsDebuggerPresent.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
-   Per recuperare le informazioni di accounting per tutte le operazioni di I/O eseguite dal processo, usare la [**funzione GetProcessIoCounters.**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)

 

 
