---
title: Barra delle applicazioni
description: La barra delle applicazioni è il punto di accesso per i programmi visualizzati sul desktop. Con le nuove funzionalità della barra delle applicazioni di Windows 7, gli utenti possono fornire comandi, accedere alle risorse e visualizzare lo stato del programma direttamente dalla barra delle applicazioni.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3e549e665f0200a448144ddf7202b258e88ff26
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443392"
---
# <a name="taskbar"></a>Barra delle applicazioni

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

La barra delle applicazioni è il punto di accesso per i programmi visualizzati sul desktop. Con le nuove funzionalità della barra delle applicazioni di Windows 7, gli utenti possono fornire comandi, accedere alle risorse e visualizzare lo stato del programma direttamente dalla barra delle applicazioni.

La barra delle applicazioni è il punto di accesso per i programmi visualizzati sul desktop, anche se il programma è ridotto a icona. Si dice che tali programmi hanno la presenza sul desktop. Con la barra delle applicazioni, gli utenti possono visualizzare le finestre primarie aperte e alcune finestre secondarie sul desktop e passare rapidamente da una finestra all'altro.

![Screenshot della barra delle applicazioni con funzionalità chiamate ](images/winenv-taskbar-image1.png)

Barra delle applicazioni di Microsoft Windows.

I controlli sulla barra delle applicazioni sono definiti pulsanti della barra delle applicazioni. Quando un programma crea una finestra primaria (o una finestra secondaria con determinate caratteristiche), Windows aggiunge un pulsante della barra delle applicazioni per tale finestra e lo rimuove alla chiusura della finestra.

I programmi progettati per Windows 7 possono sfruttare le nuove funzionalità dei pulsanti della barra delle applicazioni:

-   Le jump list consentono di accedere rapidamente alle destinazioni usate di frequente (ad esempio file, cartelle e collegamenti) e ai comandi tramite un menu di scelta rapida accessibile dal pulsante della barra delle applicazioni e dall'elemento menu Start del programma anche se il programma non è attualmente in esecuzione.
-   Le barre degli strumenti di anteprima consentono di accedere rapidamente ai comandi usati di frequente per una determinata finestra. Le barre degli strumenti dell'anteprima vengono visualizzate nell'anteprima del pulsante della barra delle applicazioni.
-   Le icone di sovrapposizione mostrano la modifica dello stato sull'icona del pulsante della barra delle applicazioni del programma.
-   Gli barre di stato mostrano lo stato di avanzamento per le attività a esecuzione lunga sul pulsante della barra delle applicazioni del programma.
-   I pulsanti della barra delle applicazioni della finestra secondaria consentono agli utenti di usare le anteprime dei pulsanti della barra delle applicazioni per passare direttamente alle schede delle finestre, alle finestre di progetto, alle finestre figlio dell'interfaccia a documenti multipli e alle finestre secondarie.
-   I pulsanti della barra delle applicazioni aggiunti consentono agli utenti di aggiungere pulsanti di programma alla barra delle applicazioni per fornire accesso rapido ai programmi anche quando non sono in esecuzione.

Tecnicamente, la barra delle applicazioni si estende sull'intera barra dal pulsante Start all'area di notifica. più comunemente, tuttavia, la barra delle applicazioni si riferisce solo all'area contenente i pulsanti della barra delle applicazioni. Per più configurazioni di monitoraggio, solo un monitor ha una barra delle applicazioni e tale monitoraggio è il monitor predefinito.

**Nota:** Le linee guida relative alla gestione del [desktop,](winenv-desktop.md) [dell'area](winenv-notification.md)di notifica e [della](win-window-mgt.md) finestra sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

I programmi progettati per Windows 7 possono sfruttare queste funzionalità dei pulsanti della barra delle applicazioni. Porsi le domande chiave seguenti per determinare se usarle o meno:

**Jump List**

-   **Gli utenti spesso devono avviare nuove attività usando il programma?** In tal caso, è consigliabile fornire un Jump List. Sebbene le Jump List possano essere usate per altri scopi, la maggior parte degli scenari comporta l'avvio di una nuova attività.
-   **Gli utenti devono spesso accedere a file, cartelle, collegamenti o altre risorse usati di recente o di frequente?** In tal caso, è consigliabile fornire Jump List per accedere a queste risorse utili.

    ![Screenshot della barra delle applicazioni con Internet Explorer jump list ](images/winenv-taskbar-image2.png)

    In questo esempio, Windows Internet Explorer usa un Jump List per presentare le pagine visitate di frequente.

-   **Gli utenti spesso necessitano di accesso rapido a un numero ridotto di comandi del programma durante l'uso di altri programmi, anche se il programma non è in esecuzione?** In tal caso, è consigliabile fornire un Jump List questi comandi usati di frequente. Questi comandi devono funzionare anche se il programma non è in esecuzione e devono essere applicati all'intero programma, non a una finestra specifica. In alternativa, è consigliabile fornire una barra degli strumenti di anteprima per i comandi che si applicano a una finestra specifica.

    ![Screenshot della barra delle applicazioni con note jump list ](images/winenv-taskbar-image3.png)

    In questo esempio, l'Memo consente agli utenti di creare rapidamente una nuova nota durante l'uso di altri programmi.

-   **Si stanno promuovendo funzionalità nuove, a uso singolo o difficili da trovare?** In tal caso, non usare Jump List perché non sono destinate a questo scopo. È invece possibile migliorare l'individuabilità di tali comandi direttamente nel programma.

**Barre degli strumenti delle anteprime**

Si applicano tutte le condizioni seguenti?

-   **I comandi si applicano a una finestra specifica?** Le barre degli strumenti di anteprima sono per i comandi che si applicano alle attività esistenti, Jump List comandi sono per l'avvio di nuove attività.
-   **Gli utenti devono interagire rapidamente con un'attività in esecuzione durante l'uso di altri programmi?** In tal caso, le barre degli strumenti di anteprima sono una scelta ottimale. Le barre degli strumenti di anteprima possono presentare un massimo di sette comandi, ma in genere è preferibile usare un massimo di cinque comandi.
-   **I comandi sono immediati?** Ciò significa che non richiedono input aggiuntivo? Le barre degli strumenti delle anteprime devono avere comandi immediati per essere efficienti, mentre le Jump List funzionano meglio con i comandi che richiedono input aggiuntivo.

    **Non corretto:**

    ![Screenshot della barra delle applicazioni con finestre sovrapposte ](images/winenv-taskbar-image4.png)

    I comandi che richiedono input aggiuntivo non funzionano correttamente nelle barre degli strumenti delle anteprime.

-   **I comandi sono diretti?** In altri, gli utenti possono interagire con essi con un solo clic? Le barre degli strumenti devono avere comandi diretti per essere efficienti.
-   **I comandi sono rappresentati in modo ben da icone?** I comandi della barra degli strumenti anteprima vengono presentati usando icone non etichette di testo, Jump List comandi sono rappresentati da etichette di testo.

    **Non corretto:**

    ![Screenshot del comando thumbnail con l'icona ](images/winenv-taskbar-image5.png)

    In questo esempio il comando non è ben rappresentato dalle icone.

**Icone di sovrimpressione**

-   **Il programma ha "presenza desktop"?** In caso contrario, usare invece un'icona dell'area di notifica. In tal caso, è consigliabile usare un'icona di sovrimpressione invece di inserire lo stato sull'icona dell'area di notifica per i programmi progettati per Windows 7. In questo modo si garantisce che l'icona sia sempre visibile (quando vengono usate icone grandi) e si consolida il programma con il relativo stato in un'unica posizione.
-   **L'icona di sovrimpressione viene visualizzata temporaneamente per mostrare una modifica dello stato?** In tal caso, potrebbe essere appropriata un'icona di sovrimpressione, a seconda dei fattori seguenti:
    -   **Lo stato è utile e pertinente durante l'uso di altri programmi?** In caso contrario, visualizzare le [](ctrl-status-bars.md) informazioni nelle barre di stato del programma o in un'altra area di stato del programma.

        ![Screenshot della barra di stato della finestra di Internet Explorer ](images/winenv-taskbar-image7.png)

        In questo esempio viene usata la barra di stato perché lo stato non è utile quando si usano altri programmi.

    -   **Lo stato mostra lo stato di avanzamento?** In tal caso, usare invece un indicatore di stato del pulsante della barra delle applicazioni.
    -   **Lo stato è critico? È necessaria un'azione immediata?** In tal caso, visualizzare le informazioni in modo che richiede attenzione e non possa essere facilmente ignorata, ad esempio una finestra [di dialogo](win-dialog-box.md).

**Barre di stato**

-   **Il feedback sullo stato di avanzamento è utile e pertinente durante l'uso di altri programmi?** In altre parole, è probabile che gli utenti monitorino lo stato di avanzamento durante l'uso di altri programmi e cambino il comportamento di conseguenza? Questo stato utile e pertinente viene in genere visualizzato usando una finestra di dialogo di stato non modabile o una pagina di stato dedicata, ma non con un puntatore occupato, un indicatore di attività o un indicatore di stato su una barra di stato. Se lo stato non è utile quando si usano altri programmi, è sufficiente visualizzare il feedback sullo stato di avanzamento direttamente nel programma stesso.

    **Corretto:**

    ![Screenshot della finestra di dialogo copia con l'indicatore di stato ](images/winenv-taskbar-image8.png)

    **Non corretto:**

    ![Screenshot dell'indicatore di stato sul pulsante della barra delle applicazioni ](images/winenv-taskbar-image9.png)

    Nell'esempio non corretto, l'indicatore di stato del pulsante della barra delle applicazioni non è molto utile.

-   **L'attività è continua?** Se l'attività non viene mai completata, non è necessario visualizzarne lo stato di avanzamento. Esempi di attività continue includono le analisi antivirus non avviate dagli utenti e l'indicizzazione di file.

    **Non corretto:**

    ![Screenshot dell'icona di stato di un'attività continua ](images/winenv-taskbar-image10.png)

    In questo esempio non è necessario che un'attività continua mostri lo stato di avanzamento.

**Barre delle applicazioni della finestra secondaria**

-   **Il programma contiene schede, finestre di progetto, finestre figlio MDI o finestre secondarie a cui gli utenti spesso vogliono passare direttamente?** In tal caso, potrebbe essere appropriato fornire a queste finestre le anteprime dei pulsanti della barra delle applicazioni.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Uso efficace delle jump list e delle barre degli strumenti delle anteprime

Le jump list e le barre degli strumenti delle anteprime consentono agli utenti di accedere alle risorse ed eseguire i comandi in modo più efficiente. Tuttavia, quando si progetta il modo in cui il programma supporta queste funzionalità, non dare per scontata una maggiore efficienza. Se gli utenti non possono prevedere con precisione quale funzionalità ha il comando necessario o devono controllare più posizioni, alla fine gli utenti diventeranno frustranti e smetteranno di usare queste funzionalità.

Le jump list e le barre degli strumenti delle anteprime funzionano in modo più efficace quando sono:

-   **Chiaramente differenziata.** Gli utenti sanno quando cercare una destinazione o un comando in un Jump List e quando eseguire la ricerca in una barra degli strumenti di anteprima. Esiste uno scopo chiaro per ognuno di essi, quindi gli utenti raramente confondono il contenuto dei due. In genere, le jump list vengono usate per avviare nuove attività, mentre le barre degli strumenti di anteprima vengono usate per interagire con le attività in esecuzione mentre si usano altri programmi.
-   **Utile.** Le destinazioni e i comandi offerti sono quelli necessari per gli utenti. Se è probabile che gli utenti non necessitino di qualcosa, non è incluso. Non usare il numero massimo di elementi se non sono necessari.
-   **Prevedibile.** Le destinazioni e i comandi offerti sono quelli che gli utenti si aspettano di trovare. Gli utenti raramente devono cercare in più di una posizione.
-   **Ben organizzato.** Gli utenti sono in grado di trovare rapidamente ciò che cercano. Usano etichette descrittive ma concise e icone adatte per facilitare il riconoscimento.

Assicurarsi di eseguire ricerche degli utenti per assicurarsi di aver ottenuto il giusto. Se in definitiva non è possibile progettare jump list e barre degli strumenti di anteprima per raggiungere questi obiettivi, è consigliabile specificarne solo uno. È meglio avere un modo prevedibile per assegnare comandi rispetto a due comandi confusi.

## <a name="guidelines"></a>Indicazioni

### <a name="taskbar-buttons"></a>Pulsanti della barra delle applicazioni

-   **Fare in modo che i tipi di finestra seguenti vengano visualizzati sulla barra delle applicazioni (per Windows 7, usando un'anteprima del pulsante della barra delle applicazioni):**
    -   Finestre primarie (che includono finestre di dialogo senza proprietari)
    -   Finestre delle proprietà
    -   Finestre di dialogo di stato non modali
    -   Procedure guidate
-   **Per Windows 7, usa le anteprime dei pulsanti della barra delle applicazioni per raggruppare i tipi di finestra seguenti con il pulsante della barra delle applicazioni della finestra principale da cui è stato avviato.** Ogni programma (in particolare, ogni programma percepito come programma separato) deve avere un singolo pulsante della barra delle applicazioni.

    -   Finestre secondarie
    -   Schede dell'area di lavoro
    -   Finestre del progetto
    -   finestre figlio MDI

    **Corretto:**

    ![Screenshot di Esplora risorse e dell'indicatore di stato ](images/winenv-taskbar-image11.png)

    In questo esempio una finestra secondaria viene raggruppata con il pulsante della barra delle applicazioni della finestra primaria.

    **Non corretto:**

    ![Screenshot di Esplora risorse e del Pannello di controllo ](images/winenv-taskbar-image12.png)

    In questo esempio, Pannello di controllo è raggruppato in modo errato con Esplora risorse. Gli utenti li percepiranno come programmi separati.

    **Non corretto:**

    ![screenshot del programma, dell'indicatore di stato e di una barra delle applicazioni ](images/winenv-taskbar-image13.png)

    In questo esempio, Windows Backup usa erroneamente due pulsanti della barra delle applicazioni per un singolo programma.

-   **Il ripristino di una finestra primaria dovrebbe ripristinare anche tutte le finestre secondarie,** anche se tali finestre secondarie hanno pulsanti della barra delle applicazioni propri. Durante il ripristino, posizionare le finestre secondarie sopra la finestra primaria.
-   **Per Windows 7, i programmi che normalmente hanno la presenza sul desktop possono visualizzare temporaneamente un pulsante della barra delle applicazioni per mostrare lo stato.** Eseguire questa operazione solo se il programma viene normalmente visualizzato sul desktop e gli utenti interagiscono spesso con esso. Un programma che in genere viene eseguito senza presenza del desktop deve usare l'icona dell'area di notifica, anche se potrebbe non essere sempre visibile.

    **Non corretto:**

    ![Screenshot del pulsante della barra delle applicazioni del Centro sincronizzazione Windows ](images/winenv-taskbar-image14.png)

    In questo esempio, Centro sincronizzazione Windows usa erroneamente un pulsante temporaneo della barra delle applicazioni per visualizzare lo stato. Deve invece usare l'icona dell'area di notifica.

### <a name="icons"></a>Icone

-   **Progettare l'icona del programma in modo che sia molto simile alla barra delle applicazioni.** Assicurarsi che sia significativo e rifletta la funzione e il marchio. Renderlo distinto, renderlo speciale e assicurarsi che il rendering sia ben eseguito in tutte le dimensioni delle icone. Dedicare il tempo necessario per ottenere il giusto. Seguire le [linee guida per le icone in stile Aereo](vis-icons.md).
-   **Se il programma usa icone di sovrimpressione, progettare l'icona di base del programma per gestire correttamente le sovrimpressione.** Le icone di sovrapposizione vengono visualizzate nell'angolo inferiore destro, quindi progettare l'icona in modo che tale area possa essere nascosta.

    ![screenshot delle icone e con sovrimpressione in basso a destra ](images/winenv-taskbar-image15.png)

    In questo esempio l'icona del pulsante della barra delle applicazioni del programma non contiene informazioni importanti nell'area inferiore destra.

-   **Non usare sovrimpressione nell'icona di base del programma,** indipendentemente dal fatto che il programma usi icone sovrapposte o meno. L'uso di una sovrimpressione nell'icona di base può generare confusione perché gli utenti devono capire che non sta comunicando lo stato.

    **Non corretto:**

    ![Screenshot dell'icona di base con sovrimpressione ](images/winenv-taskbar-image16.png)

    In questo esempio l'icona di base del programma ha l'aspetto di mostrare lo stato.

Per linee guida ed esempi generali sulle icone, vedere [Icone.](vis-icons.md)

### <a name="overlay-icons"></a>Icone di sovrimpressione

-   **Usare le icone di sovrimpressione per indicare solo lo stato utile e pertinente.** Si consideri la visualizzazione di un'icona di sovrimpressione come potenziale interruzione del lavoro dell'utente, quindi la modifica dello stato deve essere sufficientemente importante da intasare una potenziale interruzione.

    **Non corretto:**

    ![Screenshot di tre icone di sovrimpressione ](images/winenv-taskbar-image17.png)

    In questi esempi, l'icona di sovrimpressione non è sufficientemente importante da intasare una potenziale interruzione.

-   **Usare le icone di sovrapposizione per lo stato temporaneo.** Le icone di sovrimpressione perdono il valore se visualizzate costantemente, quindi lo stato normale del programma non dovrebbe mostrare un'icona. Rimuovere l'icona di sovrimpressione quando l'icona:

    -   **È per un problema:** Rimuovere l'icona dopo aver risolto il problema.
    -   **Avvisi che segnalano una novità:** Rimuovere l'icona dopo che l'utente ha attivato il programma.

    **Eccezione:** Il programma può visualizzare costantemente un'icona di sovrimpressione se gli utenti devono sempre conoscerne lo stato.

    ![Screenshot di Live Messenger con icona di sovrimpressione ](images/winenv-taskbar-image18.png)

    In questo esempio, Windows Live Messenger visualizza sempre un'icona di sovrimpressione in modo che gli utenti possano sempre controllare la presenza segnalata.

-   **Non visualizzare un'icona per indicare che un problema è stato risolto.** È invece sufficiente rimuovere qualsiasi icona precedente che indica un problema. Si supponga che gli utenti in genere si aspettino che il programma sia in esecuzione senza problemi.
-   **Visualizzare icone sovrapposte o icone dell'area di notifica, ma mai entrambe.** Il programma può supportare entrambi i meccanismi per la compatibilità con le versioni precedenti, ma se il programma visualizza lo stato usando icone di sovrimpressione, non deve usare anche le icone dell'area di notifica per lo stato.

    **Non corretto:**

    ![Screenshot della barra delle applicazioni con l'icona visualizzata due volte ](images/winenv-taskbar-image19.png)

    In questo esempio la nuova icona di posta elettronica viene visualizzata in modo ridondante.

-   **Non eseguire il flash del pulsante della barra delle applicazioni per attirare l'attenzione su una modifica dello stato.** In questo modo sarebbe troppo distrazione. Consentire agli utenti di individuare le icone sovrapposte in modo personalizzato.
-   **Preferire le icone di sovrimpressione standard per indicare le modifiche di stato o di stato.** Usare queste icone di sovrimpressione standard: 

    | Sovrapposizione (Overlay) | Stato |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot dell'icona di avviso di piccole dimensioni ](images/winenv-taskbar-image20.png)<br/>               | Avviso<br/>               |
    | ![Screenshot di una piccola icona di errore ](images/winenv-taskbar-image21.png)<br/>                 | Errore<br/>                 |
    | ![Screenshot dell'icona piccola disabilitata/disconnessa ](images/winenv-taskbar-image22.png)<br/> | Disabilitato/Disconnesso<br/> |
    | ![Screenshot dell'icona piccola bloccata/offline ](images/winenv-taskbar-image23.png)<br/>       | Bloccato/Offline<br/>       |

    

     

-   **Per le icone di sovrapposizione personalizzate, scegliere una progettazione facilmente riconoscibile.** Usare icone a colori 16x16 pixel di alta qualità. Preferisce le icone con contorni distintivi rispetto alle icone a forma quadrata o rettangolare. Applicare anche le [altre linee guida per le icone in stile](vis-icons.md) Aero.
-   **Mantenere semplice la progettazione delle icone di sovrapposizione personalizzate.** Non provare a comunicare idee complesse, sconosciute o astratte. Se non si può pensare a un'icona personalizzata appropriata, usare un'icona standard di errore o di avviso, se appropriato. Queste icone possono essere usate in modo efficace per comunicare molti tipi di stato.
-   **Non modificare lo stato troppo frequentemente.** Le icone di sovrapposizione non dovrebbero apparire rumorose, instabili o richiedono attenzione. L'occhio è sensibile ai cambiamenti nel campo periferico della visione, quindi le modifiche di stato devono essere sottili.
    -   **Non modificare rapidamente l'icona.** Se lo stato sottostante cambia rapidamente, fare in modo che l'icona rifletta lo stato di alto livello.

        **Non corretto:**

        ![Screenshot dell'icona di sovrimpressione in due stati ](images/winenv-taskbar-image24.png)

        In questo esempio, l'icona di sovrapposizione in rapida evoluzione richiede attenzione.

    -   **Non usare animazioni.** Questa operazione è troppo distrazione.
    -   **Non lampeggiare l'icona.** Questa operazione è troppo distrazione. Se un evento richiede attenzione immediata, usare invece una finestra di dialogo. Se in caso contrario, l'evento richiede attenzione, usare una notifica.

### <a name="taskbar-button-flashing"></a>Lampeggiamento del pulsante della barra delle applicazioni

-   **Usare il pulsante della barra delle applicazioni lampeggiante con parsimonio per richiedere l'attenzione immediata dell'utente per mantenere in esecuzione un'attività in corso.** È difficile che gli utenti si concentrino mentre un pulsante della barra delle applicazioni lampeggia, quindi si supponga che interrompa ciò che sta facendo per arrestarlo. Mentre il flashing di un pulsante della barra delle applicazioni è meglio che rubare lo stato attivo per l'input, i pulsanti lampeggianti della barra delle applicazioni sono ancora molto invadente. Assicurarsi che l'interruzione sia giustificata, ad esempio per indicare che l'utente deve salvare i dati prima di chiudere una finestra. I programmi inattivi devono raramente richiedere un'azione immediata. Non far lampeggiare il pulsante della barra delle applicazioni se l'unica cosa che l'utente deve fare è attivare il programma, leggere un messaggio o visualizzare una modifica dello stato.
-   **Se non è necessaria un'azione immediata, considerare queste alternative:**
    -   Usare una [notifica di esito positivo dell'azione](mess-notif.md) per indicare che un'attività è stata completata.
    -   Non eseguire alcuna operazione. È sufficiente attendere che gli utenti attendano il problema alla successiva attivazione del programma. Questa è spesso la scelta migliore.
-   **Se un programma inattivo richiede attenzione immediata, fare lampeggiare il pulsante della barra delle applicazioni per attirare l'attenzione e lasciarlo evidenziato.** Non eseguire altre operazioni: non ripristinare o attivare la finestra e non riprodurre effetti sonori. Rispettare invece la selezione dello stato della finestra dell'utente e consentire all'utente di attivare la finestra quando è pronto.
-   **Per le finestre secondarie con un pulsante della barra delle applicazioni, lampeggiare il pulsante anziché il pulsante della barra delle applicazioni della finestra primaria.** In questo modo gli utenti possono partecipare direttamente alla finestra.
-   **Per le finestre secondarie che non hanno un pulsante della barra delle applicazioni, fare lampeggiare il pulsante della barra delle applicazioni della finestra primaria e portare la finestra secondaria sopra tutte le altre finestre del programma.** Le finestre secondarie che richiedono attenzione devono essere in primo piano per garantire che gli utenti le vedano.
-   **Flash un solo pulsante della barra delle applicazioni per una finestra alla volta.** Lampeggiare più di un pulsante non è necessario e distrarre troppo.
-   **Rimuovere l'evidenziazione del pulsante della barra delle applicazioni quando il programma diventa attivo.**
-   **Quando il programma diventa attivo, assicurarsi che ci sia qualcosa di ovvio da fare.** In genere, questo obiettivo viene raggiunto visualizzando una finestra di dialogo che pone una domanda o avvia un'azione.

### <a name="quick-launch-shortcuts"></a>Avvio veloce tasti di scelta rapida

-   **Inserire i collegamenti ai programmi nell'area Avvio veloce solo se gli utenti acconsentino esplicitamente.** Poiché Avvio veloce è stato rimosso da Windows 7, i programmi progettati per Windows 7 non devono aggiungere collegamenti ai programmi all'area Avvio veloce né fornire opzioni a tale scopo.

### <a name="jump-lists"></a>Jump List

**Progettazione**

-   **Progettare jump list per soddisfare gli obiettivi degli utenti per le attività quotidiane.** Tenere in considerazione:
    -   **Scopo del programma.** È probabile che gli utenti esereranno le prossime. Per i programmi di creazione di documenti, è probabile che gli utenti tornino ai documenti usati di recente. Per i programmi che mostrano contenuto esistente, gli utenti potrebbero voler accedere alle risorse usate di frequente. Per altri programmi, è probabile che gli utenti eseereranno attività non eseguite in precedenza, ad esempio leggere nuovi messaggi, guardare nuovi video o controllare la riunione successiva.
    -   **Ciò che gli utenti si preoccupano di più.** Si pensi al motivo per cui gli utenti userebbero Jump List invece di altri mezzi. Ad esempio, è più probabile che gli utenti si occupino delle destinazioni identificate in modo esplicito come importanti, ad esempio indirizzi Web inseriti dagli utenti sulla barra dei collegamenti o nei Preferiti o digitati in . È meno probabile che si occupino di quelli ottenuti indirettamente o con poco sforzo ,ad esempio gli indirizzi Web visitati tramite reindirizzamento o facendo clic sui collegamenti.

        **Corretto:**

        ![Screenshot dell'jump list con un collegamento a una destinazione ](images/winenv-taskbar-image25.png)

        **Non corretto:**

        ![Screenshot dell'jump list con cinque collegamenti alla destinazione ](images/winenv-taskbar-image26.png)

        Nell'esempio non corretto il Jump List contiene molte destinazioni che gli utenti probabilmente non hanno a cuore.

-   **Non rendere le destinazioni troppo granulari.** Rendere le destinazioni troppo ristrette e specifiche può comportare ridondanza, con diversi modi per passare alla stessa posizione. Ad esempio, invece di elencare singole pagine Web, elencare le home page di primo livello; invece di elencare i brani, elencare gli album.

    **Corretto:**

    ![Screenshot dell'jump list organizzati in base ai gruppi ](images/winenv-taskbar-image27.png)

    **Non corretto:**

    ![Screenshot del jump list organizzato in base ai brani ](images/winenv-taskbar-image28.png)

    Nell'esempio non corretto, elencare i brani in un Jump List verrà riempito con un singolo album.

-   **Non riempire tutti gli slot Jump List disponibili se non è necessario.** Concentrarsi Jump List sugli elementi più utili se il programma ha solo tre elementi utili, fornire solo tre elementi. Più elementi in un Jump List, maggiore è il lavoro necessario per trovare qualsiasi elemento specifico.

    ![Screenshot dell'jump list con un comando ](images/winenv-taskbar-image29.png)

    In questo esempio, Memo'accessorio fornisce un singolo Jump List comando, perché è tutto ciò che serve.

-   **Fornire descrizioni comando solo quando necessario per consentire agli utenti di Jump List elementi.** Evitare descrizioni comando ridondanti perché sono una distrazione non necessaria. Per altre linee guida per la descrizione comando, [vedere Descrizioni comando e suggerimenti.](ctrl-tooltips-and-infotips.md)

    **Non corretto:**

    ![Screenshot di un'jump list con descrizione comando ridondante ](images/winenv-taskbar-image30.png)

    In questo esempio, la descrizione Jump List comando è ridondante.

**Jump List funzionalità e funzionalità del programma**

-   **Non rendere disponibili destinazioni e comandi solo tramite Jump List.** Le stesse destinazioni e gli stessi comandi devono essere disponibili direttamente dal programma stesso.
-   **Usare nomi coerenti per le destinazioni e le etichette per i comandi.** Jump List elementi devono essere etichettati come gli elementi equivalenti a cui si accede direttamente dal programma.
-   **Abilitare il programma per gestire le destinazioni e i comandi anche quando il programma non è in esecuzione.** Questa operazione è necessaria per un'esperienza coerente, affidabile e pratica.

**Raggruppamento**

-   **Specificare almeno uno e al massimo tre gruppi.** Jump List elementi vengono sempre raggruppati per etichettarne lo scopo. La presenza di più di tre gruppi rende più difficile trovare gli elementi.
-   **Usare i nomi dei gruppi standard quando appropriato.** I nomi dei gruppi standard sono familiari e più facili da comprendere per gli utenti.

    Ai comandi viene assegnato il nome del gruppo Attività, assegnato da Windows e pertanto non può essere modificato.

    **Corretto:**

    ![Screenshot dell'jump list con il nome del gruppo recente ](images/winenv-taskbar-image31.png)

    **Non corretto:**

    ![Screenshot del jump list con il nome del gruppo di cronologia ](images/winenv-taskbar-image32.png)

    Recente è il nome del gruppo migliore perché è familiare e la sottile distinzione tra cronologia e recente non vale la pena fare.

**Comandi**

-   **Fornire un set fisso di comandi indipendentemente dallo stato di esecuzione del programma, dal documento corrente o dall'utente corrente.** I comandi devono essere applicati all'intero programma, non a una finestra o a un documento specifico. Questa operazione è necessaria per un'esperienza coerente, affidabile e pratica. I comandi non devono essere rimossi o disabilitati.

    **Eccezioni:** È possibile sostituire o rimuovere i comandi quando:

    -   Un set di comandi che si escludono a vicenda condividono un singolo slot di comando, purché sia sempre applicabile un comando.
    -   I comandi non vengono applicati fino a quando non vengono usate funzionalità specifiche, purché i comandi siano sempre applicabili.

    **Non corretto:**

    ![Screenshot dell'jump list con l'attività di stampa ](images/winenv-taskbar-image33.png)

    In questo esempio Print non è un comando Jump List perché dipende dal documento corrente.

    **Corretto:**

    ![Screenshot dell'jump list con accesso e disconnessione ](images/winenv-taskbar-image34.png)

    In questo esempio, l'accesso e la disconnessione sono comandi che si escludono a vicenda. Inoltre, i separatori vengono usati per raggruppare i comandi correlati.

-   **Usare le etichette dei comandi standard seguenti quando appropriato.** Le etichette dei comandi standard sono più facili da comprendere per gli utenti.
-   **Presentare i comandi in un ordine logico.** Gli ordini comuni includono la frequenza di utilizzo o l'ordine di utilizzo. Posizionare comandi altamente correlati uno accanto all'altro. All'interno del gruppo Attività inserire i separatori tra i gruppi di comandi correlati in base alle esigenze.
-   **Non fornire comandi per l'apertura o la chiusura del programma.** Questi comandi sono incorporati in tutte le Jump List.

**Icone dei comandi**

-   **All'interno del** gruppo Attività specificare un'icona di comando solo quando consente agli utenti di comprendere, riconoscere o distinguere i comandi, soprattutto quando è presente un'icona stabilita per il comando usato all'interno del programma.

    -   **Eccezione:** Se il programma usa entrambe le destinazioni (che hanno sempre icone) e comandi, valutare la possibilità di fornire icone per tutti i comandi se non lo si fa.

    **Non corretto:**

    ![Screenshot dell'jump list'uso incoerente delle icone ](images/winenv-taskbar-image35.png)

    In questo esempio, Internet Explorer le icone per tutti i comandi per evitare un aspetto scomodo.

**Destinazioni**

-   **Fornire un set dinamico di destinazioni specifiche per l'utente corrente, ma indipendentemente dallo stato di esecuzione del programma o dal documento corrente.** Come accennato in precedenza, assicurarsi che si adattino allo scopo del programma, siano ciò che gli utenti si preoccupano di più e che abbia il giusto livello di specificità.
-   **Se appropriato, usare un elenco di destinazione "automatico".** Le destinazioni automatiche vengono gestite da Windows, ma il programma controlla le destinazioni specifiche passate.
    -   Prendere in considerazione l'uso di Recenti per i programmi di creazione di documenti in cui è probabile che gli utenti tornino alle destinazioni usate di recente.

        ![Screenshot dell'jump list con il nome del gruppo "recente" ](images/winenv-taskbar-image36.png)

        In questo esempio Blocco note di Windows usa destinazioni recenti.

    -   Prendere in considerazione l'uso di Frequente per i programmi che mostrano contenuto esistente, in cui è probabile che gli utenti tornino agli elementi che usano spesso. Le destinazioni frequenti vengono ordinate in ordine di frequenza, le destinazioni più frequenti per prime.

        ![Screenshot dell'jump list con il nome del gruppo frequente ](images/winenv-taskbar-image37.png)

        In questo esempio, Esplora risorse destinazioni frequenti.

    -   Usare Frequente se Recenti comporta molte destinazioni inutili. Gli elenchi frequenti sono più stabili e la scelta migliore quando gli utenti passano a molte destinazioni diverse, ma non è probabile che tornino a quelle usate raramente.

        **Non corretto:**

        ![Screenshot dell'jump list con diversi elementi recenti ](images/winenv-taskbar-image38.png)

        L'uso di Recenti in Windows Internet Explorer comporta molte destinazioni inutili.

    -   Se le opzioni Recenti o Frequenti sono ugualmente appropriate, usare Recenti perché questo approccio è più facile da comprendere ed è più prevedibile per gli utenti.
    -   Se si usa Recenti e il programma ha un equivalente nel menu File, fare in modo che gli elenchi presentino lo stesso contenuto nello stesso ordine. Per gli utenti, questi dovrebbero essere gli stessi elenchi.

-   **Se necessario, usare un elenco di destinazione personalizzato.** Il programma ha il controllo completo sul contenuto e sull'ordinamento di un elenco di destinazione personalizzato e può pertanto basare l'elenco su qualsiasi fattori.
    -   Creare versioni personalizzate di Recenti o Frequenti se sono adatte, ma la gestione automatica non funziona correttamente per il programma. Ad esempio, il programma potrebbe dover tenere traccia di diversi fattori oltre ai comandi per l'apertura di file. In questo caso, usare lo stesso nome (Recente o Frequente) e l'ordinamento perché gli utenti non saranno consapevoli della differenza.
    -   In caso contrario, usare un tipo diverso di destinazione per soddisfare meglio gli obiettivi dell'utente. Spesso questi elenchi consentono agli utenti di eseguire attività non eseguite in precedenza, ad esempio leggere nuovi messaggi, guardare nuovi video o controllare la riunione successiva.

        ![Screenshot dell'jump list con il nome del gruppo "nuovo" ](images/winenv-taskbar-image39.png)

        In questo esempio, Windows Media Center elenca gli eventi registrati di recente che l'utente non ha ancora visto.

    -   Scegliere un ordinamento che corrisponda al modello mentale dell'utente dell'elenco. Ad esempio, un elenco di stili attività dovrebbe avere la prima cosa da fare. Se non esiste un modello mentale chiaro, ordinare l'elenco di destinazione in ordine alfabetico.

-   **Non usare più elenchi di destinazione che forniscono visualizzazioni diverse degli stessi dati.** Invece, più elenchi di destinazione devono avere dati principalmente diversi per supportare scenari di differenza. Ad esempio, è possibile specificare un elenco Recenti o frequente, ma non entrambi. Questa operazione è disserta se sono presenti elementi sovrapposti, ma confonde se gli elementi sovrapposti vengono rimossi.

    **Non corretto:**

    ![Screenshot dell'jump list con elementi di gruppo ripetuti ](images/winenv-taskbar-image40.png)

    In questo esempio, fornire visualizzazioni diverse delle stesse destinazioni è uno spreco.

    **Corretto:**

    ![Screenshot dell'jump list con attività ben organizzate ](images/winenv-taskbar-image41.png)

    In questo esempio, gli elenchi di destinazione hanno dati diversi per attività diverse.

-   **Se il programma ha un comando per cancellare i dati per la privacy, deselezionare anche gli elenchi Destinazioni.** Gli elenchi di destinazione possono contenere dati sensibili.

### <a name="thumbnail-toolbars"></a>Barre degli strumenti di anteprima

**Interazione**

-   **Fornire fino a sette dei comandi più importanti usati di frequente che si applicano alla finestra visualizzata nell'anteprima.** Non essere obbligati a fornire il maggior numero possibile di comandi se il programma ha solo tre comandi importanti, usati di frequente, e ne fornisce solo tre.

    **Non corretto:**

    ![Screenshot della barra degli strumenti con troppi comandi ](images/winenv-taskbar-image42.png)

    In questo esempio la barra degli strumenti dell'anteprima include comandi non importanti.

-   **Usare comandi diretti e immediati.** Questi comandi dovrebbero avere un effetto immediato facendo clic sul comando non dovrebbe visualizzare un menu a discesa o una finestra di dialogo per un altro input.

    **Non corretto:**

    ![Screenshot dell'anteprima con menu a discesa ](images/winenv-taskbar-image43.png)

    I comandi della barra degli strumenti dell'anteprima devono avere un effetto immediato.

-   **Disabilitare i comandi che non si applicano al contesto corrente o che restituirebbero direttamente un errore.** Non nascondere questi comandi perché in questo modo la presentazione della barra degli strumenti diventa instabile.
-   **Non chiudere l'anteprima quando gli utenti fanno clic su un comando se è probabile che rivedranno i risultati o fare immediatamente clic su un altro comando.** Rimuovere l'anteprima per i comandi che indicano che l'utente è terminato per il momento, ad esempio con i comandi che visualizzano altre finestre.

    ![Screenshot dell'anteprima del lettore multimediale con il comando ](images/winenv-taskbar-image44.png)

    In questo esempio, facendo clic su Avanti Windows Media Player continua a visualizzare l'anteprima perché gli utenti potrebbero voler fornire altri comandi.

    ![Screenshot dell'anteprima con l'icona della chat ](images/winenv-taskbar-image45.png)

    In questo esempio, facendo clic su Chat in Windows Live Messenger l'anteprima viene chiusa perché è più probabile che gli utenti inviino un messaggio.

**Presentazione**

-   **Assicurarsi che le icone della barra degli strumenti dell'anteprima siano conformi alle linee guida per le icone in stile Aereo.** Per ogni comando, fornire icone a colori completo di alta qualità 16x16, 20x20 e 24x24 pixel. Le versioni più grandi vengono usate in modalità di visualizzazione a dpi elevato.
-   **Assicurarsi che le icone siano chiaramente visibili sul colore di sfondo della barra degli strumenti negli stati normale e al passaggio del mouse.** Valutare sempre le icone nel contesto e nelle modalità a contrasto elevato.
-   **Scegliere progettazioni di icone di comando che comunicano chiaramente il loro effetto.** Le icone dei comandi ben progettate sono auto-esplicativi per aiutare gli utenti a trovare e comprendere i comandi in modo efficiente.
-   **Scegliere icone riconoscibili e distinguibili.** Assicurarsi che le icone presentino forme e colori distintivi. In questo modo gli utenti possono trovare rapidamente i comandi, anche se non ricordano il simbolo dell'icona. Dopo l'uso iniziale, gli utenti non devono basarsi sulle descrizioni comando per distinguere tra i comandi.
-   **Fornire una descrizione comando per etichettare ogni comando.** Una descrizione comando buona etichetta il controllo senza etichetta a cui punta. Per linee guida ed esempi, vedere [Descrizioni comando e suggerimenti.](ctrl-tooltips-and-infotips.md)

### <a name="progress-bars"></a>Barre di stato

-   **Seguire le linee guida generali sull'indicatore di stato,** tra cui il non riavvio o il backup dello stato di avanzamento e l'uso di un indicatore di stato rosso per indicare un problema.
-   **Evitare l'uso di barre di stato indeterminate.** Gli barre di stato indeterminati mostrano l'attività, non lo stato di avanzamento. Riservare barre di stato indeterminate per le rare situazioni in cui gli utenti non prendono per scontata l'attività.

Per altre linee guida, vedere [ProgressBars](progress-bars.md).

## <a name="text"></a>Testo

### <a name="window-titles"></a>Titoli delle finestre

Quando si scelgono i titoli delle finestre, considerare l'aspetto del titolo sulla barra delle applicazioni:

-   Ottimizzare i titoli per la visualizzazione sulla barra delle applicazioni posizionando concisamente le informazioni distintive per prime.
-   Per le finestre di dialogo di stato non modali, riepilogare innanzitutto lo stato di avanzamento. Esempio: "66% Completato".
-   Evitare i titoli delle finestre con troncamenti difficili.

    **Non corretto:**

    ![Screenshot del titolo che taglia il nome del programma ](images/winenv-taskbar-image48.png)

    In questo esempio il titolo della finestra troncata ha risultati non ottimali.

### <a name="jump-list-commands"></a>Jump List comandi

-   **Avviare i comandi con un verbo.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**

Per altre linee guida sulle etichette dei comandi, vedere [Menu.](cmd-menus.md)

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alla barra delle applicazioni:

-   Fare riferimento all'intera barra come barra delle applicazioni (una singola parola composta in minuscolo).
-   Fare riferimento agli elementi della barra delle applicazioni in modo specifico in base all'etichetta o in genere come pulsanti della barra delle applicazioni.
-   Quando possibile, formattare le etichette della barra delle applicazioni usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.
-   Fare riferimento alle icone sovrapposte come icone dei pulsanti della barra delle applicazioni. Non fare riferimento a queste notifiche come notifiche, anche se lo scopo è quello di inviare notifiche agli utenti. Tuttavia, è possibile dire che queste icone notificano agli utenti eventi specifici.

Esempio: l'icona del pulsante della barra delle applicazioni Nuovo messaggio notifica che è arrivato un nuovo messaggio di posta elettronica.

 

