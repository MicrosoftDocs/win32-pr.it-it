---
UID: ''
title: Funzione di callback GetMsgProc
description: Il sistema chiama questa funzione quando una funzione Message riceve un messaggio da una coda di messaggi dell'applicazione.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "106303666"
---
# <a name="getmsgproc-function"></a>GetMsgProc (funzione)

## <a name="-description"></a>-Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) . Il sistema chiama questa funzione ogni volta che la funzione [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ha recuperato un messaggio da una coda di messaggi dell'applicazione.
Prima di restituire il messaggio recuperato al chiamante, il sistema passa il messaggio alla routine hook.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**GetMsgProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-parametri

### <a name="code-in"></a>Codice [in]

Tipo: **int**

Specifica se la routine hook deve elaborare il messaggio.
Se il *codice* è **HC_ACTION**, la routine hook deve elaborare il messaggio.
Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Specifica se il messaggio è stato rimosso dalla coda.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | Il messaggio non è stato rimosso dalla coda. (Applicazione chiamata funzione **PeekMessage** , che specifica il flag di **PM_NOREMOVE** ). |
| **PM_REMOVE** 0x0001 | Il messaggio è stato rimosso dalla coda. (Un'applicazione denominata **GetMessage** o chiamata funzione  **PeekMessage** , che specifica il flag di **PM_REMOVE** ).|

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntatore a una struttura [msg](/windows/desktop/api/winuser/ns-winuser-msg) che contiene i dettagli sul messaggio.

## <a name="-returns"></a>-Restituisce

Se il *codice* è minore di zero, la routine hook deve restituire il valore restituito da [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).

Se il *codice* è maggiore o uguale a zero, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_GETMESSAGE](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.
Se la routine hook non chiama **CallNextHookEx**, il valore restituito deve essere zero.

## <a name="-remarks"></a>-Note

La procedura **GetMsgProc** hook può esaminare o modificare il messaggio.
Dopo che la routine hook restituisce il controllo al sistema, la funzione **GetMessage** o **PeekMessage** restituisce il messaggio, insieme alle eventuali modifiche, all'applicazione che l'ha originariamente chiamata.

Un'applicazione installa questa routine hook specificando il tipo di hook **WH_GETMESSAGE** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MESSAGGIO](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hook](hooks.md)
