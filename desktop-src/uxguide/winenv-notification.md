---
title: Area di notifica
description: L'area di notifica fornisce notifiche e stato. I programmi ben progettati usano l'area di notifica in modo appropriato, senza irritare o distrazione.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0293038dd155f12b96b22dd1c273a50f1c030ffa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968834"
---
# <a name="notification-area"></a>Area di notifica

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

L'area di notifica fornisce notifiche e stato. I programmi ben progettati usano l'area di notifica in modo appropriato, senza irritare o distrazione.

L'area di notifica è una parte della barra delle applicazioni che fornisce un'origine temporanea per le notifiche e lo stato. Può anche essere usato per visualizzare le icone per le funzionalità di sistema e di programma che non hanno presenza sul desktop.

Gli elementi nell'area di notifica sono detti icone dell'area di notifica o semplicemente icone se il contesto dell'area di notifica è già definito in modo chiaro.

![screenshot dell'area di notifica, dell'ora e della data ](images/winenv-notification-image1.png)

Area di notifica.

Per consentire agli utenti di controllare il desktop in Windows 7, non tutte le icone dell'area di notifica vengono visualizzate per impostazione predefinita. Al contrario, le icone vengono visualizzate nell'overflow dell'area di notifica, a meno che l'utente non sia stato promosso all'area di notifica.

![Screenshot che mostra un'area di notifica e un overflow.](images/winenv-notification-image2.png)

Overflow dell'area di notifica.

**Nota:** Le linee guida relative alla [barra delle applicazioni](winenv-taskbar.md), alle [notifiche](mess-notif.md) e ai [palloni](ctrl-balloons.md) vengono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **È necessario che il programma visualizzi una notifica?** In tal caso, è necessario utilizzare un'icona dell'area di notifica.
-   **L'icona viene visualizzata temporaneamente per visualizzare una modifica dello stato?** In tal caso, è possibile che sia appropriata un'icona dell'area di notifica, a seconda dei fattori seguenti:

    -   **Lo stato è utile e pertinente?** Ovvero, è probabile che gli utenti monitorino l'icona e ne modifichino il comportamento in seguito a queste informazioni? In caso contrario, non visualizzare lo stato o inserirlo in un file di log.

        **Non corretto:**

        ![screenshot dell'area di notifica con icona dell'unità ](images/winenv-notification-image3.png)

        In questo esempio, l'icona di attività dell'unità disco non è appropriata perché gli utenti non possono modificare il proprio comportamento in base a tale icona.

    -   **Lo stato è critico? È richiesta un'azione immediata?** In tal caso, visualizzare le informazioni in un modo che richiede attenzione e che non possono essere facilmente ignorate, ad esempio una finestra di [dialogo](win-dialog-box.md).

    I programmi progettati per Windows 7 possono usare icone sovrapposte sul pulsante della barra delle applicazioni del programma per visualizzare la modifica dello stato, nonché le barre di stato del pulsante della barra delle applicazioni per mostrare lo stato di avanzamento delle attività a esecuzione prolungata.

-   **Per la funzionalità è già presente "desktop Presence"?** Ovvero, quando viene eseguito, la funzionalità viene visualizzata in una finestra sul desktop (probabilmente ridotta a icona)? In tal caso, visualizzare lo stato nella [barra di stato](ctrl-status-bars.md)del programma, in un'altra area dello stato oppure, per Windows 7, direttamente sul pulsante della barra delle applicazioni. Se la funzionalità non ha una presenza sul desktop, è possibile usare un'icona per l'accesso al programma e per visualizzare lo stato.
-   **L'icona viene utilizzata principalmente per avviare un programma o accedere rapidamente alle relative funzionalità o impostazioni?** In tal caso, utilizzare il menu Start per avviare i programmi. L'area di notifica non è destinata all'accesso rapido a programmi o comandi.

    ![screenshot della barra degli strumenti Avvio veloce ](images/winenv-notification-image4.png)

    In questo esempio di Windows Vista, avvio veloce viene utilizzato per avviare rapidamente Windows Explorer e Windows Internet Explorer.

    Per i programmi progettati per Windows 7, gli utenti possono aggiungere pulsanti della barra delle applicazioni per l'accesso rapido al programma. I programmi possono usare un Jump List o una barra degli strumenti dell'anteprima per accedere ai comandi usati di frequente direttamente dal pulsante della barra degli strumenti di un programma. L'area avvio veloce non viene visualizzata per impostazione predefinita in Windows 7.

    ![screenshot della barra delle applicazioni e della Jump List con icone ](images/winenv-notification-image5.png)

    In questo esempio viene usata una Jump List per l'accesso rapido ai comandi.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="the-windows-desktop"></a>Desktop di Windows

Il desktop di Windows presenta i seguenti punti di accesso al programma:

-   **Area di lavoro.** Area sullo schermo in cui gli utenti possono eseguire il proprio lavoro, oltre ad archiviare programmi, documenti e collegamenti. Sebbene tecnicamente il desktop includa la barra delle applicazioni, nella maggior parte dei contesti si riferisce solo all'area di lavoro.
-   **Pulsante Avvia.** Il punto di accesso per tutti i programmi e i luoghi speciali di Windows (documenti, immagini, musica, giochi, computer, pannello di controllo) con gli elenchi "usati di recente" per accedere rapidamente ai programmi e ai documenti usati di recente.
-   **Avvio veloce.** Un punto di accesso diretto per i programmi selezionati dall'utente. Avvio veloce rimosso da Windows 7.
-   **Barra delle applicazioni.** Il punto di accesso per l'esecuzione di programmi con presenza desktop. Sebbene tecnicamente la barra delle applicazioni si estenda sull'intera barra dal pulsante Start all'area di notifica, nella maggior parte dei contesti sulla barra delle applicazioni si fa riferimento all'area in cui è presente la barra delle applicazioni. Questa area viene a volte definita TaskBand.
-   **Deskbands. Non consigliato.**
-   **Area di notifica.** Un'origine a breve termine per le notifiche e lo stato, oltre a un punto di accesso per le funzionalità relative al sistema e al programma che non hanno alcuna presenza sul desktop.

![screenshot che identifica i punti di accesso desktop ](images/winenv-notification-image6.png)

I punti di accesso desktop di Windows includono il pulsante avvia, la barra delle applicazioni e l'area di notifica. Si noti la funzionalità di anteprima del pulsante della barra delle applicazioni.

**Il desktop è una risorsa condivisa limitata che rappresenta il punto di ingresso dell'utente per Windows.** Lascia gli utenti sotto controllo. È consigliabile usare le aree desktop come previsto. qualsiasi altro uso dovrebbe essere considerato un abuso. Ad esempio, non visualizzare mai le aree del desktop come modalità per promuovere il programma o il suo [marchio](exper-branding.md).

### <a name="using-the-notification-area-appropriately"></a>Utilizzo appropriato dell'area di notifica

L'area di notifica è stata originariamente progettata come origine temporanea per le notifiche e lo stato. L'efficienza e la praticità hanno incoraggiato gli sviluppatori a fornire altri scopi, ad esempio l'avvio di programmi e l'esecuzione di comandi. Sfortunatamente nel tempo, queste aggiunte hanno reso l'area di notifica troppo grande e rumorosa e hanno confuso lo scopo con gli altri punti di accesso desktop.

Windows XP ha risolto il problema di scalabilità rendendo l'area comprimibile e nascondendo le icone inutilizzate. Windows Vista ha risolto il rumore rimuovendo notifiche superflue e fastidiose. Windows 7 ha fatto un ulteriore passo avanti concentrando la notifica sullo scopo originale di essere un'origine di notifica. **La maggior parte delle icone è nascosta per impostazione predefinita in Windows 7, ma può essere promossa manualmente dall'utente nell'area di notifica. Per consentire agli utenti di controllare i desktop, non esiste alcun modo per consentire al programma di eseguire automaticamente questa promozione.** Windows Visualizza ancora le notifiche per le icone nascoste promuovendo temporaneamente.

![screenshot dell'area di notifica e dell'overflow ](images/winenv-notification-image7.png)

In Windows 7, la maggior parte delle icone dell'area di notifica è nascosta per impostazione predefinita.

Windows 7 supporta inoltre numerose funzionalità direttamente nei pulsanti della barra delle applicazioni. In particolare, è possibile usare:

-   Jump List e barre degli strumenti di anteprima per accedere rapidamente ai comandi usati di frequente.
-   Icone sovrapposte per visualizzare lo stato dei programmi in esecuzione.
-   Barre di stato del pulsante della barra delle applicazioni per mostrare lo stato delle attività con esecuzione prolungata.

In breve, se il programma ha una presenza sul desktop, sfruttare appieno le funzionalità dei pulsanti della barra delle applicazioni di Windows 7 per questi scopi. **Mantieni le icone dell'area di notifica incentrate sulla visualizzazione delle notifiche e dello stato.**

### <a name="keeping-users-in-control"></a>Controllo degli utenti

Il controllo degli utenti si estende oltre l'utilizzo corretto dell'area di notifica. A seconda della natura dell'icona, può essere utile consentire agli utenti di eseguire le operazioni seguenti:

-   **Rimuovere l'icona.** L'icona può fornire lo stato pertinente e utile, ma anche in questo caso gli utenti potrebbero non volerne visualizzarlo. Windows consente agli utenti di nascondere le icone, ma questa funzionalità non è facilmente individuabile. Per garantire agli utenti un controllo, specificare un' **icona di visualizzazione nell'area di notifica nel** menu di scelta rapida dell'icona. Si noti che la rimozione di un'icona non ha alcun effetto sul programma, la funzionalità o il processo sottostante.
-   **Consente di selezionare i tipi di notifiche da visualizzare.** La notifica deve essere utile e pertinente, ma è possibile che gli utenti non vogliano vedere le notifiche. Questo vale soprattutto per le [notifiche](mess-notif.md)FYI. Consentire agli utenti di scegliere di abilitare quelli meno importanti.
-   **Sospendere le funzionalità facoltative.** Le icone vengono usate per visualizzare lo stato delle funzionalità senza presenza sul desktop. Tali funzionalità tendono a eseguire attività in background con esecuzione prolungata e facoltative, quali stampa, indicizzazione, analisi o sincronizzazione. È possibile che gli utenti desiderino sospendere tali funzionalità per migliorare le prestazioni del sistema, ridurre il consumo di energia o perché sono offline.
-   **Uscire dal programma.** Fornire le opzioni più appropriate:
    -   **Uscire temporaneamente dal programma.** Il programma viene arrestato e riavviato al riavvio di Windows. Questo approccio è adatto per utilità di sistema importanti, ad esempio i programmi di sicurezza.
    -   **Chiusura definitiva del programma.** Il programma viene arrestato e non riavviato quando Windows viene riavviato (a meno che l'utente non scelga di riavviare successivamente). L'utente non vuole più eseguire il programma o vuole eseguire il programma su richiesta, ad esempio per migliorare le prestazioni del sistema.

Sebbene sia consigliabile fornire la maggior parte di queste impostazioni nel menu di scelta rapida dell'icona, l'esperienza predefinita del programma dovrebbe essere adatta per la maggior parte degli utenti. Non attivare tutti gli elementi per impostazione predefinita e si prevede che gli utenti disattivino le funzionalità. Per impostazione predefinita, attivare le funzionalità importanti e consentire agli utenti di abilitare le funzionalità aggiuntive desiderate.

**Se si eseguono solo quattro operazioni...**

1.  Non abusa dell'area di notifica. Utilizzarlo solo come origine per le notifiche e lo stato e per le funzionalità senza presenza desktop.
2.  Mantieni gli utenti sotto controllo. Fornire le opzioni appropriate per controllare l'icona, le relative notifiche e le funzionalità sottostanti.
3.  Presentare un'esperienza predefinita adatta per la maggior parte degli utenti. Consentire agli utenti di abilitare le funzionalità desiderate, anziché aspettarsi di disabilitare quelle indesiderate.
4.  Sfruttare al meglio le funzionalità dei pulsanti della barra delle applicazioni di Windows 7 per visualizzare lo stato e rendere efficienti le attività eseguite più di frequente dal programma.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le icone dell'area di notifica includono diversi modelli di utilizzo:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Stato del sistema e accesso</strong><br/> Visualizzato continuamente per visualizzare lo stato del sistema importante ma non critico e per fornire l'accesso alle funzionalità e alle impostazioni pertinenti. <br/></td>
<td>Le funzionalità di sistema che richiedono icone dell'area di notifica non hanno una presenza sul desktop permanente. Può essere usato anche come origine di notifica. <br/> <img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br/> In questo esempio, le icone della batteria, della rete e del volume vengono visualizzate continuamente quando applicabile.<br/></td>
</tr>
<tr class="even">
<td><strong>Stato e accesso attività in background</strong><br/> Visualizzato durante l'esecuzione di un'attività in background per visualizzare lo stato e fornire l'accesso alle funzionalità e alle impostazioni. <br/></td>
<td>I processi in background necessitano di icone dell'area di notifica quando non hanno una presenza sul desktop. Può essere usato anche come origine di notifica. <br/> <img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br/> In questo esempio, l'icona del centro operativo consente agli utenti di controllarne lo stato anche se non è presente alcun desktop.<br/></td>
</tr>
<tr class="odd">
<td><strong>Stato evento temporaneo</strong><br/> I programmi con presenza desktop possono visualizzare temporaneamente le icone per visualizzare eventi importanti o modifiche allo stato. <br/></td>
<td><img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br/> In questo esempio, le icone per la stampa e l'installazione degli aggiornamenti vengono visualizzate temporaneamente per visualizzare eventi importanti o modifiche nello stato.<br/></td>
</tr>
<tr class="even">
<td><strong>Origine notifica temporanea</strong><br/> Visualizzato temporaneamente per visualizzare una notifica. Rimosso dopo un timeout o quando il problema sottostante viene risolto o viene eseguita un'attività. <br/></td>
<td>Le icone temporanee sono preferite per le origini delle notifiche pure. Non visualizzare un'icona che non fornisca uno stato utile, pertinente e dinamico solo perché una funzionalità potrebbe dover visualizzare una notifica in futuro. <br/> <img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br/> In questo esempio viene visualizzata l'icona del plug-and-Play quando viene visualizzata una nuova notifica di hardware rilevata.<br/></td>
</tr>
<tr class="odd">
<td><strong>Applicazione a istanza singola ridotta a icona</strong><br/> Per ridurre il disordine della barra delle applicazioni, è possibile ridurre al minimo un'applicazione a istanza singola e a esecuzione prolungata a un'icona dell'area di notifica. <br/></td>
<td><img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br/> In questo esempio di Windows Vista, Outlook e Windows Live Messenger sono applicazioni a istanza singola che riducono al minimo le icone dell'area di notifica.<br/> Considerare l'uso di questo modello solo se si applicano tutte le condizioni seguenti: <br/>
<ul>
<li>L'applicazione può avere una sola istanza.</li>
<li>L'applicazione viene eseguita per un periodo di tempo prolungato.</li>
<li>L'icona Mostra lo stato.</li>
<li>L'icona può essere un'origine di notifica.</li>
<li>Questa operazione è facoltativa e gli utenti devono <a href="glossary.md">acconsentire esplicitamente</a>.</li>
</ul>
Se si applicano tutte le condizioni, la riduzione a icona di un'icona comporta l'eliminazione di due punti di accesso quando ne è necessario solo uno. <br/> <strong>Nota:</strong> Questo modello di icona non è più consigliato per Windows 7. Usare invece i pulsanti normali della barra delle applicazioni se il programma ha una presenza sul desktop.<br/> <img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br/> In questo esempio di Windows 7, un pulsante normale della barra delle applicazioni occupa spazio su disco, ma trae vantaggio dalle funzionalità del pulsante della barra delle applicazioni di Windows 7, tra cui Jump List, icone sovrapposte e anteprime avanzate.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Fornire solo un'icona dell'area di notifica per ogni componente.**
-   **Usare un'icona con le versioni 16x16, 20x20 e 24x24 pixel.** Le versioni più grandi vengono usate nelle modalità di visualizzazione a DPI elevato.

### <a name="when-to-show"></a>Quando visualizzare

-   Per il modello di origine della notifica temporanea:
    -   Windows Visualizza l'icona quando viene visualizzata la notifica.
    -   Rimuovere l'icona in base al modello di [progettazione della notifica](mess-notif.md) :



    | Modello                                     | Quando rimuovere                                         |
    |--------------------------------------|------------------------------------------|
    | Azione riuscita<br/>            | Quando la notifica viene rimossa.<br/> |
    | Errore azione<br/>            | Quando il problema viene risolto.<br/>     |
    | Evento di sistema non critico<br/> | Quando il problema viene risolto.<br/>     |
    | Attività utente facoltativa<br/>        | Al termine dell'attività.<br/>            |
    | FYI<br/>                       | Quando la notifica viene rimossa.<br/> |



 

-   **Per il modello di stato dell'evento temporaneo, visualizzare l'icona mentre è in corso l'evento.**
-   Per tutti gli altri modelli, **visualizzare l'icona quando il programma, la funzionalità o il processo è in esecuzione e l'icona è pertinente** , a meno che l'utente non abbia cancellato la relativa **icona di visualizzazione nell'area di notifica** (per altre informazioni, vedere [menu di scelta rapida](#context-menus)). La maggior parte delle icone è nascosta per impostazione predefinita in Windows 7, ma può essere innalzata di livello nell'area di notifica dall'utente.
-   **Non visualizzare le icone destinate agli amministratori agli utenti standard.** Registrare le informazioni nel registro eventi di Windows.

### <a name="where-to-show"></a>Dove visualizzare

-   **Visualizzare le finestre avviate dalle icone dell'area di notifica accanto all'area di notifica.**

![Figura di una finestra vicino all'area di notifica ](images/winenv-notification-image14.png)

Le finestre avviate dalle icone dell'area di notifica vengono visualizzate accanto all'area di notifica.

### <a name="icons"></a>Icone

-   **Scegliere l'icona in base al modello di progettazione:**

    | Modello                                                 | Tipo di icona                                   |
    |--------------------------------------------------|------------------------------------|
    | Stato del sistema e accesso<br/>              | Icona della funzionalità di sistema<br/>     |
    | Stato e accesso attività in background<br/>     | Icona del programma o della funzionalità<br/> |
    | Origine notifica temporanea<br/>         | Icona del programma o della funzionalità<br/> |
    | Stato evento temporaneo<br/>                | Icona del programma o della funzionalità<br/> |
    | Applicazione a istanza singola ridotta a icona<br/> | Icona del programma<br/>            |

    

     

    ![screenshot dell'area di notifica e delle icone di Outlook ](images/winenv-notification-image15.png)

    In questo esempio, Outlook usa un'icona della funzionalità di posta elettronica per un'origine di notifica temporanea e la relativa icona dell'applicazione per l'applicazione ridotta a icona.

-   **Scegliere una progettazione di icone facilmente riconoscibile.** Preferisce icone con strutture univoche su icone quadrate o rettangolari. Mantieni i progetti semplici che preferiscono i simboli sulle immagini realistiche. Applicare anche le altre [linee guida sulle icone di tipo Aero](vis-icons.md) .
-   **Usare le variazioni delle icone o le sovrapposizioni per indicare le modifiche dello stato o dello stato.** Usare le variazioni delle icone per visualizzare le modifiche apportate a quantità o punti di forza. Per altri tipi di stato, usare le sovrimpressioni standard seguenti. Usare una sola sovrapposizione e individuarla in basso a destra per coerenza. 

    | Sovrapposizione (Overlay)                                                                                                       | Stato                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![screenshot dell'icona di avviso piccola ](images/winenv-notification-image16.png)<br/>               | Avviso<br/>               |
    | ![screenshot dell'icona di errore piccolo ](images/winenv-notification-image17.png)<br/>                 | Errore<br/>                 |
    | ![screenshot della piccola icona disabilitata/disconnessa ](images/winenv-notification-image18.png)<br/> | Disabilitato/disconnesso<br/> |
    | ![screenshot dell'icona Small blocked/offline ](images/winenv-notification-image19.png)<br/>       | Bloccato/offline<br/>       |

    

     

    ![screenshot dell'area di notifica e due icone ](images/winenv-notification-image20.png)

    In questo esempio, le icone wireless e batteria mostrano le modifiche apportate a quantità o punti di forza.

    ![screenshot dell'area di notifica e due sovrimpressioni ](images/winenv-notification-image21.png)

    In questo esempio, le sovrimpressioni vengono usate per visualizzare gli Stati di errore e di avviso.

-   **Evitare le porzioni di colore rosso, giallo e verde puri nelle icone di base.** Per evitare confusione, riservare questi colori per comunicare lo stato. Se la [personalizzazione](exper-branding.md) usa questi colori, provare a usare i toni silenziati per le icone dell'area di notifica di base.
-   Per l' [escalation progressiva](mess-notif.md), **usare icone con un aspetto progressivamente più enfatico, perché la situazione diventa più urgente.**

    ![screenshot dell'area di notifica e cinque icone ](images/winenv-notification-image22.png)

    In questi esempi, l'aspetto dell'icona della batteria diventa più enfatico Man mano che aumenta l'urgenza.

-   **Non modificare lo stato troppo spesso.** Le icone dell'area di notifica non devono essere rumorose, instabili o richiedere attenzione. L'occhio è sensibile alle modifiche apportate al campo periferico della visione, quindi le modifiche di stato devono essere minime.
    -   **Non modificare rapidamente l'icona.** Se lo stato sottostante sta cambiando rapidamente, fare in modo che l'icona rifletta lo stato di alto livello.

        **Non corretto:**

        ![screenshot dell'area di notifica e dell'icona del modem ](images/winenv-notification-image23.png)

        In questo esempio, l'icona del modem Visualizza le spie lampeggianti (come avviene in un modem hardware), ma tali modifiche di stato non sono significative per gli utenti.

    -   **Non usare animazioni con esecuzione prolungata per mostrare le attività continue.** Queste animazioni sono una distrazione. La presenza di un'icona nell'area di notifica indica sufficientemente l'attività continua.
    -   **Brevi animazioni minime sono accettabili per mostrare lo stato di avanzamento durante importanti modifiche temporanee di stato transitive.**

        ![screenshot dell'area di notifica e dell'icona wireless ](images/winenv-notification-image24.png)

        In questo esempio, l'icona wireless Visualizza un indicatore di attività per indicare che il lavoro è in corso.

    -   **Non lampeggiare l'icona.** Questa operazione è troppo distrazione. Se per un evento è richiesta l'attenzione immediata, utilizzare invece una finestra di dialogo. Se l'evento altrimenti richiede attenzione, utilizzare una notifica.

-   **Non disabilitare le icone dell'area di notifica.** Se l'icona non è attualmente applicabile, rimuoverla. Tuttavia, è possibile visualizzare un'icona abilitata con una sovrapposizione di stato disabilitata se gli utenti possono abilitare dall'icona.

    ![screenshot dell'area di notifica e del dispositivo di scorrimento del volume ](images/winenv-notification-image25.png)

    In questo esempio, gli utenti possono abilitare l'output audio dall'icona.

Per le linee guida e gli esempi dell'icona generale, vedere [Icone](vis-icons.md).

### <a name="interaction"></a>Interazione

**Nota:** Gli eventi Click seguenti dovrebbero verificarsi al passaggio del mouse, non al passaggio del mouse.

**Passaggio del mouse**

-   **Visualizza una descrizione comando o infotip che indica l'icona rappresentata dall'icona.**

    ![screenshot dell'area di notifica e della descrizione comando ](images/winenv-notification-image26.png)

    In questo esempio viene usata una descrizione comando per descrivere l'icona al passaggio del mouse.

Per le linee guida del testo infotip, vedere la sezione [testo](#context-menus) di questo articolo.

**A sinistra con un solo clic**

-   **Visualizza gli utenti che più probabilmente vogliono visualizzare**, che può essere:

    -   Una finestra a comparsa, una finestra di dialogo o una finestra del programma con le impostazioni più utili e le attività comunemente eseguite. Per le linee guida di presentazione, vedere [area di notifica riquadri a comparsa](#notification-area-flyouts).

        ![screenshot dell'area di notifica e riquadri a comparsa ](images/winenv-notification-image27.png)

        In questi esempi, facendo clic su vengono visualizzate le finestre popup con le impostazioni più utili.

    -   Riquadro A comparsa dello stato.

        ![screenshot dell'area di notifica e del riquadro a comparsa dello stato ](images/winenv-notification-image28.png)

        In questo esempio, facendo clic su viene visualizzato il riquadro a comparsa stato.

        -   Elemento del pannello di controllo correlato.
        -   Menu di scelta rapida.

    Gli utenti si aspettano che vengano visualizzati solo i clic con il pulsante destro del mouse per visualizzare un elemento, quindi non viene visualizzata alcuna icona.

-   **Visualizzare un menu di scelta rapida solo se non si applicano le altre opzioni**, con il comando predefinito in grassetto. In questo caso, visualizzare lo stesso menu di scelta rapida visualizzato facendo clic con il pulsante destro del mouse per evitare confusione.
-   **Preferisci usare una finestra popup su una** finestra di dialogo per un aspetto più leggero. Mostra solo le impostazioni più comuni e le rende immediatamente effettive per un'interazione più semplice. Chiudere la finestra popup se l'utente fa clic in un punto qualsiasi all'esterno della finestra.
-   **Visualizzare le finestre piccole accanto all'icona associata.** Tuttavia, le finestre di grandi dimensioni, ad esempio gli elementi del pannello di controllo, possono essere visualizzate al centro del monitor predefinito.

**Doppio clic con pulsante sinistro**

-   **Eseguire il comando predefinito dal menu di scelta rapida.** In genere, viene visualizzata l'interfaccia utente primaria associata all'icona, ad esempio l'elemento del pannello di controllo associato, la finestra delle proprietà o la finestra del programma.
-   **Se non è presente alcun comando predefinito, eseguire la stessa azione di un singolo clic a sinistra.**

**Fare clic con il pulsante destro del mouse su**

-   **Visualizzare il menu di scelta rapida** con il comando predefinito in grassetto.

### <a name="context-menus"></a>Menu di scelta rapida

-   **Visualizzare il menu di scelta rapida accanto all'icona associata**, ma lontano dalla barra delle applicazioni.
-   **Il menu di scelta rapida può includere gli elementi seguenti**, a seconda delle esigenze, nell'ordine elencato (il testo esatto è racchiuso tra virgolette):

Comandi primari

Apri (impostazione predefinita, elenco per primo, in grassetto)

Esegui

Comandi secondari

Separatore <>

Sospendi/Riprendi comando Abilita/Disabilita (segno di spunta)

"Ridotta a icona nell'area di notifica" (segno di spunta)

Acconsenti esplicitamente alle notifiche (segno di spunta)

"Icona di visualizzazione nell'area di notifica" (segno di spunta)

Separatore <>

Opzioni

Uscita

-   **Rimuovere anziché disabilitare le voci del menu di scelta rapida che non si applicano.**
-   Per i comandi Apri, Esegui e Sospendi/Riprendi, è **necessario specificare gli elementi aperti, eseguiti, sospesi e ripresi.**

![Screenshot che mostra un'area di notifica e i comandi.](images/winenv-notification-image29.png)

In questo esempio, Windows Defender dispone di comandi di apertura ed esecuzione specifici.

-   **Usare Sospendi/Riprendi esecuzione di attività in background, Abilita/Disabilita per tutti gli altri.**
-   **Usare segni di spunta per indicare lo stato.** Elencare e abilitare tutti gli Stati e posizionare il segno di spunta accanto allo stato corrente. Non disabilitare le opzioni o modificare le etichette delle opzioni per indicare lo stato corrente.

**Corretto:**

![Screenshot di un comando con segno di spunta ](images/winenv-notification-image29.png)

**Non corretto:**

![Screenshot di un comando senza segno di spunta ](images/winenv-notification-image30.png)

Nell'esempio errato, Windows Defender deve utilizzare un segno di spunta per indicare lo stato corrente.

-   **Tutte le attività in background devono disporre di un comando Suspend/Resume.** La scelta del comando deve sospendere temporaneamente l'attività. Gli utenti potrebbero voler sospendere temporaneamente le attività in background per aumentare le prestazioni del sistema o ridurre il consumo di energia. Le attività in background sospese vengono riavviate quando riprendete dall'utente o quando Windows viene riavviato.
-   **Consente agli utenti di acconsentire o rifiutare esplicitamente i diversi tipi di notifica** se il programma dispone di notifiche che alcuni utenti potrebbero non voler visualizzare. Il modello di notifica [FYI](mess-notif.md) richiede agli utenti di acconsentire esplicitamente, quindi queste notifiche devono essere disabilitate per impostazione predefinita.

![screenshot dell'area di notifica e dei comandi ](images/winenv-notification-image31.png)

In questo esempio Outlook consente agli utenti di scegliere le notifiche ricevute dall'icona.

-   **Deselezionando l'opzione "Visualizza icona nell'area di notifica", l'icona viene rimossa dall'area di notifica**, ma non influisce sul programma, la funzionalità o il processo sottostante. Gli utenti possono visualizzare nuovamente l'icona dalla finestra di dialogo Opzioni del programma. Non visualizzare automaticamente di nuovo l'icona quando Windows viene riavviato.
-   **Il comando Exit chiude il programma per la sessione di Windows corrente e rimuove l'icona.** Non è disponibile un comando exit se non è possibile arrestare il programma. Il programma viene riavviato al riavvio di Windows. Gli utenti possono uscire definitivamente dal programma dalla finestra di dialogo Opzioni.
-   **Non si dispone di un comando about.** Tali informazioni devono essere comunicate tramite l'icona, il relativo infotip e il menu di scelta rapida. Se gli utenti desiderano ulteriori informazioni, possono visualizzare l'interfaccia utente primaria.
    -   **Eccezione:** Se l'icona è per un programma che non dispone di una presenza sul desktop, è possibile fornire un comando about.

Per le linee guida e gli esempi generali del menu di scelta rapida, vedere [menu](cmd-menus.md).

### <a name="rich-tooltips"></a>Descrizioni comandi avanzate

-   **Utilizzare descrizioni comandi avanzate solo per semplificare la comprensione delle informazioni.** Non usare descrizioni comandi avanzate solo per decorare la funzionalità. Se non è possibile usare la ricchezza per semplificare la comprensione delle informazioni, usare invece una descrizione comando normale.

    **Non corretto:**

    ![screenshot dell'area di notifica e della descrizione comando avanzata ](images/winenv-notification-image32.png)

    **Corretto:**

    ![screenshot dell'area di notifica e della descrizione comando normale ](images/winenv-notification-image33.png)

    Nell'esempio errato, l'icona del calendario non semplifica la comprensione della data.

-   **Usare una presentazione concisa.** Usare testo conciso e un layout conciso con un'icona a forma di pixel 32x32. Le descrizioni comandi spaziose rischiano la distrazione, soprattutto quando vengono visualizzate involontariamente.
-   **Non inserire controlli o elementi che appaiono interattivi in una descrizione comando avanzata.** Le descrizioni comandi non sono interattive e pertanto non dovrebbero apparire interattive. Non usare il testo blu o sottolineato.

    **Corretto:**

    ![screenshot della descrizione comando avanzata con testo nero ](images/winenv-notification-image34.png)

    **Non corretto:**

    ![screenshot della descrizione comando avanzata con testo blu ](images/winenv-notification-image35.png)

    Nell'esempio errato, la combinazione per il risparmio di energia corrente sembra essere un collegamento, ma non è possibile fare clic su.

### <a name="notification-area-flyouts"></a>Area di notifica riquadri a comparsa

-   Quando appropriato, presentare l'area di notifica riquadri a comparsa con tre sezioni:
    -   **Riepilogo.** Visualizzare le stesse informazioni visualizzate nella descrizione comando dell'icona o infotip, possibilmente con maggiori dettagli. Per coerenza, usare lo stesso testo e le stesse icone e, in genere, lo stesso layout (se si usa una descrizione comando avanzata). A differenza di infotip, queste informazioni sono accessibili quando si usa il tocco.
    -   **Attività comuni.** Presentare le attività eseguite più di frequente direttamente nel riquadro a comparsa.
    -   **Collegamenti correlati.** Fornire al massimo uno dei tipi di collegamenti facoltativi seguenti:
        -   Un collegamento all'attività eseguita più di frequente nel pannello di controllo. Specificare se è presente un'attività eseguita di frequente che non può essere presentata nella sezione attività comuni.
        -   Collegamento all'elemento del pannello di controllo correlato. Questo elemento del pannello di controllo deve consentire agli utenti di eseguire qualsiasi attività che non può essere eseguita nella sezione attività comuni.
        -   Collegamento a un argomento della Guida specifico e pertinente. Seguire le [linee guida](winenv-help.md)per il collegamento alla guida standard.

![screenshot dell'area di notifica e del riquadro a comparsa ](images/winenv-notification-image36.png)

Questo esempio mostra un riquadro a comparsa dell'area di notifica usando la presentazione consigliata.

### <a name="options-dialog-box"></a>Opzioni (finestra di dialogo)

-   Le opzioni non accessibili direttamente dal menu di scelta rapida devono trovarsi nella finestra di dialogo Opzioni. Questa finestra di dialogo può essere il pannello di controllo della funzionalità.
-   **La finestra di dialogo Opzioni può includere i seguenti elementi** nel modo appropriato (il testo esatto è racchiuso tra virgolette):
    -   Abilita \[ Nome funzionalità \] (casella di controllo)
        -   Se si deseleziona questa opzione, il programma verrà chiuso in modo permanente. Il programma può essere riavviato dall'elemento del pannello di controllo. Il comando Esci dal menu di scelta rapida chiude il programma solo per la sessione corrente di Windows.
    -   "Icona di visualizzazione nell'area di notifica" (casella di controllo)
        -   La rimozione dell'icona dall'area di notifica non influisce sulla funzionalità sottostante.
        -   La selezione di questa opzione consente all'utente di ripristinare l'icona, che naturalmente non può essere eseguita dall'icona stessa.
-   Disabilitare le funzionalità usate raramente o potenzialmente fastidiose. Consentire agli utenti di [acconsentire esplicitamente](glossary.md) a tali funzionalità.

Per le linee guida e gli esempi della finestra di dialogo Opzioni generali, vedere [finestra delle proprietà](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Riduzione dei programmi nell'area di notifica

**Nota: la riduzione delle finestre di programma all'area di notifica non è più consigliata per Windows 7.** Usare invece i normali pulsanti della [barra delle applicazioni](winenv-taskbar.md) . Il programma può supportare entrambi i meccanismi per la compatibilità con le versioni precedenti.

-   Per ridurre il disordine della barra delle applicazioni, è consigliabile fornire la possibilità di ridurre al minimo i programmi nell'area di notifica solo se si applicano tutte le condizioni seguenti:
    -   Il programma può avere una sola istanza.
    -   Il programma viene eseguito per un lungo periodo di tempo.
    -   L'icona Mostra lo stato.
    -   L'icona può essere un'origine di notifica.
    -   Questa operazione è facoltativa e gli utenti devono [acconsentire esplicitamente](glossary.md).
-   Usare il pulsante Riduci a icona sulla barra del titolo dell'applicazione, non il pulsante Chiudi.

## <a name="text"></a>Testo

### <a name="infotips"></a>Infotip

-   L'icona infotip deve avere uno dei formati seguenti (dove il nome della società è facoltativo):
    -   (Nome della società) Nome della funzionalità, del programma o del dispositivo
    -   ![Screenshot di infotip con il nome della società ](images/winenv-notification-image37.png)
    -   (Nome della società) Funzionalità, programma o nome dispositivo-Riepilogo stato
    -   ![Screenshot di infotip che Visualizza il riepilogo dello stato ](images/winenv-notification-image38.png)
    -   (Nome della società) Dichiarazione di funzionalità, programma o stato del nome del dispositivo.
    -   ![Screenshot di infotip che Visualizza l'istruzione di stato ](images/winenv-notification-image39.png)
    -   (Nome della società) Nome della funzionalità, del programma o del dispositivo
    -   Elenco di stato con ogni elemento in una riga separata
    -   ![Screenshot di infotip che Visualizza l'elenco di stato ](images/winenv-notification-image40.png)

Formulazione infotip:

-   Concentrarsi sulle informazioni più utili. Visualizza altre informazioni in un solo clic sinistro.
-   Essere concisi. Usare frammenti di frase o istruzioni semplici.
-   Non usare la punteggiatura finale a meno che Tip non venga formulata come frase completa.
-   Omettere parole superflue. Non includere la versione del software o altre informazioni estranee.

    **Non corretto:**

    ![Screenshot di infotip con informazioni non necessarie ](images/winenv-notification-image41.png)

    In questo esempio infotip contiene informazioni estranee.

-   Non spiegare come interagire con l'icona.

    **Non corretto:**

    ![Screenshot di infotip con istruzioni con il pulsante destro del mouse ](images/winenv-notification-image42.png)

    In questo esempio, l'icona di connessione alla rete wireless fornisce istruzioni di clic con il pulsante destro del mouse.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento all'area di notifica:

-   Fare riferimento all'area di notifica come area di notifica, non alla barra di sistema.

Quando si fa riferimento a un'icona dell'area di notifica:

-   Fare riferimento all'icona usando il nome esatto specificato in infotip, inclusa la relativa maiuscola, seguita da icona.
-   Per il primo riferimento, vedere anche l'area di notifica.
-   Quando possibile, formattare il testo dell'intestazione usando grassetto. In caso contrario, inserire l'intestazione tra virgolette solo se necessario per evitare confusione.

**Esempio:** Per controllare rapidamente lo stato della rete, fare clic sull'icona della **rete** nell'area di notifica.

 

