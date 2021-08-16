---
UID: ''
title: Funzione di callback JournalPlaybackProc
description: Riproduce una serie di messaggi di mouse e tastiera registrati in precedenza.
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
ms.openlocfilehash: bee538bf2c20cc3cadb6f0bdf6f5dd6a2ae12dfe8a21baeb56b8ad62cb23ff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437128"
---
# <a name="journalplaybackproc-function"></a>Funzione JournalPlaybackProc

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria usata con la [funzione SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
In genere, un'applicazione usa questa funzione per riprodurre una serie di messaggi di mouse e tastiera registrati in precedenza dalla procedura hook **JournalRecordProc.**
Se è installata una procedura hook **JournalPlaybackProc,** l'input normale da mouse e tastiera è disabilitato.

Il **tipo HOOKPROC** definisce un puntatore a questa funzione di callback.
**JournalPlaybackProc è un** segnaposto per il nome della funzione definita dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>codice [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare come elaborare il messaggio.
Se *il* codice è minore di zero, la procedura hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx.**
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_GETNEXT** 1 | La routine hook deve copiare il messaggio corrente del mouse o della tastiera nella [struttura EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) a cui punta il *parametro lParam.* |
| **HC_NOREMOVE** 3 | Un'applicazione ha chiamato la funzione [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) con wRemoveMsg impostato su **PM_NOREMOVE**, a indicare che il messaggio non viene rimosso dalla coda di messaggi dopo l'elaborazione **di PeekMessage.** |
| **HC_NOREMOVE** 2 | La procedura hook deve preparare la copia del messaggio successivo del mouse o della tastiera nella **struttura EVENTMSG** a cui punta *lParam*. Al momento della **ricezione HC_GETNEXT** codice, la routine hook deve copiare il messaggio nella struttura . |
| **HC_SYSMODALOFF** 5 | Una finestra di dialogo modale di sistema è stata rimossa. La procedura hook deve riprendere la riproduzione dei messaggi. |
| **HC_SYSMODALON** 4 | Viene visualizzata una finestra di dialogo modale di sistema. Fino a quando la finestra di dialogo non viene distrutta, la procedura hook deve interrompere la riproduzione dei messaggi. |

### <a name="wparam"></a>wParam

Tipo: **WPARAM**

Questo parametro non viene usato.

### <a name="lparam"></a>lParam

Tipo: **LPARAM**

Puntatore a una **struttura EVENTMSG** che rappresenta un messaggio elaborato dalla routine hook.
Questo parametro è valido solo quando il *parametro di* codice è **HC_GETNEXT**.

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Per fare in modo che il sistema attenda prima di elaborare il messaggio, il valore restituito deve essere la quantità di tempo, in tick di clock, che il sistema deve attendere.

Questo valore può essere calcolato calcolando la differenza tra i membri dell'ora nei messaggi di input correnti e precedenti.

Per elaborare immediatamente il messaggio, il valore restituito deve essere zero. Il valore restituito viene usato solo se il codice hook **è HC_GETNEXT**; in caso contrario, viene ignorato.

## <a name="remarks"></a>Commenti

Una routine hook **JournalPlaybackProc** deve copiare un messaggio di input nel *parametro lParam.*
Il messaggio deve essere stato registrato in precedenza tramite una routine hook **JournalRecordProc,** che non deve modificare il messaggio.

Per recuperare lo stesso messaggio più volte, la routine  hook può essere chiamata più volte con  il parametro di codice impostato su **HC_GETNEXT** senza una chiamata con codice impostato su **HC_SKIP**.

Se *il* codice **HC_GETNEXT** e il valore restituito è maggiore di zero, il sistema viene in sospensione per il numero di millisecondi specificato dal valore restituito. Quando il sistema continua, chiama di nuovo la routine hook con *codice* impostato su HC_GETNEXT **per** recuperare lo stesso messaggio.
Il valore restituito da questa nuova chiamata a **JournalPlaybackProc** deve essere zero. In caso contrario, il sistema tornerà in sospensione per il numero di millisecondi specificato dal valore restituito, chiamerà di nuovo **JournalPlaybackProc** e così via.
Il sistema sembra non rispondere.

A differenza della maggior parte delle altre routine hook globali, le routine hook **JournalRecordProc** e **JournalPlaybackProc** vengono sempre chiamate nel contesto del thread che ha impostato l'hook.

Dopo che la routine hook ha restituito il controllo al sistema, il messaggio continua a essere elaborato. Se *il* codice **HC_SKIP**, la routine hook deve prepararsi a restituire il messaggio di evento registrato successivo alla chiamata successiva.

Installare la procedura hook **JournalPlaybackProc** specificando il [tipo WH_JOURNALPLAYBACK](about-hooks.md) e un puntatore alla routine hook in una chiamata alla **funzione SetWindowsHookEx.**

Se l'utente preme CTRL+ESC O CTRL+ALT+CANC durante la riproduzione del journal, il sistema arresta la riproduzione, annulla l'hook della procedura di riproduzione del journal e invia un messaggio WM_CANCELJOURNAL all'applicazione di inserimento [nel](wm-canceljournal.md) journal.

Se la routine hook restituisce un messaggio nell'intervallo WM_KEYFIRST **a** **WM_KEYLAST**, si applicano le condizioni seguenti:

* Il **membro paramL** della **struttura EVENTMSG** specifica il codice del tasto virtuale del tasto premuto.
* Il **membro paramH** della struttura **EVENTMSG** specifica il codice di analisi.
* Non è possibile specificare un conteggio delle ripetizioni.
L'evento viene sempre utilizzato per rappresentare un evento chiave.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[Setwindowshookex](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hook](hooks.md)
