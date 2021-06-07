---
title: Prima esperienza
description: Nella prima esperienza ideale, gli utenti installano il programma e lo usano immediatamente in modo produttivo, senza rispondere a una serie di domande o apprendere una serie di cose.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 04610b75e8ca4ea7602d00b840bbbd9002397d9e
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524455"
---
# <a name="first-experience"></a>Prima esperienza

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Nella prima esperienza ideale, gli utenti installano il programma e lo usano immediatamente in modo produttivo, senza rispondere a una serie di domande o apprendere una serie di cose.

Una prima esperienza utente consente agli utenti di passare dalla prima esposizione a un nuovo programma o funzionalità all'uso quotidiano.

Per i programmi Windows, la prima esperienza iniziale si verifica quando gli utenti eseguono il programma di installazione. Programmi di installazione in genere:

-   Richiedere all'utente di accettare un contratto di licenza con l'utente finale (EULA).
-   Richiedere un codice Product Key.
-   Presenta le opzioni necessarie relative alla configurazione, inclusa l'installazione di software facoltativo.
-   Copiare il software sul disco rigido dell'utente.
-   Presentare le opzioni del programma che si applicano a tutti gli utenti.

![Screenshot della finestra di dialogo "Digitare il codice Product Key" ](images/exper-first-exper-image1.png)

Parte di una tipica esperienza di installazione di Windows.

La prima esperienza continua quindi con il primo uso del programma o della funzionalità. Questa esperienza di primo utilizzo può:

-   Presenta le opzioni del programma che si applicano solo all'utente corrente.
-   Offrire esercitazioni su prodotti o funzionalità.

![Screenshot della finestra di dialogo "centro di benvenuto" ](images/exper-first-exper-image2.png)

La prima esperienza d'uso.

**Nota:** Le linee guida relative [alle opzioni del](win-property-win.md) programma sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, considerare le domande seguenti.

### <a name="setup-experience"></a>Esperienza di installazione

Si applicano le condizioni seguenti?

-   Per usare il programma sono necessarie le impostazioni corrette e si applicano a tutti gli utenti.
-   Le impostazioni personalizzano un'esperienza di base o un'esperienza fondamentale per l'identificazione personale dell'utente con il programma.
-   Non esiste un'impostazione predefinita sicura, è probabile che l'utente sceva le impostazioni che non sono predefinite o che le impostazioni predefinite richiedano il consenso dell'utente.
-   È improbabile che l'utente cambi le impostazioni dopo l'installazione.
-   La modifica delle impostazioni richiede l'elevazione dei privilegi.

In tal caso, è consigliabile presentare le impostazioni durante l'esperienza di installazione.

### <a name="first-use-experience"></a>Esperienza di primo utilizzo

Si applicano le condizioni seguenti?

-   Le impostazioni o le attività corrette sono necessarie per usare il programma o la funzionalità e si applicano ai singoli utenti.
-   Le impostazioni personalizzano un'esperienza di base o un'esperienza fondamentale per l'identificazione personale dell'utente con il programma.
-   Non esiste un'impostazione predefinita sicura, è probabile che l'utente sceva le impostazioni che non sono predefinite o che le impostazioni predefinite richiedano il consenso dell'utente.
-   È probabile che gli utenti eseeranno scelte migliori nel contesto del programma rispetto all'installazione.
-   È improbabile che l'utente cambi le impostazioni usando Opzioni.

In tal caso, è consigliabile presentare le attività e le impostazioni durante la prima esperienza d'uso del programma o della funzionalità.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Nella prima esperienza ideale, gli utenti installano il programma (o anche solo avviarlo se non richiede l'installazione) e lo usano in modo produttivo immediatamente senza rispondere a una serie di domande o apprendere una serie di cose.

Questo ideale è ottenibile per la maggior parte dei programmi, quindi è consigliabile cercare questa esperienza ideale ogni volta che è possibile. Tuttavia, questo obiettivo spesso non è ottenibile per i programmi che richiedono un'integrazione significativa del sistema, hanno molte funzionalità facoltative o hanno implicazioni sulla privacy. Ad esempio, se il programma dispone di funzionalità che potrebbero rivelare informazioni personali a parti non attendibili, i tenet di [trustworthy computing](https://www.microsoft.com/mscorp/twc/default.mspx) richiedono di ottenere il consenso dell'utente prima di abilitare queste funzionalità.

### <a name="questions-arent-choices"></a>Le domande non sono scelte

Le domande richiedono risposte a cui devono rispondere prima che gli utenti possano procedere. Le domande durante la prima esperienza sono ostacoli che gli utenti devono saltare prima di poter usare il programma in modo produttivo. Al contrario, le scelte sono facoltative. Gli utenti non devono rispondere o possono scegliere di vederli solo quando vogliono.

Di conseguenza, le impostazioni presentate nel flusso principale di una configurazione guidata sono domande, mentre le impostazioni all'esterno del flusso di installazione principale o in una finestra di dialogo delle opzioni del programma sono scelte. Le domande non necessarie rendono la prima esperienza del programma complicata e lunga, eliminando in modo efficace l'aspettativa positiva e gli utenti che si preoccupano di iniziare a usare il programma.

### <a name="use-the-first-experience-when-you-must"></a>Usare la prima esperienza quando è necessario

Presentare le impostazioni e le attività agli utenti durante le prime esperienze quando è necessario, ma in genere esistono alternative migliori:



| Prima esperienza  | Alternativi       |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Domande sulla configurazione<br/>                  | Selezionare le impostazioni predefinite appropriate.<br/> Consente agli utenti di modificare le opzioni del programma.<br/> Specificare percorsi di installazione tipici e personalizzati. <br/> |
| Domande sul primo utilizzo<br/>              | Selezionare le impostazioni predefinite appropriate e consentire agli utenti di modificare le opzioni del programma.<br/>                                                            |
| Attività da usare per la prima volta<br/>                  | Presentare invece contestualmente.<br/>                                                                                                           |
| Primo uso degli annunci di funzionalità<br/> | Rendere individuabili e contestuali le attività più comuni e importanti.<br/>                                                                   |
| Esercitazioni per il primo uso<br/>              | Rendere le funzionalità del programma di auto-esplicativo.<br/>                                                                                                 |
| Registrazione del prodotto<br/>             | Specificare il comando nel menu Guida e nella casella Informazioni su.<br/>                                                                                             |



 

**Se si fa una sola cosa...**

Mantenere la prima esperienza il più semplice possibile. Iniziare subito a lavorare con il programma. Scegliere impostazioni predefinite sicure, sicure e pratiche e porre domande durante la configurazione e usarle per la prima volta solo quando è necessario.

Si ha una sola possibilità di fare una buona prima impressione e la prima impressione è durevole.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Limitare le prime esperienze alle attività e alle impostazioni necessarie per usare un programma o una funzionalità e includete solo quando non esiste un'alternativa migliore.** Per le alternative, vedere la tabella precedente.
    -   **Eccezione:** Aggiungere impostazioni di personalizzazione o personalizzazione del programma alla prima esperienza se la personalizzazione fa parte dell'esperienza di base o è fondamentale per l'identificazione personale dell'utente con il programma.

![Screenshot della finestra di dialogo "Digitare un nome computer" ](images/exper-first-exper-image3.png)

Windows chiede agli utenti il nome del computer e la scelta dello sfondo durante l'installazione perché queste impostazioni consentono di creare una connessione emotivo al prodotto.

-   **Usare l'esperienza di configurazione per** le attività e le impostazioni se si applicano a tutti gli utenti o se la modifica delle impostazioni richiede l'elevazione dei privilegi.
-   **Usare la prima esperienza d'uso** per le attività e le impostazioni se si applicano ai singoli utenti.

### <a name="presentation"></a>Presentazione

-   **Preferire le attività e le impostazioni facoltative alle attività e alle impostazioni necessarie.** Evitare di forzare gli utenti a configurare il programma.

    ![Screenshot della finestra di dialogo "Trovato nuovo hardware" ](images/exper-first-exper-image4.png)

    La finestra di dialogo Trovato nuovo hardware rende facoltativa l'installazione del software driver anziché renderlo un'attività obbligatoria.

-   **Prendere le attività e le impostazioni facoltative dal flusso di attività principale ogni volta che è possibile.** Ad esempio, molti programmi di installazione forniscono un percorso di installazione personalizzato per rimuovere le impostazioni modificate raramente dal flusso di attività principale.

    ![Screenshot dei pulsanti di opzione completi e personalizzati ](images/exper-first-exper-image5.png)

    Esperienza di installazione che facilita il flusso di attività principale se l'utente non intende personalizzare l'installazione.

-   **Non sovraccaricare gli utenti con attività e impostazioni:**
    -   **Iniziare con operazioni semplici.** Iniziare con semplici impostazioni di personalizzazione e avanzamento verso attività e impostazioni tecniche più complesse. Ad esempio, il programma di installazione di Windows inizia con le informazioni personali e termina con la configurazione di rete.
    -   **Usare una prima esperienza contestuale** per le attività e le impostazioni se si applicano solo a funzionalità che non sono fondamentali per il programma principale.

        ![Screenshot della finestra di dialogo "Installazione audio e video" ](images/exper-first-exper-image6.png)

        Windows Live Messenger ha una configurazione contestuale per audio e video perché vengono usati dalle funzionalità secondarie.

-   **Non presentare tutti gli elementi contemporaneamente.** Consolidare per usare una singola interfaccia utente invece di più superfici dell'interfaccia utente o visualizzare le attività in momenti diversi anziché contemporaneamente.

    **Non corretto:**

    ![Screenshot di cinque finestre di dialogo sovrapposte ](images/exper-first-exper-image7.png)

    In questo esempio, la prima esperienza d'uso è travolgente.

-   **Esprimere domande e opzioni in termini di obiettivi e attività degli utenti, non in termini di tecnologia.** Fornire opzioni che gli utenti comprendono e differenziano chiaramente. Assicurarsi di fornire informazioni sufficienti per consentire agli utenti di prendere decisioni informate.
-   **Se la necessità di informazioni personali non è ovvia, spiegare perché il programma necessita delle informazioni e come verranno usate.**

    ![Screenshot del testo che indica l'uso dell'indirizzo di posta elettronica ](images/exper-first-exper-image8.png)

    In questo esempio, un'applicazione di e-commerce spiega come verranno usate le informazioni personali.

-   **Presentare le prime esperienze a schermo intero solo se gli utenti non possono eseguire in modo produttivo altre attività.** Ad esempio, l'installazione di Windows viene visualizzata a schermo intero per non consentire agli utenti di eseguire altre attività durante l'installazione di Windows. La maggior parte delle prime esperienze non deve essere a schermo intero.

### <a name="settings"></a>Impostazioni

-   **Per tutte le impostazioni, selezionare il valore più sicuro (per evitare la perdita di dati o di accesso al sistema), il valore più sicuro e privato per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare il valore più probabile o conveniente. La scelta di valori predefiniti efficaci è un modo efficace per semplificare la prima esperienza.
-   **Richiedere agli utenti di acconsentire esplicitamente:**

    -   Impostazioni con implicazioni legali, ad esempio i contratti di licenza con l'utente finale. Tali impostazioni non possono avere selezioni predefinite.
    -   Funzionalità che eseguono modifiche automatiche alla configurazione del sistema, ad esempio gli aggiornamenti automatici di Windows.
    -   Funzionalità che rivelano informazioni personali (PII) o informazioni di sistema.
    -   Modifiche al desktop dell'utente oltre all'aggiunta di voci al menu Start, ad esempio l'aggiunta di icone al desktop o alla barra di avvio veloce.
    -   Software facoltativo, ad esempio miglioramenti del prodotto, sottoscrizioni e prodotti di terze parti.

    ![Screenshot della finestra di dialogo Scegliere le funzionalità desiderate ](images/exper-first-exper-image9.png)

    In questo esempio, gli utenti acconsentino esplicitamente a miglioramenti del prodotto, sottoscrizioni e prodotti di terze parti.

-   **Se un'impostazione è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** Per i pulsanti di opzione e le caselle di controllo, assicurarsi di aggiungere all'etichetta del controllo, non alle note supplementari.
-   **Se un'impostazione è destinata solo agli utenti esperti, aggiungere "(advanced)" all'etichetta.** Per i pulsanti di opzione e le caselle di controllo, assicurarsi di aggiungere all'etichetta del controllo, non alle note supplementari.

### <a name="tasks"></a>Attività

-   **Aiutare gli utenti a passare il tempo di attesa in modo produttivo.**
    -   Se il tempo di attesa è in genere compreso tra uno e due minuti, è consigliabile fornire informazioni utili durante l'attesa degli utenti, ad esempio una presentazione delle novità durante l'installazione.
    -   Se il tempo di attesa è in genere superiore a due minuti, semplificare l'esecuzione di altre attività da parte degli utenti. Visualizzare il tempo di attesa stimato, consigliare agli utenti di eseguire altre operazioni nel frattempo e rendere ovvio il completamento dell'attività modificando significativamente lo schermo.
-   **Riconsiderare la presentazione delle esercitazioni durante la prima esperienza.** Molto probabilmente gli utenti vogliono usare subito il programma e sono interessati alle esercitazioni in un secondo momento.
-   **Non usare le notifiche degli annunci di funzionalità nella prima esperienza.** Invece di usare una notifica annuncio di [funzionalità,](mess-notif.md)progettare la funzionalità in modo che sia più facile da individuare nei contesti in cui è necessaria oppure non eseguire operazioni speciali e consentire agli utenti di individuare la funzionalità in modo personalizzato.
-   **Non usare notifiche durante l'esperienza iniziale di Windows.** Per migliorare la prima esperienza, Windows 7 elimina tutte le notifiche visualizzate durante le prime ore di utilizzo. Progettare il programma presupponendo che gli utenti non vedano tali notifiche.

 

