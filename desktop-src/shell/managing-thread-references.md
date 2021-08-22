---
description: Questo articolo contiene informazioni sulla gestione dei riferimenti ai thread usando le funzioni delle funzioni lightweight di Shell.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Gestione dei riferimenti ai thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6380957f5f8ef9be62e291820fe12d715f31a5f5bb5ba81b80aa1c8606478e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968920"
---
# <a name="managing-thread-references"></a>Gestione dei riferimenti ai thread

Questo articolo contiene informazioni sulla gestione dei riferimenti ai thread usando le funzioni delle funzioni lightweight di Shell.


Le situazioni si verificano quando un thread padre deve essere mantenuto attivo per la durata di un thread figlio. Ad esempio, se un oggetto Component Object Model (COM) viene creato nel thread padre ed è stato effettuato il marshalling nel thread figlio, tale thread padre non può terminare prima del thread figlio. A tale scopo, Shell fornisce queste funzioni.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Usare queste funzioni nel thread padre, come descritto di seguito.

1.  Dichiarare una routine di thread definita dall'applicazione sotto forma di [*funzione ThreadProc.*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  In [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))chiamare [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) per creare un riferimento al thread. Fornisce un puntatore a un'istanza di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Questo **IUnknown usa** il valore a cui punta *pcRef* per mantenere un conteggio dei riferimenti. Finché questo conteggio è maggiore di 0, il thread rimane attivo.
3.  Usando tale puntatore [**a IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), chiamare [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) in [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)). In questo modo il riferimento viene impostato in modo che le chiamate successive [**a SHGetThreadRef hanno**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) qualcosa da recuperare.
4.  Se [*ThreadProc crea*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) un altro thread, *threadProc* del thread può chiamare [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) con il puntatore a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ottenuto da [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref). In questo modo viene incrementato il conteggio dei riferimenti a cui punta *il parametro pcRef* in **SHCreateThreadRef**.
5.  Creare il thread. Questa operazione viene in genere eseguita chiamando [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread), passando un puntatore a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) nel *parametro pfnThreadProc.* Passare anche il flag CTF \_ THREAD REF nel parametro \_ *dwFlags.* Il thread è attivo fino a quando *ThreadProc* è in esecuzione.
6.  Quando viene creato un thread figlio, passare il flag **CTF \_ REF \_ COUNTED** nel *parametro dwFlags* nella chiamata a [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  Quando i thread figlio vengono completati e rilasciati, il valore a cui punta *il pcRef* del thread padre diminuisce. Al termine di tutti i thread figlio, [*threadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) originale può completare e rilasciare il riferimento finale del thread, eliminando il conteggio dei riferimenti a 0. A questo punto, viene rilasciato il riferimento al thread originale aperto da [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) e il thread viene completato.

Un'altra funzione correlata [**è SHReleaseThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref). Questa funzione viene chiamata da [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) se il thread è stato creato usando [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) con il flag **REF \_ THREAD \_ CTF.** Tuttavia, *ThreadProc* non è necessario per eseguire questa operazione in modo implicito. Chiamare [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore [**a IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ottenuto tramite [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) è tutto ciò che deve essere eseguito.

 

 
