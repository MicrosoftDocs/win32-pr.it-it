---
title: Punti di ripristino
description: I punti di ripristino vengono creati per consentire agli utenti di scegliere gli Stati del sistema precedenti. Ogni punto di ripristino contiene le informazioni necessarie per ripristinare lo stato scelto per il sistema. I punti di ripristino vengono creati prima che vengano apportate modifiche alla chiave al sistema.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338751"
---
# <a name="restore-points"></a>Punti di ripristino

I punti di ripristino vengono creati per consentire agli utenti di selezionare uno stato precedente del sistema. Ogni punto di ripristino contiene le informazioni necessarie per ripristinare lo stato selezionato per il sistema. I punti di ripristino vengono creati prima che vengano apportate modifiche alla chiave al sistema.

Ripristino configurazione di sistema gestisce automaticamente lo spazio su disco allocato per i punti di ripristino. Elimina i punti di ripristino meno recenti per fare spazio a quelli nuovi. Ripristino configurazione di sistema alloca lo spazio in base alle dimensioni del disco rigido e alla versione di Windows eseguita dal computer, come illustrato nella tabella seguente.

|Versione di Windows |&nbsp;Dimensioni del disco rigido |Spazio ripristino sistema |
| --- | --- | --- |
|Windows 7 e versioni successive | > 64 GB |Fino al 5% dello spazio totale su disco o a un massimo di 10 GB, a seconda del valore minore |
|  | &le; 64 GB |Fino al 3% dello spazio totale su disco |
|Windows Vista |  |Fino al 15% dello spazio totale su disco o fino al 30% dello spazio disponibile su disco, a seconda del valore minore |
|Windows XP | >4 GB |Fino al 12% dello spazio totale su disco<br /><br />Per modificare il limite massimo di archiviazione in Windows XP, utilizzare l'elemento di **sistema** nel pannello di controllo. |
|  | \< 4 GB |Fino a 400 MB |

## <a name="event-triggered-restore-points"></a>Punti di ripristino attivati da eventi

Ripristino configurazione di sistema crea automaticamente un punto di ripristino prima che si verifichi uno degli eventi seguenti:

- **Installazione applicazione** (si applica solo alle applicazioni che usano un programma di installazione conforme al ripristino del sistema). Se l'installazione dell'applicazione causa problemi di sistema, l'utente può ripristinare il sistema in uno stato che precede l'installazione.
- **Installazione di Windows Update o AutoUpdate**. Windows Update (noto in precedenza come AutoUpdate) Scarica e installa automaticamente gli aggiornamenti di Windows. Inoltre, offre agli utenti un modo semplice per scaricare e installare manualmente gli aggiornamenti. Ripristino configurazione di sistema crea un punto di ripristino prima dell'installazione di un aggiornamento, sia in modo automatico che manuale.
- **Operazione di ripristino del sistema**. Ripristino configurazione di sistema crea automaticamente un punto di ripristino come backup prima che venga avviata un'operazione di ripristino. Si supponga, ad esempio, che un utente ripristini accidentalmente Windows a un punto di ripristino errato. Per annullare il ripristino, l'utente può ripristinare Windows a un punto di ripristino precedente al primo punto di ripristino. Una volta ripristinato lo stato iniziale di Windows, l'utente può ripetere il processo, selezionando il punto di ripristino corretto.

## <a name="scheduled-restore-points"></a>Punti di ripristino pianificati

Gli utenti possono configurare ripristino configurazione di sistema per creare punti di ripristino a intervalli regolari. Gli utenti possono anche creare manualmente un punto di ripristino e denominarlo in qualsiasi momento dall'interfaccia utente di ripristino del sistema. Questi punti di ripristino vengono salvati e compressi e sono disponibili nell'elenco dei punti di ripristino.

In Windows 7 e versioni successive, ripristino configurazione di sistema crea un punto di ripristino pianificato solo se non sono stati creati altri punti di ripristino nei sette giorni precedenti. In Windows Vista, ripristino configurazione di sistema crea un checkpoint ogni 24 ore se non sono stati creati altri punti di ripristino in quel giorno. In Windows XP, ripristino configurazione di sistema crea un checkpoint ogni 24 ore, indipendentemente dalle altre operazioni.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Problema noto: non è possibile ripristinare il sistema a un punto di ripristino dopo l'installazione di un aggiornamento di Windows 10

Considerare lo scenario seguente:

1. Installare Windows 10 in un computer pulito.
1. Si attiva la protezione del sistema e quindi si crea un punto di ripristino di sistema denominato "R1".
1. Installare uno o più aggiornamenti di Windows 10.
1. Al termine dell'installazione degli aggiornamenti, ripristinare il sistema nel punto di ripristino "R1".

In questo scenario, il sistema non viene ripristinato al punto di ripristino "R1". Al contrario, si verifica un errore irreversibile del computer (0xC000021A). Il computer viene riavviato, ma il sistema non può tornare al desktop di Windows.

### <a name="cause"></a>Causa

Si tratta di un problema noto in Windows 10.

Durante il processo di ripristino del sistema, Windows esegue temporaneamente il ripristino dei file in uso. Quindi Salva le informazioni nel registro di sistema. Quando il computer viene riavviato, viene completata l'operazione di gestione temporanea.

In questa situazione, Windows ripristina i file del catalogo e inserisce i file del driver (sys) da ripristinare quando il computer viene riavviato. Tuttavia, quando il computer viene riavviato, Windows carica i driver esistenti prima di ripristinare le versioni più recenti dei driver. Poiché le versioni dei driver non corrispondono alle versioni dei file di catalogo ripristinati, il processo di riavvio viene interrotto.

### <a name="workaround"></a>Soluzione alternativa

**Per eseguire il ripristino dal riavvio non riuscito e continuare il processo di ripristino**

Quando si verifica un errore, riavviare il computer fino a quando non entra in ambiente ripristino Windows (WinRE). A tale scopo, potrebbe essere necessario usare un cambio di riavvio hardware e potrebbe essere necessario riavviare più volte.

In ambiente ripristino Windows:

1. Selezionare **risoluzione dei problemi**  >  **Opzioni avanzate**  >  **altre**  >  **impostazioni di avvio** opzioni di ripristino e quindi fare clic su **Riavvia ora**.
1. Nell'elenco delle impostazioni di avvio selezionare **Disabilita imposizione firma driver**.
   > [!NOTE]  
   > Per selezionare questa impostazione, potrebbe essere necessario usare il tasto F7.
1. Consente di continuare il processo di avvio. Quando Windows viene riavviato, il processo di ripristino del sistema deve essere ripreso e terminato.

Questa procedura consente di ripristinare lo stato "R1" del computer.

**Per eseguire il ripristino dal riavvio non riuscito**

Per eseguire il ripristino dal riavvio non riuscito ed eseguire il rollback del processo di ripristino, attenersi alla seguente procedura:

1. Come descritto nella procedura precedente, riavviare il computer e quindi immettere WinRE.  
1. In ambiente ripristino Windows selezionare **risoluzione dei problemi**  >  **Opzioni avanzate**  >  **Ripristino configurazione di sistema**, quindi selezionare **Annulla ripristino configurazione di sistema**.

Questa procedura riporta il computer allo stato in cui si trovava prima di avviare il processo di ripristino.

**Per ripristinare Windows a un punto di ripristino tramite WinRE**

Per avviare Ripristino configurazione di sistema in un computer interessato, utilizzare WinRE anziché la finestra di dialogo **Impostazioni** . A questo scopo, seguire questa procedura:

1. Selezionare **Avvia**  >  **Impostazioni**  >  **Aggiorna &**  >  **ripristino** di sicurezza.
1. In **Opzioni avanzate** selezionare **Riavvia ora**.
1. Dopo l'avvio di WinRE, selezionare **Risolvi** le  >  **Opzioni avanzate**  >  **Ripristino configurazione di sistema**.
1. Immettere la chiave di ripristino visualizzata sullo schermo, quindi seguire le istruzioni della procedura guidata ripristino configurazione di sistema.

### <a name="references"></a>Riferimenti

Per ulteriori informazioni sull'utilizzo di WinRE, vedere gli articoli seguenti:

- [Ambiente ripristino Windows (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Avviare il PC in modalità provvisoria in Windows 10](https://support.microsoft.com/help/12376) 