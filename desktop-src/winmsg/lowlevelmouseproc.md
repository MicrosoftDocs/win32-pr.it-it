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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/26/2020
ms.locfileid: "104047547"
---
# <a name="lowlevelmouseproc-function"></a>LowLevelMouseProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Il sistema chiama questa funzione ogni volta che un nuovo evento di input del mouse sta per essere inserito in una coda di input del thread.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**LowLevelMouseProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

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

Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.
Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | I parametri *wParam* e *lParam* contengono informazioni su un messaggio del mouse. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Identificatore del messaggio del mouse.
Questo parametro può essere uno dei messaggi seguenti: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) o [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntatore a una struttura [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.

Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_MOUSE_LL](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.
Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena di hook o alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la routine hook specificando il tipo di hook **WH_MOUSE_LL** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

Questo hook viene chiamato nel contesto del thread che lo ha installato.
La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.
Pertanto, il thread che ha installato l'hook deve disporre di un ciclo di messaggi.

L'input del mouse può provenire dal driver del mouse locale o dalle chiamate alla funzione [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .
Se l'input deriva da una chiamata a **mouse_event**, l'input è stato "inserito".
Tuttavia, l'hook **WH_MOUSE_LL** non viene inserito in un altro processo.
Al contrario, il contesto ritorna al processo che ha installato l'hook e viene chiamato nel contesto originale.
Il contesto ritorna quindi all'applicazione che ha generato l'evento.

La routine hook deve elaborare un messaggio in meno tempo rispetto all'immissione dati specificata nel valore **LowLevelHooksTimeout** nella seguente chiave del registro di sistema: **HKEY_CURRENT_USER\Control Panel\Desktop**.

Il valore è espresso in millisecondi.
Se la procedura di hook scade, il sistema passa il messaggio al gancio successivo.
Tuttavia, in Windows 7 e versioni successive, l'hook viene rimosso automaticamente senza essere chiamato.
L'applicazione non è in grado di sapere se l'hook è stato rimosso.

**Nota:**  Gli hook di debug non possono tenere traccia di questo tipo di hook del mouse di basso livello.
Se l'applicazione deve usare hook di basso livello, deve eseguire gli hook in un thread dedicato che passa il lavoro a un thread di lavoro e quindi restituisce immediatamente il risultato.
Nella maggior parte dei casi in cui l'applicazione deve usare hook di basso livello, deve invece monitorare l'input non elaborato.
Questo perché l'input non elaborato può monitorare in modo asincrono i messaggi del mouse e della tastiera destinati ad altri thread in modo più efficace rispetto agli hook di basso livello.
Per ulteriori informazioni sull'input non elaborato, vedere [input non elaborato](/windows/desktop/inputdev/raw-input).

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Hook](hooks.md)

[Informazioni sugli hook](about-hooks.md)
