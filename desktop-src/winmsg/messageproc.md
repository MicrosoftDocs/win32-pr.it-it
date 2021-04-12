---
UID: ''
title: Funzione di callback MessageProc
description: Questa funzione viene chiamata dal sistema dopo un evento di input in una finestra di dialogo, in una finestra di messaggio, in un menu o in una barra di scorrimento. | Funzione di callback MessageProc
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
ms.openlocfilehash: 00a1d1c52d50d0d9a028829181c886a813112a15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353571"
---
# <a name="messageproc-function"></a>MessageProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Il sistema chiama questa funzione dopo che si è verificato un evento di input in una finestra di dialogo, in una finestra di messaggio, in un menu o in una barra di scorrimento, ma prima dell'elaborazione del messaggio generato dall'evento di input.
La procedura hook può monitorare i messaggi per una finestra di dialogo, una finestra di messaggio, un menu o una barra di scorrimento creata da una particolare applicazione o da tutte le applicazioni.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**MessageProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK MessageProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>Codice [in]

Tipo: **int**

Tipo di evento di input che ha generato il messaggio.
Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | L'evento di input si è verificato mentre la libreria di gestione Dynamic Data Exchange (DDEML) era in attesa del completamento di una transazione sincrona. Per ulteriori informazioni su DDEML, vedere [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md). |
| **MSGF_DIALOGBOX** 0 | L'evento di input si è verificato in una finestra di messaggio o in una finestra di dialogo. |
| **MSGF_MENU** 2 | L'evento di input si è verificato in un menu. |
| **MSGF_SCROLLBAR** 5 | L'evento di input si è verificato in una barra di scorrimento. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Questo parametro non viene usato.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntatore a una struttura [msg](/windows/win32/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se il *codice* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.

Se il *codice* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_MSGFILTER](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.
Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena di hook o alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la routine hook specificando il tipo di hook **WH_MSGFILTER** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

Se un'applicazione che usa DDEML ed esegue transazioni sincrone deve elaborare i messaggi prima che vengano inviati, deve usare l'hook **WH_MSGFILTER** .

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[MESSAGGIO](/windows/win32/api/winuser/ns-winuser-msg)

[Hook](hooks.md)
