---
UID: ''
title: Funzione di callback GetMsgProc
description: Il sistema chiama questa funzione quando una funzione di messaggio ottiene un messaggio da una coda di messaggi dell'applicazione.
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
ms.openlocfilehash: e5c51f2abe8b3660ae40bae05c13428e0622fd4d5c4b8020fea8caa924a35681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200793"
---
# <a name="getmsgproc-function"></a>Funzione GetMsgProc

## <a name="-description"></a>-description

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) Il sistema chiama questa funzione ogni volta che la [funzione GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) recupera un messaggio da una coda di messaggi dell'applicazione.
Prima di restituire il messaggio recuperato al chiamante, il sistema passa il messaggio alla routine hook.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**GetMsgProc è un** segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-parameters

### <a name="code-in"></a>codice [in]

Tipo: **int**

Specifica se la routine hook deve elaborare il messaggio.
Se *il* codice **HC_ACTION**, la routine hook deve elaborare il messaggio.
Se *il* codice è minore di zero, la procedura hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx.**

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Specifica se il messaggio è stato rimosso dalla coda.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | Il messaggio non è stato rimosso dalla coda. Un'applicazione denominata **funzione PeekMessage,** che specifica il flag **PM_NOREMOVE.** |
| **PM_REMOVE** 0x0001 | Il messaggio è stato rimosso dalla coda. Un'applicazione denominata **GetMessage** o ha chiamato la **funzione PeekMessage,** specificando il flag **PM_REMOVE.**|

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntatore a una [struttura MSG](/windows/desktop/api/winuser/ns-winuser-msg) che contiene i dettagli sul messaggio.

## <a name="-returns"></a>-returns

Se *il* codice è minore di zero, la routine hook deve restituire il valore restituito [da CallNextHookEx.](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

Se *il* codice è maggiore o uguale a zero, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito. In caso contrario, le altre applicazioni WH_GETMESSAGE [hook](about-hooks.md) non riceveranno notifiche hook e potrebbero comportarsi in modo non corretto.
Se la routine hook non chiama **CallNextHookEx,** il valore restituito deve essere zero.

## <a name="-remarks"></a>-remarks

La procedura hook **GetMsgProc** può esaminare o modificare il messaggio.
Dopo che la routine hook ha restituito il controllo al sistema, la funzione **GetMessage** o **PeekMessage** restituisce il messaggio, insieme alle eventuali modifiche, all'applicazione che lo ha chiamato in origine.

Un'applicazione installa questa procedura hook specificando il tipo hook **WH_GETMESSAGE** e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[Msg](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hook](hooks.md)
