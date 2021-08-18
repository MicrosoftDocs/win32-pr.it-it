---
title: Punti di ripristino
description: I punti di ripristino vengono creati per consentire agli utenti di scegliere gli stati di sistema precedenti. Ogni punto di ripristino contiene le informazioni necessarie per ripristinare lo stato scelto del sistema. I punti di ripristino vengono creati prima di apportare modifiche chiave al sistema.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 56cc7035f2e5a152ad90205257fb86ddaef8bf565f8459cb5067874280946db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968040"
---
# <a name="restore-points"></a>Punti di ripristino

I punti di ripristino vengono creati per consentire agli utenti di selezionare uno stato precedente del sistema. Ogni punto di ripristino contiene le informazioni necessarie per ripristinare lo stato selezionato del sistema. I punti di ripristino vengono creati prima di apportare modifiche chiave al sistema.

Ripristino configurazione di sistema gestisce automaticamente lo spazio su disco allocato per i punti di ripristino. Elimina i punti di ripristino meno recenti per fare spazio a quelli nuovi. Ripristino configurazione di sistema alloca spazio in base alle dimensioni del disco rigido e alla versione Windows esecuzione del computer, come illustrato nella tabella seguente.

|Versione di Windows |Dimensioni &nbsp; del disco rigido |Ripristino configurazione di sistema spazio |
| --- | --- | --- |
|Windows 7 e versioni successive | > 64 GB |Fino al 5% dello spazio totale su disco o un massimo di 10 GB, a seconda del valore minore |
|  | &le; 64 GB |Fino al 3% dello spazio totale su disco |
|Windows Vista |  |Fino al 15% dello spazio totale su disco o un massimo del 30% dello spazio disponibile su disco, a seconda del valore minore |
|Windows XP | >4 GB |Fino al 12% dello spazio totale su disco<br /><br />Per modificare il limite massimo di archiviazione in Windows XP, usare **l'elemento System** in Pannello di controllo. |
|  | \< 4gb |Fino a 400 MB |

## <a name="event-triggered-restore-points"></a>Punti di ripristino attivati da eventi

Ripristino configurazione di sistema crea automaticamente un punto di ripristino prima che si verifichi uno degli eventi seguenti:

- **Installazione dell'applicazione** (si applica solo alle applicazioni che usano un programma Ripristino configurazione di sistema programma di installazione conforme. Se l'installazione dell'applicazione causa problemi di sistema, l'utente può ripristinare lo stato precedente all'installazione.
- **Windows'installazione di Aggiornamento automatico o Aggiornamento automatico**. Windows L'aggiornamento (noto in precedenza come Aggiornamento automatico) scarica e installa automaticamente Windows aggiornamenti. Offre inoltre agli utenti un modo semplice per scaricare e installare manualmente gli aggiornamenti. Ripristino configurazione di sistema crea un punto di ripristino prima dell'installazione di un aggiornamento, sia automaticamente che manualmente.
- **Operazione di ripristino del sistema**. Ripristino configurazione di sistema crea automaticamente un punto di ripristino come backup prima dell'avvio di qualsiasi operazione di ripristino. Si supponga, ad esempio, che un utente ripristini accidentalmente Windows un punto di ripristino non corretto. Per annullare il ripristino, l'utente può Windows un punto di ripristino precedente al primo punto di ripristino. Dopo Windows stato iniziale, l'utente può ripetere il processo, questa volta selezionando il punto di ripristino corretto.

## <a name="scheduled-restore-points"></a>Punti di ripristino pianificati

Gli utenti possono configurare Ripristino configurazione di sistema per creare punti di ripristino a intervalli regolari. Gli utenti possono anche creare e assegnare manualmente un nome a un punto di ripristino in qualsiasi momento dall'Ripristino configurazione di sistema utente. Questi punti di ripristino vengono salvati e compressi e sono disponibili nell'elenco dei punti di ripristino.

In Windows 7 e versioni successive, Ripristino configurazione di sistema crea un punto di ripristino pianificato solo se non sono stati creati altri punti di ripristino nei sette giorni precedenti. In Windows Vista, Ripristino configurazione di sistema un checkpoint ogni 24 ore se non sono stati creati altri punti di ripristino in quel giorno. In Windows XP, Ripristino configurazione di sistema un checkpoint ogni 24 ore, indipendentemente da altre operazioni.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Problema noto: non è possibile ripristinare il sistema in un punto di ripristino dopo l'installazione di un Windows 10 aggiornamento

Considerare lo scenario seguente:

1. Si installa Windows 10 in un computer pulito.
1. Si attiva la protezione del sistema e quindi si crea un punto di ripristino di sistema denominato "R1".
1. Si installano uno o più Windows 10 aggiornamenti.
1. Al termine dell'installazione degli aggiornamenti, si ripristina il sistema nel punto di ripristino "R1".

In questo scenario il sistema non viene ripristinato nel punto di ripristino "R1". Al contrario, nel computer si verifica un errore di arresto (0xc000021a). Il computer viene riavviato, ma il sistema non può tornare al Windows desktop.

### <a name="cause"></a>Causa

Si tratta di un problema noto in Windows 10.

Durante il processo di ripristino del sistema, Windows temporaneamente il ripristino dei file in uso. Le informazioni vengono quindi salvate nel Registro di sistema. Quando il computer viene riavviato, completa l'operazione di gestione a fasi.

In questo caso, Windows i file del catalogo e i file del driver (.sys) da ripristinare al riavvio del computer. Tuttavia, quando il computer viene riavviato, Windows i driver esistenti prima di ripristinare le versioni successive dei driver. Poiché le versioni del driver non corrispondono alle versioni dei file del catalogo ripristinati, il processo di riavvio viene arrestato.

### <a name="workaround"></a>Soluzione alternativa

**Per eseguire il ripristino dal riavvio non riuscito e continuare il processo di ripristino**

Dopo che si è verificato l'errore, riavviare il computer fino a quando non entra nell'Windows recovery environment (WinRE). A tale scopo, potrebbe essere necessario usare un'opzione di riavvio hardware e potrebbe essere necessario riavviare più volte.

Nell'Windows di ripristino:

1. Selezionare **Risoluzione dei problemi** Opzioni  >  **avanzate** Altre opzioni di  >  **ripristino** Impostazioni di  >  **avvio** e quindi selezionare **Riavvia ora**.
1. Nell'elenco delle impostazioni di avvio selezionare Disabilita imposizione **firma driver**.
   > [!NOTE]  
   > Potrebbe essere necessario usare il tasto F7 per selezionare questa impostazione.
1. Lasciare che il processo di avvio continui. Quando Windows riavvio, il processo di ripristino del sistema deve riprendere e terminare.

Questi passaggi ripristinano lo stato "R1" del computer.

**Per eseguire il ripristino dal riavvio non riuscito**

Per eseguire il ripristino dal riavvio non riuscito ed eseguire il rollback del processo di ripristino, seguire questa procedura:

1. Come descritto nella procedura precedente, riavviare il computer e quindi immettere WinRE.  
1. Nell'Windows di ripristino selezionare Risoluzione **dei problemi**  >  **opzioni avanzate** Ripristino di sistema e quindi  >  scegliere Annulla ripristino **di sistema**.

Questi passaggi restituiscono il computer allo stato in cui si era presente prima di iniziare il processo di ripristino.

**Per ripristinare Windows in un punto di ripristino tramite WinRE**

Per avviare la Ripristino configurazione di sistema guidata in un computer interessato, usare WinRE anziché la Impostazioni **finestra** di dialogo. A questo scopo, seguire questa procedura:

1. Selezionare **Start**  >  **Impostazioni**  >  Update & Security Recovery (Avvia aggiornamento &**Security**  >  **Recovery).**
1. In **Opzioni avanzate** selezionare **Riavvia ora**.
1. Dopo l'avvio di WinRE, selezionare **Risoluzione dei problemi opzioni** avanzate  >  **Ripristino** del  >  **sistema**.
1. Immettere la chiave di ripristino così come viene visualizzata sullo schermo e quindi seguire le istruzioni nella Ripristino configurazione di sistema guidata.

### <a name="references"></a>Riferimenti

Per altre informazioni su come usare WinRE, vedere gli articoli seguenti:

- [Windows Ambiente di ripristino (Ambiente ripristino Windows)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Avviare il PC in modalità provvisoria in Windows 10](https://support.microsoft.com/help/12376) 