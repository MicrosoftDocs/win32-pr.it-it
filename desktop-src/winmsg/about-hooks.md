---
description: Questo argomento illustra come usare gli hook.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Panoramica degli hook
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10754f7275ce06c17b668e04c7792e6296a854fbe14a6ebc9544fbb70c73e9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201226"
---
# <a name="hooks-overview"></a>Panoramica degli hook

Un *hook* è un meccanismo tramite il quale un'applicazione può intercettare eventi, ad esempio messaggi, azioni del mouse e sequenze di tasti. Una funzione che intercetta un particolare tipo di evento è nota come *routine hook*. Una routine hook può agire su ogni evento ricevuto e quindi modificare o rimuovere l'evento.

L'esempio seguente usa per gli hook:

-   Monitorare i messaggi a scopo di debug
-   Fornire supporto per la registrazione e la riproduzione di macro
-   Fornire supporto per un tasto della Guida (F1)
-   Simulare l'input di mouse e tastiera
-   Implementare un'applicazione di training basato su computer (CBT)

> [!Note]  
> Gli hook tendono a rallentare il sistema perché aumentano la quantità di elaborazione che il sistema deve eseguire per ogni messaggio. È consigliabile installare un hook solo quando necessario e rimuoverlo appena possibile.

 

In questa sezione vengono illustrati gli elementi seguenti:

-   [Catene di hook](#hook-chains)
-   [Procedure hook](#hook-procedures)
-   [Tipi hook](#hook-types)
    -   [WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [WH \_ CBT](#wh_cbt)
    -   [WH \_ DEBUG](#wh_debug)
    -   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [WH \_ GETMESSAGE](#wh_getmessage)
    -   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [WH \_ JOURNALRECORD](#wh_journalrecord)
    -   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
    -   [TASTIERA \_ WH](#wh_keyboard)
    -   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
    -   [WH \_ MOUSE](#wh_mouse)
    -   [WH \_ MSGFILTER e WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [WH \_ SHELL](#wh_shell)

## <a name="hook-chains"></a>Catene di hook

Il sistema supporta molti tipi diversi di hook. ogni tipo fornisce l'accesso a un aspetto diverso del meccanismo di gestione dei messaggi. Ad esempio, un'applicazione può usare l'hook [ \_ MOUSE WH](#wh_mouse) per monitorare il traffico dei messaggi del mouse.

Il sistema mantiene una catena di hook separata per ogni tipo di hook. Una *catena di hook* è un elenco di puntatori a funzioni di callback speciali definite dall'applicazione denominate procedure *hook.* Quando si verifica un messaggio associato a un particolare tipo di hook, il sistema lo passa a ogni routine hook a cui si fa riferimento nella catena di hook, una dopo l'altra. L'azione che può essere eseguita da una procedura hook dipende dal tipo di hook interessato. Le procedure hook per alcuni tipi di hook possono monitorare solo i messaggi. altri utenti possono modificare i messaggi o arrestarne lo stato di avanzamento attraverso la catena, impedendo loro di raggiungere la procedura hook successiva o la finestra di destinazione.

## <a name="hook-procedures"></a>Procedure hook

Per sfruttare un particolare tipo di hook, lo sviluppatore fornisce una procedura hook e usa la [**funzione SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) per installarlo nella catena associata all'hook. Una routine hook deve avere la sintassi seguente:

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

Il *parametro nCode* è un codice hook utilizzato dalla routine hook per determinare l'azione da eseguire. Il valore del codice hook dipende dal tipo di hook. ogni tipo ha un proprio set di caratteristiche di codici hook. I valori dei *parametri wParam* e *lParam* dipendono dal codice hook, ma in genere contengono informazioni su un messaggio inviato o pubblicato.

La [**funzione SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) installa sempre una routine hook all'inizio di una catena di hook. Quando si verifica un evento monitorato da un particolare tipo di hook, il sistema chiama la routine all'inizio della catena di hook associata all'hook. Ogni routine hook nella catena determina se passare l'evento alla routine successiva. Una routine hook passa un evento alla routine successiva chiamando la [**funzione CallNextHookEx.**](/windows/win32/api/winuser/nf-winuser-callnexthookex)

Si noti che le procedure hook per alcuni tipi di hook possono monitorare solo i messaggi. il sistema passa messaggi a ogni routine hook, indipendentemente dal fatto che una particolare routine chiami [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex).

Un *hook globale* monitora i messaggi per tutti i thread nello stesso desktop del thread chiamante. Un *hook specifico del thread* monitora i messaggi solo per un singolo thread. Una routine hook globale può essere chiamata nel contesto di qualsiasi applicazione nello stesso desktop del thread chiamante, quindi la procedura deve essere in un modulo DLL separato. Una routine hook specifica del thread viene chiamata solo nel contesto del thread associato. Se un'applicazione installa una procedura hook per uno dei propri thread, la routine hook può essere nello stesso modulo del resto del codice dell'applicazione o in una DLL. Se l'applicazione installa una procedura hook per un thread di un'applicazione diversa, la procedura deve essere in una DLL. Per informazioni, vedere [Librerie a collegamento dinamico](../dlls/dynamic-link-libraries.md).

> [!Note]  
> È consigliabile usare hook globali solo a scopo di debug. In caso contrario, è consigliabile evitarli. Gli hook globali danneggiano le prestazioni del sistema e causano conflitti con altre applicazioni che implementano lo stesso tipo di hook globale.

 

## <a name="hook-types"></a>Tipi hook

Ogni tipo di hook consente a un'applicazione di monitorare un aspetto diverso del meccanismo di gestione dei messaggi del sistema. Le sezioni seguenti descrivono gli hook disponibili.

-   [WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [WH \_ CBT](#wh_cbt)
-   [WH \_ DEBUG](#wh_debug)
-   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [WH \_ GETMESSAGE](#wh_getmessage)
-   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [WH \_ JOURNALRECORD](#wh_journalrecord)
-   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
-   [TASTIERA \_ WH](#wh_keyboard)
-   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
-   [WH \_ MOUSE](#wh_mouse)
-   [WH \_ MSGFILTER e WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [WH \_ SHELL](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET

Gli hook **\_ WH CALLWNDPROC** e **WH \_ CALLWNDPROCRET** consentono di monitorare i messaggi inviati alle procedure della finestra. Il sistema chiama una routine hook **WH \_ CALLWNDPROC** prima di passare il messaggio alla routine della finestra ricevente e chiama la routine hook **WH \_ CALLWNDPROCRET** dopo che la routine della finestra ha elaborato il messaggio.

**L'hook \_ WH CALLWNDPROCRET** passa un puntatore a una [**struttura CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) alla routine hook. La struttura contiene il valore restituito dalla routine della finestra che ha elaborato il messaggio, nonché i parametri del messaggio associati al messaggio. La creazione di sottoclassi della finestra non funziona per i messaggi impostati tra processi.

Per altre informazioni, vedere le funzioni di callback [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) e [*CallWndRetProc.*](/windows/win32/api/winuser/nc-winuser-hookproc)

### <a name="wh_cbt"></a>WH \_ CBT

Il sistema chiama una procedura hook **\_ WH CBT** prima di attivare, creare, eliminare, ridurre al minimo, ottimizzare, spostare o ridimensionare una finestra; prima di completare un comando di sistema; prima di rimuovere un evento del mouse o della tastiera dalla coda dei messaggi di sistema; prima di impostare lo stato attivo di input o prima della sincronizzazione con la coda dei messaggi di sistema. Il valore restituito dalla routine hook determina se il sistema consente o impedisce una di queste operazioni. **L'hook \_ WH CBT** è destinato principalmente alle applicazioni CBT (Computer-Based Training).

Per altre informazioni, vedere la funzione di callback [*CBTProc.*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))

Per informazioni, vedere [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>WH \_ DEBUG

Il sistema chiama una routine hook **WH \_ DEBUG** prima di chiamare le routine hook associate a qualsiasi altro hook nel sistema. È possibile usare questo hook per determinare se consentire al sistema di chiamare routine hook associate ad altri tipi di hook.

Per altre informazioni, vedere la funzione di callback [*DebugProc.*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85))

### <a name="wh_foregroundidle"></a>WH \_ FOREGROUNDIDLE

**L'hook \_ WH FOREGROUNDIDLE** consente di eseguire attività con priorità bassa nei periodi in cui il thread in primo piano è inattivo. Il sistema chiama una routine hook **WH \_ FOREGROUNDIDLE** quando il thread in primo piano dell'applicazione sta per diventare inattivo.

Per altre informazioni, vedere la funzione di callback [*ForegroundIdleProc.*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85))

### <a name="wh_getmessage"></a>WH \_ GETMESSAGE

**L'hook \_ WH GETMESSAGE** consente a un'applicazione di monitorare i messaggi che devono essere restituiti dalla [**funzione GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) È possibile usare l'hook **WH \_ GETMESSAGE** per monitorare l'input da mouse e tastiera e altri messaggi inviati alla coda di messaggi.

Per altre informazioni, vedere la funzione di callback [*GetMsgProc.*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))

### <a name="wh_journalplayback"></a>WH \_ JOURNALPLAYBACK

**L'hook \_ WH JOURNALPLAYBACK** consente a un'applicazione di inserire messaggi nella coda di messaggi di sistema. È possibile usare questo hook per riprodurre una serie di eventi di mouse e tastiera registrati in precedenza usando [ \_ WH JOURNALRECORD](#wh_journalrecord). L'input normale da mouse e tastiera è disabilitato purché sia installato un hook **\_ WH JOURNALPLAYBACK.** Un hook **\_ WH JOURNALPLAYBACK** è un hook globale e non può essere usato come hook specifico del thread.

**L'hook \_ WH JOURNALPLAYBACK** restituisce un valore di timeout. Questo valore indica al sistema il numero di millisecondi di attesa prima di elaborare il messaggio corrente dall'hook di riproduzione. In questo modo l'hook può controllare l'intervallo degli eventi riprodotti.

Per altre informazioni, vedere la funzione di callback [*JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))

### <a name="wh_journalrecord"></a>WH \_ JOURNALRECORD

**L'hook \_ WH JOURNALRECORD** consente di monitorare e registrare gli eventi di input. In genere, questo hook viene usato per registrare una sequenza di eventi del mouse e della tastiera da riprodurre in un secondo momento usando [ \_ WH JOURNALPLAYBACK.](#wh_journalplayback) **L'hook \_ WH JOURNALRECORD** è un hook globale e non può essere usato come hook specifico del thread.

Per altre informazioni, vedere la funzione di callback [*JournalRecordProc.*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))

### <a name="wh_keyboard_ll"></a>WH \_ KEYBOARD \_ LL

**L'hook \_ WH KEYBOARD \_ LL** consente di monitorare gli eventi di input della tastiera che sta per essere inseriti in una coda di input del thread.

Per altre informazioni, vedere la funzione di callback [*LowLevelKeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85))

### <a name="wh_keyboard"></a>TASTIERA \_ WH

**L'hook \_ WH KEYBOARD** consente a un'applicazione di monitorare il traffico dei messaggi WM [**\_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) che sta per essere restituiti dalla [**funzione GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) È possibile usare l'hook **WH \_ KEYBOARD** per monitorare l'input da tastiera inviato a una coda di messaggi.

Per altre informazioni, vedere la funzione di callback [*KeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85))

### <a name="wh_mouse_ll"></a>WH \_ MOUSE \_ LL

**L'hook \_ WH MOUSE \_ LL** consente di monitorare gli eventi di input del mouse che sta per essere inseriti in una coda di input del thread.

Per altre informazioni, vedere la funzione di callback [*LowLevelMouseProc.*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85))

### <a name="wh_mouse"></a>WH \_ MOUSE

**L'hook \_ WH MOUSE** consente di monitorare i messaggi del mouse che devono essere restituiti dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) È possibile usare l'hook **WH \_ MOUSE** per monitorare l'input del mouse inviato a una coda di messaggi.

Per altre informazioni, vedere la funzione di callback [*MouseProc.*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ MSGFILTER e WH \_ SYSMSGFILTER

Gli hook **WH \_ MSGFILTER** e **WH \_ SYSMSGFILTER** consentono di monitorare i messaggi che devono essere elaborati da un menu, una barra di scorrimento, una finestra di messaggio o una finestra di dialogo e di rilevare quando sta per essere attivata un'altra finestra in seguito alla combinazione di tasti ALT+TAB o ALT+ESC dell'utente. **L'hook \_ WH MSGFILTER** può monitorare solo i messaggi passati a un menu, a una barra di scorrimento, a una finestra di messaggio o a una finestra di dialogo creata dall'applicazione che ha installato la procedura hook. **L'hook \_ WH SYSMSGFILTER** monitora tali messaggi per tutte le applicazioni.

Gli hook **WH \_ MSGFILTER** e **WH \_ SYSMSGFILTER** consentono di filtrare i messaggi durante i cicli modali equivalenti al filtro eseguito nel ciclo di messaggi principale. Ad esempio, un'applicazione esamina spesso un nuovo messaggio nel ciclo principale tra il momento in cui recupera il messaggio dalla coda e il momento in cui invia il messaggio, eseguendo un'elaborazione speciale in base alle esigenze. Tuttavia, durante un ciclo modale, il sistema recupera e invia i messaggi senza consentire a un'applicazione di filtrare i messaggi nel ciclo di messaggi principale. Se un'applicazione installa una procedura hook **WH \_ MSGFILTER** o **WH \_ SYSMSGFILTER,** il sistema chiama la procedura durante il ciclo modale.

Un'applicazione può chiamare **direttamente l'hook \_ WH MSGFILTER** chiamando la [**funzione CallMsgFilter.**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) Usando questa funzione, l'applicazione può usare lo stesso codice per filtrare i messaggi durante i cicli modali utilizzati nel ciclo di messaggi principale. A tale scopo, incapsulare le operazioni di filtro in una routine hook **WH \_ MSGFILTER** e chiamare **CallMsgFilter** tra le chiamate alle [**funzioni GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

L'ultimo argomento [**di CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) viene semplicemente passato alla routine hook. È possibile immettere qualsiasi valore. La routine hook, definendo una costante come **MSGF \_ MAINLOOP,** può usare questo valore per determinare da dove è stata chiamata la routine.

Per altre informazioni, vedere le funzioni di callback [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) [*e SysMsgProc.*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85))

### <a name="wh_shell"></a>WH \_ SHELL

Un'applicazione shell può usare **l'hook WH \_ SHELL** per ricevere notifiche importanti. Il sistema chiama una procedura hook **WH \_ SHELL** quando l'applicazione shell sta per essere attivata e quando viene creata o distrutta una finestra di primo livello.

Si noti che le applicazioni shell personalizzate non ricevono **messaggi WH \_ SHELL.** Pertanto, qualsiasi applicazione che registra se stessa come shell predefinita deve chiamare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) prima che (o qualsiasi altra applicazione) possa ricevere messaggi **WH \_ SHELL.** Questa funzione deve essere chiamata con **SPI \_ SETMINIMIZEDMETRICS** e una [**struttura MINIMIZEDMETRICS.**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) Impostare il **membro iArrange** di questa struttura su **ARW \_ HIDE**.

Per altre informazioni, vedere la funzione di callback [*ShellProc.*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))

 

 
