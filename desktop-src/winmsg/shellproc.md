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
ms.openlocfilehash: 3776748994b44b3a870fd4689fa9f4019bff99ae8d6f7dd7b13edbf2c98054d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449101"
---
# <a name="shellproc-function"></a>Funzione ShellProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
La funzione riceve le notifiche degli eventi della shell dal sistema.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**ShellProc** è un segnaposto per il nome di funzione definito dall'applicazione o definito dalla libreria.

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
Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla [funzione CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito **da CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | Lo stato di accessibilità è stato modificato. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | La shell dovrebbe attivare la finestra principale. |
| **HSHELL_APPCOMMAND** 12 | L'utente ha completato un evento di input (ad esempio, ha premuto un pulsante di comando [](/windows/desktop/inputdev/wm-appcommand) dell'applicazione sul mouse o un tasto di comando dell'applicazione sulla tastiera) e l'applicazione non ha gestito il messaggio WM_APPCOMMAND generato da tale input. Se la routine Shell gestisce il [WM_COMMAND,](/windows/desktop/menurc/wm-command) non deve chiamare **CallNextHookEx**. Per altre informazioni, vedere la sezione Valore restituito. |
| **HSHELL_GETMINRECT** 5 | Una finestra viene ridotta a icona o ingrandita. Il sistema richiede le coordinate del rettangolo ridotto a icona per la finestra. |
| **HSHELL_LANGUAGE** 8 | La lingua della tastiera è stata modificata o è stato caricato un nuovo layout di tastiera. |
| **HSHELL_REDRAW** 6 | Il titolo di una finestra nella barra delle applicazioni è stato ridisegnato. |
| **HSHELL_TASKMAN** 7 | L'utente ha selezionato l'elenco attività. Un'applicazione shell che fornisce un elenco di attività deve restituire **TRUE** per impedire Windows l'avvio del relativo elenco attività. |
| **HSHELL_WINDOWACTIVATED** 4 | L'attivazione è stata modificata in un'altra finestra senzawned di primo livello. |
| **HSHELL_WINDOWCREATED** 1 | È stata creata una finestra di primo livello senzawned. La finestra esiste quando il sistema chiama questo hook. |
| **HSHELL_WINDOWDESTROYED** 2 | Una finestra di primo livello senzawned sta per essere distrutta. La finestra esiste ancora quando il sistema chiama questo hook. |
| **HSHELL_WINDOWREPLACED** 13 | Viene sostituita una finestra di primo livello. La finestra esiste quando il sistema chiama questo hook. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Questo parametro dipende dal valore del *parametro nCode,* come illustrato nella tabella seguente.

| Ncode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Indica quale funzionalità di accessibilità ha modificato lo stato. Questo valore è uno dei seguenti: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** o **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Indica dove è stato **WM_APPCOMMAND** messaggio originale; ad esempio l'handle per una finestra. Per altre informazioni, vedere il parametro cmd in **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Handle per la finestra ridotta a icona o ingrandita. |
| **HSHELL_LANGUAGE** | Handle per la finestra. |
| **HSHELL_REDRAW** | Handle per la finestra ridisegnata. |
| **HSHELL_WINDOWACTIVATED** | Handle per la finestra attivata. |
| **HSHELL_WINDOWCREATED** | Handle per la finestra creata. |
| **HSHELL_WINDOWDESTROYED** | Handle per la finestra distrutta. |
| **HSHELL_WINDOWREPLACED** | Handle per la finestra da sostituire. Windows 2000: non supportato. |

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Questo parametro dipende dal valore del *parametro nCode,* come illustrato nella tabella seguente.

| Ncode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` è il comando dell'applicazione corrispondente all'evento di input. `GET_DEVICE_LPARAM(lParam)` indica l'elemento che ha generato l'evento di input. ad esempio mouse o tastiera. Per altre informazioni, vedere la descrizione *del parametro uDevice* **in WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` dipende dal valore di *cmd* in **WM_APPCOMMAND**. Ad esempio, potrebbe indicare quali chiavi virtuali sono state mantenute quando è stato WM_APPCOMMAND **messaggio** originale. Per altre informazioni, vedere il *parametro description dwCmdFlags* **in WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Puntatore a una [struttura RECT.](/previous-versions/dd162897(v=vs.85)) |
| **HSHELL_LANGUAGE** | Handle per un layout di tastiera. |
| **HSHELL_MONITORCHANGED** | Handle della finestra spostato in un monitor diverso. |
| **HSHELL_REDRAW** | Il valore è **TRUE se** la finestra lampeggia o FALSE in **caso contrario.** |
| **HSHELL_WINDOWACTIVATED** | Il valore è TRUE se la finestra è in modalità schermo intero oppure FALSE in caso **contrario.** |
| **HSHELL_WINDOWREPLACED** | Handle per la nuova finestra. Windows 2000: non supportato. |

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Il valore restituito deve essere zero a meno che il valore di nCode non sia HSHELL_APPCOMMAND **e** la routine della shell gestisca il WM_COMMAND **messaggio.**
In questo caso, il valore restituito deve essere diverso da zero.

## <a name="remarks"></a>Commenti

Installare questa procedura hook specificando il tipo [hook](about-hooks.md) WH_SHELL e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Hook](hooks.md)
