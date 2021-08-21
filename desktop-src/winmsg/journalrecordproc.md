---
UID: ''
title: Funzione di callback JournalRecordProc
description: La funzione registra i messaggi rimossi dal sistema dalla coda di messaggi di sistema.
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
ms.openlocfilehash: cc5e1bdbd99b234b347d0b9c10caa7125aead9b68138472e125c8e2a11180609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437118"
---
# <a name="journalrecordproc-function"></a>Funzione JournalRecordProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
La funzione registra i messaggi rimossi dal sistema dalla coda di messaggi di sistema.
In un secondo momento, un'applicazione può usare una procedura hook [JournalPlaybackProc](journalplaybackproc.md) per riprodurre i messaggi.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**JournalRecordProc** è un segnaposto per il nome di funzione definito dall'applicazione o definito dalla libreria.

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>codice [in]

Tipo: **int**

Specifica come elaborare il messaggio.
Se *il* codice è minore di zero, la routine hook deve passare il messaggio alla [funzione CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito **da CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_ACTION** 0 | Il *parametro lParam* è un puntatore a [una struttura EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) contenente informazioni su un messaggio rimosso dalla coda di sistema. La routine hook deve registrare il contenuto della struttura copiandoli in un buffer o in un file. |
| **HC_SYSMODALOFF** 5 | Una finestra di dialogo modale di sistema è stata distrutta. La procedura hook deve riprendere la registrazione. |
| **HC_SYSMODALON** 4 | Viene visualizzata una finestra di dialogo modale di sistema. Finché la finestra di dialogo non viene distrutta, la procedura hook deve arrestare la registrazione. |

### <a name="wparam"></a>wParam

Tipo: **WPARAM**

Questo parametro non viene usato.

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntatore a una **struttura EVENTMSG** che contiene il messaggio da registrare.

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Una **routine hook JournalRecordProc** deve copiare ma non modificare i messaggi.
Dopo che la routine hook ha restituito il controllo al sistema, il messaggio continua a essere elaborato.

Installare la routine hook **JournalRecordProc** specificando il tipo WH_JOURNALRECORD e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.** [](about-hooks.md)

Una routine hook **JournalRecordProc** non deve essere presente in una libreria a collegamento dinamico.
Una routine hook **JournalRecordProc** può essere eseguita nell'applicazione stessa.

A differenza della maggior parte delle altre routine hook globali, le routine hook **JournalRecordProc** e [JournalPlaybackProc](journalplaybackproc.md) vengono sempre chiamate nel contesto del thread che imposta l'hook.

Un'applicazione che ha installato una procedura hook **JournalRecordProc** deve controllare il codice del tasto virtuale [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (implementato come combinazione di tasti CTRL+BREAK nella maggior parte delle tastiere).
Questo codice della chiave virtuale deve essere interpretato dall'applicazione come un segnale che l'utente vuole arrestare la registrazione nel journal.
L'applicazione deve rispondere terminando la sequenza di registrazione e rimuovendo la procedura hook **JournalRecordProc.**
La rimozione è importante.
Impedisce a un'applicazione di inserimento nel journal di bloccare il sistema bloccando all'interno di una procedura hook.

Questo ruolo come segnale per arrestare la registrazione journl significa che non è possibile registrare una combinazione di tasti CTRL+INTERR.
Poiché la combinazione di tasti CTRL+C non ha tale ruolo come segnale di inserimento nel journal, può essere registrata.
Non è possibile registrare altre due combinazioni di tasti: CTRL+ESC e CTRL+ALT+CANC.
Queste due combinazioni di tasti causano l'arresto del sistema di tutte le attività [](wm-canceljournal.md) di inserimento nel journal (registrazione o riproduzione), la rimozione di tutti gli hook di inserimento nel journal e la registrazione di un messaggio WM_CANCELJOURNAL nell'applicazione di inserimento nel journal.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hook](hooks.md)
