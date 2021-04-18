---
description: Questo argomento descrive come usare gli hook.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Panoramica degli hook
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c5d89f111604418d1dc3ea9a4ebce6fe0a8124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315939"
---
# <a name="hooks-overview"></a>Panoramica degli hook

Un *hook* è un meccanismo mediante il quale un'applicazione può intercettare gli eventi, ad esempio i messaggi, le azioni del mouse e le sequenze di tasti. Una funzione che intercetta un particolare tipo di evento è nota come *routine hook*. Una routine hook può agire su ogni evento ricevuto, quindi modificare o eliminare l'evento.

Di seguito viene riportato un esempio di utilizzo di per hook:

-   Monitorare i messaggi a scopo di debug
-   Fornire supporto per la registrazione e la riproduzione di macro
-   Fornire supporto per un tasto guida (F1)
-   Simulare l'input del mouse e della tastiera
-   Implementare un'applicazione di training basata su computer (CBT)

> [!Note]  
> Gli hook tendono a rallentare il sistema perché aumentano la quantità di elaborazione che il sistema deve eseguire per ogni messaggio. È consigliabile installare un hook solo quando necessario e rimuoverlo appena possibile.

 

In questa sezione vengono descritte le operazioni seguenti:

-   [Catene di hook](#hook-chains)
-   [Procedure Hook](#hook-procedures)
-   [Tipi di hook](#hook-types)
    -   [WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [\_CBT WH](#wh_cbt)
    -   [DEBUG di WH \_](#wh_debug)
    -   [FOREGROUNDIDLE di WH \_](#wh_foregroundidle)
    -   [WH \_ GETmessage](#wh_getmessage)
    -   [JOURNALPLAYBACK di WH \_](#wh_journalplayback)
    -   [JOURNALRECORD di WH \_](#wh_journalrecord)
    -   [tastiera di WH \_ \_](#wh_keyboard_ll)
    -   [\_tastiera WH](#wh_keyboard)
    -   [WH \_ mouse \_ ll](#wh_mouse_ll)
    -   [\_mouse WH](#wh_mouse)
    -   [WH \_ msgfilter e WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [\_Shell WH](#wh_shell)

## <a name="hook-chains"></a>Catene di hook

Il sistema supporta molti tipi diversi di hook; ogni tipo fornisce l'accesso a un aspetto diverso del meccanismo di gestione dei messaggi. Ad esempio, un'applicazione può usare l' [hook \_ del mouse WH](#wh_mouse) per monitorare il traffico dei messaggi per i messaggi del mouse.

Il sistema mantiene una catena di hook separata per ogni tipo di hook. Una *catena di hook* è un elenco di puntatori a funzioni di callback speciali definite dall'applicazione denominate *routine hook*. Quando si verifica un messaggio associato a un particolare tipo di hook, il sistema passa il messaggio a ogni routine di hook a cui viene fatto riferimento nella catena di hook, una dopo l'altra. L'azione che può essere eseguita da una procedura hook dipende dal tipo di hook necessario. Le procedure hook per alcuni tipi di hook possono monitorare solo i messaggi; altri utenti possono modificare i messaggi o arrestarne lo stato di avanzamento attraverso la catena, impedendo loro di raggiungere la successiva routine hook o la finestra di destinazione.

## <a name="hook-procedures"></a>Procedure Hook

Per sfruttare i vantaggi di un particolare tipo di hook, lo sviluppatore fornisce una procedura di hook e usa la funzione [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) per installarla nella catena associata all'hook. Una routine hook deve avere la sintassi seguente:

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

*HookProc* è un segnaposto per un nome definito dall'applicazione.

Il parametro *nCode* è un codice hook usato dalla routine hook per determinare l'azione da eseguire. Il valore del codice hook dipende dal tipo di hook; ogni tipo ha un proprio set caratteristico di codici hook. I valori dei parametri *wParam* e *lParam* dipendono dal codice hook, ma in genere contengono informazioni su un messaggio inviato o inviato.

La funzione [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) installa sempre una routine hook all'inizio di una catena di hook. Quando si verifica un evento monitorato da un particolare tipo di hook, il sistema chiama la stored procedure all'inizio della catena di hook associata all'hook. Ogni routine hook nella catena determina se passare l'evento alla procedura successiva. Una routine hook passa un evento alla procedura successiva chiamando la funzione [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) .

Si noti che le procedure hook per alcuni tipi di hook possono monitorare solo i messaggi. il sistema passa i messaggi a ogni routine hook, indipendentemente dal fatto che una determinata procedura chiami [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex).

Un *hook globale* monitora i messaggi per tutti i thread nello stesso desktop del thread chiamante. Un *hook specifico del thread* monitora i messaggi solo per un singolo thread. Una procedura di hook globale può essere chiamata nel contesto di qualsiasi applicazione nello stesso desktop del thread chiamante, quindi la procedura deve trovarsi in un modulo DLL separato. Una routine hook specifica del thread viene chiamata solo nel contesto del thread associato. Se un'applicazione installa una routine di hook per uno dei propri thread, è possibile che la procedura di hook sia nello stesso modulo del resto del codice dell'applicazione o in una DLL. Se l'applicazione installa una procedura di hook per un thread di un'applicazione diversa, la stored procedure deve trovarsi in una DLL. Per informazioni, vedere [librerie a collegamento dinamico](../dlls/dynamic-link-libraries.md).

> [!Note]  
> È consigliabile utilizzare hook globali solo a scopo di debug; in caso contrario, è consigliabile evitarli. Gli hook globali danneggiano le prestazioni del sistema e provocano conflitti con altre applicazioni che implementano lo stesso tipo di hook globale.

 

## <a name="hook-types"></a>Tipi di hook

Ogni tipo di hook consente a un'applicazione di monitorare un aspetto diverso del meccanismo di gestione dei messaggi del sistema. Le sezioni seguenti descrivono i Hook disponibili.

-   [WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [\_CBT WH](#wh_cbt)
-   [DEBUG di WH \_](#wh_debug)
-   [FOREGROUNDIDLE di WH \_](#wh_foregroundidle)
-   [WH \_ GETmessage](#wh_getmessage)
-   [JOURNALPLAYBACK di WH \_](#wh_journalplayback)
-   [JOURNALRECORD di WH \_](#wh_journalrecord)
-   [tastiera di WH \_ \_](#wh_keyboard_ll)
-   [\_tastiera WH](#wh_keyboard)
-   [WH \_ mouse \_ ll](#wh_mouse_ll)
-   [\_mouse WH](#wh_mouse)
-   [WH \_ msgfilter e WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [\_Shell WH](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET

Gli **hook \_ CALLWNDPROC** e **WH \_ CALLWNDPROCRET** consentono di monitorare i messaggi inviati alle routine della finestra. Il sistema chiama una procedura di hook **\_ CALLWNDPROC di WH** prima di passare il messaggio alla routine della finestra ricevente e chiama la procedura hook **\_ CALLWNDPROCRET di WH** dopo che la routine della finestra ha elaborato il messaggio.

L' **hook \_ CALLWNDPROCRET di WH** passa un puntatore a una struttura [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) alla routine hook. La struttura contiene il valore restituito dalla routine della finestra che ha elaborato il messaggio, nonché i parametri del messaggio associati al messaggio. La sottoclasse della finestra non funziona per i messaggi impostati tra i processi.

Per ulteriori informazioni, vedere le funzioni di callback [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) e [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) .

### <a name="wh_cbt"></a>\_CBT WH

Il sistema chiama una procedura di hook del **\_ token** di rete prima di attivare, creare, eliminare, ridurre a icona, massimizzare, spostare o ridimensionare una finestra; prima di completare un comando di sistema, prima di rimuovere un evento del mouse o della tastiera dalla coda dei messaggi di sistema, prima di impostare lo stato attivo per l'input o prima della sincronizzazione con la coda messaggi di sistema. Il valore restituito dalla routine hook determina se il sistema consente o impedisce una di queste operazioni. L' **hook \_ CBT di WH** è destinato principalmente alle applicazioni di training basato su computer (CBT).

Per ulteriori informazioni, vedere la funzione di callback [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) .

Per informazioni, vedere [winEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>DEBUG di WH \_

Il sistema chiama una procedura di hook di **\_ debug WH** prima di chiamare le routine hook associate a qualsiasi altro hook nel sistema. È possibile utilizzare questo hook per determinare se consentire al sistema di chiamare le routine hook associate ad altri tipi di hook.

Per ulteriori informazioni, vedere la funzione di callback [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) .

### <a name="wh_foregroundidle"></a>FOREGROUNDIDLE di WH \_

L' **hook \_ FOREGROUNDIDLE di WH** consente di eseguire attività con priorità bassa durante i periodi in cui il thread in primo piano è inattivo. Il sistema chiama una procedura di hook **\_ FOREGROUNDIDLE di WH** quando il thread in primo piano dell'applicazione sta per diventare inattivo.

Per ulteriori informazioni, vedere la funzione di callback [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) .

### <a name="wh_getmessage"></a>WH \_ GETmessage

L'hook di **WH \_ GetMessage** consente a un'applicazione di monitorare i messaggi che stanno per essere restituiti dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . È possibile utilizzare l'hook di **WH \_ GetMessage** per monitorare l'input da mouse e tastiera e altri messaggi inviati alla coda di messaggi.

Per ulteriori informazioni, vedere la funzione di callback [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) .

### <a name="wh_journalplayback"></a>JOURNALPLAYBACK di WH \_

L'hook **WH \_ JOURNALPLAYBACK** consente a un'applicazione di inserire messaggi nella coda di messaggi di sistema. È possibile usare questo hook per riprodurre una serie di eventi di mouse e tastiera registrati in precedenza usando [WH \_ JOURNALRECORD](#wh_journalrecord). L'input del mouse e della tastiera normale è disabilitato fino a quando è installato un hook **\_ JOURNALPLAYBACK di WH** . Un **hook \_ JOURNALPLAYBACK di WH** è un hook globale, ma non può essere usato come hook specifico del thread.

L' **hook \_ JOURNALPLAYBACK di WH** restituisce un valore di timeout. Questo valore indica al sistema il numero di millisecondi di attesa prima dell'elaborazione del messaggio corrente dall'hook di riproduzione. Ciò consente all'hook di controllare la tempistica degli eventi riprodotti.

Per ulteriori informazioni, vedere la funzione di callback [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .

### <a name="wh_journalrecord"></a>JOURNALRECORD di WH \_

L' **hook \_ JOURNALRECORD di WH** consente di monitorare e registrare gli eventi di input. In genere, questo hook viene usato per registrare una sequenza di eventi di mouse e tastiera da riprodurre in un secondo momento usando [WH \_ JOURNALPLAYBACK](#wh_journalplayback). L' **hook \_ JOURNALRECORD di WH** è un hook globale, ma non può essere usato come hook specifico del thread.

Per ulteriori informazioni, vedere la funzione di callback [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) .

### <a name="wh_keyboard_ll"></a>tastiera di WH \_ \_

L'hook del tasto di scelta rapida di WH consente di monitorare gli eventi di input da tastiera che possono essere inseriti in una coda di input del thread. **\_ \_**

Per ulteriori informazioni, vedere la funzione di callback [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) .

### <a name="wh_keyboard"></a>\_tastiera WH

L'hook della **\_ tastiera WH** consente a un'applicazione di monitorare il traffico dei messaggi per i messaggi [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) e [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) che stanno per essere restituiti dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . È possibile usare l'hook della **\_ tastiera WH** per monitorare l'input da tastiera inserito in una coda di messaggi.

Per ulteriori informazioni, vedere la funzione di callback [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) .

### <a name="wh_mouse_ll"></a>WH \_ mouse \_ ll

L'hook del mouse di WH consente di monitorare gli eventi di input del mouse che stanno per essere inseriti in una coda di input del thread. **\_ \_**

Per ulteriori informazioni, vedere la funzione di callback [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) .

### <a name="wh_mouse"></a>\_mouse WH

L' **hook \_ del mouse di WH** consente di monitorare i messaggi del mouse che stanno per essere restituiti dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . È possibile utilizzare l'hook del **\_ mouse WH** per monitorare l'input del mouse inviato a una coda di messaggi.

Per ulteriori informazioni, vedere la funzione di callback [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) .

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ msgfilter e WH \_ SYSMSGFILTER

Gli hook **WH \_ msgfilter** e **WH \_ SYSMSGFILTER** consentono di monitorare i messaggi che verranno elaborati da un menu, una barra di scorrimento, una finestra di messaggio o una finestra di dialogo e per rilevare quando un'altra finestra sta per essere attivata a seguito della pressione della combinazione di tasti ALT + TAB o ALT + ESC. L' **hook \_ msgfilter di WH** può monitorare solo i messaggi passati a un menu, a una barra di scorrimento, a una finestra di messaggio o a una finestra di dialogo creata dall'applicazione che ha installato la procedura di hook. L' **hook \_ SYSMSGFILTER di WH** monitora tali messaggi per tutte le applicazioni.

Gli **hook \_ msgfilter** e **WH \_ SYSMSGFILTER** consentono di eseguire il filtro dei messaggi durante i cicli modali equivalenti al filtro eseguito nel ciclo di messaggi principale. Ad esempio, un'applicazione esamina spesso un nuovo messaggio nel ciclo principale tra il momento in cui recupera il messaggio dalla coda e il momento in cui invia il messaggio, eseguendo un'elaborazione speciale nel modo appropriato. Tuttavia, durante un ciclo modale, il sistema recupera e invia i messaggi senza consentire a un'applicazione di filtrare i messaggi nel relativo ciclo di messaggi principale. Se un'applicazione installa una routine di hook **\_ msgfilter** o **WH \_ SYSMSGFILTER** , il sistema chiama la procedura durante il ciclo modale.

Un'applicazione può chiamare direttamente l'hook **\_ msgfilter di WH** chiamando la funzione [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) . Utilizzando questa funzione, l'applicazione può utilizzare lo stesso codice per filtrare i messaggi durante i cicli modali utilizzati nel ciclo di messaggi principale. A tale scopo, incapsulare le operazioni di filtro in una procedura di hook **\_ msgfilter di WH** e chiamare **CallMsgFilter** tra le chiamate alle funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

L'ultimo argomento di [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) viene semplicemente passato alla routine hook; è possibile immettere qualsiasi valore. La routine hook, definendo una costante come **MSGF \_ MAINLOOP**, può utilizzare questo valore per determinare la posizione da cui è stata chiamata la stored procedure.

Per ulteriori informazioni, vedere le funzioni di callback [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) e [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) .

### <a name="wh_shell"></a>\_Shell WH

Un'applicazione shell può usare l'hook della **\_ Shell di WH** per ricevere notifiche importanti. Il sistema chiama una procedura di hook della **\_ Shell di WH** quando sta per essere attivata l'applicazione shell e quando viene creata o distrutta una finestra di primo livello.

Si noti che le applicazioni shell personalizzate non ricevono messaggi di **WH \_ Shell** . Pertanto, qualsiasi applicazione che si registra come shell predefinita deve chiamare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) prima che (o qualsiasi altra applicazione) possa ricevere messaggi **WH \_ Shell** . Questa funzione deve essere chiamata con **\_ SETMINIMIZEDMETRICS SPI** e una struttura [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) . Impostare il membro **iArrange** della struttura su **ARW \_ Hide**.

Per ulteriori informazioni, vedere la funzione di callback [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) .

 

 
