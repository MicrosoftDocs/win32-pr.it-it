---
description: Il gestore di simboli è progettato per tenere traccia di diversi set di file di simboli.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inizializzazione del gestore di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126051"
---
# <a name="symbol-handler-initialization"></a>Inizializzazione del gestore di simboli

Il gestore di simboli è progettato per tenere traccia di diversi set di file di simboli.

Per inizializzare il gestore di simboli, chiamare la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Il parametro *hProcess* può essere un numero arbitrario univoco, un valore restituito dalla funzione [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o l'identificatore di qualsiasi processo in esecuzione. Il parametro *fInvadeProcess* indica se il gestore di simboli deve enumerare i moduli caricati dal processo e caricare i simboli per ogni modulo. Se *fInvadeProcess* è **true**, il parametro *hProcess* deve essere il valore restituito da **GetCurrentProcess** o l'identificatore di un processo esistente. Per aggiornare l'elenco, usare la funzione [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .

L'uso di *fInvadeProcess* è un modo semplice per caricare tutti i file di simboli per un processo. Tuttavia, il gestore di simboli non tenterà di caricare i simboli per i moduli caricati successivamente dalla funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . In questo caso, è necessario utilizzare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .

 

 
