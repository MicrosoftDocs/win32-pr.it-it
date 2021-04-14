---
description: Il gestore di simboli caricherà i simboli quando si chiama la funzione SymInitialize con il parametro fInvadeProcess impostato su TRUE o quando si chiama la funzione SymLoadModuleEx per specificare un modulo.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Caricamento simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705a7af3525c784b2bbcd512b267309a466a11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401376"
---
# <a name="symbol-loading"></a>Caricamento simboli

Il gestore di simboli caricherà i simboli quando si chiama la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con il parametro *FInvadeProcess* impostato su **true** o quando si chiama la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) per specificare un modulo. In entrambi i casi, il gestore di simboli carica i simboli o rinvia il caricamento dei simboli fino a quando non vengono richiesti i simboli, a seconda delle opzioni impostate dalla funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

Il gestore di simboli può essere usato per recuperare informazioni sui simboli per qualsiasi modulo; non è necessario che sia associato a un processo specificato nella chiamata [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Per usare un modulo arbitrario, specificare il percorso completo dell'immagine del modulo nel parametro *ImageName* . È possibile usare un percorso per qualsiasi modulo eseguibile con informazioni di debug (exe, dll, DRV, sys, SCR, cpl o com). Usare il parametro *BaseOfDll* per specificare un indirizzo di caricamento, quindi gli indirizzi dei simboli saranno basati su tale indirizzo.

Potrebbe non essere necessario tenere un modulo dei simboli caricato per tutta la durata di un'applicazione. Per rilasciare il modulo Symbol dall'elenco dei moduli del gestore di simboli, usare la funzione [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) . Questa funzione rilascia la memoria allocata per il modulo symbol. Per usare nuovamente i simboli per il modulo, è necessario chiamare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) anche se è impostata l'opzione di caricamento posticipato del simbolo.

## <a name="diagnosing-symbol-load-problems"></a>Diagnosi dei problemi di caricamento dei simboli

Per visualizzare tutti i tentativi di caricamento dei simboli, chiamare [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT \_ debug. Questo fa in modo che DbgHelp chiami la funzione [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) con informazioni dettagliate sulle ricerche di simboli, ad esempio le directory in cui è in corso la ricerca e i messaggi di errore. Se il codice usa [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback), dbghelp chiamerà la funzione di callback anziché chiamare **OutputDebugString**. Il parametro *ActionCode* è impostato su CBA \_ debug \_ info e il parametro *CallbackData* è una stringa che può essere visualizzata.

Per consentire la visualizzazione di questo output di debug nella console senza modificare il codice sorgente, impostare la \_ variabile di ambiente dbghelp DBGOUT su un valore non **null** prima di chiamare la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Per registrare le informazioni in un file, impostare la \_ variabile di ambiente log dbghelp sul nome del file di log da utilizzare.

Si noti che queste funzionalità devono essere usate solo quando necessario. Potrebbero rallentare il caricamento dei simboli dei moduli che contengono molti simboli.

 

 
