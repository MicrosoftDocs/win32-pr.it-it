---
title: Macro e messaggi di funzioni MCI
description: Macro e messaggi di funzioni MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Messaggi MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726994"
---
# <a name="mci-functions-macros-and-messages"></a>Macro e messaggi di funzioni MCI

La maggior parte delle applicazioni MCI usa le funzioni [**mciSendString**](/previous-versions//dd757161(v=vs.85)) e [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) dozzine di volte. MCI fornisce altre funzioni utili che l'applicazione utilizzerà con minore frequenza.

L'identificatore del dispositivo richiesto dalla maggior parte dei comandi MCI viene in genere recuperato in una chiamata al comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)). Se è necessario un identificatore di dispositivo ma non si vuole aprire il dispositivo, ad esempio se si vuole eseguire una query sulle funzionalità del dispositivo prima di eseguire qualsiasi altra azione, è possibile chiamare la funzione [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .

La funzione [**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) consente all'applicazione di usare un identificatore di dispositivo per recuperare un handle per l'attività che ha creato tale identificatore.

È possibile utilizzare le funzioni [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) e [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) per assegnare e recuperare l'indirizzo della funzione di callback associata al flag di attesa (MCI \_ Wait).

La funzione [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) recupera una stringa che descrive un valore di errore MCI. Ogni stringa restituita da MCI, che indica se i dati o una descrizione dell'errore, sono costituiti da un massimo di 128 caratteri. I campi della finestra di dialogo di dimensioni inferiori a 128 caratteri troncano le stringhe più lunghe restituite da MCI. Per ulteriori informazioni su queste stringhe, vedere [MCIERR return values](mcierr-return-values.md).

Le macro MCI sono strumenti che è possibile usare per creare e disassemblare valori che specificano i formati di ora. Questi formati di ora vengono usati in molti comandi MCI. I formati utilizzati dalle macro sono ore/minuti/secondi (HMS), minuti/secondi/frame (MSF) e tracce/minuti/secondi/frame (TMSF). Nella tabella seguente sono elencate le macro e le relative descrizioni.



| Macro                                        | Descrizione                                        |
|----------------------------------------------|----------------------------------------------------|
| [**ora di MCI \_ \_**](mci-hms-hour.md)       | Recupera il componente ore da un valore HMS.   |
| [**\_minuto dell'ottavo MCI \_**](mci-hms-minute.md)   | Recupera il componente minuti da un valore HMS. |
| [**\_secondo MCI \_**](mci-hms-second.md)   | Recupera il componente secondi da un valore HMS. |
| [**MCI \_ make \_ HMS**](mci-make-hms.md)       | Crea un valore HMS.                              |
| [**MCI \_ make \_ MSF**](mci-make-msf.md)       | Crea un valore MSF.                              |
| [**MCI \_ make \_ TMSF**](mci-make-tmsf.md)     | Crea un valore TMSF.                              |
| [**\_frame MSF di MCI \_**](/previous-versions//dd743438(v=vs.85))     | Recupera il componente frame da un valore MSF.  |
| [**\_minuto MSF di MCI \_**](mci-msf-minute.md)   | Recupera il componente minuti da un valore MSF. |
| [**\_secondo MSF di MCI \_**](mci-msf-second.md)   | Recupera il componente secondi da un valore MSF. |
| [**\_frame TMSF \_ MCI**](mci-tmsf-frame.md)   | Recupera il componente frames da un valore TMSF.  |
| [**\_TMSF \_ minuto MCI**](mci-tmsf-minute.md) | Recupera il componente minuti da un valore TMSF. |
| [**\_secondo TMSF \_ MCI**](mci-tmsf-second.md) | Recupera il componente secondi da un valore TMSF. |
| [**\_traccia TMSF \_ MCI**](mci-tmsf-track.md)   | Recupera il componente Tracks da un valore TMSF.  |



 

MCI fornisce anche due messaggi: [**mm \_ MCINOTIFY**](mm-mcinotify.md) e [**mm \_ MCISIGNAL**](mm-mcisignal.md). Il \_ messaggio mm MCINOTIFY notifica a un'applicazione il risultato di un comando MCI ogni volta che il comando specifica il flag di notifica (MCI \_ Notify). Il \_ messaggio MCISIGNAL mm è specifico per i dispositivi video digitali. Invia una notifica all'applicazione quando viene raggiunta una posizione specificata.

 

 