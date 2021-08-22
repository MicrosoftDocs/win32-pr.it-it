---
UID: ''
title: Funzione di callback LowLevelMouseProc
description: Il sistema chiama questa funzione ogni volta che un nuovo evento di input del mouse sta per essere inserito in una coda di input del thread.
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
ms.openlocfilehash: 53f75d14395388ce22ce86ef73f8819892c3fe7285909b1f38c801af476636a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705787"
---
# <a name="lowlevelmouseproc-function"></a>Funzione LowLevelMouseProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
Il sistema chiama questa funzione ogni volta che un nuovo evento di input del mouse sta per essere inserito in una coda di input del thread.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**LowLevelMouseProc** è un segnaposto per il nome di funzione definito dall'applicazione o definito dalla libreria.

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare come elaborare il messaggio.
Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla [funzione CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito **da CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | I *parametri wParam* *e lParam* contengono informazioni su un messaggio del mouse. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Identificatore del messaggio del mouse.
Questo parametro può essere uno dei messaggi seguenti: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) [o WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntatore a una [struttura MSLLHOOKSTRUCT.](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito **da CallNextHookEx**.

Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborata il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito. In caso contrario, altre applicazioni che hanno [installato](about-hooks.md) WH_MOUSE_LL hook non riceveranno notifiche hook e potrebbero comportarsi in modo non corretto.
Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena hook o alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la procedura hook specificando il tipo **hook** WH_MOUSE_LL e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

Questo hook viene chiamato nel contesto del thread che lo ha installato.
La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.
Pertanto, il thread che ha installato l'hook deve avere un ciclo di messaggi.

L'input del mouse può derivare dal driver del mouse locale o dalle chiamate alla [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) funzione.
Se l'input proviene da una chiamata a **mouse_event**, l'input è stato "inserito".
Tuttavia, **l WH_MOUSE_LL** hook non viene inserito in un altro processo.
Al contrario, il contesto torna al processo che ha installato l'hook e viene chiamato nel contesto originale.
Il contesto torna quindi all'applicazione che ha generato l'evento.

La procedura hook deve elaborare un messaggio in meno tempo rispetto alla voce di dati specificata nel **valore LowLevelHooksTimeout** nella chiave del Registro di **sistema seguente:HKEY_CURRENT_USER\Control Panel\Desktop**.

Il valore è espresso in millisecondi.
Se si verifica il timeout della procedura hook, il sistema passa il messaggio all'hook successivo.
Tuttavia, in Windows 7 e versioni successive, l'hook viene rimosso automaticamente senza essere chiamato.
Non è possibile che l'applicazione sappia se l'hook viene rimosso.

**Nota:**  Gli hook di debug non possono tenere traccia di questo tipo di hook del mouse di basso livello.
Se l'applicazione deve usare hook di basso livello, deve eseguire gli hook in un thread dedicato che passa il lavoro a un thread di lavoro e quindi restituisce immediatamente .
Nella maggior parte dei casi in cui l'applicazione deve usare hook di basso livello, deve monitorare invece l'input non elaborato.
Questo perché l'input non elaborato può monitorare in modo asincrono i messaggi del mouse e della tastiera destinati ad altri thread in modo più efficace rispetto agli hook di basso livello.
Per altre informazioni sull'input non elaborato, vedere [Input non elaborato.](/windows/desktop/inputdev/raw-input)

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[Wm_mousemove](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Hook](hooks.md)

[Informazioni sugli hook](about-hooks.md)
