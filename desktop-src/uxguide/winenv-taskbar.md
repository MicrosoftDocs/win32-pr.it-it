---
title: Barra delle applicazioni
description: La barra delle applicazioni è il punto di accesso per i programmi visualizzati sul desktop. Con le nuove funzionalità della barra delle applicazioni di Windows 7, gli utenti possono assegnare comandi, accedere alle risorse e visualizzare lo stato del programma direttamente dalla barra delle applicazioni.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f8b2bc21a75bc11c43df2cbdd37381165b89a793
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560764"
---
# <a name="taskbar"></a>Barra delle applicazioni

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

La barra delle applicazioni è il punto di accesso per i programmi visualizzati sul desktop. Con le nuove funzionalità della barra delle applicazioni di Windows 7, gli utenti possono assegnare comandi, accedere alle risorse e visualizzare lo stato del programma direttamente dalla barra delle applicazioni.

La barra delle applicazioni è il punto di accesso per i programmi visualizzati sul desktop, anche se il programma è ridotto a icona. Tali programmi si affermano che hanno una presenza sul desktop. Con la barra delle applicazioni, gli utenti possono visualizzare le finestre primarie aperte e alcune finestre secondarie sul desktop e possono passare rapidamente da una all'altra.

![screenshot della barra delle applicazioni con le funzionalità richiamate ](images/winenv-taskbar-image1.png)

Barra delle applicazioni di Microsoft Windows.

I controlli sulla barra delle applicazioni sono detti pulsanti della barra delle applicazioni. Quando un programma crea una finestra primaria (o una finestra secondaria con determinate caratteristiche), Windows aggiunge un pulsante della barra delle applicazioni per la finestra e lo rimuove quando si chiude la finestra.

I programmi progettati per Windows 7 possono sfruttare le nuove funzionalità dei pulsanti della barra delle applicazioni:

-   Le Jump List consentono di accedere rapidamente alle destinazioni usate di frequente (ad esempio file, cartelle e collegamenti) e ai comandi tramite un menu di scelta rapida accessibile dal pulsante della barra delle applicazioni del programma e dalla voce del menu Start anche se il programma non è attualmente in esecuzione.
-   Le barre degli strumenti dell'anteprima consentono di accedere rapidamente ai comandi utilizzati di frequente per una particolare finestra. Le barre degli strumenti dell'anteprima vengono visualizzate nell'anteprima del pulsante della barra delle applicazioni.
-   Le icone sovrapposte mostrano la modifica dello stato nell'icona del pulsante della barra delle applicazioni del programma.
-   Gli indicatori di stato mostrano lo stato delle attività a esecuzione prolungata sul pulsante della barra delle applicazioni del programma.
-   I pulsanti della barra delle applicazioni della finestra secondaria consentono agli utenti di usare le anteprime del pulsante della barra delle applicazioni per passare direttamente a schede di finestra, finestre di progetto, finestre figlio MDI (Multiple Document Interface) e finestre secondarie.
-   I pulsanti della barra delle applicazioni bloccati consentono agli utenti di aggiungere pulsanti di programma alla barra delle applicazioni per fornire accesso rapido ai programmi anche quando non sono in esecuzione.

Tecnicamente, la barra delle applicazioni si estende sull'intera barra dal pulsante avvia all'area di notifica; in genere, tuttavia, la barra delle applicazioni si riferisce solo all'area che contiene i pulsanti della barra delle applicazioni. Per più configurazioni di monitoraggio, solo un monitor dispone di una barra delle applicazioni e tale monitoraggio è il monitoraggio predefinito.

**Nota:** Le linee guida relative al [Desktop](winenv-desktop.md), all' [area di notifica](winenv-notification.md)e alla [gestione delle finestre](win-window-mgt.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

I programmi progettati per Windows 7 possono sfruttare le funzionalità dei pulsanti della barra delle applicazioni. Porsi le domande principali seguenti per determinare se utilizzarle o meno:

**Jump List**

-   **Gli utenti devono spesso avviare nuove attività usando il programma?** In tal caso, è consigliabile fornire un Jump List. Sebbene le Jump List possano essere usate per altri scopi, la maggior parte degli scenari implica l'avvio di una nuova attività.
-   **È spesso necessario che gli utenti accedano a file, cartelle, collegamenti o altre risorse usate di recente o di frequente?** In tal caso, è consigliabile fornire un Jump List per accedere a queste risorse utili.

    ![screenshot della barra delle applicazioni con Internet Explorer Jump List ](images/winenv-taskbar-image2.png)

    In questo esempio, Windows Internet Explorer utilizza un Jump List per presentare le pagine visitate di frequente.

-   **Gli utenti spesso hanno bisogno di accesso rapido a un numero ridotto di comandi del programma durante l'uso di altri programmi, anche se il programma non è in esecuzione?** In tal caso, è consigliabile fornire un Jump List con questi comandi usati di frequente. Questi comandi devono funzionare anche se il programma non è in esecuzione e deve essere applicato all'intero programma, non a una finestra specifica. In alternativa, è consigliabile fornire una barra degli strumenti di anteprima per i comandi che si applicano a una finestra specifica.

    ![screenshot della barra delle applicazioni con la Jump List delle note permanenti ](images/winenv-taskbar-image3.png)

    In questo esempio, il Memo accessorio consente agli utenti di creare rapidamente una nuova nota quando si usano altri programmi.

-   **Si sta innalzando di livello le funzionalità nuove, monouso o difficili da trovare?** In tal caso, non utilizzare Jump List perché non sono destinati a questo scopo. Al contrario, migliorare l'individuabilità di tali comandi direttamente nel programma.

**Barre degli strumenti delle anteprime**

Si applicano tutte le condizioni seguenti?

-   **I comandi si applicano a una finestra specifica?** Le barre degli strumenti dell'anteprima sono per i comandi che si applicano alle attività esistenti, mentre i comandi di Jump List sono per l'avvio di nuove attività.
-   **Gli utenti devono interagire rapidamente con un'attività in esecuzione durante l'uso di altri programmi?** In tal caso, le barre degli strumenti dell'anteprima rappresentano una scelta ottimale. Le barre degli strumenti dell'anteprima possono presentare un massimo di sette comandi, ma in genere è preferibile un massimo di cinque comandi.
-   **I comandi sono immediati?** Ovvero non richiedono input aggiuntivo? Le barre degli strumenti delle anteprime devono avere comandi immediati per essere efficienti, mentre le Jump List funzionano meglio con i comandi che richiedono input aggiuntivo.

    **Non corretto:**

    ![screenshot della barra delle applicazioni con finestre sovrapposte ](images/winenv-taskbar-image4.png)

    I comandi che richiedono input aggiuntivo non funzionano correttamente nelle barre degli strumenti delle anteprime.

-   **I comandi sono diretti?** Ovvero, gli utenti possono interagire con loro usando un solo clic? Per le barre degli strumenti è necessario che i comandi diretti siano efficienti.
-   **I comandi sono ben rappresentati dalle icone?** I comandi della barra degli strumenti dell'anteprima vengono presentati usando icone non etichette di testo, mentre i comandi di Jump List sono rappresentati da etichette di testo.

    **Non corretto:**

    ![screenshot del comando anteprima con icona ](images/winenv-taskbar-image5.png)

    In questo esempio, il comando non è ben rappresentato dalle icone.

**Icone sovrapposte**

-   **Il programma ha "presenza sul desktop"?** In caso contrario, utilizzare un'icona dell'area di notifica. In tal caso, è consigliabile utilizzare un'icona di sovrapposizione anziché inserire lo stato nell'icona dell'area di notifica per i programmi progettati per Windows 7. In questo modo si garantisce che l'icona sarà sempre visibile (quando vengono usate icone grandi) e consoliderà il programma con il relativo stato in un'unica posizione.
-   **L'icona della sovrimpressione viene visualizzata temporaneamente per visualizzare una modifica dello stato?** In tal caso, è possibile che sia appropriata un'icona di sovrapposizione, a seconda dei fattori seguenti:
    -   **Lo stato è utile e pertinente durante l'uso di altri programmi?** In caso contrario, visualizzare le informazioni nelle barre di [stato](ctrl-status-bars.md) del programma o in un'altra area dello stato del programma.

        ![screenshot della barra di stato della finestra di Internet Explorer ](images/winenv-taskbar-image7.png)

        In questo esempio viene usata la barra di stato perché lo stato non è utile quando si usano altri programmi.

    -   **Lo stato indica lo stato di avanzamento?** In caso affermativo, usare invece un indicatore di stato del pulsante della barra delle applicazioni.
    -   **Lo stato è critico? È richiesta un'azione immediata?** In tal caso, visualizzare le informazioni in un modo che richiede attenzione e che non possono essere facilmente ignorate, ad esempio una finestra di [dialogo](win-dialog-box.md).

**Indicatori di stato**

-   **Il feedback sullo stato di avanzamento è utile e pertinente durante l'uso di altri programmi?** Ovvero, è probabile che gli utenti monitorino lo stato di avanzamento durante l'uso di altri programmi e modifichino il comportamento di conseguenza? Questo stato utile e pertinente viene in genere visualizzato utilizzando una finestra di dialogo di stato non modale o una pagina di avanzamento dedicata, ma non con un puntatore occupato, un indicatore di attività o un indicatore di stato su una barra di stato. Se lo stato non è utile quando si usano altri programmi, è sufficiente visualizzare il feedback sullo stato di avanzamento direttamente nel programma.

    **Corretto:**

    ![screenshot della finestra di dialogo Copia con indicatore di stato ](images/winenv-taskbar-image8.png)

    **Non corretto:**

    ![screenshot della barra di stato nel pulsante della barra delle applicazioni ](images/winenv-taskbar-image9.png)

    Nell'esempio errato, l'indicatore di stato del pulsante della barra delle applicazioni non è molto utile.

-   **L'attività è continua?** Se l'attività non viene mai completata, non è necessario visualizzarne lo stato di avanzamento. Esempi di attività continue sono le analisi antivirus non avviate dagli utenti e l'indicizzazione dei file.

    **Non corretto:**

    ![screenshot dell'icona di avanzamento di un'attività continua ](images/winenv-taskbar-image10.png)

    In questo esempio, un'attività continua non deve mostrare lo stato di avanzamento.

**Barra delle applicazioni della finestra secondaria**

-   **Il programma contiene schede, finestre di progetto, finestre figlio MDI o finestre secondarie a cui gli utenti dovrebbero spesso passare direttamente?** In tal caso, è possibile assegnare le anteprime dei pulsanti della barra delle applicazioni di Windows.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Utilizzo efficace delle barre degli strumenti Jump List e delle anteprime

Le barre degli strumenti Jump List e thumbnail consentono agli utenti di accedere alle risorse ed eseguire i comandi in modo più efficiente. Tuttavia, quando si progetta il modo in cui il programma supporta queste funzionalità, non è necessario migliorare l'efficienza per l'autorizzazione. Se gli utenti non sono in grado di prevedere con precisione quale funzionalità dispone del comando necessario o se devono verificare più posizioni, gli utenti diventeranno frustrati e smetteranno di usare queste funzionalità.

Le Jump List e le barre degli strumenti delle anteprime interagiscono in modo più efficace quando sono:

-   **Differenze evidenti.** Gli utenti sanno quando cercare una destinazione o un comando in una Jump List e quando esaminare una barra degli strumenti delle anteprime. Lo scopo è chiaro per ognuno, quindi gli utenti raramente confondeno il contenuto dei due. In genere, le Jump List vengono usate per avviare nuove attività, mentre le barre degli strumenti di anteprima vengono usate per interagire con le attività in esecuzione durante l'uso di altri programmi.
-   **Utile.** Le destinazioni e i comandi offerti sono quelli necessari agli utenti. Se gli utenti non hanno bisogno di qualcosa, non sono inclusi. Non usare il numero massimo di elementi se non sono necessari.
-   **Prevedibile.** Le destinazioni e i comandi offerti sono quelli che gli utenti si aspettano di trovare. Gli utenti devono raramente esaminare più di una posizione.
-   **Ben organizzata.** Gli utenti sono in grado di trovare rapidamente ciò che cercano. Usano etichette descrittive ma concise e icone appropriate per facilitare il riconoscimento.

Assicurati di eseguire ricerche utente per assicurarsi che tu abbia diritto. Se infine si scopre che non è possibile progettare elenchi Jump List e barre degli strumenti di anteprima che raggiungono questi obiettivi, è consigliabile fornire solo uno di essi. È preferibile disporre di un modo prevedibile per assegnare comandi rispetto a due confusione.

## <a name="guidelines"></a>Indicazioni

### <a name="taskbar-buttons"></a>Pulsanti della barra delle applicazioni

-   **Fare in modo che i tipi di finestra seguenti siano visualizzati sulla barra delle applicazioni (per Windows 7, usando un'anteprima pulsante della barra delle applicazioni):**
    -   Finestre primarie (incluse le finestre di dialogo senza proprietario)
    -   Finestre delle proprietà
    -   Finestre di dialogo di stato non modale
    -   Procedure guidate
-   **Per Windows 7, usare le anteprime dei pulsanti della barra delle applicazioni per raggruppare i tipi di finestra seguenti con il pulsante della barra delle applicazioni della finestra principale da cui è stato avviato** Ogni programma (in particolare, ogni programma percepito come programma separato) deve avere un solo pulsante della barra delle applicazioni.

    -   Finestre secondarie
    -   Schede area di lavoro
    -   Finestre di progetto
    -   finestre figlio MDI

    **Corretto:**

    ![Screenshot di Esplora risorse e indicatore di stato ](images/winenv-taskbar-image11.png)

    In questo esempio, una finestra secondaria viene raggruppata con il pulsante della barra delle applicazioni della finestra primaria.

    **Non corretto:**

    ![Screenshot di Esplora risorse e del pannello di controllo ](images/winenv-taskbar-image12.png)

    In questo esempio il pannello di controllo è raggruppato in modo errato con Esplora risorse. Gli utenti li percepiscono come programmi distinti.

    **Non corretto:**

    ![screenshot del programma, dell'indicatore di stato e di una barra delle applicazioni ](images/winenv-taskbar-image13.png)

    In questo esempio Windows Backup usa erroneamente due pulsanti della barra delle applicazioni per un singolo programma.

-   **Il ripristino di una finestra primaria deve anche ripristinare tutte le finestre secondarie,** anche se tali finestre secondarie dispongono di pulsanti della barra delle applicazioni. Quando si esegue il ripristino, posizionare le finestre secondarie nella parte superiore della finestra principale.
-   **Per Windows 7, i programmi che in genere dispongono di una presenza desktop possono visualizzare temporaneamente un pulsante della barra delle applicazioni per visualizzare lo stato.** Eseguire questa operazione solo se il programma viene normalmente visualizzato sul desktop e gli utenti interagiscono spesso con esso. Un programma che in genere viene eseguito senza presenza sul desktop deve invece usare l'icona dell'area di notifica, anche se potrebbe non essere sempre visibile.

    **Non corretto:**

    ![screenshot del pulsante della barra delle applicazioni di Windows Sync Center ](images/winenv-taskbar-image14.png)

    In questo esempio, Centro sincronizzazione Windows usa erroneamente un pulsante della barra delle applicazioni temporaneo per visualizzare lo stato. Deve invece usare l'icona dell'area di notifica.

### <a name="icons"></a>Icone

-   **Progettare l'icona del programma per un aspetto interessante sulla barra delle applicazioni.** Verificare che sia significativo e rispecchi la funzione e il marchio. È necessario distinguerlo, renderlo speciale e assicurarsi che venga eseguito correttamente in tutte le dimensioni delle icone. Dedicare il tempo necessario per ottenere il giusto. Seguire le [linee guida sulle icone di tipo Aero](vis-icons.md).
-   **Se il programma usa icone sovrapposte, progettare l'icona di base del programma per gestire correttamente le sovrapposizioni.** Le icone sovrapposte vengono visualizzate nell'angolo inferiore destro, quindi progettare l'icona in modo che l'area possa essere nascosta.

    ![screenshot delle icone e con sovrimpressione in basso a destra ](images/winenv-taskbar-image15.png)

    In questo esempio, l'icona del pulsante della barra delle applicazioni del programma non contiene informazioni importanti nell'area in basso a destra.

-   **Non usare sovrimpressioni nell'icona di base del programma,** indipendentemente dal fatto che il programma usi o meno le icone sovrapposte. L'uso di una sovrapposizione nell'icona di base creerà confusione perché gli utenti dovranno capire che non sta comunicando lo stato.

    **Non corretto:**

    ![screenshot dell'icona di base con sovrapposizione ](images/winenv-taskbar-image16.png)

    In questo esempio, l'icona di base del programma è simile alla visualizzazione dello stato.

Per le linee guida e gli esempi dell'icona generale, vedere [Icone](vis-icons.md).

### <a name="overlay-icons"></a>Icone sovrapposte

-   **Usare le icone sovrapposte per indicare solo lo stato utile e pertinente.** Si consideri la visualizzazione di un'icona sovrapposta come una potenziale interruzione del lavoro dell'utente, quindi la modifica dello stato deve essere sufficientemente importante da meritare una potenziale interruzione.

    **Non corretto:**

    ![Screenshot di tre icone sovrapposte ](images/winenv-taskbar-image17.png)

    In questi esempi, l'icona di sovrapposizione non è abbastanza importante per meritare una potenziale interruzione.

-   **Usare le icone sovrapposte per lo stato temporaneo.** Se visualizzate costantemente, le icone sovrapposte perdono il relativo valore, quindi lo stato normale del programma non dovrebbe visualizzare un'icona. Rimuovere l'icona della sovrimpressione quando l'icona:

    -   **Per un problema:** Rimuovere l'icona dopo che il problema è stato risolto.
    -   **Avvisa che un elemento è nuovo:** Rimuovere l'icona dopo che l'utente ha attivato il programma.

    **Eccezione:** Il programma può visualizzare costantemente un'icona di sovrapposizione se gli utenti devono sempre conoscerne lo stato.

    ![Screenshot di Live Messenger con icona overlay ](images/winenv-taskbar-image18.png)

    In questo esempio, Windows Live Messenger Visualizza sempre un'icona di sovrapposizione in modo che gli utenti possano sempre controllare la presenza segnalata.

-   **Non visualizzare un'icona per indicare che è stato risolto un problema.** In alternativa, è sufficiente rimuovere qualsiasi icona precedente che indichi un problema. Si supponga che gli utenti normalmente si aspettano che il programma venga eseguito senza problemi.
-   **Visualizzare icone sovrapposte o icone dell'area di notifica, ma mai entrambe.** Il programma può supportare entrambi i meccanismi per la compatibilità con le versioni precedenti, ma se il programma Visualizza lo stato usando le icone sovrapposte, non dovrebbe usare anche le icone dell'area di notifica per lo stato.

    **Non corretto:**

    ![screenshot della barra delle applicazioni con icona visualizzata due volte ](images/winenv-taskbar-image19.png)

    In questo esempio, l'icona nuova posta viene visualizzata in ridondanza.

-   **Non lampeggiare il pulsante della barra delle applicazioni per attirare l'attenzione su una modifica dello stato.** Questa operazione risulterebbe troppo distrazione. Consentire agli utenti di individuare le icone sovrapposte in modo autonomo.
-   **Preferisci le icone sovrapposte standard per indicare le modifiche dello stato o dello stato.** Usare le icone di sovrapposizione standard seguenti: 

    |                                                                                                   |                                  |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | **Sovrapposizione**<br/>                                                                            | **Status**<br/>            |
    | ![screenshot dell'icona di avviso piccola ](images/winenv-taskbar-image20.png)<br/>               | Avviso<br/>               |
    | ![screenshot dell'icona di errore piccolo ](images/winenv-taskbar-image21.png)<br/>                 | Errore<br/>                 |
    | ![screenshot della piccola icona disabilitata/disconnessa ](images/winenv-taskbar-image22.png)<br/> | Disabilitato/disconnesso<br/> |
    | ![screenshot dell'icona Small blocked/offline ](images/winenv-taskbar-image23.png)<br/>       | Bloccato/offline<br/>       |

    

     

-   **Per le icone di sovrapposizione personalizzate, scegliere una progettazione facilmente riconoscibile.** Usare icone pixel 16x16 di alta qualità, icone a colori completi. Preferisce le icone con strutture distinte su icone quadrate o rettangolari. Applicare anche le altre [linee guida sulle icone di tipo Aero](vis-icons.md) .
-   **Mantieni semplice la progettazione delle icone di sovrapposizione personalizzate.** Non provare a comunicare idee complesse, non note o astratte. Se non è possibile pensare a un'icona personalizzata adatta, usare invece un'icona standard di errore o di avviso quando appropriato. Queste icone possono essere usate in modo efficace per comunicare molti tipi di stato.
-   **Non modificare lo stato troppo spesso.** Le icone sovrapposte non devono essere rumorose, instabili o richiedere attenzione. L'occhio è sensibile alle modifiche apportate al campo periferico della visione, quindi le modifiche di stato devono essere minime.
    -   **Non modificare rapidamente l'icona.** Se lo stato sottostante sta cambiando rapidamente, fare in modo che l'icona rifletta lo stato di alto livello.

        **Non corretto:**

        ![screenshot dell'icona sovrapposta in due Stati ](images/winenv-taskbar-image24.png)

        In questo esempio, l'icona sovrapposta a modifica rapida richiede attenzione.

    -   **Non usare animazioni.** Questa operazione è troppo distrazione.
    -   **Non lampeggiare l'icona.** Questa operazione è troppo distrazione. Se per un evento è richiesta l'attenzione immediata, utilizzare invece una finestra di dialogo. Se l'evento altrimenti richiede attenzione, utilizzare una notifica.

### <a name="taskbar-button-flashing"></a>Pulsante della barra delle applicazioni lampeggiante

-   **Usare il pulsante della barra delle applicazioni lampeggiando sporadicamente per richiedere l'attenzione immediata dell'utente per continuare a eseguire un'attività in corso.** È difficile per gli utenti concentrarsi mentre un pulsante della barra delle applicazioni lampeggia, quindi si supponga che interrompano le operazioni che fanno per arrestarlo. Quando si lampeggia un pulsante della barra delle applicazioni, è preferibile non rubare lo stato attivo per l'input, i pulsanti della barra delle applicazioni sono Verificare che l'interruzione sia giustificata, ad esempio per indicare che l'utente deve salvare i dati prima di chiudere una finestra. I programmi inattivi dovrebbero raramente richiedere un'azione immediata. Non lampeggiare il pulsante della barra delle applicazioni se l'unica operazione che l'utente deve eseguire è attivare il programma, leggere un messaggio o visualizzare una modifica dello stato.
-   **Se l'azione immediata non è obbligatoria, prendere in considerazione le alternative seguenti:**
    -   Utilizzare una [notifica](mess-notif.md) di operazione riuscita per indicare che un'attività è stata completata.
    -   Non eseguire alcuna operazione. È sufficiente attendere che gli utenti partecipino al problema alla successiva attivazione del programma. Questa è spesso la scelta migliore.
-   **Se un programma inattivo richiede attenzione immediata, lampeggiare il pulsante della barra delle applicazioni per attirare l'attenzione e lasciarlo evidenziato.** Non eseguire altre operazioni: non ripristinare o attivare la finestra e non riprodurre effetti acustici. Al contrario, rispettare la selezione dello stato della finestra dell'utente e consentire all'utente di attivare la finestra quando è pronta.
-   **Per le finestre secondarie che dispongono di un pulsante della barra delle applicazioni, lampeggiare il pulsante anziché il pulsante della barra delle applicazioni della finestra primaria.** Questa operazione consente agli utenti di partecipare direttamente alla finestra.
-   **Per le finestre secondarie che non dispongono di un pulsante della barra delle applicazioni, fare lampeggiare il pulsante della barra delle applicazioni della finestra primaria e portare la finestra secondaria sopra tutte le altre finestre per il programma.** Le finestre secondarie che richiedono attenzione devono essere in primo piano per assicurarsi che vengano visualizzate dagli utenti.
-   **Lampeggiare solo un pulsante della barra delle applicazioni per una finestra alla volta.** Il lampeggio di più di un pulsante è superfluo ed è troppo fastidioso.
-   **Rimuovi il pulsante della barra delle applicazioni evidenziato quando il programma diventa attivo.**
-   **Quando il programma diventa attivo, assicurarsi che sia presente qualcosa di ovvio.** In genere, questo obiettivo viene eseguito visualizzando una finestra di dialogo che pone una domanda o avvia un'azione.

### <a name="quick-launch-shortcuts"></a>Collegamenti di avvio veloce

-   **Inserire i tasti di scelta rapida del programma nell'area avvio veloce solo se gli utenti scelgono esplicitamente.** Poiché avvio veloce è stato rimosso da Windows 7, i programmi progettati per Windows 7 non devono aggiungere collegamenti al programma all'area avvio veloce o fornire opzioni a tale scopo.

### <a name="jump-lists"></a>Jump List

**Progettazione**

-   **Jump List di progettazione per soddisfare gli obiettivi degli utenti per le attività quotidiane.** Tenere in considerazione:
    -   **Scopo del programma.** Si pensi a quali utenti più probabilmente verranno eseguite successivamente. Per i programmi di creazione di documenti, è probabile che gli utenti tornino ai documenti utilizzati di recente. Per i programmi che mostrano il contenuto esistente, gli utenti possono accedere alle risorse usate di frequente. Per altri programmi, è probabile che gli utenti eseguano le attività che non hanno eseguito prima, ad esempio la lettura di nuovi messaggi, il controllo di nuovi video o la riunione successiva.
    -   **Quali sono gli utenti più interessati.** Si pensi ai motivi per cui gli utenti usano la Jump List anziché altri mezzi. Ad esempio, è più probabile che gli utenti si occupino delle destinazioni che identificano in modo esplicito come importanti, ad esempio gli utenti di indirizzi Web posizionati sulla barra dei collegamenti o nei Preferiti oppure digitati in. È meno probabile che si occupino di quelli ottenuti indirettamente o con un minimo sforzo (ad esempio, gli indirizzi Web visitati tramite Reindirizzamento o facendo clic sui collegamenti).

        **Corretto:**

        ![screenshot della Jump List con un collegamento a una destinazione ](images/winenv-taskbar-image25.png)

        **Non corretto:**

        ![screenshot della Jump List con cinque collegamenti a destinazione ](images/winenv-taskbar-image26.png)

        Nell'esempio errato, la Jump List contiene molte destinazioni a cui gli utenti non sono interessati.

-   **Non rendere le destinazioni troppo granulari.** Rendere le destinazioni troppo strette e specifiche può comportare la ridondanza, con diversi modi per passare alla stessa posizione. Ad esempio, anziché elencare singole pagine Web, elencare invece le Home page di primo livello; anziché elencare canzoni, elencare gli album.

    **Corretto:**

    ![screenshot della Jump List organizzata per gruppi ](images/winenv-taskbar-image27.png)

    **Non corretto:**

    ![screenshot della Jump List organizzata per canzoni ](images/winenv-taskbar-image28.png)

    Nell'esempio errato, l'elenco di canzoni in una Jump List compilerà un singolo album.

-   **Se non è necessario, non compilare tutti gli slot della Jump List disponibili.** Concentrare il contenuto della Jump List sugli elementi più utili se il programma include solo tre elementi utili, fornire solo tre elementi. Maggiore è il numero di elementi in una Jump List, maggiore è il lavoro richiesto per trovare un elemento specifico.

    ![screenshot della Jump List con un comando ](images/winenv-taskbar-image29.png)

    In questo esempio, il Memo accessorio fornisce un solo comando Jump List, perché è tutto ciò che è necessario.

-   **Fornire descrizioni comandi solo quando necessario per aiutare gli utenti a comprendere gli elementi Jump List.** Evitare le descrizioni comandi ridondanti perché si tratta di una distrazione non necessaria. Per altre linee guida della descrizione comando, vedere [Tooltips and infotip](ctrl-tooltips-and-infotips.md).

    **Non corretto:**

    ![screenshot della Jump List con descrizione comando ridondante ](images/winenv-taskbar-image30.png)

    In questo esempio la descrizione comando Jump List è ridondante.

**Funzionalità di Jump List rispetto alle funzionalità del programma**

-   **Non rendere le destinazioni e i comandi disponibili solo tramite Jump List.** Le stesse destinazioni e i comandi devono essere disponibili direttamente dal programma stesso.
-   **Usare nomi coerenti per destinazioni ed etichette per i comandi.** Gli elementi della Jump List devono essere etichettati come gli elementi equivalenti a cui si accede direttamente dal programma.
-   **Consentire al programma di gestire destinazioni e comandi anche quando il programma non è in esecuzione.** Questa operazione è necessaria per un'esperienza coerente, affidabile e pratica.

**Raggruppamento**

-   **Fornire almeno uno e tre gruppi.** Gli elementi della Jump List sono sempre raggruppati per etichettarne lo scopo. La presenza di più di tre gruppi rende più difficile trovare gli elementi.
-   **Usare i nomi di gruppo standard quando appropriato.** I nomi dei gruppi standard sono noti e più semplici da comprendere per gli utenti.

    Ai comandi viene assegnato il nome del gruppo di attività, che viene assegnato da Windows e pertanto non può essere modificato.

    **Corretto:**

    ![screenshot della Jump List con il nome del gruppo recente ](images/winenv-taskbar-image31.png)

    **Non corretto:**

    ![screenshot della Jump List con il nome del gruppo di cronologia ](images/winenv-taskbar-image32.png)

    Recente è il nome del gruppo migliore perché è familiare e la distinzione minima tra la cronologia e la recente non è importante.

**Comandi**

-   **Fornire un set di comandi fisso indipendentemente dallo stato di esecuzione del programma, dal documento corrente o dall'utente corrente.** I comandi devono essere applicati all'intero programma, non a una finestra o a un documento specifico. Questa operazione è necessaria per un'esperienza coerente, affidabile e pratica. I comandi non devono essere rimossi o disabilitati.

    **Eccezioni:** I comandi possono essere sostituiti o rimossi nei casi seguenti:

    -   Un set di comandi che si escludono a vicenda condivide un singolo slot di comandi, purché venga sempre applicato un comando.
    -   I comandi non sono applicabili fino a quando non vengono usate funzionalità specifiche, purché i comandi vengano sempre applicati.

    **Non corretto:**

    ![screenshot della Jump List con l'attività di stampa ](images/winenv-taskbar-image33.png)

    In questo esempio, Print non è un comando Jump List valido perché dipende dal documento corrente.

    **Corretto:**

    ![screenshot della Jump List con accesso e disconnessione ](images/winenv-taskbar-image34.png)

    In questo esempio, l'accesso e la disconnessione sono comandi che si escludono a vicenda. Inoltre, i separatori vengono utilizzati per raggruppare i comandi correlati.

-   **Usare le etichette di comando standard seguenti quando appropriato.** Le etichette dei comandi standard sono più semplici da comprendere per gli utenti.
-   **Presentare i comandi in un ordine logico.** Gli ordini comuni includono la frequenza d'uso o l'ordine di utilizzo. Posizionare i comandi strettamente correlati tra loro. All'interno del gruppo Tasks, inserire i separatori tra i gruppi di comandi correlati, in base alle esigenze.
-   **Non fornire comandi per l'apertura o la chiusura del programma.** Questi comandi sono incorporati in tutte le Jump List.

**Icone dei comandi**

-   **All'interno del gruppo attività fornire un'icona di comando solo quando consente agli utenti di comprendere, riconoscere o distinguere i comandi,** soprattutto quando è presente un'icona stabilita per il comando utilizzato all'interno del programma.

    -   **Eccezione:** Se il programma usa entrambe le destinazioni (che hanno sempre icone) e i comandi, provare a fornire le icone per tutti i comandi in caso contrario.

    **Non corretto:**

    ![cattura di schermata dell'utilizzo incoerente delle icone nella Jump List ](images/winenv-taskbar-image35.png)

    In questo esempio Internet Explorer deve fornire icone per tutti i comandi per evitare un aspetto imbarazzante.

**Destinazioni**

-   **Fornire un set dinamico di destinazioni specifiche dell'utente corrente, ma indipendentemente dallo stato di esecuzione del programma o dal documento corrente.** Come indicato in precedenza, assicurarsi che corrispondano allo scopo del programma, che gli utenti si occupino maggiormente del più possibile e abbiano il giusto livello di specificità.
-   **Quando appropriato, usare un elenco di destinazione "automatico".** Le destinazioni automatiche sono gestite da Windows, ma il programma controlla le destinazioni specifiche che vengono passate.
    -   Si consiglia di utilizzare i programmi recenti per la creazione di documenti, in cui è probabile che gli utenti tornino alle destinazioni utilizzate di recente

        ![screenshot della Jump List con il nome del gruppo ' recente ' ](images/winenv-taskbar-image36.png)

        In questo esempio, il blocco note di Windows utilizza le destinazioni recenti.

    -   Prendere in considerazione l'uso di frequente per programmi che mostrano contenuto esistente, in cui è probabile che gli utenti restituiscano gli elementi che usano spesso. Le destinazioni frequenti sono ordinate in ordine di frequenza, più frequenti per prime.

        ![screenshot della Jump List con il nome frequente del gruppo ](images/winenv-taskbar-image37.png)

        In questo esempio Esplora risorse utilizza destinazioni frequenti.

    -   Usare frequenti se recenti generano molte destinazioni inutili. Gli elenchi frequenti sono più stabili e la scelta migliore quando gli utenti passano a molte destinazioni diverse, ma non possono tornare a quelli usati raramente.

        **Non corretto:**

        ![screenshot della Jump List con diversi elementi recenti ](images/winenv-taskbar-image38.png)

        L'utilizzo di recenti in Windows Internet Explorer comporta numerose destinazioni superflue.

    -   Se recenti o frequenti sono opzioni ugualmente appropriate, usare recenti perché questo approccio è più semplice da comprendere per gli utenti ed è più prevedibile.
    -   Se si usa recente e il programma ha un equivalente nel menu file, fare in modo che gli elenchi abbiano lo stesso contenuto nello stesso ordine. Per gli utenti, questi sembrano essere gli stessi elenchi.

-   **Quando necessario, utilizzare un elenco di destinazione personalizzato.** Il programma ha il controllo completo sul contenuto e sul tipo di ordinamento di un elenco di destinazione personalizzato e pertanto può basare l'elenco su qualsiasi fattore.
    -   Creare versioni personalizzate di recenti o frequenti se sono adatte, ma la gestione automatica non funziona correttamente per il programma. Ad esempio, il programma potrebbe avere la necessità di tenere traccia di diversi fattori oltre ai comandi di file aperti. In questo caso, usare lo stesso nome (recente o frequente) e il tipo di ordinamento perché gli utenti non saranno a conoscenza della differenza.
    -   In caso contrario, usare un tipo diverso di destinazione per soddisfare al meglio gli obiettivi dell'utente. Spesso, questi elenchi consentono agli utenti di eseguire attività che non hanno eseguito prima, ad esempio leggere nuovi messaggi, guardare nuovi video o controllare la riunione successiva.

        ![screenshot della Jump List con il nome del gruppo ' New ' ](images/winenv-taskbar-image39.png)

        In questo esempio Windows Media Center elenca le segnalazioni registrate di recente che l'utente non ha ancora visualizzato.

    -   Scegliere un tipo di ordinamento corrispondente al modello mentale dell'utente dell'elenco. Ad esempio, un elenco di stili to-do avrà l'aspetto successivo da eseguire prima di tutto. Se non è presente alcun modello mentale chiaro, ordinare l'elenco di destinazione in ordine alfabetico.

-   **Non usare più elenchi di destinazione che offrono visualizzazioni diverse degli stessi dati.** Piuttosto, più elenchi di destinazione devono disporre di dati di gran parte diversi per supportare scenari di differenza. Ad esempio, è possibile fornire un elenco recente o un elenco frequente, ma non entrambi. Questa operazione è inutile se sono presenti elementi sovrapposti, ma si confonde se gli elementi sovrapposti vengono rimossi.

    **Non corretto:**

    ![screenshot della Jump List con elementi di gruppo ripetuti ](images/winenv-taskbar-image40.png)

    In questo esempio, fornire visualizzazioni diverse delle stesse destinazioni è uno spreco.

    **Corretto:**

    ![screenshot della Jump List con attività ben organizzate ](images/winenv-taskbar-image41.png)

    In questo esempio, gli elenchi di destinazione hanno dati diversi per le diverse attività.

-   **Se il programma dispone di un comando per cancellare i dati per la privacy, deselezionare anche gli elenchi di destinazioni.** Gli elenchi di destinazione possono contenere dati riservati.

### <a name="thumbnail-toolbars"></a>Barre degli strumenti delle anteprime

**Interazione**

-   **Fornire fino a sette dei comandi più importanti e usati di frequente che si applicano alla finestra visualizzata nell'anteprima.** Non è necessario che venga fornito il numero di comandi possibile se il programma dispone solo di tre comandi importanti, di uso frequente, che forniscono solo tre.

    **Non corretto:**

    ![cattura di schermata della barra degli strumenti con troppi comandi ](images/winenv-taskbar-image42.png)

    In questo esempio, la barra degli strumenti dell'anteprima contiene comandi che non sono importanti.

-   **Usare i comandi diretti e immediati.** Questi comandi devono avere un effetto immediato facendo clic sul comando non deve visualizzare un menu a discesa o una finestra di dialogo per ottenere ulteriori input.

    **Non corretto:**

    ![screenshot dell'anteprima con menu a discesa ](images/winenv-taskbar-image43.png)

    I comandi dell'anteprima della barra degli strumenti devono avere un effetto immediato.

-   **Disabilitare i comandi che non si applicano al contesto corrente o che restituiscono direttamente un errore.** Non nascondere tali comandi perché questa operazione rende instabile la presentazione della barra degli strumenti.
-   **Non chiudere l'anteprima quando gli utenti fanno clic su un comando se è probabile che rivedano i risultati o fanno clic immediatamente su un altro comando.** Rimuovere l'anteprima per i comandi che indicano che l'utente è terminato per ora, ad esempio con comandi che visualizzano altre finestre.

    ![screenshot dell'anteprima di Media Player con comando ](images/winenv-taskbar-image44.png)

    In questo esempio, facendo clic su avanti in Windows Media Player continua a visualizzare l'anteprima perché gli utenti potrebbero voler assegnare altri comandi.

    ![screenshot dell'anteprima con icona della chat ](images/winenv-taskbar-image45.png)

    In questo esempio, facendo clic su chat in Windows Live Messenger viene rilasciata l'anteprima perché è più probabile che gli utenti inviino un messaggio.

**Presentazione**

-   **Assicurarsi che le icone della barra degli strumenti di anteprima siano conformi alle linee guida dell'icona di tipo Aero** Per ogni comando, fornire icone a colori 16x16, 20x20 e 24x24 di alta qualità. Le versioni più grandi vengono usate nelle modalità di visualizzazione a DPI elevato.
-   **Assicurarsi che le icone siano chiaramente visibili rispetto al colore di sfondo della barra degli strumenti sia negli Stati normale che nel passaggio del mouse.** Valutare sempre le icone nel contesto e nelle modalità a contrasto elevato.
-   **Scegliere l'icona del comando progettazioni che comunicano chiaramente il loro effetto.** Le icone del comando ben progettate sono autoesplicative per consentire agli utenti di trovare e comprendere i comandi in modo efficiente.
-   **Scegliere le icone riconoscibili e distinguibili.** Assicurarsi che le icone abbiano forme e colori distinti. Questa operazione consente agli utenti di trovare rapidamente i comandi, anche se non ricordano il simbolo dell'icona. Dopo l'utilizzo iniziale, gli utenti non devono fare affidamento sulle descrizioni comando per distinguere tra i comandi.
-   **Fornire una descrizione comando per etichettare ogni comando.** Una descrizione comando corretta etichetta il controllo senza etichetta a cui si fa riferimento. Per linee guida ed esempi, vedere [Tooltips and infotip](ctrl-tooltips-and-infotips.md).

### <a name="progress-bars"></a>Indicatori di stato

-   **Seguire le linee guida generali sull'indicatore di stato, incluso il** riavvio o il backup dello stato di avanzamento, e l'uso di un indicatore di stato rosso per indicare un problema.
-   **Evitare di utilizzare indicatori di stato indeterminati.** Gli indicatori di stato indeterminati mostrano l'attività, non lo stato di avanzamento. Riservare indicatori di stato indeterminati per le rare situazioni in cui gli utenti non accettano attività per la concessione.

Per altre linee guida, vedere [indicatori di stato](progress-bars.md).

## <a name="text"></a>Testo

### <a name="window-titles"></a>Titoli delle finestre

Quando si scelgono i titoli delle finestre, prendere in considerazione l'aspetto del titolo sulla barra delle applicazioni:

-   Ottimizzare i titoli per la visualizzazione sulla barra delle applicazioni inserendo prima di tutto le informazioni di distinzione.
-   Per le finestre di dialogo di stato non modale, riepilogare prima di tutto lo stato di avanzamento. Esempio: "66% completato".
-   Evitare i titoli di finestra con troncamenti imbarazzanti.

    **Non corretto:**

    ![screenshot del titolo che interrompe il nome del programma ](images/winenv-taskbar-image48.png)

    In questo esempio il titolo della finestra troncata presenta risultati sfavorevoli.

### <a name="jump-list-commands"></a>Comandi della Jump List

-   **Avviare i comandi con un verbo.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**

Per altre linee guida sulle etichette dei comandi, vedere [menu](cmd-menus.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alla barra delle applicazioni:

-   Fare riferimento all'intera barra come barra delle applicazioni (una singola parola composta in minuscolo).
-   Fare riferimento agli elementi sulla barra delle applicazioni in modo specifico in base all'etichetta o in genere come pulsanti della barra delle applicazioni.
-   Quando possibile, formattare le etichette della barra delle applicazioni usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.
-   Fare riferimento alle icone sovrapposte come icone del pulsante della barra delle applicazioni. Non fare riferimento ad essi come notifiche, anche se lo scopo è quello di inviare una notifica agli utenti. Tuttavia, si può dire che queste icone segnalano agli utenti eventi specifici.

Esempio: l'icona del pulsante nuova barra delle applicazioni di posta elettronica informa che è arrivato un nuovo messaggio di posta elettronica.

 

