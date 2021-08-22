---
UID: ''
title: Funzione di callback LowLevelKeyboardProc
description: Il sistema chiama questa funzione ogni volta che un nuovo evento di input della tastiera sta per essere pubblicato in una coda di input del thread.
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
ms.openlocfilehash: 5a9a2a0cb5ccf60fe5cfc9f495b621669ba1d85ca04eeb7ecd345cdc60d48bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548571"
---
# <a name="lowlevelkeyboardproc-function"></a>Funzione LowLevelKeyboardProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
Il sistema chiama questa funzione ogni volta che un nuovo evento di input della tastiera sta per essere pubblicato in una coda di input del thread.

**Nota:**  Quando questa funzione di callback viene chiamata in risposta a una modifica dello stato di una chiave, la funzione di callback viene chiamata prima dell'aggiornamento dello stato asincrono della chiave.
Di conseguenza, lo stato asincrono della chiave non può essere determinato chiamando [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) dall'interno della funzione di callback.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**LowLevelKeyboardProc** è un segnaposto per il nome di funzione definito dall'applicazione o definito dalla libreria.

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>codice [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare come elaborare il messaggio.
Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla [funzione CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito **da CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | I *parametri wParam* *e lParam* contengono informazioni su un messaggio della tastiera. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Identificatore del messaggio della tastiera.
Questo parametro può essere uno dei messaggi seguenti: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)o [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntatore a una [struttura KBDLLHOOKSTRUCT.](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito **da CallNextHookEx**.

Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborata il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito. In caso contrario, altre applicazioni che hanno [installato](about-hooks.md) WH_KEYBOARD_LL hook non riceveranno notifiche hook e potrebbero comportarsi in modo non corretto.
Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena hook o alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la procedura hook specificando il tipo **hook** WH_KEYBOARD_LL e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

Questo hook viene chiamato nel contesto del thread che lo ha installato.
La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.
Pertanto, il thread che ha installato l'hook deve avere un ciclo di messaggi.

L'input da tastiera può derivare dal driver della tastiera locale o dalle chiamate alla [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) funzione.
Se l'input proviene da una chiamata a **keybd_event**, l'input è stato "inserito".
Tuttavia, l WH_KEYBOARD_LL hook non viene inserito in un altro processo.
Al contrario, il contesto torna al processo che ha installato l'hook e viene chiamato nel contesto originale.
Il contesto torna quindi all'applicazione che ha generato l'evento.

La procedura hook deve elaborare un messaggio in meno tempo rispetto alla voce di dati specificata nel **valore LowLevelHooksTimeout** nella chiave del Registro di sistema seguente: **HKEY_CURRENT_USER\Control Panel\Desktop**.

Il valore è espresso in millisecondi.
Se si verifica il timeout della procedura hook, il sistema passa il messaggio all'hook successivo.
Tuttavia, in Windows 7 e versioni successive, l'hook viene rimosso automaticamente senza essere chiamato.
Non è possibile che l'applicazione sappia se l'hook viene rimosso.

Nota: gli hook di debug non possono tenere traccia di questo tipo di hook della tastiera di basso livello.
Se l'applicazione deve usare hook di basso livello, deve eseguire gli hook in un thread dedicato che passa il lavoro a un thread di lavoro e quindi restituisce immediatamente .
Nella maggior parte dei casi in cui l'applicazione deve usare hook di basso livello, deve monitorare invece l'input non elaborato.
Questo perché l'input non elaborato può monitorare in modo asincrono i messaggi del mouse e della tastiera destinati ad altri thread in modo più efficace rispetto agli hook di basso livello.
Per altre informazioni sull'input non elaborato, vedere [Input non elaborato.](/windows/desktop/inputdev/raw-input)

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Wm_keydown](/windows/desktop/inputdev/wm-keydown)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)

[WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup)

[Hook](hooks.md)

[Informazioni sugli hook](about-hooks.md)
