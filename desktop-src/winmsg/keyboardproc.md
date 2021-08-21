---
UID: ''
title: Funzione di callback KeyboardProc
description: Il sistema chiama questa funzione ottiene una funzione di messaggio ed è presente un messaggio da elaborare.
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
ms.openlocfilehash: ed2f3943667d09f42a7bc843adac69eaa4043454d93b409b193513b8ab43fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437156"
---
# <a name="keyboardproc-function"></a>Funzione KeyboardProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
Il sistema chiama questa funzione ogni volta che un'applicazione chiama la [funzione GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ed è presente un messaggio della tastiera ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) [o WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) da elaborare.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**KeyboardProc** è un segnaposto per il nome di funzione definito dall'applicazione o definito dalla libreria.

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>codice [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare come elaborare il messaggio.
Se *il* codice è minore di zero, la routine hook deve passare il messaggio alla [funzione CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito **da CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | I *parametri wParam* *e lParam* contengono informazioni su un messaggio di sequenza di tasti. |
| **HC_NOREMOVE** 3 | I *parametri wParam* *e lParam* contengono informazioni su un messaggio di sequenza di tasti e il messaggio della sequenza di tasti non è stato rimosso dalla coda di messaggi. Un'applicazione denominata **funzione PeekMessage,** che specifica il flag **PM_NOREMOVE.** |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Codice [del tasto virtuale del](/windows/desktop/inputdev/virtual-key-codes) tasto che ha generato il messaggio di sequenza di tasti.

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice di contesto, flag di stato della chiave precedente e flag di stato di transizione.
Per altre informazioni sul parametro *lParam,* vedere [Flag dei messaggi di sequenza di tasti](/windows/desktop/inputdev/about-keyboard-input).
Nella tabella seguente vengono descritti i bit di questo valore.

| BITS | Descrizione |
|-------|---------|
| 0-15 | Numero di ripetizioni. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in seguito alla pressione del tasto da parte dell'utente. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM. |
| 24 | Indica se il tasto è un tasto esteso, ad esempio un tasto funzione o un tasto sul tastierino numerico. Il valore è 1 se la chiave è una chiave estesa. in caso contrario, è 0. |
| 25-28 | Riservato. |
| 29 | Codice del contesto. Il valore è 1 se il tasto ALT è premuto; in caso contrario, è 0. |
| 30 | Stato della chiave precedente. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio. è 0 se la chiave è in alto. |
| 31 | Stato della transizione. Il valore è 0 se il tasto viene premuto e 1 se viene rilasciato. |

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se *il* codice è minore di zero, la routine hook deve restituire il valore restituito **da CallNextHookEx**.

Se *il* codice è maggiore o uguale a zero e la routine hook non ha elaborata il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito. In caso contrario, altre applicazioni che hanno [installato](about-hooks.md) WH_KEYBOARD hook non riceveranno notifiche hook e potrebbero comportarsi in modo non corretto.
Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena hook o alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la procedura hook specificando il tipo **hook** WH_KEYBOARD e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

Questo hook può essere chiamato nel contesto del thread che lo ha installato.
La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.
Pertanto, il thread che ha installato l'hook deve avere un ciclo di messaggi.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[Wm_keydown](/windows/desktop/inputdev/wm-keydown)

[Hook](hooks.md)
