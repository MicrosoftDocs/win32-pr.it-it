---
title: Area di notifica
description: L'area di notifica fornisce notifiche e stato. I programmi ben progettati usano l'area di notifica in modo appropriato, senza essere fastidiosi o distratti.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c580d80bd95684cc80dc24e59273553f4a08e11f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985454"
---
# <a name="notification-area"></a>Area di notifica

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

L'area di notifica fornisce notifiche e stato. I programmi ben progettati usano l'area di notifica in modo appropriato, senza essere fastidiosi o distratti.

L'area di notifica è una parte della barra delle applicazioni che fornisce un'origine temporanea per le notifiche e lo stato. Può anche essere usato per visualizzare le icone per le funzionalità del sistema e del programma che non sono presenti sul desktop.

Gli elementi nell'area di notifica vengono definiti icone dell'area di notifica o semplicemente icone se il contesto dell'area di notifica è già chiaramente stabilito.

![Screenshot dell'area di notifica, dell'ora e della data ](images/winenv-notification-image1.png)

Area di notifica.

Per concedere agli utenti il controllo del desktop in Windows 7, non tutte le icone dell'area di notifica vengono visualizzate per impostazione predefinita. Le icone vengono invece visualizzate nell'overflow dell'area di notifica, a meno che non vengano promosse all'area di notifica dall'utente.

![Screenshot che mostra un'area di notifica e un overflow.](images/winenv-notification-image2.png)

Overflow dell'area di notifica.

**Nota:** Le linee guida relative alla barra delle [applicazioni,](winenv-taskbar.md) [alle](mess-notif.md) notifiche e [ai palloncini](ctrl-balloons.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **Il programma deve visualizzare una notifica?** In tal caso, è necessario usare un'icona dell'area di notifica.
-   **L'icona viene visualizzata temporaneamente per visualizzare una modifica dello stato?** In tal caso, un'icona dell'area di notifica potrebbe essere appropriata, a seconda dei fattori seguenti:

    -   **Lo stato è utile e pertinente?** In altre informazioni, è probabile che gli utenti monitorino l'icona e ne cambino il comportamento? In caso contrario, non visualizzare lo stato o inserirlo in un file di log.

        **Non corretto:**

        ![Screenshot dell'area di notifica con l'icona dell'unità ](images/winenv-notification-image3.png)

        In questo esempio l'icona dell'attività unità disco non è appropriata perché è improbabile che gli utenti cambino il comportamento in base a essa.

    -   **Lo stato è critico? È necessaria un'azione immediata?** In tal caso, visualizzare le informazioni in modo che richiede attenzione e non possa essere facilmente ignorata, ad esempio una [finestra di dialogo](win-dialog-box.md).

    I programmi progettati per Windows 7 possono usare le icone di sovrapposizione sul pulsante della barra delle applicazioni del programma per mostrare la modifica dello stato, nonché le barre di stato dei pulsanti della barra delle applicazioni per visualizzare lo stato di avanzamento delle attività con esecuzione lunga.

-   **La funzionalità ha già "presenza desktop"?** Ovvero, quando viene eseguita, la funzionalità viene visualizzata in una finestra sul desktop (possibilmente ridotta a icona)? In tal caso, visualizzare lo stato nella barra di stato del [programma,](ctrl-status-bars.md)in un'altra area di stato o, Windows 7, direttamente sul pulsante della barra delle applicazioni. Se la funzionalità non è presente sul desktop, è possibile usare un'icona per l'accesso al programma e per visualizzare lo stato.
-   **L'icona è principalmente per avviare un programma o accedere rapidamente alle relative funzionalità o impostazioni?** In tal caso, usare il menu Start per avviare i programmi. L'area di notifica non è destinata all'accesso rapido al programma o ai comandi.

    ![Screenshot della barra degli strumenti Avvio veloce ](images/winenv-notification-image4.png)

    In questo esempio di Windows Vista, Avvio veloce viene usato per avviare Windows Explorer e Windows Internet Explorer rapidamente.

    Per i programmi progettati per Windows 7, gli utenti possono aggiungere pulsanti della barra delle applicazioni per l'accesso rapido ai programmi. I programmi possono usare una barra Jump List o anteprima per accedere ai comandi usati di frequente direttamente dal pulsante della barra degli strumenti di un programma. L Avvio veloce area non viene visualizzata per impostazione predefinita in Windows 7.

    ![Screenshot della barra delle applicazioni e jump list con le icone ](images/winenv-notification-image5.png)

    In questo esempio viene usato un Jump List per l'accesso rapido ai comandi.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="the-windows-desktop"></a>Il Windows desktop

Il Windows desktop ha i punti di accesso del programma seguenti:

-   **Area di lavoro.** Area su schermo in cui gli utenti possono eseguire il lavoro, nonché archiviare programmi, documenti e i relativi collegamenti. Anche se tecnicamente il desktop include la barra delle applicazioni, nella maggior parte dei contesti fa riferimento solo all'area di lavoro.
-   **pulsante Start.** Punto di accesso per tutti i programmi e le posizioni Windows speciali (Documenti, Immagini, Musica, Giochi, Computer, Pannello di controllo), con elenchi usati più di recente per l'accesso rapido ai programmi e ai documenti usati di recente.
-   **Avvio veloce.** Punto di accesso diretto per i programmi selezionati dall'utente. Avvio veloce stato rimosso da Windows 7.
-   **Taskbar.** Punto di accesso per l'esecuzione di programmi con presenza del desktop. Anche se tecnicamente la barra delle applicazioni si estende sull'intera barra dal pulsante Start all'area di notifica, nella maggior parte dei contesti la barra delle applicazioni si riferisce all'area in mezzo, contenente i pulsanti della barra delle applicazioni. Questa area viene talvolta definita banda di attività.
-   **Fasce da tavolo. Non consigliato.**
-   **Area di notifica.** Un'origine a breve termine per le notifiche e lo stato, nonché un punto di accesso per le funzionalità correlate al sistema e al programma che non sono presenti sul desktop.

![Screenshot che identifica i punti di accesso del desktop ](images/winenv-notification-image6.png)

I Windows di accesso desktop includono il pulsante Start, la barra delle applicazioni e l'area di notifica. Si noti la funzionalità di anteprima del pulsante della barra delle applicazioni.

**Il desktop è una risorsa condivisa limitata che rappresenta il punto di ingresso dell'utente Windows.** Lasciare gli utenti sotto controllo. È consigliabile usare le aree desktop come previsto qualsiasi altro utilizzo deve essere considerato un abuso. Ad esempio, non visualizzare mai le aree desktop come modi per promuovere il programma o il [relativo marchio.](exper-branding.md)

### <a name="using-the-notification-area-appropriately"></a>Uso appropriato dell'area di notifica

L'area di notifica era originariamente destinata come origine temporanea per le notifiche e lo stato. La sua efficienza e praticità ha incoraggiato gli sviluppatori a fornire altri scopi, ad esempio l'avvio di programmi e l'esecuzione di comandi. Sfortunatamente nel corso del tempo, queste aggiunte hanno reso l'area di notifica troppo grande e rumorosa e ne ha confuso lo scopo con gli altri punti di accesso del desktop.

Windows XP ha risolto il problema di scalabilità rendendo l'area comprimibile e nascondendo le icone non utilizzate. Windows Vista ha corretto il rumore rimuovendo le notifiche inutili e fastidiose. Windows 7 ha fatto un ulteriore passo avanti concentrando la notifica sullo scopo originale di essere un'origine di notifica. **La maggior parte delle icone è nascosta per impostazione Windows 7, ma può essere promossa manualmente all'area di notifica dall'utente. Per mantenere gli utenti in controllo dei desktop, il programma non può eseguire automaticamente questa promozione.** Windows visualizza ancora le notifiche per le icone nascoste promuovendole temporaneamente.

![Screenshot dell'area di notifica e dell'overflow ](images/winenv-notification-image7.png)

In Windows 7, la maggior parte delle icone dell'area di notifica è nascosta per impostazione predefinita.

Inoltre, Windows 7 supporta molte funzionalità direttamente nei pulsanti della barra delle applicazioni. In particolare, è possibile usare:

-   Jump List e barre degli strumenti delle anteprime per accedere rapidamente ai comandi usati di frequente.
-   Sovrapporre le icone per visualizzare lo stato dei programmi in esecuzione.
-   Barre di stato dei pulsanti della barra delle applicazioni per visualizzare lo stato di avanzamento per le attività con esecuzione lunga.

In breve, se il programma ha la presenza sul desktop, sfruttare appieno le funzionalità del pulsante della barra delle applicazioni Windows 7 per questi scopi. **Mantenere le icone dell'area di notifica incentrate sulla visualizzazione di notifiche e stato.**

### <a name="keeping-users-in-control"></a>Mantenere gli utenti sotto controllo

Mantenere gli utenti sotto controllo si estende oltre l'uso corretto dell'area di notifica. A seconda della natura dell'icona, è possibile consentire agli utenti di eseguire le operazioni seguenti:

-   **Rimuovere l'icona.** L'icona può fornire uno stato pertinente e utile, ma anche in questo caso gli utenti potrebbero non volerlo visualizzare. Windows consente agli utenti di nascondere le icone, ma questa funzionalità non è facilmente individuabile. Per mantenere gli utenti sotto controllo, specificare **un'opzione Icona di visualizzazione nell'area di** notifica nel menu di scelta rapida dell'icona. Si noti che la rimozione di un'icona non deve influire sul programma, sulla funzionalità o sul processo sottostante.
-   **Selezionare i tipi di notifiche da visualizzare.** La notifica deve essere utile e pertinente, ma potrebbero essere presenti notifiche che gli utenti non vogliono visualizzare. Questo vale soprattutto per [](mess-notif.md)le notifiche FYI. Consentire agli utenti di scegliere di abilitare quelli meno importanti.
-   **Sospendere le funzionalità facoltative.** Le icone vengono usate per visualizzare lo stato delle funzionalità senza presenza del desktop. Queste funzionalità tendono a essere attività in background facoltative a esecuzione continua, ad esempio stampa, indicizzazione, analisi o sincronizzazione. Gli utenti possono voler sospendere tali funzionalità per aumentare le prestazioni del sistema, ridurre il consumo di energia o perché sono offline.
-   **Chiudere il programma.** Specificare le opzioni più adatte:
    -   **Chiudere temporaneamente il programma.** Il programma viene arrestato e riavviato al Windows riavvio. Questo approccio è adatto per importanti utilità di sistema, ad esempio i programmi di sicurezza.
    -   **Chiudere definitivamente il programma.** Il programma viene arrestato e non riavviato quando Windows riavvio (a meno che l'utente non scesi a riavviare in un secondo momento). L'utente non vuole più eseguire il programma o vuole eseguire il programma su richiesta, ad esempio per migliorare le prestazioni del sistema.

Anche se è consigliabile fornire la maggior parte di queste impostazioni nel menu di scelta rapida dell'icona, l'esperienza predefinita del programma deve essere adatta alla maggior parte degli utenti. Non attivare tutto per impostazione predefinita e prevedere che gli utenti dissegnino le funzionalità. Attivare invece le funzionalità importanti per impostazione predefinita e consentire agli utenti di abilitare funzionalità aggiuntive in base alle esigenze.

**Se si eservino solo quattro operazioni...**

1.  Non utilizzare in modo improprio l'area di notifica. Usarlo solo come origine per le notifiche e lo stato e per le funzionalità senza presenza del desktop.
2.  Mantenere gli utenti sotto controllo. Fornire le opzioni appropriate per controllare l'icona, le relative notifiche e le funzionalità sottostanti.
3.  Presentare un'esperienza predefinita adatta alla maggior parte degli utenti. Consentire agli utenti di abilitare le funzionalità desiderate anziché prevederle di disabilitare quelle indesiderate.
4.  Sfruttare al meglio le funzionalità Windows 7 pulsanti della barra delle applicazioni per visualizzare lo stato e rendere efficienti le attività eseguite più di frequente del programma.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le icone dell'area di notifica hanno diversi modelli di utilizzo:




| Etichetta | Valore |
|--------|-------|
| <strong>Stato del sistema e accesso</strong><br /> Visualizzato in modo continuo per mostrare lo stato del sistema importante ma non critico e per fornire l'accesso alle funzionalità e alle impostazioni pertinenti. <br /> | Le funzionalità di sistema che necessitano di icone dell'area di notifica non hanno una presenza desktop permanente. Può essere usato anche come origine di notifica. <br /><img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br /> In questo esempio, le icone della batteria, della rete e del volume vengono visualizzate in modo continuo, se applicabile.<br /> | 
| <strong>Stato e accesso dell'attività in background</strong><br /> Visualizzato durante l'esecuzione di un'attività in background per visualizzare lo stato e fornire l'accesso a funzionalità e impostazioni. <br /> | I processi in background necessitano di icone dell'area di notifica quando non sono presenti sul desktop. Può essere usato anche come origine di notifica. <br /><img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br /> In questo esempio l'icona del Centro notifiche consente agli utenti di verificarne lo stato anche quando non è presente sul desktop.<br /> | 
| <strong>Stato dell'evento temporaneo</strong><br /> I programmi con presenza del desktop possono visualizzare temporaneamente le icone per visualizzare eventi importanti o modifiche nello stato. <br /> | <img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br /> In questo esempio, le icone per la stampa e l'installazione degli aggiornamenti vengono visualizzate temporaneamente per visualizzare eventi importanti o modifiche dello stato.<br /> | 
| <strong>Origine notifica temporanea</strong><br /> Visualizzato temporaneamente per visualizzare una notifica. Rimozione dopo un timeout o quando viene risolto il problema sottostante o viene eseguita un'attività. <br /> | Le icone temporanee sono preferite per le origini di notifica pure. Non visualizzare un'icona che non fornisce uno stato dinamico utile, pertinente solo perché una funzionalità potrebbe dover visualizzare una notifica in futuro. <br /><img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br /> In questo esempio viene visualizzata l'icona plug-and-play mentre viene visualizzata una nuova notifica rilevata dall'hardware.<br /> | 
| <strong>Applicazione a istanza singola ridotta a icona</strong><br /> Per ridurre l'ingombro della barra delle applicazioni, un'applicazione a esecuzione lunga a istanza singola può essere ridotta a icona dell'area di notifica. <br /> | <img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br /> In questo esempio di Windows Vista, Outlook e Windows Live Messenger sono applicazioni a istanza singola che vengono ridotte a icona dell'area di notifica.<br /> È consigliabile usare questo modello solo se si applicano tutte le condizioni seguenti: <br /><ul><li>L'applicazione può avere una sola istanza.</li><li>L'applicazione viene eseguita per un periodo di tempo prolungato.</li><li>L'icona mostra lo stato.</li><li>L'icona può essere un'origine di notifica.</li><li>Questa operazione è facoltativa e gli utenti devono <a href="glossary.md">acconsentire esplicitamente a</a>.</li></ul>Se si applicano tutte queste condizioni, la riduzione al minimo di un'icona elimina la presenza di due punti di accesso quando ne è necessario solo uno. <br /><strong>Nota:</strong> Questo modello di icona non è più consigliato per Windows 7. Usare i normali pulsanti della barra delle applicazioni se il programma ha la presenza sul desktop.<br /><img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br /> In questo esempio di Windows 7, un normale pulsante della barra delle applicazioni richiede poco spazio, ma trae vantaggio dalle funzionalità del pulsante della barra delle applicazioni di Windows 7, tra cui Jump List, icone di sovrapposizione e anteprime avanzate.<br /> | 




 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Fornire una sola icona dell'area di notifica per componente.**
-   **Usare un'icona con versioni 16x16, 20x20 e 24x24 pixel.** Le versioni più grandi vengono usate in modalità di visualizzazione a dpi elevato.

### <a name="when-to-show"></a>Quando visualizzare

-   Per il modello di origine della notifica temporanea:
    -   Windows l'icona quando viene visualizzata la notifica.
    -   Rimuovere l'icona in base al modello [di progettazione delle](mess-notif.md) notifiche:



    | Modello                                     | Quando rimuovere                                         |
    |--------------------------------------|------------------------------------------|
    | Azione riuscita<br/>            | Quando la notifica viene rimossa.<br/> |
    | Errore dell'azione<br/>            | Quando il problema viene risolto.<br/>     |
    | Evento di sistema non critico<br/> | Quando il problema viene risolto.<br/>     |
    | Attività utente facoltativa<br/>        | Al termine dell'attività.<br/>            |
    | FYI<br/>                       | Quando la notifica viene rimossa.<br/> |



 

-   **Per il modello di stato dell'evento temporaneo, visualizzare l'icona mentre si verifica l'evento.**
-   Per tutti gli altri modelli, visualizzare l'icona quando il programma, la funzionalità o il processo è in esecuzione e l'icona è pertinente a meno che l'utente non abbia deselezionato l'opzione Icona di visualizzazione nell'area di notifica . Per altre **informazioni,** vedere [Menu](#context-menus)di scelta rapida .  La maggior parte delle icone è nascosta per impostazione Windows 7, ma può essere promossa all'area di notifica dall'utente.
-   **Non visualizzare icone destinate agli amministratori per gli utenti standard.** Registrare le informazioni nel Windows eventi.

### <a name="where-to-show"></a>Dove visualizzare

-   **Visualizzare le finestre avviate dalle icone dell'area di notifica vicino all'area di notifica.**

![Figura di una finestra vicino all'area di notifica ](images/winenv-notification-image14.png)

Windows le icone dell'area di notifica avviate vengono visualizzate vicino all'area di notifica.

### <a name="icons"></a>Icone

-   **Scegliere l'icona in base al modello di progettazione:**

    | Modello                                                 | Tipo di icona                                   |
    |--------------------------------------------------|------------------------------------|
    | Stato del sistema e accesso<br/>              | Icona della funzionalità di sistema<br/>     |
    | Stato e accesso dell'attività in background<br/>     | Icona del programma o della funzionalità<br/> |
    | Origine notifica temporanea<br/>         | Icona programma o funzionalità<br/> |
    | Stato temporaneo dell'evento<br/>                | Icona programma o funzionalità<br/> |
    | Applicazione a istanza singola ridotta a icona<br/> | Icona programma<br/>            |

    

     

    ![Screenshot dell'area di notifica e delle icone di Outlook ](images/winenv-notification-image15.png)

    In questo esempio, Outlook un'icona di funzionalità di posta elettronica per un'origine di notifica temporanea e la relativa icona applicazione per l'applicazione ridotta a icona.

-   **Scegliere una progettazione di icona facilmente riconoscibile.** Preferisce icone con contorni univoci rispetto a icone a forma quadrata o rettangolare. Mantenere le progettazioni semplici preferisce i simboli rispetto alle immagini realistiche. Applicare anche le [altre linee guida per le icone in stile](vis-icons.md) Aereo.
-   **Usare varianti di icona o sovrimpressione per indicare lo stato o le modifiche dello stato.** Usare le varianti delle icone per visualizzare le modifiche nelle quantità o nei punti di forza. Per altri tipi di stato, usare le sovrimpressione standard seguenti. Usare una sola sovrimpressione e individuarla in basso a destra per coerenza. 

    | Sovrapposizione (Overlay)                                                                                                       | Stato                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot dell'icona di avviso piccola ](images/winenv-notification-image16.png)<br/>               | Avviso<br/>               |
    | ![Screenshot dell'icona di errore piccola ](images/winenv-notification-image17.png)<br/>                 | Errore<br/>                 |
    | ![Screenshot dell'icona piccola disabilitata/disconnessa ](images/winenv-notification-image18.png)<br/> | Disabilitato/Disconnesso<br/> |
    | ![Screenshot dell'icona piccola bloccata/offline ](images/winenv-notification-image19.png)<br/>       | Bloccato/Offline<br/>       |

    

     

    ![Screenshot dell'area di notifica e di due icone ](images/winenv-notification-image20.png)

    In questo esempio, le icone wireless e della batteria mostrano modifiche in quantità o punti di forza.

    ![Screenshot dell'area di notifica e due sovrimpressione ](images/winenv-notification-image21.png)

    In questo esempio le sovrimpressione vengono usate per visualizzare gli stati di errore e avviso.

-   **Evitare swath di rosso puro, giallo e verde nelle icone di base.** Per evitare confusione, riservare questi colori per comunicare lo stato. Se la [personalizzazione usa questi](exper-branding.md) colori, è consigliabile usare toni disattivati per le icone dell'area di notifica di base.
-   Per [l'escalation progressiva,](mess-notif.md)usare icone con un aspetto progressivamente **più enfatico quando la situazione diventa più urgente.**

    ![Screenshot dell'area di notifica e cinque icone ](images/winenv-notification-image22.png)

    In questi esempi, l'aspetto dell'icona della batteria diventa più enfatico con l'aumentare dell'urgenza.

-   **Non modificare lo stato troppo frequentemente.** Le icone dell'area di notifica non devono apparire rumorose, instabili o richiedere attenzione. L'occhio è sensibile ai cambiamenti nel campo periferico della vista, quindi le modifiche dello stato devono essere meno sensibili.
    -   **Non modificare rapidamente l'icona.** Se lo stato sottostante cambia rapidamente, fare in modo che l'icona rifletta lo stato di alto livello.

        **Non corretto:**

        ![Screenshot dell'area di notifica e dell'icona del modem ](images/winenv-notification-image23.png)

        In questo esempio, l'icona del modem visualizza luci lampeggianti (come un modem hardware), ma tali modifiche di stato non sono significative per gli utenti.

    -   **Non usare animazioni a esecuzione continua per visualizzare le attività continue.** Tali animazioni sono una distrazione. La presenza di un'icona nell'area di notifica indica sufficientemente l'attività continua.
    -   **Brevi animazioni leggere sono accettabili per mostrare lo stato di avanzamento durante importanti modifiche temporanee dello stato transitivo.**

        ![Screenshot dell'area di notifica e dell'icona wireless ](images/winenv-notification-image24.png)

        In questo esempio, l'icona Wireless visualizza un indicatore di attività per mostrare che il lavoro è in corso.

    -   **Non lampeggiare l'icona.** Questa operazione è troppo distrazione. Se un evento richiede attenzione immediata, usare invece una finestra di dialogo. Se l'evento richiede attenzione, usare una notifica.

-   **Non disabilitare le icone dell'area di notifica.** Se l'icona non è attualmente applicabile, rimuoverla. Tuttavia, è possibile visualizzare un'icona abilitata con una sovrimpressione di stato disabilitata se gli utenti possono abilitarla dall'icona.

    ![Screenshot dell'area di notifica e del dispositivo di scorrimento del volume ](images/winenv-notification-image25.png)

    In questo esempio gli utenti possono abilitare l'output audio dall'icona.

Per linee guida ed esempi generali sulle icone, vedere [Icone.](vis-icons.md)

### <a name="interaction"></a>Interazione

**Nota:** Gli eventi Click seguenti devono verificarsi al passaggio del mouse verso l'alto, non verso il basso.

**Passaggio del mouse**

-   **Visualizzare una descrizione comando o una descrizione comando che indica ciò che l'icona rappresenta.**

    ![Screenshot dell'area di notifica e della descrizione comando ](images/winenv-notification-image26.png)

    In questo esempio viene usata una descrizione comando per descrivere l'icona al passaggio del mouse.

Per linee guida sul testo della descrizione comando, vedere [la sezione](#context-menus) Testo di questo articolo.

**Clic singolo a sinistra**

-   **Visualizzare tutti gli utenti che probabilmente vogliono visualizzare**, che potrebbe essere:

    -   Una finestra a comparsa, una finestra di dialogo o una finestra di programma con le impostazioni più utili e le attività eseguite comunemente. Per le linee guida per la presentazione, vedere [Riquadri a comparsa dell'area di notifica.](#notification-area-flyouts)

        ![Screenshot dell'area di notifica e dei riquadri a comparsa ](images/winenv-notification-image27.png)

        In questi esempi, facendo clic a sinistra vengono visualizzate finestre popup con le impostazioni più utili.

    -   Riquadro a comparsa di stato.

        ![Screenshot dell'area di notifica e del riquadro a comparsa dello stato ](images/winenv-notification-image28.png)

        In questo esempio, facendo clic a sinistra viene visualizzato il riquadro a comparsa dello stato.

        -   Elemento del Pannello di controllo correlato.
        -   Menu di scelta rapida.

    Gli utenti si aspettano che vengano visualizzati elementi con un solo clic, quindi se non vengono visualizzati elementi, l'icona dell'area di notifica non risponde.

-   **Visualizzare un menu di scelta rapida solo se le altre scelte non si** applicano a , con il comando predefinito in grassetto. In questo caso, visualizzare lo stesso menu di scelta rapida visualizzato quando si fa clic con il pulsante destro del mouse per evitare confusione.
-   **Preferisce usare una finestra popup rispetto a una finestra di dialogo** per un aspetto più leggero. Mostrare solo le impostazioni più comuni e fare in modo che abbia effetto immediato per un'interazione più semplice. Chiudere la finestra popup se l'utente fa clic in un punto qualsiasi all'esterno della finestra.
-   **Visualizzare finestre piccole accanto all'icona associata.** Tuttavia, le finestre di grandi dimensioni, ad esempio gli elementi del Pannello di controllo, possono essere visualizzate al centro del monitor predefinito.

**Doppio clic a sinistra**

-   **Eseguire il comando predefinito nel menu di scelta rapida.** In genere, viene visualizzata l'interfaccia utente principale associata all'icona, ad esempio l'elemento del Pannello di controllo, la finestra delle proprietà o la finestra del programma associata.
-   **Se non è presente alcun comando predefinito, eseguire la stessa azione di un singolo clic a sinistra.**

**Fare clic con il pulsante destro del mouse su**

-   **Visualizzare il menu di scelta** rapida , con il comando predefinito in grassetto.

### <a name="context-menus"></a>Menu di scelta rapida

-   **Visualizzare il menu di scelta rapida accanto all'icona associata,** ma lontano dalla barra delle applicazioni.
-   **Il menu di scelta rapida può includere le voci seguenti,** in base alle esigenze, nell'ordine elencato (il testo esatto è racchiuso tra virgolette):

Comandi principali

Apri (impostazione predefinita, elenco per primo, in grassetto)

Esegui

Comandi secondari

< separatore>

Comando Suspend/resume enable/disable (segno di spunta)

"Ridotta a icona nell'area di notifica" (segno di spunta)

Acconsentire esplicitamente alle notifiche (segno di spunta)

"Icona di visualizzazione nell'area di notifica" (segno di spunta)

< separatore>

"Opzioni"

"Exit"

-   **Rimuovere invece di disabilitare le voci del menu di scelta rapida che non sono applicabili.**
-   Per i comandi Apri, Esegui e Sospendi/Riprendi, è necessario essere specifici di ciò che viene **aperto, eseguito,** sospeso e ripreso.

![Screenshot che mostra un'area di notifica e i comandi.](images/winenv-notification-image29.png)

In questo esempio, Windows Defender i comandi Open ed Run specifici.

-   **Usare Suspend/Resume running background tasks (Sospendi/Riprendi attività in background in esecuzione), Enable/Disable (Abilita/Disabilita) per tutti gli altri elementi.**
-   **Usare i segni di spunta per indicare lo stato.** Elencare e abilitare tutti gli stati e inserire il segno di spunta accanto allo stato corrente. Non disabilitare le opzioni o modificare le etichette delle opzioni per indicare lo stato corrente.

**Corretto:**

![Screenshot di un comando con un segno di spunta ](images/winenv-notification-image29.png)

**Non corretto:**

![Screenshot di un comando senza segno di spunta ](images/winenv-notification-image30.png)

Nell'esempio non corretto, Windows Defender deve usare un segno di spunta per indicare lo stato corrente.

-   **Tutte le attività in background devono avere un comando Suspend/Resume.** La scelta del comando dovrebbe sospendere temporaneamente l'attività. Gli utenti potrebbero voler sospendere temporaneamente le attività in background per migliorare le prestazioni del sistema o ridurre il consumo di energia. Le attività in background sospese vengono riavviate quando viene ripreso dall'utente o quando Windows viene riavviato.
-   **Consentire agli utenti di acconsentire esplicitamente o** meno a tipi di notifica diversi se il programma ha notifiche che alcuni utenti potrebbero non voler visualizzare. Il [modello di notifica FYI](mess-notif.md) richiede agli utenti di acconsentire esplicitamente, quindi queste notifiche devono essere disabilitate per impostazione predefinita.

![Screenshot dell'area di notifica e dei comandi ](images/winenv-notification-image31.png)

In questo esempio, Outlook agli utenti di scegliere le notifiche ricevute dall'icona.

-   **Se si deseleziona l'opzione "Icona** di visualizzazione nell'area di notifica", l'icona viene rimossa dall'area di notifica, ma non influisce sul programma, sulla funzionalità o sul processo sottostante. Gli utenti possono visualizzare nuovamente l'icona dalla finestra di dialogo Opzioni del programma. Non visualizzare nuovamente automaticamente l'icona quando Windows viene riavviato.
-   **Il comando Esci chiude il programma per la sessione Windows corrente e rimuove l'icona.** Se non è possibile arrestare il programma, non è necessario un comando Exit. Il programma viene riavviato quando Windows viene riavviato. Gli utenti possono chiudere definitivamente il programma dalla finestra di dialogo Opzioni .
-   **Non è necessario un comando Informazioni su.** Tali informazioni devono essere comunicate tramite l'icona, la descrizione comandi e il menu di scelta rapida. Se gli utenti vogliono altre informazioni, possono visualizzare l'interfaccia utente primaria.
    -   **Eccezione:** È possibile specificare un comando Informazioni su se l'icona è relativa a un programma che non ha la presenza del desktop.

Per linee guida generali ed esempi relativi ai menu di scelta rapida, vedere [Menu.](cmd-menus.md)

### <a name="rich-tooltips"></a>Descrizioni comando rtf

-   **Usare descrizioni comando dettagliate solo per semplificare la comprensione delle informazioni.** Non usare descrizioni comando rtf solo per decorare la funzionalità. Se non è possibile usare le funzionalità dettagliate per semplificare la comprensione delle informazioni, usare invece una semplice descrizione comando.

    **Non corretto:**

    ![Screenshot dell'area di notifica e della descrizione comando rtf ](images/winenv-notification-image32.png)

    **Corretto:**

    ![Screenshot dell'area di notifica e della descrizione comando normale ](images/winenv-notification-image33.png)

    Nell'esempio non corretto, l'icona del calendario non semplifica la comprensione della data.

-   **Usare una presentazione concisa.** Usare testo conciso e un layout conciso con un'icona da 32x32 pixel. Le descrizioni comando sconsate rischiano di distrarre, soprattutto quando vengono visualizzate involontariamente.
-   **Non inserire controlli o elementi che appaiono interattivi in una descrizione comando rtf.** Le descrizioni comando non sono interattive e pertanto non devono essere visualizzate in modo interattivo. Non usare testo blu o sottolineato.

    **Corretto:**

    ![Screenshot della descrizione comando rtf con testo nero ](images/winenv-notification-image34.png)

    **Non corretto:**

    ![Screenshot della descrizione comando rtf con testo blu ](images/winenv-notification-image35.png)

    Nell'esempio errato la combinazione per il risparmio di energia corrente sembra essere un collegamento, ma non è possibile fare clic su .

### <a name="notification-area-flyouts"></a>Riquadri a comparsa dell'area di notifica

-   Quando appropriato, presentare riquadri a comparsa dell'area di notifica con tre sezioni:
    -   **Riepilogo.** Visualizzare le stesse informazioni visualizzate nella descrizione comando o nella descrizione comando dell'icona, possibilmente con maggiori dettagli. Per coerenza, usare lo stesso testo e le stesse icone e in genere lo stesso layout (se si usa una descrizione comando rtf). A differenza delle descrizioni comandi, queste informazioni sono accessibili quando si usa il tocco.
    -   **Attività comuni.** Presentare le attività più comunemente eseguite direttamente nel riquadro a comparsa.
    -   **Collegamenti correlati.** Specificare al massimo uno dei tipi di collegamenti facoltativi seguenti:
        -   Collegamento all'attività eseguita più di frequente in Pannello di controllo. Specificare se è presente un'attività eseguita di frequente che non può essere presentata nella sezione attività comuni.
        -   Collegamento all'elemento Pannello di controllo correlato. Questo Pannello di controllo elemento deve consentire agli utenti di eseguire qualsiasi attività che non può essere eseguita nella sezione attività comuni.
        -   Collegamento a un argomento della Guida specifico e pertinente. Seguire le linee guida standard [per il collegamento alla Guida.](winenv-help.md)

![Screenshot dell'area di notifica e del riquadro a comparsa ](images/winenv-notification-image36.png)

Questo esempio mostra un riquadro a comparsa dell'area di notifica usando la presentazione consigliata.

### <a name="options-dialog-box"></a>Opzioni (finestra di dialogo)

-   Le opzioni non accessibili direttamente dal menu di scelta rapida devono essere disponibili nella finestra di dialogo Opzioni . Questa finestra di dialogo potrebbe essere il pannello di controllo della funzionalità.
-   **La finestra di dialogo Opzioni può includere gli elementi seguenti** in base alle esigenze (il testo esatto è racchiuso tra virgolette):
    -   Abilita \[ nome funzionalità \] (casella di controllo)
        -   Se si deseleziona questa opzione, il programma viene chiuso definitivamente. Il programma può essere riavviato dall'elemento del Pannello di controllo. Il comando Esci del menu di scelta rapida chiude il programma solo per la sessione Windows corrente.
    -   "Icona di visualizzazione nell'area di notifica" (casella di controllo)
        -   La rimozione dell'icona dall'area di notifica non influisce sulla funzionalità sottostante.
        -   La selezione di questa opzione consente all'utente di ripristinare l'icona, che naturalmente non può essere eseguita dall'icona stessa.
-   Disabilitare le funzionalità usate raramente o potenzialmente fastidiose o distrazioni. Consentire agli [utenti di acconsentire](glossary.md) esplicitamente a tali funzionalità.

Per esempi e linee guida generali per la finestra di dialogo [Opzioni,](win-property-win.md)vedere Proprietà Windows .

### <a name="minimizing-programs-to-the-notification-area"></a>Riduzione al minimo dei programmi nell'area di notifica

**Nota: la riduzione al minimo delle finestre del programma nell'area di notifica non è più consigliata per Windows 7.** Usare invece i normali [pulsanti della](winenv-taskbar.md) barra delle applicazioni. Il programma può supportare entrambi i meccanismi per la compatibilità con le versioni precedenti.

-   Per ridurre il disordine della barra delle applicazioni, valutare la possibilità di ridurre al minimo i programmi nell'area di notifica solo se si verificano tutte le condizioni seguenti:
    -   Il programma può avere una sola istanza.
    -   Il programma viene eseguito per un lungo periodo di tempo.
    -   L'icona mostra lo stato.
    -   L'icona può essere un'origine di notifica.
    -   Questa operazione è facoltativa e gli utenti devono [acconsentire esplicitamente a](glossary.md).
-   Usare il pulsante Riduci a icona sulla barra del titolo dell'applicazione, non il pulsante Chiudi.

## <a name="text"></a>Testo

### <a name="infotips"></a>Descrizioni comandi

-   La descrizione comandi dell'icona deve avere uno dei formati seguenti (dove il nome della società è facoltativo):
    -   (Nome società) Nome della funzionalità, del programma o del dispositivo
    -   ![Screenshot della descrizione comando con il nome della società ](images/winenv-notification-image37.png)
    -   (Nome società) Nome della funzionalità, del programma o del dispositivo - Riepilogo dello stato
    -   ![Screenshot della descrizione comando che visualizza il riepilogo dello stato ](images/winenv-notification-image38.png)
    -   (Nome società) Dichiarazione di stato del nome di funzionalità, programma o dispositivo.
    -   ![Screenshot della descrizione comandi che visualizza l'istruzione di stato ](images/winenv-notification-image39.png)
    -   (Nome società) Nome della funzionalità, del programma o del dispositivo
    -   Elenco di stato con ogni elemento in una riga separata
    -   ![Screenshot della descrizione comando che visualizza l'elenco di stato ](images/winenv-notification-image40.png)

Formulazione infotip:

-   Concentrarsi sulle informazioni più utili. Visualizzare altre informazioni al clic con il pulsante sinistro del mouse.
-   Essere concisi. Usare frammenti di frase o istruzioni semplici.
-   Non usare la punteggiatura finale a meno che la mancia non venga formulata come frase completa.
-   Omettere le parole non necessarie. Non includere la versione del software o altre informazioni estranee.

    **Non corretto:**

    ![Screenshot della descrizione comando con informazioni non necessarie ](images/winenv-notification-image41.png)

    In questo esempio la descrizione comandi contiene informazioni estranee.

-   Non spiegare come interagire con l'icona.

    **Non corretto:**

    ![Screenshot della descrizione comando con le istruzioni di clic con il pulsante destro del mouse ](images/winenv-notification-image42.png)

    In questo esempio, l'icona Connessione di rete wireless fornisce istruzioni per il clic con il pulsante destro del mouse.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento all'area di notifica:

-   Fare riferimento all'area di notifica come area di notifica, non come area di notifica.

Quando si fa riferimento a un'icona dell'area di notifica:

-   Fare riferimento all'icona usando il nome esatto specificato nella descrizione comandi, inclusa l'uso di maiuscole e minuscole, seguito dall'icona .
-   Per il primo riferimento, fare riferimento anche all'area di notifica.
-   Quando possibile, formattare il testo dell'intestazione in grassetto. In caso contrario, inserire l'intestazione tra virgolette solo se necessario per evitare confusione.

**Esempio:** Per controllare rapidamente lo stato della rete, fare clic **sull'icona** Rete nell'area di notifica.

 

