---
description: Il gestore dei simboli carica i simboli quando chiami la funzione SymInitialize con il parametro fInvadeProcess impostato su TRUE o quando chiami la funzione SymLoadModuleEx per specificare un modulo.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Caricamento dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1459f0fd05b490730739852b77edd29df38c04cbe246699552a53b7e30decf11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912363"
---
# <a name="symbol-loading"></a>Caricamento dei simboli

Il gestore dei simboli carica i simboli quando chiami la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con il parametro *fInvadeProcess* impostato su **TRUE** o quando chiami la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) per specificare un modulo. In entrambi i casi, il gestore dei simboli carica i simboli o rinvia il caricamento dei simboli fino a quando non vengono richiesti, a seconda delle opzioni impostate dalla [**funzione SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)

Il gestore dei simboli può essere usato per recuperare informazioni simboliche per qualsiasi modulo. non deve essere associato a un processo specificato nella [**chiamata a SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) Per usare un modulo arbitrario, specificare il percorso completo dell'immagine del modulo nel *parametro ImageName.* È possibile usare un percorso a qualsiasi modulo eseguibile con informazioni di debug (.exe, .dll, drv, .sys, scr, .cpl o com). Usare il *parametro BaseOfDll* per specificare qualsiasi indirizzo di carico, quindi gli indirizzi dei simboli saranno basati su tale indirizzo.

Potrebbe non essere necessario mantenere un modulo di simboli caricato per tutta la durata di un'applicazione. Per rilasciare il modulo simbolo dall'elenco di moduli del gestore dei simboli, usare la [**funzione SymUnloadModule64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) Questa funzione rilascia la memoria allocata per il modulo dei simboli. Per usare di nuovo i simboli per il modulo, è necessario chiamare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) anche se è impostata l'opzione di caricamento posticipato dei simboli.

## <a name="diagnosing-symbol-load-problems"></a>Diagnosi dei problemi di caricamento dei simboli

Per visualizzare tutti i tentativi di caricamento dei simboli, [**chiamare SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT \_ DEBUG. In questo modo DbgHelp chiama la funzione [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) con informazioni dettagliate sulle ricerche di simboli, ad esempio le directory in cui viene eseguita la ricerca e i messaggi di errore. Se il codice usa [**SymRegisterCallback64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)DbgHelp chiamerà la funzione di callback anziché **OutputDebugString.** Il *parametro ActionCode* è impostato su CBA \_ DEBUG INFO e il parametro \_ *CallbackData* è una stringa che può essere visualizzata.

Per consentire la visualizzazione dell'output di debug nella console senza modificare il codice sorgente, impostare la variabile di ambiente DBGHELP DBGOUT su un valore diverso da NULL prima di chiamare la funzione \_ [**SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  Per registrare le informazioni in un file, impostare la variabile di ambiente DBGHELP LOG sul \_ nome del file di log da usare.

Si noti che queste funzionalità devono essere usate solo quando necessario. Possono rallentare il caricamento dei simboli dei moduli che contengono molti simboli.

 

 
