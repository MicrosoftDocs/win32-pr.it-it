---
UID: ''
title: Funzione di callback SysMsgProc
description: Questa funzione viene chiamata dal sistema dopo un evento di input in una finestra di dialogo, in una finestra di messaggio, in un menu o in una barra di scorrimento. | Funzione di callback SysMsgProc
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
ms.openlocfilehash: 0d5c7fc116b74dada141e88116ba67209da4a103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321952"
---
# <a name="sysmsgproc-function"></a>SysMsgProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Il sistema chiama questa funzione dopo che si è verificato un evento di input in una finestra di dialogo, in una finestra di messaggio, in un menu o in una barra di scorrimento, ma prima dell'elaborazione del messaggio generato dall'evento di input.
La funzione può monitorare i messaggi per qualsiasi finestra di dialogo, finestra di messaggio, menu o barra di scorrimento nel sistema.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**SysMsgProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK SysMsgProc(
  _In_ int    nCode,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Tipo di evento di input che ha generato il messaggio.
Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **MSGF_DIALOGBOX** 0 | L'evento di input si è verificato in una finestra di messaggio o in una finestra di dialogo. |
| **MSGF_MENU** 2 | L'evento di input si è verificato in un menu. |
| **MSGF_SCROLLBAR** 5 | L'evento di input si è verificato in una barra di scorrimento. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Questo parametro non viene usato.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntatore a una struttura di messaggi [msg](/windows/desktop/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.

Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_SYSMSGFILTER](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.
Se la routine hook elabora il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la routine hook specificando il tipo di hook **WH_SYSMSGFILTER** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[MESSAGGIO](/windows/desktop/api/winuser/ns-winuser-msg)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hook](hooks.md)
