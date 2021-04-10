---
UID: ''
title: Funzione di callback JournalRecordProc
description: La funzione registra i messaggi rimossi dal sistema dalla coda dei messaggi di sistema.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "103956291"
---
# <a name="journalrecordproc-function"></a>JournalRecordProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
La funzione registra i messaggi rimossi dal sistema dalla coda dei messaggi di sistema.
Successivamente, un'applicazione può usare una procedura di hook [JournalPlaybackProc](journalplaybackproc.md) per riprodurre i messaggi.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**JournalRecordProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>Codice [in]

Tipo: **int**

Specifica la modalità di elaborazione del messaggio.
Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | Il parametro *lParam* è un puntatore a una struttura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) contenente informazioni su un messaggio rimosso dalla coda di sistema. La procedura di hook deve registrare il contenuto della struttura copiando gli elementi in un buffer o in un file. |
| **HC_SYSMODALOFF** 5 | Una finestra di dialogo modale del sistema è stata eliminata. La procedura di hook deve riprendere la registrazione. |
| **HC_SYSMODALON** 4 | Viene visualizzata una finestra di dialogo modale del sistema. Finché la finestra di dialogo non viene distrutta, la procedura di hook deve arrestare la registrazione. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Questo parametro non viene usato.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntatore a una struttura **EVENTMSG** contenente il messaggio da registrare.

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Una procedura di hook **JournalRecordProc** deve copiare ma non modificare i messaggi.
Quando la routine hook restituisce il controllo al sistema, il messaggio continua a essere elaborato.

Installare la routine hook **JournalRecordProc** specificando il tipo di [WH_JOURNALRECORD](about-hooks.md) e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

Non è necessario che una routine hook **JournalRecordProc** risieda in una libreria a collegamento dinamico.
Una procedura di hook **JournalRecordProc** può risiedere nell'applicazione stessa.

A differenza della maggior parte delle altre routine hook globali, le routine hook **JournalRecordProc** e [JournalPlaybackProc](journalplaybackproc.md) vengono sempre chiamate nel contesto del thread che imposta l'hook.

Un'applicazione che ha installato una procedura **JournalRecordProc** hook deve controllare il codice di chiave virtuale [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (implementato come combinazione di tasti Ctrl + Break sulla maggior parte delle tastiere).
Questo codice di chiave virtuale deve essere interpretato dall'applicazione come un segnale che l'utente desidera arrestare la registrazione del journal.
L'applicazione deve rispondere terminando la sequenza di registrazione e rimuovendo la procedura di hook **JournalRecordProc** .
La rimozione è importante.
Impedisce a un'applicazione di inserimento nel journal di bloccare il sistema con una procedura di hook.

Questo ruolo come segnale per arrestare la registrazione di Journl significa che non è possibile registrare una combinazione di tasti CTRL + BREAK.
Poiché la combinazione di tasti CTRL + C non ha alcun ruolo come un segnale di inserimento nel journal, può essere registrata.
Sono disponibili altre due combinazioni di tasti che non possono essere registrate: CTRL + ESC e CTRL + ALT + CANC.
Queste due combinazioni di tasti comportano l'arresto di tutte le attività di inserimento nel Journal (record o riproduzione), la rimozione di tutti gli hook di inserimento nel journal e la pubblicazione di un messaggio di [WM_CANCELJOURNAL](wm-canceljournal.md) nell'applicazione di inserimento nel journal.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hook](hooks.md)
