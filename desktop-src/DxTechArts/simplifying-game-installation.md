---
title: Semplificazione dell'installazione del gioco
description: Questo articolo illustra alcuni concetti che gli sviluppatori di giochi per Windows possono e devono implementare per migliorare l'esperienza complessiva.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8728eb2c9c53a99673ee742a5c961b91e37abed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338431"
---
# <a name="simplifying-game-installation"></a>Semplificazione dell'installazione del gioco

Uno dei principali vantaggi dei giochi eseguiti in una console anziché in Windows è il processo di installazione o la loro mancanza. Quando un gioco viene eseguito per la prima volta in una console di, il lettore effettua alcune scelte o conferme ed è in grado di iniziare a giocare quasi immediatamente. L'installazione di un gioco in Windows è più complicata, in base al confronto, dalla necessità di un input utente sostanziale e dal processo di installazione potenzialmente lungo. Questo processo di installazione può tuttavia essere migliorato per offrire un'esperienza migliore per i giocatori di giochi basati su Windows. Questo articolo illustra alcuni concetti che gli sviluppatori di giochi per Windows possono e devono implementare per migliorare l'esperienza complessiva.

-   [Installazione tipica del gioco](#typical-game-installation)
-   [Installazione semplificata del gioco](#simplified-game-installation)
    -   [Porre tutte le domande in primo piano](#ask-all-questions-up-front)
    -   [Fornire modalità di installazione speciali](#provide-special-installation-modes)
    -   [Ridurre al minimo la quantità di domande sull'installazione](#minimize-the-quantity-of-installation-questions)
    -   [Modificare i componenti facoltativi in componenti necessari](#change-optional-components-into-required-components)
    -   [Installare sempre DirectX ed eseguire questa operazione in modo invisibile all'utente](#always-install-directx-and-do-so-silently)
    -   [Considerare il contratto di licenza](#think-about-your-eula)
    -   [Avvia automaticamente dopo l'installazione](#automatically-launch-after-installation)
    -   [Ottimizzare le prestazioni di installazione](#optimize-your-installation-performance)
    -   [Registra con Windows Firewall durante l'installazione](#register-with-windows-firewall-during-installation)
    -   [Installare per tutti gli utenti, non solo per l'utente corrente](#install-for-all-users-not-just-the-current-user)
-   [Esempio di installazione semplificata](#example-of-simplified-installation)
-   [Summary](#summary)

## <a name="typical-game-installation"></a>Installazione tipica del gioco

Quando si confronta la facilità di installazione e la quantità di tempo necessaria per iniziare la riproduzione di un gioco, la tipica esperienza Xbox è molto migliore di Windows. Il diagramma di flusso nella figura 1 Mostra i processi di installazione tipici in Xbox e in Windows, per il confronto.

**Figura 1. Processo di installazione tipico, Xbox rispetto a Windows**

![Xbox \- vs \- PC](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Installazione semplificata del gioco

Tuttavia, i requisiti maggiori per l'installazione di un gioco in Windows non devono necessariamente essere. Implementando i concetti seguenti, si riduce il numero di passaggi che un utente deve completare, che può ridurre la quantità di tempo necessaria per l'installazione.

### <a name="ask-all-questions-up-front"></a>Porre tutte le domande in primo piano

Tutte le scelte selezionate dal Gamer durante l'installazione che potrebbero causare l'interruzione dell'installazione devono essere offerte prima di quelle che non interrompono l'installazione. lo scenario peggiore si riferisce al giocatore a cui viene offerta una scelta che può causare l'interruzione dell'installazione dopo che il gioco è stato completamente copiato dal supporto di installazione. Questo può essere particolarmente frustrante se l'installazione richiede il completamento dello scambio di più dischi. È consigliabile progettare il programma di installazione per porre tutte le domande importanti, ad esempio l'accettazione del contratto di licenza, all'inizio del processo, in modo che non sia necessario eseguire il rollback dell'installazione al termine del processo.

È anche possibile richiedere all'utente di accettare il contratto di licenza e immettere il codice Product Key quando il gioco viene avviato per la prima volta, anziché richiederli come parte dell'installazione. In questo scenario, se si rifiuta di accettare il contratto di licenza o di annullare l'operazione durante l'immissione del codice "Product Key", non verrà eseguito il rollback dell'installazione, perché queste richieste fanno parte del gioco stesso. Questo potrebbe essere utile se sono stati preinstallati o gli scenari OEM. Tuttavia, prestare attenzione a non richiedere all'utente di effettuare scelte durante l'avvio iniziale che richiedono credenziali amministrative.

### <a name="provide-special-installation-modes"></a>Fornire modalità di installazione speciali

Idealmente, i programmi di installazione di Windows Game devono offrire solo modalità di installazione completamente automatica e personalizzata e niente di più.

La modalità automatica non dovrebbe porre altre domande rispetto a quanto sia assolutamente necessario per creare un'installazione funzionante e utilizzare semplicemente le impostazioni predefinite senza richiedere altre opzioni. Molti giocatori non sono interessati alla posizione del gioco sul disco rigido o alle impostazioni iniziali del gioco, ma vogliono semplicemente riprodurre il gioco il prima possibile.

La modalità personalizzata deve essere solo per gli utenti esperti che necessitano o vogliono modificare il percorso di installazione o altre opzioni di installazione e non deve essere la modalità predefinita.

La modalità personalizzata può offrire la scelta di un'installazione completa o di un'installazione minima che installa solo i file necessari per riprodurre il gioco. Se il giocatore sceglie l'installazione minima, il gioco può usare le tecniche di installazione su richiesta o di streaming per leggere i dati di installazione rimanenti, consentendo al giocatore di iniziare a giocare rapidamente senza dover attendere il completamento di un'installazione completa. Tuttavia, l'installazione dei dati in questo modo influisca sulla progettazione del motore di gioco. Per ulteriori informazioni sull'installazione del contenuto su richiesta, vedere [Install-on-demand per giochi](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Ridurre al minimo la quantità di domande sull'installazione

In entrambe le modalità di installazione, è consigliabile tentare di limitare il numero di volte in cui viene richiesto al giocatore durante l'installazione. In questo modo si riduce la quantità di letture necessaria per installare ed eseguire il gioco. Se necessario, al termine dell'installazione dovrebbe essere presente un solo prompt di completamento. Come si può notare, l'esempio illustrato nella figura 1 contiene troppi prompt di post-installazione.

### <a name="change-optional-components-into-required-components"></a>Modificare i componenti facoltativi in componenti necessari

Eseguire l'installazione di tutti i componenti necessari anziché renderli facoltativi, a meno che non esista un motivo valido per eseguire altre operazioni. Semplicemente l'installazione di tutti i componenti farà iniziare il gioco senza ulteriori ritardi e complicazioni.

### <a name="always-install-directx-and-do-so-silently"></a>Installare sempre DirectX ed eseguire questa operazione in modo invisibile all'utente

Si consiglia vivamente di installare il gioco in modo invisibile all'utente DirectX ridistribuibile su cui è stato compilato il gioco. Il processo di installazione di DirectX è progettato in modo da verificare se è necessario aggiornare qualsiasi elemento e restituisce rapidamente un risultato in caso contrario. Non è quindi necessario richiedere agli utenti se si vuole che DirectX sia installato. Un'installazione invisibile all'utente di DirectX può essere eseguita eseguendo questo comando dal pacchetto di installazione: **dxsetup.exe/Silent**

Chiedere a un utente se desidera installare DirectX può causare molti problemi. Se, ad esempio, l'utente presume che disponga dell'ultimo componente ridistribuibile installato e sceglie di ignorare l'installazione di DirectX; l'installazione del gioco può comunque continuare. Tuttavia, se il gioco richiede una versione specifica di D3DX o altre funzionalità aggiornate ignorate, il gioco non funzionerà e l'utente sarà frustrato.

Se per qualche motivo è necessario chiedere all'utente se desidera installare DirectX, il programma di installazione deve almeno interrompere ed eseguire il rollback dell'intero processo di installazione se l'utente sceglie di non installare DirectX. Il rollback dell'installazione eviterà eventuali errori causati dal sistema in cui non è installata la versione più recente di DirectX quando viene avviato il gioco.

Si noti che è importante fornire il ridistribuibile con cui è stato compilato il gioco anziché semplicemente il ridistribuibile dalla versione più recente di DirectX SDK. Il più recente ridistribuibile potrebbe non contenere tutti i componenti disponibili in una versione precedente.

È anche importante fare in modo che il programma di installazione verifichi che cosa è già installato e determinare se il riavvio del sistema è necessario. Se DirectX è aggiornato, la copia di una DLL non dovrebbe richiedere il riavvio.

### <a name="think-about-your-eula"></a>Considerare il contratto di licenza

Il contratto di licenza DirectX può e deve essere aggiunto al contratto di licenza per gli sviluppatori di giochi. Non è possibile consentire all'utente di accettare le condizioni di licenza per gli sviluppatori e non il contratto di licenza DirectX. L'utente deve accettare sia EULA che non installare il gioco. Se uno sviluppatore ritiene che debba offrire la scelta dell'utente, l'intera installazione avrà esito negativo se l'utente sceglie di non accettare il contratto di licenza DirectX.

Se possibile, consultare il reparto legale per verificare se è possibile evitare il totale delle EULA e usare un contratto di licenza con ritorno a capo ridotto come l'uso dei giochi console. In questo modo si eviterà la necessità di richiedere agli utenti di accettare il contratto di licenza. Il contratto di licenza DirectX deve essere aggiunto al contratto di licenza con incapsulamento ridotto; in caso contrario, deve essere visualizzato e accettato il contratto di licenza DirectX che vanifica lo scopo dell'uso di un contratto di licenza con ritorno a capo ridotto.

Un'eccezione a un contratto di licenza con incapsulamento ridotto è per un editor di contenuto. Qualsiasi editor deve visualizzare un contratto di licenza durante l'installazione dell'editor o quando l'editor viene avviato per la prima volta. Molti giocatori sono interessati solo alla riproduzione e non alla creazione di contenuto, pertanto l'installazione di un editor deve essere un processo separato.

### <a name="automatically-launch-after-installation"></a>Avvia automaticamente dopo l'installazione

Quasi tutti i giocatori vogliono giocare un gioco non appena lo ricevono. Per impostazione predefinita, il programma di installazione deve avviare il gioco dopo aver completato l'installazione, sebbene sia consigliabile, in un'installazione personalizzata, specificare questa opzione in una casella di controllo che l'utente potrebbe ignorare.

### <a name="optimize-your-installation-performance"></a>Ottimizzare le prestazioni di installazione

Gli sviluppatori devono testare le proprie installazioni per determinare la quantità di tempo necessaria per l'installazione. Gli sviluppatori possono ridurre i tempi di installazione utilizzando la versione più recente degli strumenti di installazione e ottimizzando il layout dei dati nei supporti di installazione. La maggior parte degli strumenti di creazione DVD include opzioni per l'ottimizzazione del layout che possono migliorare i tempi di installazione senza aumentare il carico di lavoro di sviluppo

### <a name="register-with-windows-firewall-during-installation"></a>Registra con Windows Firewall durante l'installazione

Se il gioco può essere eseguito come server o il modello di rete del gioco è peer-to-peer, registrare il gioco con Windows Firewall al momento dell'installazione. In questo modo si impedisce la visualizzazione della finestra di dialogo del firewall al centro del gioco quando l'utente tenta di accedere alla rete. Se il gioco è un client puro, il programma di installazione non dovrebbe aggiungere il gioco all'elenco di eccezioni del firewall.

Per ulteriori informazioni, vedere Windows Firewall per gli sviluppatori di giochi.

### <a name="install-for-all-users-not-just-the-current-user"></a>Installare per tutti gli utenti, non solo per l'utente corrente

Per impostazione predefinita, è sufficiente installare il gioco per tutti gli utenti. Ciò consentirà a tutti i nuovi utenti del sistema di riprodurre il gioco senza doverlo installare. Se viene effettuato un tentativo di installazione per tutti gli utenti su un account utente Least-Privileged, il programma di installazione non riuscirà o richiederà all'utente una password di amministratore. Quindi, provare a rilevare se l'account dispone di privilegi appropriati prima di offrire l'opzione per l'installazione di tutti gli utenti. Se l'utente sceglie di installare il gioco solo per l'utente corrente, assicurarsi di modificare il percorso di installazione in un percorso all'interno del profilo dell'utente. Idealmente, modificare il percorso in un punto qualsiasi nei dati dell'applicazione non in roaming, ad esempio una sottodirectory di CSIDL \_ Local \_ AppData.

## <a name="example-of-simplified-installation"></a>Esempio di installazione semplificata

Nella figura 2 è riportato un esempio di un processo migliorato per l'installazione di un gioco in Windows, con finestre di dialogo di installazione semplificate.

**Figura 2. Processo di installazione semplificato**

![Installazione](images/simplifiedgameinstall.png)

Di seguito sono riportati alcuni aspetti importanti:

-   Il programma di installazione viene avviato automaticamente al momento dell'inserimento del disco di installazione (esecuzione automatica).
-   La schermata iniziale, con le opzioni per installare, rimuovere, visualizzare il sito Web o uscire, non viene visualizzata se il gioco non è ancora installato nel computer.
-   La finestra di dialogo di **installazione** è la prima finestra di dialogo visualizzata dal programma di installazione.
-   Il pulsante **Installa** indica l'implementazione della modalità di installazione automatica.
-   Il pulsante **Opzioni** è l'implementazione della modalità di installazione personalizzata.
-   Il pulsante **Annulla** chiuderà immediatamente il programma di installazione. Poiché l'avvio del programma di installazione è un'azione semplice per l'utente, non richiedere conferma.
-   Quando l'utente accetta il contratto di licenza e immette un codice Product Key valido, viene avviata l'installazione.
-   Al termine del processo di installazione, il gioco viene avviato automaticamente o Visualizza una finestra di dialogo che avvisa l'utente che l'installazione è stata completata e offre opzioni aggiuntive, a seconda che sia stata selezionata l'opzione **Esegui gioco dopo l'installazione** .
-   La casella di controllo **Esegui gioco** offre un'altra possibilità di avviare il gioco per praticità. Per impostazione predefinita, questa opzione è sempre deselezionata, perché la finestra di dialogo **installazione completata** può essere visualizzata solo se l'opzione **Esegui gioco dopo l'installazione** è stata deselezionata nella finestra di dialogo **Opzioni di installazione** .
-   Il pulsante **OK** consente di escludere la finestra di dialogo e, facoltativamente, di **eseguire** un'azione sulle caselle di controllo Esegui e **Visualizza il file Leggimi** .

## <a name="summary"></a>Riepilogo

I giocatori desiderano giocare una partita appena possibile. L'ultima cosa che un giocatore vuole fare è guadare i dialoghi ed effettuare scelte identiche a quelle di tutti gli altri giochi installati. Implementando queste idee è possibile ridurre la quantità di tempo impiegato da un giocatore per l'installazione di un gioco in Windows e contribuire a migliorare la qualità complessiva dell'esperienza di gioco Windows.

 

 