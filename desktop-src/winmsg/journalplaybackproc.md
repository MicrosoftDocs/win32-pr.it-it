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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "104398815"
---
# <a name="journalplaybackproc-function"></a>JournalPlaybackProc (funzione)

## <a name="description"></a>Descrizione

Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
In genere, un'applicazione utilizza questa funzione per riprodurre una serie di messaggi di mouse e tastiera registrati in precedenza dalla procedura di hook **JournalRecordProc** .
Finché viene installata una procedura **JournalPlaybackProc** Hook, l'input del mouse e della tastiera normale è disabilitato.

Il tipo **HookProc** definisce un puntatore a questa funzione di callback.
**JournalPlaybackProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parametri

### <a name="code-in"></a>Codice [in]

Tipo: **int**

Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.
Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.
Questo parametro può avere uno dei valori seguenti.

| Valore | Significato |
|-------|---------|
| **HC_GETNEXT** 1 | La routine hook deve copiare il mouse o il messaggio della tastiera corrente nella struttura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) a cui punta il parametro *lParam* . |
| **HC_NOREMOVE** 3 | Un'applicazione ha chiamato la funzione [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) con wRemoveMsg impostato su **PM_NOREMOVE**, a indicare che il messaggio non viene rimosso dalla coda di messaggi dopo l'elaborazione di **PeekMessage** . |
| **HC_NOREMOVE** 2 | La procedura di hook deve prepararsi a copiare il mouse o il messaggio della tastiera successivo nella struttura **EVENTMSG** a cui punta *lParam*. Quando riceve il codice di **HC_GETNEXT** , la routine hook deve copiare il messaggio nella struttura. |
| **HC_SYSMODALOFF** 5 | Una finestra di dialogo modale del sistema è stata eliminata. La procedura di hook deve riprendere la riproduzione dei messaggi. |
| **HC_SYSMODALON** 4 | Viene visualizzata una finestra di dialogo modale del sistema. Finché la finestra di dialogo non viene distrutta, la procedura di hook deve interrompere la riproduzione dei messaggi. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Questo parametro non viene usato.

### <a name="lparam"></a>lParam

Tipo: **lParam**

Puntatore a una struttura **EVENTMSG** che rappresenta un messaggio elaborato dalla routine hook.
Questo parametro è valido solo quando il parametro di *codice* è **HC_GETNEXT**.

## <a name="returns"></a>Restituisce

Tipo: **LRESULT**

Per fare in modo che il sistema attenda prima di elaborare il messaggio, il valore restituito deve corrispondere alla quantità di tempo, espressa in cicli di clock, che il sistema deve attendere.

(Questo valore può essere calcolato calcolando la differenza tra i membri temporali nei messaggi di input correnti e precedenti).

Per elaborare immediatamente il messaggio, il valore restituito deve essere zero. Il valore restituito viene usato solo se il codice hook è **HC_GETNEXT**; in caso contrario, viene ignorato.

## <a name="remarks"></a>Commenti

Una routine hook **JournalPlaybackProc** deve copiare un messaggio di input nel parametro *lParam* .
Il messaggio deve essere stato registrato in precedenza tramite una procedura di hook **JournalRecordProc** , che non deve modificare il messaggio.

Per recuperare lo stesso messaggio ripetutamente, è possibile chiamare la procedura hook più volte con il parametro *Code* impostato su **HC_GETNEXT** senza una chiamata corrispondente con *codice* impostato su **HC_SKIP**.

Se il *codice* è **HC_GETNEXT** e il valore restituito è maggiore di zero, il sistema dorme per il numero di millisecondi specificato dal valore restituito. Quando il sistema continua, chiama di nuovo la routine hook con il *codice* impostato su **HC_GETNEXT** per recuperare lo stesso messaggio.
Il valore restituito da questa nuova chiamata a **JournalPlaybackProc** deve essere zero. in caso contrario, il sistema torna a dormire per il numero di millisecondi specificato dal valore restituito, chiama di nuovo **JournalPlaybackProc** e così via.
Il sistema sembra non rispondere.

A differenza della maggior parte delle altre routine hook globali, le routine hook **JournalRecordProc** e **JournalPlaybackProc** vengono sempre chiamate nel contesto del thread che imposta l'hook.

Quando la routine hook restituisce il controllo al sistema, il messaggio continua a essere elaborato. Se il *codice* è **HC_SKIP**, la procedura di hook deve prepararsi a restituire il messaggio di evento registrato successivo alla chiamata successiva.

Installare la routine hook **JournalPlaybackProc** specificando il tipo di [WH_JOURNALPLAYBACK](about-hooks.md) e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .

Se l'utente preme CTRL + ESC o CTRL + ALT + CANC durante la riproduzione del Journal, il sistema interrompe la riproduzione, Annulla l'hook della procedura di riproduzione Journal e invia un messaggio di [WM_CANCELJOURNAL](wm-canceljournal.md) all'applicazione di inserimento nel journal.

Se la routine hook restituisce un messaggio nell'intervallo **WM_KEYFIRST** **WM_KEYLAST**, si applicano le condizioni seguenti:

* Il membro **paraml** della struttura **EVENTMSG** specifica il codice di chiave virtuale della chiave che è stata premuta.
* Il membro **paramH** della struttura **EVENTMSG** specifica il codice di analisi.
* Non è possibile specificare un numero di ripetizioni.
L'evento viene sempre impiegato per rappresentare un evento chiave.

## <a name="see-also"></a>Vedi anche

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hook](hooks.md)
