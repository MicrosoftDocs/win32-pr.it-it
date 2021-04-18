---
UID: ''
title: Funzione di callback ShellProc
description: La funzione riceve le notifiche degli eventi della shell dal sistema.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299556"
---
# <a name="shellproc-function"></a>ShellProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
La funzione riceve le notifiche degli eventi della shell dal sistema.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**ShellProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Codice hook.
Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | Lo stato di accessibilità è stato modificato. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | La shell deve attivare la finestra principale. |
| **HSHELL_APPCOMMAND** 12 | L'utente ha completato un evento di input (ad esempio, ha premuto un pulsante di comando dell'applicazione sul mouse o un tasto di comando dell'applicazione sulla tastiera) e l'applicazione non ha gestito il messaggio [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) generato da tale input. Se la routine della shell gestisce il messaggio di [WM_COMMAND](/windows/desktop/menurc/wm-command) , non deve chiamare **CallNextHookEx**. Per ulteriori informazioni, vedere la sezione valore restituito. |
| **HSHELL_GETMINRECT** 5 | Una finestra viene ridotta A icona o ingrandita. Il sistema richiede le coordinate del rettangolo ridotto a icona per la finestra. |
| **HSHELL_LANGUAGE** 8 | La lingua della tastiera è stata modificata o è stato caricato un nuovo layout di tastiera. |
| **HSHELL_REDRAW** 6 | Il titolo di una finestra nella barra delle applicazioni è stato ridisegnato. |
| **HSHELL_TASKMAN** 7 | L'utente ha selezionato l'elenco attività. Un'applicazione shell che fornisce un elenco attività deve restituire **true** per impedire che Windows avvii l'elenco attività. |
| **HSHELL_WINDOWACTIVATED** 4 | L'attivazione è stata modificata in un'altra finestra di primo livello, senza proprietario. |
| **HSHELL_WINDOWCREATED** 1 | È stata creata una finestra di primo livello, senza proprietario. La finestra esiste quando il sistema chiama questo hook. |
| **HSHELL_WINDOWDESTROYED** 2 | Una finestra di primo livello non di proprietà sta per essere distrutta. La finestra esiste ancora quando il sistema chiama questo hook. |
| **HSHELL_WINDOWREPLACED** 13 | È in corso la sostituzione di una finestra di primo livello. La finestra esiste quando il sistema chiama questo hook. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Questo parametro dipende dal valore del parametro *nCode* , come illustrato nella tabella seguente.

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Indica quale funzionalità di accessibilità ha modificato lo stato. Questo valore è uno dei seguenti: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** o **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Indica la posizione in cui è stato originariamente inviato il messaggio di **WM_APPCOMMAND** ; ad esempio, l'handle di una finestra. Per ulteriori informazioni, vedere parametro cmd in **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Handle per la finestra ridotta a icona o ingrandita. |
| **HSHELL_LANGUAGE** | Handle per la finestra. |
| **HSHELL_REDRAW** | Handle per la finestra ridisegnato. |
| **HSHELL_WINDOWACTIVATED** | Handle per la finestra attivata. |
| **HSHELL_WINDOWCREATED** | Handle per la finestra creata. |
| **HSHELL_WINDOWDESTROYED** | Handle per la finestra distrutta. |
| **HSHELL_WINDOWREPLACED** | Handle per la finestra da sostituire. Windows 2000: non supportato. |

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Questo parametro dipende dal valore del parametro *nCode* , come illustrato nella tabella seguente.

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` comando dell'applicazione corrispondente all'evento di input. `GET_DEVICE_LPARAM(lParam)` indica la generazione dell'evento di input. ad esempio, il mouse o la tastiera. Per ulteriori informazioni, vedere la descrizione del parametro *Udevice* in **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` dipende dal valore di *cmd* in **WM_APPCOMMAND**. Ad esempio, potrebbe indicare quali chiavi virtuali sono state mantenute al momento dell'invio del messaggio di **WM_APPCOMMAND** . Per ulteriori informazioni, vedere il parametro *dwCmdFlags* description in **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Puntatore a una struttura [Rect](/previous-versions/dd162897(v=vs.85)) . |
| **HSHELL_LANGUAGE** | Handle per un layout di tastiera. |
| **HSHELL_MONITORCHANGED** | Handle per la finestra che è stato spostato in un monitor diverso. |
| **HSHELL_REDRAW** | Il valore è **true** se la finestra è lampeggiante o **false** in caso contrario. |
| **HSHELL_WINDOWACTIVATED** | Il valore è TRUE se la finestra è in modalità schermo intero oppure **false** in caso contrario. |
| **HSHELL_WINDOWREPLACED** | Handle per la nuova finestra. Windows 2000: non supportato. |

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Il valore restituito deve essere zero, a meno che il valore di nCode non sia **HSHELL_APPCOMMAND** e la routine della shell gestisca il messaggio di **WM_COMMAND** .
In questo caso, il valore restituito deve essere diverso da zero.

## <a name="remarks"></a>Commenti

Installare questa routine hook specificando il tipo di hook [WH_SHELL](about-hooks.md) e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Hook](hooks.md)
