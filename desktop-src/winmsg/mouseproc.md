---
UID: ''
title: Funzione di callback MouseProc
description: Il sistema chiama questa funzione quando un'applicazione chiama una funzione di messaggio ed è presente un messaggio del mouse da elaborare.
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
ms.openlocfilehash: fa1528ce2910e563e3fe930fe19960aa43b437b22c53c03d0febc51b98bcc55b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200692"
---
# <a name="mouseproc-function"></a>Funzione MouseProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
Il sistema chiama questa funzione ogni volta che un'applicazione chiama [la funzione GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ed è presente un messaggio del mouse da elaborare.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**MouseProc è** un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare come elaborare il messaggio.
Se *nCode* è minore di zero, la procedura hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | I *parametri wParam* *e lParam* contengono informazioni su un messaggio del mouse. |
| **HC_NOREMOVE** 3 | I *parametri wParam* *e lParam* contengono informazioni su un messaggio del mouse e il messaggio del mouse non è stato rimosso dalla coda di messaggi. Un'applicazione denominata **funzione PeekMessage,** che specifica il flag **PM_NOREMOVE.** |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Identificatore del messaggio del mouse.

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntatore a una [struttura MOUSEHOOKSTRUCT.](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito **da CallNextHookEx.**

Se *nCode* è maggiore o uguale a zero e la procedura hook non ha elaborata il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito. In caso contrario, le altre applicazioni in cui [WH_MOUSE](about-hooks.md) hook non riceveranno notifiche hook e potrebbero comportarsi in modo non corretto.
Se la procedura hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio alla routine della finestra di destinazione.

## <a name="remarks"></a>Commenti

Un'applicazione installa la procedura hook specificando il tipo hook WH_MOUSE e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

La routine hook non deve installare una funzione [WH_JOURNALPLAYBACK](about-hooks.md) callback.

Questo hook può essere chiamato nel contesto del thread che lo ha installato.
La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.
Pertanto, il thread che ha installato l'hook deve avere un ciclo di messaggi.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hook](hooks.md)

[Informazioni sugli hook](about-hooks.md)
