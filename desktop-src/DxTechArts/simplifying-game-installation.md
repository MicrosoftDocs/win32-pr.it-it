---
title: Semplificazione dell'installazione del gioco
description: Questo articolo illustra alcuni concetti che gli sviluppatori di giochi per Windows possono e devono implementare per migliorare l'esperienza complessiva.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53062b9905e59435f1b9175eb95832294d93e51193003622d3bcc6dd16ee07df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042471"
---
# <a name="simplifying-game-installation"></a>Semplificazione dell'installazione del gioco

Uno dei principali vantaggi dei giochi che vengono eseguiti in una console anziché Windows è il processo di installazione o la loro mancanza. Quando un gioco viene eseguito per la prima volta in una console, il giocatore effettua alcune scelte o conferme ed è in grado di iniziare a giocare quasi immediatamente. L'installazione di un gioco Windows è più complessa, a confronto, dalla necessità di input utente sostanziale e dal processo di installazione potenzialmente lungo. Tuttavia, questo processo di installazione può essere migliorato per offrire un'esperienza migliore per i giocatori Windows giochi basati su Windows. Questo articolo illustra alcuni concetti che gli sviluppatori di giochi per Windows possono e devono implementare per migliorare l'esperienza complessiva.

-   [Installazione tipica del gioco](#typical-game-installation)
-   [Installazione semplificata del gioco](#simplified-game-installation)
    -   [Porre tutte le domande in anticipo](#ask-all-questions-up-front)
    -   [Fornire modalità di installazione speciali](#provide-special-installation-modes)
    -   [Ridurre al minimo la quantità di domande di installazione](#minimize-the-quantity-of-installation-questions)
    -   [Modificare i componenti facoltativi in componenti necessari](#change-optional-components-into-required-components)
    -   [Installare sempre DirectX e farlo in modo invisibile all'utente](#always-install-directx-and-do-so-silently)
    -   [Pensare al proprio EULA](#think-about-your-eula)
    -   [Avvia automaticamente dopo l'installazione](#automatically-launch-after-installation)
    -   [Ottimizzare le prestazioni di installazione](#optimize-your-installation-performance)
    -   [Eseguire la registrazione con Windows firewall durante l'installazione](#register-with-windows-firewall-during-installation)
    -   [Installazione per tutti gli utenti, non solo per l'utente corrente](#install-for-all-users-not-just-the-current-user)
-   [Esempio di installazione semplificata](#example-of-simplified-installation)
-   [Summary](#summary)

## <a name="typical-game-installation"></a>Installazione tipica del gioco

Quando si confrontano la facilità di installazione e la quantità di tempo necessaria per iniziare a riprodurre un gioco, l'esperienza tipica di Xbox è molto migliore di Windows. Il diagramma di flusso nella figura 1 mostra i processi di installazione tipici in Xbox e Windows, per il confronto.

**Figura 1. Processo di installazione tipico, Xbox e Windows**

![xbox \- e \- pc](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Installazione semplificata del gioco

Tuttavia, non è necessario che i requisiti più richiesti all'utente per installare un gioco Windows non siano necessari. Implementando i concetti seguenti, si ridurrà il numero di passaggi che un utente deve completare, riducendo così la quantità di tempo necessaria per l'installazione.

### <a name="ask-all-questions-up-front"></a>Porre tutte le domande in anticipo

Tutte le scelte selezionate dal giocatore durante l'installazione che potrebbero causare l'interruzione dell'installazione devono essere offerte prima di quelle che non arrestano l'installazione. Lo scenario peggiore è che al giocatore sia offerta una scelta che potrebbe causare l'interruzione dell'installazione dopo che il gioco è stato completamente copiato dal supporto di installazione. Questo può essere particolarmente frustrante se l'installazione richiede lo scambio di più dischi per il completamento. È consigliabile progettare il programma di installazione in modo da porre tutte le domande importanti (ad esempio l'accettazione dell'EULA) all'inizio del processo, in modo che non sia necessario eseguire il rollback dell'installazione in corrispondenza o in prossimità del completamento.

È anche possibile richiedere all'utente di accettare il contratto di licenza e di immettere il codice Product Key quando il gioco viene avviato per la prima volta, anziché richiederlo come parte dell'installazione. In questo scenario, il rifiuto di accettare il contratto di licenza o l'annullamento durante l'immissione del codice Product Key non esegue il rollback dell'installazione, perché queste richieste fanno parte del gioco stesso. Questo potrebbe essere utile se sono stati preinstallati o scenari OEM. È tuttavia necessario non chiedere all'utente di effettuare scelte durante l'avvio iniziale che richiedono credenziali amministrative.

### <a name="provide-special-installation-modes"></a>Fornire modalità di installazione speciali

Idealmente, Windows programmi di installazione del gioco dovrebbero offrire solo modalità di installazione completamente automatiche e personalizzate e niente in mezzo.

La modalità automatica non deve porre altre domande del necessario per creare un'installazione funzionante e usare semplicemente le impostazioni predefinite senza richiedere altre opzioni. Molti giocatori non si preoccupano della posizione del gioco sul disco rigido o delle impostazioni iniziali del gioco, ma vogliono solo giocare il prima possibile.

La modalità personalizzata deve essere solo per gli utenti esperti che necessitano o vogliono modificare il percorso di installazione o altre opzioni di installazione e non deve essere la modalità predefinita.

La modalità personalizzata può offrire la scelta di un'installazione completa o di un'installazione minima che installa solo i file necessari per riprodurre il gioco. Se il giocatore sceglie l'installazione minima, il gioco può usare tecniche di installazione su richiesta o di streaming per leggere i dati di installazione rimanenti, che consentono al giocatore di iniziare a riprodurre rapidamente il gioco senza dover attendere il completamento di un'installazione completa. Tuttavia, l'installazione dei dati in questo modo influisce sulla progettazione del motore di gioco. Per altre informazioni sull'installazione di contenuto su richiesta, [vedere Install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Ridurre al minimo la quantità di domande di installazione

In entrambe le modalità di installazione è consigliabile provare a limitare il numero di richieste al giocatore durante l'installazione. In questo modo si ridurrà la quantità di lettura necessaria per installare e eseguire il gioco. Se necessario, al termine dell'installazione dovrebbe essere presente un solo prompt di follow-up. Come si può vedere, nell'esempio illustrato nella figura 1 sono presenti troppe richieste post-installazione.

### <a name="change-optional-components-into-required-components"></a>Modificare i componenti facoltativi in componenti necessari

Rendere l'installazione di tutti i componenti necessari anziché renderli facoltativi, a meno che non ci sia un buon motivo per farlo. La semplice installazione di tutti i componenti farà iniziare il gioco senza ulteriori ritardi e senza alcun preavviso.

### <a name="always-install-directx-and-do-so-silently"></a>Installare sempre DirectX e farlo in modo invisibile all'utente

È consigliabile che il gioco installi automaticamente directx ridistribuibile su cui è stato compilato il gioco. Il processo di installazione di DirectX è progettato in modo da verificare se è necessario aggiornare qualsiasi elemento e restituisce rapidamente in caso di errore. Non è quindi necessario chiedere agli utenti se vogliono installare DirectX. È possibile eseguire un'installazione invisibile all'utente di DirectX eseguendo questo comando dal pacchetto di installazione: **dxsetup.exe /silent**

Chiedere a un utente se vuole installare DirectX può causare molti problemi. Ad esempio, se l'utente presuppone che sia installata la versione più recente ridistribuibile e sceglie di ignorare l'installazione di DirectX; L'installazione del gioco potrebbe continuare comunque correttamente. Tuttavia, se il gioco richiede una versione specifica di D3DX o altre funzionalità aggiornate ignorate, il gioco non funzionerà e l'utente sarà molto frustrato.

Se per qualche motivo è necessario chiedere all'utente se vuole installare DirectX, il programma di installazione deve interrompere ed eseguire il rollback dell'intero processo di installazione se l'utente sceglie di non installare DirectX. Il rollback dell'installazione eviterà eventuali errori causati dal sistema che non ha installato la versione più recente di DirectX all'avvio del gioco.

Si noti che è importante distribuire il ridistribuibile su cui è stato compilato il gioco anziché semplicemente distribuirlo dalla versione più recente di DirectX SDK. La versione ridistribuibile più recente potrebbe non contenere tutti i componenti trovati in una versione precedente.

È anche importante fare in modo che il programma di installazione controlli per verificare cosa è già installato e determinare se è necessario riavviare il sistema. Se DirectX è aggiornato, la copia di una DLL non deve richiedere il riavvio.

### <a name="think-about-your-eula"></a>Pensa al tuo EULA

L'EULA di DirectX può e deve essere aggiunto all'EULA dello sviluppatore di giochi. Non è necessario consentire all'utente di accettare l'EULA dello sviluppatore e non il programma EULA di DirectX. L'utente deve accettare entrambi gli EULA o non installare il gioco. Se uno sviluppatore ritiene di doversi offrire all'utente la scelta, l'intera installazione avrà esito negativo se l'utente sceglie di non accettare l'EULA di DirectX.

Se possibile, rivolgersi al reparto legale per verificare se è possibile evitare completamente gli EULA e usare un EULA con riduzione, ad esempio l'uso di giochi per console. In questo modo non sarà necessario chiedere agli utenti se vogliono accettare il contratto di licenza. L'EULA di DirectX deve essere aggiunto all'EULA con wrapping compattato; In caso contrario, è necessario visualizzare e accettare l'EULA di DirectX, che non consente di usare un'EULA con ritorno a capo automatico.

Un'eccezione a un'EULA con wrapping compattato è per un editor di contenuto. Qualsiasi editor deve visualizzare un EULA durante l'installazione dell'editor o quando l'editor viene avviato per la prima volta. Molti giocatori sono interessati solo a giocare e non a creare contenuto, quindi l'installazione di un editor deve essere un processo separato.

### <a name="automatically-launch-after-installation"></a>Avvia automaticamente dopo l'installazione

Quasi tutti i giocatori vogliono fare un gioco non appena lo ricevono. Per impostazione predefinita, il programma di installazione deve avviare il gioco al termine dell'installazione, anche se è consigliabile, in un'installazione personalizzata, specificarlo in una casella di controllo di cui l'utente può eseguire l'override.

### <a name="optimize-your-installation-performance"></a>Ottimizzare le prestazioni di installazione

Gli sviluppatori devono testare le installazioni per determinare il tempo necessario per l'installazione. Gli sviluppatori possono ridurre i tempi di installazione usando la versione più recente degli strumenti di installazione e ottimizzando il layout dei dati nel supporto di installazione. La maggior parte degli strumenti di creazione di DVD ha opzioni per l'ottimizzazione del layout che possono migliorare i tempi di installazione senza aumentare il carico di lavoro di sviluppo.

### <a name="register-with-windows-firewall-during-installation"></a>Eseguire la registrazione con Windows firewall durante l'installazione

Se il gioco può essere eseguito come server o il modello di rete del gioco è peer-to-peer, registrare il gioco con il firewall Windows durante l'installazione. Ciò impedirà la visualizzazione della finestra di dialogo del firewall nel mezzo del gioco quando l'utente prova ad accedere alla rete. Se il gioco è un client puro, il programma di installazione non deve aggiungere il gioco all'elenco delle eccezioni del firewall.

Per altre informazioni, vedere Firewall Windows per sviluppatori di giochi.

### <a name="install-for-all-users-not-just-the-current-user"></a>Installazione per tutti gli utenti, non solo per l'utente corrente

È sufficiente installare il gioco per impostazione predefinita per tutti gli utenti. In questo modo qualsiasi nuovo utente del sistema può eseguire il gioco senza doverlo installare. Se viene tentata l'installazione per tutti gli utenti in un account utente Least-Privileged, il programma di installazione avrà esito negativo o richiederà all'utente una password amministratore. Provare quindi a rilevare se l'account dispone di privilegi adeguati prima di offrire l'opzione di installazione per tutti gli utenti. Se l'utente sceglie di installare il gioco solo per l'utente corrente, assicurarsi di modificare il percorso di installazione in un percorso all'interno del profilo dell'utente. Idealmente, modificare il percorso in un punto qualsiasi nei dati dell'applicazione non mobili (ad esempio, una sottodirectory di CSIDL \_ LOCAL \_ APPDATA).

## <a name="example-of-simplified-installation"></a>Esempio di installazione semplificata

Nella figura 2 è riportato un esempio di processo migliorato per l'installazione di un gioco in Windows, con finestre di dialogo di installazione semplificate.

**Figura 2. Processo di installazione semplificato**

![Installazione](images/simplifiedgameinstall.png)

Di seguito sono riportati alcuni punti importanti:

-   Il programma di installazione viene avviato automaticamente all'inserimento del disco di installazione (esecuzione automatica).
-   La schermata iniziale, con le opzioni per installare, rimuovere, visualizzare il sito Web o uscire, non viene visualizzata se il gioco non è ancora installato nel computer.
-   La **finestra di** dialogo Installazione è la prima finestra di dialogo visualizzata dal programma di installazione.
-   Il **pulsante** Installa è l'implementazione della modalità di installazione automatica.
-   Il **pulsante** Opzioni è l'implementazione della modalità di installazione personalizzata.
-   Il **pulsante Annulla** chiuderà immediatamente il programma di installazione. Poiché l'avvio del programma di installazione è un'azione semplice per l'utente, non richiedere conferma.
-   Dopo che l'utente ha accettato il contratto di licenza e ha immesso un codice Product Key valido, viene avviata l'installazione.
-   Al termine del processo di installazione, il gioco verrà avviato automaticamente o verrà visualizzata una finestra  di dialogo che avvisa l'utente che l'installazione è stata completata e offre opzioni aggiuntive, a seconda che sia stata selezionata l'opzione Esegui gioco dopo l'installazione.
-   La **casella di controllo** Esegui gioco offre un'altra possibilità di avviare il gioco, per praticità. Questa opzione è sempre deselezionata per  impostazione predefinita, perché la finestra di dialogo Installazione completata può essere visualizzata solo se l'opzione Esegui **gioco** dopo l'installazione è stata deselezionata nella finestra di dialogo **Opzioni di** installazione.
-   Il **pulsante OK** chiude la finestra di dialogo, eventualmente attivando le caselle di controllo **Esegui** e Visualizza **file** Leggimi.

## <a name="summary"></a>Riepilogo

I giocatori vogliono fare un gioco il prima possibile. L'ultima cosa che un giocatore vuole fare è wading attraverso i dialoghe ed effettuare scelte che sono le stesse di tutti gli altri giochi che ha installato. L'implementazione di queste idee può ridurre la quantità di tempo che un giocatore dedica all'installazione di un gioco in Windows e contribuire a migliorare la qualità complessiva dell'esperienza Windows di gioco.

 

 