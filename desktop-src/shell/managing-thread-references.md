---
description: Questo articolo contiene informazioni sulla gestione dei riferimenti ai thread usando le funzioni delle funzioni di utilità della shell Lightweight.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Gestione dei riferimenti ai thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b629cd97c99e3b30e66810b5f54720d0dbb1c87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979991"
---
# <a name="managing-thread-references"></a>Gestione dei riferimenti ai thread

Questo articolo contiene informazioni sulla gestione dei riferimenti ai thread usando le funzioni delle funzioni di utilità della shell Lightweight.


Si verificano situazioni in cui un thread padre deve essere mantenuto attivo per la durata di un thread figlio. Se, ad esempio, un oggetto Component Object Model (COM) viene creato nel thread padre ed eseguito il marshalling al thread figlio, il thread padre non può terminare prima del thread figlio. A tale scopo, la shell fornisce queste funzioni.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Usare queste funzioni nel thread padre come descritto di seguito.

1.  Dichiarare una routine del thread definita dall'applicazione che segue il form della funzione [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) .

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  In [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))chiamare [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) per creare un riferimento al thread. In questo modo viene fornito un puntatore a un'istanza di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Questo **IUnknown** usa il valore a cui punta *pcRef* per mantenere un conteggio dei riferimenti. Finché il conteggio è maggiore di 0, il thread rimane attivo.
3.  Usando tale puntatore a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), chiamare [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) in [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)). In questo modo, il riferimento viene impostato in modo che le chiamate successive a [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) abbiano qualcosa da recuperare.
4.  Se il [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) crea un altro thread, il *ThreadProc* del thread può chiamare [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) con il puntatore a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ottenuto da [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref). In questo modo si incrementa il conteggio dei riferimenti a cui punta il parametro *pcRef* in **SHCreateThreadRef**.
5.  Creare il thread. Questa operazione viene in genere eseguita chiamando [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread), passando un puntatore a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) nel parametro *pfnThreadProc* . Passare anche il \_ \_ flag di riferimento del thread CTF nel parametro *dwFlags* . Il thread è attivo fino a quando *ThreadProc* è in esecuzione.
6.  Quando viene creato un thread figlio, passa il flag **CTF \_ ref \_ conteggiato** nel parametro *DwFlags* della chiamata al relativo [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  Quando i thread figlio vengono completati e vengono rilasciati, il valore a cui fa riferimento il *pcRef* del thread padre diminuisce. Una volta completati tutti i thread figlio, il [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) originale può completare e rilasciare il riferimento finale al thread, eliminando il conteggio dei riferimenti a 0. A questo punto, il riferimento al thread originale aperto da [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) viene rilasciato e il thread viene completato.

Un'altra funzione correlata è [**SHReleaseThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref). Questa funzione viene chiamata da [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) se il thread è stato creato usando [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) con il flag **di \_ \_ riferimento del thread CTF** . Tuttavia, *ThreadProc* non è necessario eseguire questa operazione in modo implicito. La chiamata a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ottenuta tramite [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) è tutto ciò che è necessario eseguire.

 

 
