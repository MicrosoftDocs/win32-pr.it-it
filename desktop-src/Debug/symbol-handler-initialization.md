---
description: Il gestore dei simboli è progettato per tenere traccia di vari set di file di simboli.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inizializzazione del gestore di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d3664a564b0198d97549f2815abebf0e5e6058beb197ed33ca191a64407f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406081"
---
# <a name="symbol-handler-initialization"></a>Inizializzazione del gestore di simboli

Il gestore dei simboli è progettato per tenere traccia di vari set di file di simboli.

Per inizializzare il gestore dei simboli, chiamare la [**funzione SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) Il *parametro hProcess* può essere un numero arbitrario univoco, un valore restituito dalla [**funzione GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o l'identificatore di qualsiasi processo in esecuzione. Il *parametro fInvadeProcess* indica se il gestore dei simboli deve enumerare i moduli caricati dal processo e caricare i simboli per ogni modulo. Se *fInvadeProcess* è **TRUE,** il *parametro hProcess* deve essere il valore restituito da **GetCurrentProcess** o l'identificatore di un processo esistente. Per aggiornare questo elenco, usare la [**funzione SymRefreshModuleList.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)

*L'uso di fInvadeProcess* è un modo semplice per caricare tutti i file di simboli per un processo. Tuttavia, il gestore dei simboli non tenterà di caricare i simboli per i moduli caricati successivamente dalla [**funzione LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) In questo caso è necessario usare la funzione [**SymLoadModuleEx.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)

 

 
