---
UID: ''
title: Funzione di callback KeyboardProc
description: Il sistema chiama questa funzione per ottenere una funzione di messaggio ed è presente un messaggio da tastiera da elaborare.
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
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299551"
---
# <a name="keyboardproc-function"></a>KeyboardProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Il sistema chiama questa funzione ogni volta che un'applicazione chiama la funzione [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ed è presente un messaggio della tastiera ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) o [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) da elaborare.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**KeyboardProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>Codice [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.
Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | I parametri *wParam* e *lParam* contengono informazioni su un messaggio di sequenza di tasti. |
| **HC_NOREMOVE** 3 | I parametri *wParam* e *lParam* contengono informazioni su un messaggio di sequenza di tasti e il messaggio di sequenza di tasti non è stato rimosso dalla coda di messaggi. (Applicazione chiamata funzione **PeekMessage** , che specifica il flag di **PM_NOREMOVE** ). |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

[Codice della chiave virtuale](/windows/desktop/inputdev/virtual-key-codes) della chiave che ha generato il messaggio di sequenza di tasti.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato di chiave precedente e il flag di stato di transizione.
Per ulteriori informazioni sul parametro *lParam* , vedere [flag dei messaggi di sequenza di tasti](/windows/desktop/inputdev/about-keyboard-input).
Nella tabella seguente vengono descritti i bit di questo valore.

| BITS | Descrizione |
|-------|---------|
| 0-15 | Conteggio delle ripetizioni. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in seguito alla chiusura della chiave da parte dell'utente. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM. |
| 24 | Indica se la chiave è una chiave estesa, ad esempio un tasto funzione o una chiave sul tastierino numerico. Il valore è 1 se la chiave è una chiave estesa; in caso contrario, è 0. |
| 25-28 | Riservato. |
| 29 | Codice del contesto. Il valore è 1 se il tasto ALT è premuto; in caso contrario, è 0. |
| 30 | Stato precedente della chiave. Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio; è 0 se il tasto è attivo. |
| 31 | Stato di transizione. Il valore è 0 se viene premuto il tasto e 1 se è in fase di rilascio. |

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se il *codice* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.

Se il *codice* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_KEYBOARD](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.
Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena di hook o alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la routine hook specificando il tipo di hook **WH_KEYBOARD** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

Questo hook può essere chiamato nel contesto del thread che lo ha installato.
La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.
Pertanto, il thread che ha installato l'hook deve disporre di un ciclo di messaggi.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[Hook](hooks.md)
