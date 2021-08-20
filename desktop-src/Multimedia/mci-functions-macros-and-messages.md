---
title: Macro e messaggi delle funzioni MCI
description: Macro e messaggi delle funzioni MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Messaggi MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b411c018c55254658972d3cdc21a9d721334d5e78635b38f636892e2c80797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784321"
---
# <a name="mci-functions-macros-and-messages"></a>Macro e messaggi delle funzioni MCI

La maggior parte delle applicazioni MCI usa le funzioni [**mciSendString**](/previous-versions//dd757161(v=vs.85)) e [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) decine di volte. MCI offre alcune altre funzioni utili che l'applicazione userà meno frequentemente.

L'identificatore di dispositivo richiesto dalla maggior parte dei comandi MCI viene in genere recuperato in una chiamata al [**comando open**](open.md) ([**MCI \_ OPEN).**](mci-open.md) Se è necessario un identificatore di dispositivo ma non si vuole aprire il dispositivo, ad esempio se si vogliono eseguire query sulle funzionalità del dispositivo prima di eseguire altre azioni, è possibile chiamare la funzione [**mciGetDeviceID.**](/previous-versions//dd757156(v=vs.85))

La [**funzione mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) consente all'applicazione di usare un identificatore di dispositivo per recuperare un handle per l'attività che ha creato tale identificatore.

È possibile usare le funzioni [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) e [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) per assegnare e recuperare l'indirizzo della funzione di callback associata al flag "wait" (MCI \_ WAIT).

La [**funzione mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) recupera una stringa che descrive un valore di errore MCI. Ogni stringa restituita da MCI, indipendentemente dal fatto che i dati o una descrizione dell'errore, siano al massimo 128 caratteri. I campi della finestra di dialogo di dimensioni inferiori a 128 caratteri troncano le stringhe più lunghe restituite da MCI. Per altre informazioni su queste stringhe, vedere [VALORI RESTITUITI MCIERR](mcierr-return-values.md).

Le macro MCI sono strumenti che è possibile usare per creare e disassemblare valori che specificano i formati di ora. Questi formati di ora vengono usati in molti comandi MCI. I formati utilizzati dalle macro sono ore/minuti/secondi (HMS), minuti/secondi/fotogrammi (MSF) e tracce/minuti/secondi/fotogrammi (TMSF). Nella tabella seguente sono elencate le macro e le relative descrizioni.



| Macro                                        | Descrizione                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI \_ HMS \_ HOUR**](mci-hms-hour.md)       | Recupera il componente hours da un valore HMS.   |
| [**MINUTO \_ MCI HMS \_**](mci-hms-minute.md)   | Recupera il componente minuti da un valore HMS. |
| [**MCI \_ HMS \_ SECOND**](mci-hms-second.md)   | Recupera il componente secondi da un valore HMS. |
| [**MCI \_ MAKE \_ HMS**](mci-make-hms.md)       | Crea un valore HMS.                              |
| [**MCI \_ MAKE \_ MSF**](mci-make-msf.md)       | Crea un valore MSF.                              |
| [**MCI \_ MAKE \_ TMSF**](mci-make-tmsf.md)     | Crea un valore TMSF.                              |
| [**MCI \_ MSF \_ FRAME**](/previous-versions//dd743438(v=vs.85))     | Recupera il componente frames da un valore MSF.  |
| [**MCI \_ MSF \_ MINUTE**](mci-msf-minute.md)   | Recupera il componente minuti da un valore MSF. |
| [**MCI \_ MSF \_ SECOND**](mci-msf-second.md)   | Recupera il componente secondi da un valore MSF. |
| [**MCI \_ TMSF \_ FRAME**](mci-tmsf-frame.md)   | Recupera il componente frames da un valore TMSF.  |
| [**MCI \_ TMSF \_ MINUTE**](mci-tmsf-minute.md) | Recupera il componente minutes da un valore TMSF. |
| [**MCI \_ TMSF \_ SECOND**](mci-tmsf-second.md) | Recupera il componente secondi da un valore TMSF. |
| [**MCI \_ TMSF \_ TRACK**](mci-tmsf-track.md)   | Recupera il componente tracks da un valore TMSF.  |



 

MCI fornisce anche due messaggi: [**MM \_ MCINOTIFY**](mm-mcinotify.md) e [**MM \_ MCISIGNAL**](mm-mcisignal.md). Il messaggio MM MCINOTIFY notifica a un'applicazione il risultato di un comando MCI ogni volta che tale comando specifica il \_ flag "notify" (MCI \_ NOTIFY). Il messaggio MM MCISIGNAL è specifico per i dispositivi digital-video e invia una notifica all'applicazione quando viene raggiunta \_ una posizione specificata.

 

 