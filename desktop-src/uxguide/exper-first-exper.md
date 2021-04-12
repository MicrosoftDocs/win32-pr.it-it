---
title: Prima esperienza
description: Nella prima esperienza ideale, gli utenti installano il programma e lo usano immediatamente in modo produttivo, senza rispondere a una serie di domande o imparare un po' di cose.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c965ae77507b0041d17cabb34c4f53dc8216c134
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234452"
---
# <a name="first-experience"></a>Prima esperienza

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Nella prima esperienza ideale, gli utenti installano il programma e lo usano immediatamente in modo produttivo, senza rispondere a una serie di domande o imparare un po' di cose.

Un'interfaccia utente per la prima esperienza consente agli utenti di passare dalla prima esposizione a un nuovo programma o funzionalità all'utilizzo giornaliero.

Per i programmi Windows, la prima esperienza iniziale si verifica quando gli utenti eseguono il programma di installazione. Programmi di installazione in genere:

-   Richiedere all'utente di accettare un contratto di licenza con l'utente finale (EULA).
-   Richiedere un codice Product Key.
-   Presentare le opzioni relative alla configurazione necessarie, inclusa l'installazione del software facoltativo.
-   Copiare il software nel disco rigido dell'utente.
-   Presentare le opzioni di programma applicabili a tutti gli utenti.

![screenshot della finestra di dialogo "digitare il codice" Product Key " ](images/exper-first-exper-image1.png)

Parte di un'esperienza di installazione tipica di Windows.

La prima esperienza continua quindi al primo utilizzo del programma o della funzionalità. Questa prima esperienza di utilizzo può:

-   Presentare le opzioni di programma che si applicano solo all'utente corrente.
-   Offrire esercitazioni sui prodotti o sulle funzionalità.

![screenshot della finestra di dialogo ' Welcome Center ' ](images/exper-first-exper-image2.png)

La prima esperienza di utilizzo.

**Nota:** Le linee guida relative alle [Opzioni di programma](win-property-win.md) sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendere in considerazione le domande seguenti.

### <a name="setup-experience"></a>Esperienza di installazione

Si applicano le condizioni seguenti?

-   Le impostazioni corrette sono necessarie per usare il programma e si applicano a tutti gli utenti.
-   Le impostazioni consentono di personalizzare un'esperienza di base o una chiave cruciale per l'identificazione personale dell'utente con il programma.
-   Non esiste alcun valore predefinito sicuro. è probabile che l'utente scelga impostazioni che non sono predefinite oppure che le impostazioni predefinite richiedano il consenso dell'utente.
-   È improbabile che l'utente modifichi le impostazioni dopo l'installazione.
-   Per modificare le impostazioni è necessaria l'elevazione.

In tal caso, provare a presentare le impostazioni durante l'installazione.

### <a name="first-use-experience"></a>Prima esperienza di utilizzo

Si applicano le condizioni seguenti?

-   Le impostazioni o le attività corrette sono necessarie per usare il programma o la funzionalità e si applicano a singoli utenti.
-   Le impostazioni consentono di personalizzare un'esperienza di base o una chiave cruciale per l'identificazione personale dell'utente con il programma.
-   Non esiste alcun valore predefinito sicuro. è probabile che l'utente scelga impostazioni che non sono predefinite oppure che le impostazioni predefinite richiedano il consenso dell'utente.
-   È probabile che gli utenti effettuino scelte migliori all'interno del contesto del programma rispetto all'installazione.
-   È improbabile che l'utente modifichi le impostazioni utilizzando le opzioni.

In tal caso, provare a presentare le attività e le impostazioni durante la prima esperienza di utilizzo del programma o della funzionalità.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Nella prima esperienza ideale, gli utenti installano il programma (o addirittura si avviano solo se non richiede l'installazione) e lo usano immediatamente in modo produttivo senza rispondere a una serie di domande o imparare una serie di cose.

Questo ideale è ottenibile per la maggior parte dei programmi, quindi è consigliabile cercare questa esperienza ideale ogni volta che è possibile. Tuttavia, questo obiettivo non è spesso ottenibile per i programmi che richiedono un'integrazione significativa del sistema, presentano molte funzionalità facoltative o hanno implicazioni sulla privacy. Se, ad esempio, il programma dispone di funzionalità che potrebbero rivelare informazioni personali a entità non attendibili, i principi di [Trustworthy Computing](https://www.microsoft.com/mscorp/twc/default.mspx) richiedono l'ottenimento del consenso dell'utente prima di abilitare queste funzionalità.

### <a name="questions-arent-choices"></a>Le domande non sono scelte

Le domande richiedono risposte a cui è necessario rispondere prima che gli utenti possano procedere. Le domande durante la prima esperienza sono ostacoli per cui gli utenti devono passare prima di poter utilizzare il programma in modo produttivo. Al contrario, le scelte sono facoltative. Gli utenti non devono rispondere ad essi o possono scegliere di visualizzarli solo quando vogliono.

Pertanto, le impostazioni presentate nel flusso principale di un'installazione guidata sono domande, mentre le impostazioni esterne al flusso di installazione principale o nella finestra di dialogo Opzioni programma sono scelte. Le domande non necessarie rendono la prima esperienza del programma complessa e a lungo termine, eliminando in modo efficace gli utenti che prevedono di iniziare a usare il programma.

### <a name="use-the-first-experience-when-you-must"></a>Usare la prima esperienza quando è necessario

Presentare le impostazioni e le attività agli utenti durante le prime esperienze quando è necessario, ma in genere sono disponibili alternative migliori:



|                                             |                                                                                                                                                    |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Prima esperienza**<br/>             | **Alternativi**<br/>                                                                                                                        |
| Domande sull'installazione<br/>                  | Selezionare le impostazioni predefinite appropriate.<br/> Consente agli utenti di modificare le opzioni del programma.<br/> Fornire percorsi di installazione tipici e personalizzati. <br/> |
| Prime domande sull'uso<br/>              | Selezionare le impostazioni predefinite appropriate e consentire agli utenti di modificare le opzioni del programma.<br/>                                                            |
| Primo utilizzo delle attività<br/>                  | Presentare invece il contesto.<br/>                                                                                                           |
| Primo uso degli annunci di funzionalità<br/> | Rendere le attività più comuni e importanti individuabili e contestuali.<br/>                                                                   |
| Prime esercitazioni sull'utilizzo<br/>              | Rendere le funzionalità del programma intuitive.<br/>                                                                                                 |
| Registrazione prodotto<br/>             | Specificare il comando nel menu della guida e la casella informazioni su.<br/>                                                                                             |



 

**Se si esegue una sola operazione...**

Mantieni la tua prima esperienza il più semplice possibile. Per iniziare subito a lavorare il programma. Scegliere impostazioni predefinite sicure, sicure e convenienti e porre domande durante l'installazione e usarle solo quando è necessario.

Si ha solo una possibilità di creare una buona prima impressione e la prima impressione è duratura.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Limitare le prime esperienze alle attività e alle impostazioni necessarie per usare un programma o una funzionalità e includerle solo quando non esiste un'alternativa migliore.** Vedere la tabella precedente per le alternative.
    -   **Eccezione:** Aggiungere le impostazioni di personalizzazione o personalizzazione del programma alla prima esperienza se la loro personalizzazione fa parte dell'esperienza di base o cruciale per l'identificazione personale dell'utente con il programma.

![screenshot della finestra di dialogo ' tipo nome computer ' ](images/exper-first-exper-image3.png)

Windows chiede agli utenti il nome del computer e la scelta dello sfondo durante l'installazione, perché queste impostazioni consentono di creare una connessione emotiva al prodotto.

-   **Usare l'esperienza di installazione** per le attività e le impostazioni se si applicano a tutti gli utenti o la modifica delle impostazioni richiede l'elevazione.
-   **Usare la prima esperienza di utilizzo** per le attività e le impostazioni se si applicano a singoli utenti.

### <a name="presentation"></a>Presentazione

-   **Preferisce le impostazioni e le attività facoltative per le attività e le impostazioni richieste.** Evitare di forzare gli utenti a configurare il programma.

    ![screenshot della finestra di dialogo ' trovato nuovo hardware ' ](images/exper-first-exper-image4.png)

    La finestra di dialogo trovato nuovo hardware rende facoltativa l'installazione del software driver anziché l'esecuzione di un'attività obbligatoria.

-   **Eseguire le attività e le impostazioni facoltative dal flusso di attività principale ogni volta che è pratica.** Molti programmi di installazione, ad esempio, forniscono un percorso di installazione personalizzato per rimuovere le impostazioni modificate raramente dal flusso dell'attività principale.

    ![screenshot dei pulsanti di opzione completi e personalizzati ](images/exper-first-exper-image5.png)

    Un'esperienza di installazione che facilita il flusso dell'attività principale se l'utente non intende personalizzare l'installazione.

-   **Non sovraccaricare gli utenti con attività e impostazioni:**
    -   **Iniziare con operazioni semplici.** Inizia con le impostazioni di personalizzazione semplici e lo stato di avanzamento verso attività e impostazioni tecniche più complesse. Ad esempio, l'installazione di Windows inizia con informazioni personali e termina con la configurazione di rete.
    -   **Usare una prima esperienza contestuale** per le attività e le impostazioni se si applicano solo alle funzionalità che non sono fondamentali per il programma principale.

        ![screenshot della finestra di dialogo "installazione audio e video" ](images/exper-first-exper-image6.png)

        Windows Live Messenger include una configurazione contestuale per audio e video perché vengono usati dalle funzionalità secondarie.

-   **Non presentare tutti gli elementi contemporaneamente.** Consolidare per utilizzare una singola interfaccia utente anziché più superfici dell'interfaccia utente o visualizzare attività in momenti diversi anziché in una sola volta.

    **Non corretto:**

    ![Screenshot di cinque finestre di dialogo sovrapposte ](images/exper-first-exper-image7.png)

    In questo esempio, la prima esperienza di utilizzo è sovraccarica.

-   **Esprimere domande e opzioni in termini di obiettivi e attività degli utenti, non in termini di tecnologia.** Fornire le opzioni che gli utenti possono comprendere e distinguere chiaramente. Assicurarsi di fornire informazioni sufficienti per consentire agli utenti di prendere decisioni informate.
-   **Se la necessità di informazioni personali non è ovvia, spiegare il motivo per cui il programma richiede le informazioni e il modo in cui verrà usato.**

    ![screenshot del testo che indica l'utilizzo dell'indirizzo di posta elettronica ](images/exper-first-exper-image8.png)

    In questo esempio, un'applicazione di e-commerce spiega come verranno usate le informazioni personali.

-   **Presentare le prime esperienze a schermo intero solo se gli utenti non possono eseguire in modo produttivo altre attività.** Il programma di installazione di Windows viene ad esempio visualizzato a schermo intero per impedire agli utenti di eseguire altre attività durante l'installazione di Windows. La prima esperienza non dovrebbe essere a schermo intero.

### <a name="settings"></a>Impostazioni

-   **Per tutte le impostazioni, selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema), per impostazione predefinita il valore più sicuro e privato.** Se la sicurezza e la sicurezza non sono fattori, selezionare il valore più probabile o pratico. La scelta di valide impostazioni predefinite è un modo efficace per semplificare la prima esperienza.
-   **Richiedi agli utenti di acconsentire esplicitamente per:**

    -   Impostazioni con implicazioni legali, ad esempio i contratti di licenza con l'utente finale (EULA). Tali impostazioni non possono avere selezioni predefinite.
    -   Funzionalità che eseguono modifiche automatiche alla configurazione del sistema, ad esempio gli aggiornamenti automatici di Windows.
    -   Funzionalità che rivelano informazioni personali o informazioni di sistema.
    -   Modifiche al desktop dell'utente oltre l'aggiunta di voci al menu Start, ad esempio l'aggiunta di icone al desktop o alla barra di avvio veloce.
    -   Software facoltativo, ad esempio miglioramenti del prodotto, sottoscrizioni e prodotti di terze parti.

    ![screenshot della finestra di dialogo Scegli le funzionalità desiderate ](images/exper-first-exper-image9.png)

    In questo esempio, gli utenti scelgono i miglioramenti del prodotto, le sottoscrizioni e i prodotti di terze parti.

-   **Se un'impostazione è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** Per i pulsanti di opzione e le caselle di controllo, assicurarsi di aggiungere all'etichetta del controllo, non le note supplementari.
-   **Se un'impostazione è destinata solo agli utenti avanzati, aggiungere "(Advanced)" all'etichetta.** Per i pulsanti di opzione e le caselle di controllo, assicurarsi di aggiungere all'etichetta del controllo, non le note supplementari.

### <a name="tasks"></a>Attività

-   **Consentire agli utenti di passare il tempo di attesa in modo produttivo.**
    -   Se il tempo di attesa è in genere compreso tra uno e due minuti, è consigliabile fornire informazioni utili mentre gli utenti sono in attesa, ad esempio una presentazione delle novità durante l'installazione.
    -   Se il tempo di attesa è in genere superiore a due minuti, consentire agli utenti di eseguire altre attività in modo semplice. Visualizzare il tempo di attesa stimato, consigliare agli utenti di eseguire un'altra operazione nel frattempo e rendere ovvio il completamento delle attività cambiando notevolmente la schermata.
-   **Riprendere in considerazione le esercitazioni durante la prima esperienza.** È probabile che gli utenti usino il programma immediatamente e siano interessati a esercitazioni in un secondo momento.
-   **Non usare le notifiche degli annunci di funzionalità nella prima esperienza.** Invece di usare una [notifica degli annunci di funzionalità](mess-notif.md), progettare la funzionalità per semplificare l'individuazione nei contesti in cui è necessario o non eseguire alcuna operazione speciale e consentire agli utenti di individuare la funzionalità autonomamente.
-   **Non usare notifiche durante l'esperienza iniziale di Windows.** Per migliorare la prima esperienza, Windows 7 disattiva tutte le notifiche visualizzate durante le prime ore di utilizzo. Progettare il programma presumendo che gli utenti non visualizzino tali notifiche.

 

