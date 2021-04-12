---
title: Menu (nozioni di base sulla progettazione)
description: I menu sono elenchi gerarchici di comandi o opzioni disponibili per gli utenti nel contesto corrente.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8054a01e4198f3592a34ae09635dd60f392da1eb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234440"
---
# <a name="menus-design-basics"></a>Menu (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

I menu sono elenchi gerarchici di comandi o opzioni disponibili per gli utenti nel contesto corrente.

I menu a discesa sono menu visualizzati su richiesta al clic del mouse o al passaggio del mouse. Sono normalmente nascosti dalla visualizzazione e pertanto rappresentano un mezzo efficace per risparmiare spazio sullo schermo. Un sottomenu o un menu a cascata è un menu secondario visualizzato su richiesta dall'interno di un menu. Sono indicati da una freccia alla fine dell'etichetta del sottomenu. Una voce di menu è un singolo comando o opzione all'interno di un menu.

I menu vengono spesso visualizzati da una barra dei menu, ovvero un elenco di categorie di menu con etichetta in genere situate nella parte superiore di una finestra. Al contrario, un menu di scelta rapida scende quando gli utenti fanno clic con il pulsante destro del mouse su un oggetto o un'area della finestra che supporta un menu di scelta rapida.

![screenshot della barra dei menu con menu e sottomenu ](images/cmd-menus-image1.png)

Una tipica barra dei menu che visualizza un menu a discesa e un sottomenu.

> [!Note]  
> Le linee guida correlate ai [pulsanti di comando](ctrl-command-buttons.md), le [barre degli strumenti](cmd-toolbars.md)e la [tastiera](inter-keyboard.md) sono presentate in articoli distinti.

 

## <a name="usage-patterns"></a>Modelli di utilizzo

I menu includono diversi modelli di utilizzo:



|                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barre dei menu**<br/> una barra dei menu Visualizza comandi e opzioni nei menu a discesa. <br/>                                               | le barre dei menu sono molto comuni e facili da trovare, oltre a un uso efficiente dello spazio. <br/> ![screenshot della barra dei menu con menu a discesa ](images/cmd-menus-image2.png)<br/> Barra dei menu di Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Menu della barra degli strumenti**<br/> barra dei menu implementata come barra degli strumenti. <br/>                                                                   | i menu della barra degli strumenti sono barre degli strumenti costituite principalmente da comandi nei [pulsanti di menu](ctrl-command-buttons.md) e pulsanti di menu combinato, con solo pochi comandi diretti, se presenti. <br/> ![screenshot del menu della barra degli strumenti con menu a discesa ](images/cmd-menus-image3.png)<br/> Menu della barra degli strumenti nella raccolta foto di Windows.<br/> Per le linee guida su questo modello, vedere [barre degli strumenti](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Menu a schede**<br/> pulsanti nelle schede che visualizzano un piccolo set di comandi e opzioni correlati a una scheda in un menu a discesa. <br/> | le schede con i menu sembrano schede normali, tranne la parte inferiore, con un pulsante con la freccia a discesa. Quando si fa clic sul pulsante, viene visualizzato un menu a discesa anziché selezionare la scheda. <br/> ![screenshot del menu a schede con menu a discesa ](images/cmd-menus-image4.png)<br/> I menu a schede vengono utilizzati in Windows Media Player.<br/>                                                                                                                                                                                                                                                                                           |
| **Pulsanti di menu**<br/> pulsanti di comando che visualizzano un piccolo set di comandi correlati in un menu a discesa. <br/>                       | i [pulsanti di menu](ctrl-command-buttons.md) sono simili ai pulsanti di comando normali, ad eccezione del fatto che contengono una freccia a discesa. Quando si fa clic sul pulsante, viene visualizzato un menu a discesa anziché eseguire un comando.<br/> i pulsanti di menu [combinato](ctrl-command-buttons.md) sono simili ai pulsanti di menu, ad eccezione del fatto che sono varianti di un comando e facendo clic sulla parte sinistra del pulsante viene eseguita direttamente l'azione sull'etichetta.<br/> ![cattura di schermata del pulsante di menu con i comandi a discesa ](images/cmd-menus-image5.png)<br/> Pulsante di menu con un piccolo set di comandi correlati.<br/> |
| **Menu di scelta rapida**<br/> menu a discesa che visualizzano un piccolo set di comandi e opzioni correlate al contesto corrente. <br/>       | menu di scelta rapida a discesa quando si fa clic con il pulsante destro del mouse su un oggetto o un'area della finestra che supporta un menu di scelta rapida. <br/> ![screenshot del menu di scelta rapida per la visualizzazione dei comandi ](images/cmd-menus-image6.png)<br/> menu di scelta rapida di Esplora risorse.<br/> Se i menu di scelta rapida sono la scelta del menu migliore, ma è necessaria una soluzione adatta a tutti gli utenti, è possibile usare un pulsante della freccia a discesa menu. <br/> ![screenshot della foto con il pulsante del menu a discesa ](images/cmd-menus-image7.png)<br/> Menu di scelta rapida reso visibile con un pulsante a discesa di menu.<br/>                                                   |
| **Menu riquadro attività**<br/> un piccolo set di comandi correlati all'oggetto o alla modalità del programma selezionati. <br/>                              | a differenza dei menu di scelta rapida, vengono visualizzati automaticamente in un riquadro della finestra, anziché su richiesta. <br/> ![screenshot della foto con menu riquadro attività a destra ](images/cmd-menus-image8.png)<br/> Menu del riquadro attività del Visualizzatore raccolta foto di Windows.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

### <a name="menu-bars"></a>Barre dei menu

Si applicano le condizioni seguenti:

-   La finestra è una finestra primaria?
-   Sono disponibili molte voci di menu?
-   Sono presenti molte categorie di menu?
-   La maggior parte delle voci di menu viene applicata all'intero programma e alla finestra primaria?
-   Il menu deve funzionare per tutti gli utenti?

In tal caso, prendere in considerazione l'uso di una barra dei menu.

### <a name="toolbar-menus"></a>Menu della barra degli strumenti

Si applicano le condizioni seguenti:

-   La finestra è una finestra primaria?
-   La finestra dispone di una barra degli strumenti?
-   Sono disponibili solo alcune categorie di menu?
-   Il menu deve funzionare per tutti gli utenti?

In tal caso, è consigliabile utilizzare un menu della barra degli strumenti anziché o in aggiunta a una barra dei menu.

### <a name="tab-menus"></a>Menu a schede

Si applicano le condizioni seguenti:

-   La finestra è una finestra primaria?
-   Nella finestra sono presenti schede, in cui ogni scheda viene utilizzata per un set dedicato di attività, anziché utilizzare schede per visualizzare visualizzazioni diverse.
-   Esiste una categoria di menu applicabile a ogni scheda?
-   Sono disponibili molti comandi e opzioni, ma solo un piccolo set per ogni scheda?

In tal caso, è consigliabile utilizzare un menu a schede anziché una barra dei menu.

### <a name="context-menu"></a>Menu di scelta rapida

Si applicano le condizioni seguenti:

-   Esiste un piccolo set di comandi contestuali e di opzioni che si applicano all'oggetto o all'area della finestra selezionata?
-   Queste voci di menu sono ridondanti?
-   Gli utenti di destinazione hanno familiarità con i menu di scelta rapida?

In tal caso, è consigliabile fornire i menu di scelta rapida per gli oggetti e le aree della finestra che li richiedono.

Per i programmi basati su browser, i menu del riquadro attività rappresentano una soluzione più comune per i comandi contestuali. Attualmente, gli utenti si aspettano che i menu di scelta rapida nei programmi basati su browser siano generici e non utili.

### <a name="task-pane-menu"></a>Menu riquadro attività

Si applicano le condizioni seguenti:

-   La finestra è una finestra primaria?
-   Esiste un piccolo set di comandi contestuali e di opzioni applicabili all'oggetto o alla modalità programma selezionati?
-   Sono disponibili alcune categorie di menu?
-   Il menu deve funzionare per tutti gli utenti?

In tal caso, prendere in considerazione l'uso di un menu del riquadro attività anziché di un menu di scelta rapida.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Menu efficaci che favoriscono una corretta esperienza utente:

-   Usare una presentazione di comando che corrisponda al tipo di programma, ai tipi di finestra, all'utilizzo dei comandi e agli utenti di destinazione.
-   Sono ben organizzati, usando un'organizzazione di menu standard quando appropriato.
-   Utilizzare le barre dei menu, le barre degli strumenti e i menu di scelta rapida.
-   Usare le icone in modo efficace.
-   Usare in modo efficace chiavi di accesso e tasti di scelta rapida.

**Se si esegue una sola operazione...**

Scegliere una presentazione di comando che corrisponda al tipo di programma, ai tipi di finestra, all'utilizzo dei comandi e agli utenti di destinazione.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Tutti i modelli di menu eccetto le barre dei menu necessitano di una freccia a discesa per indicare la presenza di un menu a discesa.** La presenza di menu non viene pronunciata in una barra dei menu, ma non negli altri modelli.
-   **Non modificare i nomi delle voci di menu in modo dinamico.** Questa operazione è confusa e imprevista. Ad esempio, non modificare l'opzione modalità verticale in modalità orizzontale al momento della selezione. Per le modalità, utilizzare invece i [punti elenco e](#bullets-and-checkmarks) i segni di spunta.
    -   **Eccezione:** È possibile modificare i nomi delle voci di menu in modo dinamico in base ai nomi degli oggetti. Ad esempio, gli elenchi di nomi di file o di finestre usati di recente possono essere dinamici.

### <a name="menu-bars"></a>Barre dei menu

-   **Provare a eliminare le barre dei menu con tre o meno categorie di menu.** Se sono presenti solo pochi comandi, preferire alternative più chiare, ad esempio i menu della barra degli strumenti, o più alternative dirette, ad esempio i pulsanti di comando e i collegamenti.
-   **Non sono disponibili più di 10 categorie di menu.** Troppe categorie di menu sono sovraccaricate e rendono difficile l'utilizzo della barra dei menu.
-   Si **consiglia di nascondere la barra dei menu** se la barra degli strumenti o i comandi diretti forniscono quasi tutti i comandi necessari per la maggior parte degli utenti. Consente agli utenti di visualizzare o nascondere l'opzione del segno di spunta della barra dei menu in un menu della barra degli strumenti.

![screenshot dell'elenco di opzioni con la barra dei menu selezionata ](images/cmd-menus-image9.png)

In questo esempio, Windows Internet Explorer fornisce un'opzione della barra dei menu.

Per ulteriori informazioni, vedere [nascondere le barre dei menu](#hiding-menu-bars).

### <a name="hiding-menu-bars"></a>Nascondere le barre dei menu

In genere, le barre degli strumenti funzionano perfettamente insieme alle barre dei menu perché entrambe consentono di concentrarsi sui propri punti di forza senza compromessi.

-   Per impostazione predefinita, nascondere la barra dei menu se la progettazione della barra degli strumenti rende ridondante la barra dei menu.
-   Nascondere la barra dei menu anziché rimuoverla completamente, perché le barre dei menu sono più accessibili per gli utenti della tastiera.
-   Per ripristinare la barra dei menu, specificare un'opzione per il segno di spunta della barra dei menu nella categoria Visualizza (per le barre degli strumenti primarie) o strumenti (per le barre degli strumenti secondarie). Per ulteriori informazioni, vedere [menu standard e pulsanti di menu combinato](cmd-toolbars.md).

### <a name="menu-categories"></a>Categorie di menu

-   **Scegliere i nomi delle singole parole per le categorie di menu.** L'uso di più parole semplifica la separazione tra le categorie.
-   **Per i programmi che creano o visualizzano documenti, utilizzare le categorie di menu standard** , ad esempio file, modifica, Visualizza, strumenti e guida. In questo modo, le voci di menu comuni risultano prevedibili e più facili da trovare.
-   **Per altri tipi di programmi, è consigliabile organizzare i comandi e le opzioni in categorie più utili e naturali** in base allo scopo del programma e al modo in cui gli utenti pensano alle attività e agli obiettivi. Se non è appropriato per il programma, non è necessario utilizzare l'organizzazione di menu standard.
-   **Se si sceglie di utilizzare le categorie di menu non standard, è necessario scegliere nomi di categoria validi.** Per ulteriori informazioni, vedere la sezione [etichette](#labels) .
-   **Preferisce le categorie di menu orientate alle attività su categorie generiche.** Le categorie orientate alle attività rendono più semplice trovare le voci di menu.

![screenshot della barra dei menu con RIP, Burn e Sync ](images/cmd-menus-image10.png)

In questo esempio, Windows Media Player usa le categorie di menu orientate alle attività.

-   **Evitare le categorie di menu con solo una o due voci di menu.** Se ragionevole, consolidare con altre categorie di menu, ad esempio usando un sottomenu.
-   **Si consiglia di inserire la stessa voce di menu in più categorie solo se:**
    -   La voce di menu appartiene logicamente a più categorie di menu.
    -   Sono presenti dati che indicano che gli utenti non riescono a trovare l'elemento in una singola categoria di menu.
    -   Sono presenti solo una o due voci di menu difficili da trovare in più categorie.
-   **Non inserire voci di menu diverse che usano lo stesso nome in più categorie.** Ad esempio, non hanno voci di menu opzioni diverse in più categorie.
    -   **Eccezione:** Il modello di menu a schede può avere opzioni e voci di menu della guida diverse in ogni menu della scheda.

![screenshot dei menu a schede con voci di menu ripetute ](images/cmd-menus-image11.png)

In questo esempio, Windows Media Player dispone di opzioni e voci di menu della Guida in ogni menu della scheda.

### <a name="menu-item-organization-and-order"></a>Organizzazione e ordine delle voci di menu

-   **Organizzare le voci di menu in gruppi di sette o meno elementi strettamente correlati.** A tale proposito, i sottomenu vengono conteggiati come una singola voce di menu nel menu padre.
-   **Non inserire più di 25 elementi all'interno di un singolo livello di un menu** (senza contare i sottomenu).
-   **Inserire i separatori tra i gruppi all'interno di un menu.** Un separatore è costituito da una singola riga che si estende sulla larghezza del menu.
-   **All'interno di un menu, inserire i gruppi nell'ordine logico.** Se non è presente alcun ordine logico, inserire prima i gruppi usati più di frequente.
-   **All'interno di un gruppo, inserire gli elementi nell'ordine logico.** Se non è presente alcun ordine logico, inserire prima gli elementi utilizzati più di frequente. Inserire elementi numerici, ad esempio percentuali di zoom, in ordine numerico.

### <a name="submenus"></a>Sottomenu

-   **Evitare di usare inutilmente i sottomenu.** I sottomenu richiedono un maggiore sforzo fisico da usare e in genere rendono più difficile l'individuazione delle voci di menu.
-   **Non inserire voci di menu di uso frequente in un sottomenu.** Questa operazione renderebbe l'uso inefficiente di questi comandi. Tuttavia, è possibile inserire i comandi usati di frequente in un sottomenu se normalmente si accede più direttamente, ad esempio con una barra degli strumenti.
-   **Prendere in considerazione l'uso di un sottomenu se:**
    -   In questo modo, il menu padre viene semplificato perché contiene molti elementi (20 o più) oppure il sottomenu fa parte di un gruppo di più di sette elementi.
    -   Gli elementi del sottomenu vengono utilizzati con minore frequenza rispetto a quelli nel menu padre.
    -   Il sottomenu avrebbe tre o più elementi.
    -   Sono disponibili tre o più comandi che iniziano con la stessa parola. In questo caso, usare tale parola come etichetta di sottomenu.

![screenshot del menu ' nuovo ' con quattro voci di sottomenu ](images/cmd-menus-image12.png)

In questo esempio, il nuovo sottomenu sostituisce i comandi distinti per i nuovi messaggi di posta elettronica, nuovi messaggi di notizie, nuova cartella e nuovo contatto.

-   **Utilizzare al massimo tre livelli di menu.** Ovvero, è possibile avere un menu primario e al massimo due livelli di sottomenu. Due livelli di sottomenu dovrebbero essere rari.

### <a name="presentation"></a>Presentazione

-   **Disabilitare le voci di menu che non si applicano al contesto corrente,** anziché rimuoverle. In questo modo, il contenuto della barra dei menu risulta stabile e più facile da trovare. **Eccezioni**
    -   Per le categorie di menu contestuali, **rimuovere anziché disabilitare le voci del menu di scelta rapida che non si applicano al contesto corrente.** Una categoria di menu è contestuale quando viene visualizzata solo per modalità specifiche, ad esempio quando viene selezionato un determinato tipo di oggetto. Per informazioni dettagliate, vedere le linee guida [Remove vs. Disable](#context-menus) per i menu di scelta rapida.
    -   Se determinare quando una voce di menu deve essere disabilitata causa problemi di prestazioni evidenti, lasciare attiva la voce di menu e, se necessario, che la selezione provochi un messaggio di errore.

### <a name="tab-menus"></a>Menu a schede

-   **Ogni menu della scheda può avere opzioni specifiche del contesto e voci di menu della guida.** Questo è contrario a tutti gli altri modelli di menu. Ogni scheda viene utilizzata per un set dedicato di attività, pertanto qualsiasi ridondanza tra i menu a schede non confonde.

### <a name="context-menus"></a>Menu di scelta rapida

-   **Usare i menu di scelta rapida solo per i comandi e le opzioni contestuali.** Le voci di menu devono essere valide solo per l'oggetto o l'area della finestra selezionata (o su cui è stato fatto clic), non per l'intero programma.
-   **Non rendere i comandi disponibili solo tramite i menu di scelta rapida.** Analogamente ai tasti di scelta rapida, i menu di scelta rapida sono modi alternativi per eseguire comandi e scegliere Opzioni. Un comando Properties, ad esempio, è disponibile anche tramite la barra dei menu o il tasto di scelta ALT + INVIO.
-   **Fornire menu di scelta rapida per tutti gli oggetti e le aree della finestra** che traggono vantaggio da un piccolo set di comandi e opzioni contestuali. Molti utenti fanno clic con il pulsante destro del mouse regolarmente e prevedono di trovare menu di scelta rapida ovunque
-   **Si consiglia di utilizzare un pulsante a discesa menu per i menu di scelta rapida destinati a tutti gli utenti.** In genere i menu di scelta rapida sono adatti per i comandi e le opzioni destinati agli utenti avanzati. Tuttavia, è possibile utilizzare un pulsante a discesa dei menu nei casi in cui i menu di scelta rapida sono la scelta del menu migliore ed è necessario fare riferimento a tutti gli utenti.

![screenshot della foto con il pulsante del menu a discesa ](images/cmd-menus-image7.png)

In questo esempio viene usato un pulsante a discesa menu per rendere visibile un menu di scelta rapida.

**Organizzazione e ordine delle voci di menu**

-   **Organizzare le voci di menu in gruppi di sette o meno elementi strettamente correlati.**
-   **Evitare l'uso di sottomenu** per i menu di scelta rapida semplice, diretta ed efficiente.
-   **Non inserire più di 15 elementi all'interno di un menu di scelta rapida.**
-   **Inserire i separatori tra i gruppi all'interno di un menu.** Un separatore è costituito da una singola riga che si estende sulla larghezza del menu.
-   **Presentare le voci di menu utilizzando l'ordine seguente:**

<dl> Comandi primari (usati più di frequente)<dl> Apri  
Esegui  
Esegui  
Stampa <separator>  
</dl> </dd> <dd>Comandi secondari supportati dall'oggetto<dl> <separator>  
</dl> </dd> Comandi Transfer<dl> Taglia  
Copia  
Incolla <separator>  
</dl> </dd> <dd>Impostazioni oggetto<dl> <separator>  
</dl> </dd> Comandi per oggetti<dl> Delete  
Rinominare <separator>  
Proprietà
</dl> </dd> </dl>

**Presentazione**

-   **Visualizzare il comando predefinito utilizzando grassetto.** Quando si è pratici, impostarla anche come prima voce di menu. Il comando predefinito viene richiamato quando l'utente fa doppio clic o seleziona un oggetto e preme INVIO.
-   **Rimuovere anziché disabilitare le voci del menu di scelta rapida che non si applicano al contesto corrente.** In questo modo, i menu di scelta rapida sono contestuali ed efficienti.
    -   **Eccezione:** Disabilitare le voci di menu che non si applicano se è prevista una ragionevole previsione perché siano disponibili:
        -   Sono sempre disponibili i comandi di menu di scelta rapida standard, ad esempio taglia, copia, incolla, Elimina e Rinomina.
        -   Sono sempre disponibili i comandi che completano i set correlati. Se, ad esempio, è presente un oggetto back, dovrebbe essere presente anche un oggetto in futuro. Se è presente un taglio, avere sempre una copia e incolla.

### <a name="bullets-and-checkmarks"></a>Elenchi puntati e segni di spunta

-   **Le voci di menu che sono opzioni possono utilizzare elenchi puntati e segni di spunta.** I comandi non possono.
-   **Usare un Bullet per scegliere un'opzione da un piccolo set di scelte che si escludono a vicenda.** In un gruppo devono essere sempre presenti almeno due punti elenco. Per altre informazioni, vedere [pulsanti di opzione](ctrl-radio-buttons.md).
-   **Usare un segno di spunta per attivare o disattivare un'impostazione indipendente.** Se gli stati selezionati e deselezionati non sono chiari e non ambigui, usare invece un set di punti elenco. Per ulteriori informazioni, vedere [caselle di controllo](ctrl-check-boxes.md).
-   **Per uno stato di segno di spunta misto, visualizzare una voce di menu senza segno di spunta.** Lo stato misto viene usato per la selezione multipla per indicare che l'opzione è impostata per alcuni, ma non per tutti gli oggetti, in modo che ogni singolo oggetto abbia lo stato selezionato o deselezionato. Lo stato misto non viene utilizzato come terzo stato per un singolo elemento.
-   **Inserire i separatori tra i set di segni di spunta o i punti elenco correlati.** Un separatore è costituito da una singola riga che si estende sulla larghezza del menu.

### <a name="icons"></a>Icone

-   **Prendi in considerazione l'eventualità di fornire icone per le voci di menu relativamente a:**
    -   Voci di menu utilizzate più di frequente.
    -   Voci di menu il cui simbolo è standard e noto.
    -   Voci di menu le cui icone illustrino ampiamente la funzione del comando.
-   **Se si usano le icone, non è necessario fornirle per tutte le voci di menu.** Le icone criptiche sono di scarsa utilità, in quanto generano confusione visiva e impediscono agli utenti di concentrarsi sulle voci di menu fondamentali.

![screenshot delle voci di menu con e senza icone ](images/cmd-menus-image13.png)

In questo esempio, il menu organizza ha icone solo per le voci di menu usate più di frequente.

-   **Assicurarsi che le icone di menu siano conformi alle linee guida dell'icona di tipo Aero.**

Per ulteriori informazioni ed esempi, vedere [Icone](vis-icons.md).

### <a name="access-keys"></a>Chiavi di accesso

-   **Assegnare chiavi di accesso a tutte le voci di menu.** Nessuna eccezione.
-   **Laddove possibile, assegnare le chiavi di accesso per i comandi usati di frequente in base alle assegnazioni di chiavi di accesso standard.** Sebbene le assegnazioni di chiavi di accesso coerenti non siano sempre possibili, sono certamente preferite, soprattutto per i comandi usati di frequente.
-   **Per le voci di menu dinamiche, ad esempio i file usati di recente, assegnare chiavi di accesso numericamente.**

![screenshot delle voci di menu con chiavi di accesso numeriche ](images/cmd-menus-image14.png)

In questo esempio, il programma di disegno in Windows assegna chiavi di accesso numeriche ai file usati di recente.

-   **Assegnare chiavi di accesso univoche all'interno di un livello di menu.** È possibile riutilizzare le chiavi di accesso in diversi livelli di menu.
-   **Semplifica la ricerca delle chiavi di accesso:**
    -   Per le voci di menu utilizzate più di frequente, scegliere caratteri all'inizio della prima o della seconda parola dell'etichetta, preferibilmente il primo carattere.
    -   Per le voci di menu utilizzate meno di frequente, scegliere lettere che rappresentano una consonante distinta o una vocale nell'etichetta.
-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferisce una consonante distinta o una vocale,** ad esempio "x" in "Exit".
-   **Evitare l'uso di caratteri che rendono difficile la visualizzazione della sottolineatura,** ad esempio (dal più problematico al meno problematico):
    -   Lettere con una sola larghezza di pixel, ad esempio i e l.
    -   Lettere con discendenti, ad esempio g, j, p, q e y.
    -   Lettere accanto a una lettera con un discendente.

Per altre linee guida ed esempi, vedere [tastiera](inter-keyboard.md).

### <a name="shortcut-keys"></a>Combinazioni di tasti

-   **Assegnare i tasti di scelta rapida alle voci di menu utilizzate più di frequente.** Le voci di menu usate raramente non necessitano di tasti di scelta rapida perché gli utenti possono usare chiavi di accesso.
-   **Non creare un tasto di scelta rapida l'unico modo per eseguire un'attività.** Gli utenti devono inoltre essere in grado di utilizzare il mouse o la tastiera con la scheda, la freccia e le chiavi di accesso.
-   **Per i tasti di scelta rapida noti, usare le assegnazioni standard.**
-   **Non assegnare significati diversi ai tasti di scelta rapida noti.** Poiché vengono memorizzati, i significati incoerenti per i collegamenti noti sono frustranti ed è soggetta a errori. Vedere Tasti di scelta rapida di Windows per i tasti di scelta rapida noti usati dai programmi di Windows.
-   **Non tentare di assegnare i tasti di scelta rapida del programma a livello di sistema.** I tasti di scelta rapida del programma avranno effetto solo quando il programma ha lo stato attivo per l'input.
-   **Documentare tutti i tasti di scelta rapida.** Questa operazione consente agli utenti di apprendere le assegnazioni dei tasti di scelta rapida.
    -   **Eccezione:** Non visualizzare le assegnazioni dei tasti di scelta rapida nei menu di scelta rapida. I menu di scelta rapida non visualizzano le assegnazioni dei tasti di scelta rapida perché sono ottimizzate per l'efficienza.
-   **Per le assegnazioni di chiavi non standard:**
    -   **Scegliere i tasti di scelta rapida che non hanno assegnazioni standard.** Non riassegnare mai i tasti di scelta rapida standard.
    -   **Usare le assegnazioni di chiavi non standard in modo coerente in tutto il programma.** Non assegnare significati diversi in finestre diverse.
    -   **Se possibile, scegliere assegnazioni tasti mnemonico,** specialmente per i comandi usati di frequente.
    -   **Usare i tasti funzione per i comandi che hanno un effetto su scala ridotta,** ad esempio i comandi che si applicano all'oggetto selezionato. Ad esempio, F2 Rinomina l'elemento selezionato.
    -   **Usare le combinazioni di tasti CTRL per i comandi che hanno un effetto su larga scala,** ad esempio i comandi che si applicano a un intero documento. Ad esempio, CTRL + S Salva il documento corrente.
    -   **Usare le combinazioni di tasti MAIUSC per i comandi che estendono o completano le azioni del tasto di scelta rapida standard.** Ad esempio, il tasto di scelta rapida Alt + Tab scorre le finestre primarie aperte, mentre ALT + MAIUSC + TAB viene cicli nell'ordine inverso. Analogamente, F1 Visualizza la guida, mentre MAIUSC + F1 Visualizza la Guida sensibile al contesto.
    -   **Non usare i caratteri seguenti per i tasti di scelta rapida:** @ $ {} \[ \] \\  ~  \| ^'  < >. Questi caratteri richiedono combinazioni di chiavi diverse tra le lingue o sono specifiche delle impostazioni locali.
    -   **Non usare combinazioni CTRL + ALT** perché Windows interpreta questa combinazione in alcune versioni del linguaggio come chiave AltGr, che genera caratteri alfanumerici.
-   **Se il programma assegna molti tasti di scelta rapida, fornire la possibilità di personalizzare le assegnazioni.** In questo modo gli utenti possono riassegnare i tasti di scelta rapida in conflitto ed eseguire la migrazione da altri prodotti. La maggior parte dei programmi non assegna abbastanza tasti di scelta rapida per richiedere questa funzionalità.

Per altre linee guida e le assegnazioni dei tasti di scelta rapida standard, vedere [tastiera](inter-keyboard.md).

### <a name="standard-menus"></a>Menu standard

-   **Utilizzare l'organizzazione dei menu standard per i programmi che creano o visualizzano i documenti.** L'organizzazione del menu standard rende le voci di menu comuni prevedibili e più semplici da trovare.
-   **Per altri tipi di programmi, utilizzare l'organizzazione dei menu standard solo quando è sensato.** È consigliabile organizzare i comandi e le opzioni in categorie più utili e naturali in base allo scopo del programma e al modo in cui gli utenti considerano le attività e gli obiettivi.

**Barre dei menu standard**

La struttura della barra dei menu standard è la seguente. Questo elenco Mostra la categoria di menu e le etichette degli elementi, l'ordine con i separatori, i tasti di scelta rapida e di accesso e i relativi ellissi.

<dl> File<dl> Nuovo CTRL + N  
Apri... CTRL + O  
Chiudere <separator>  
Salva CTRL + S  
Salva con nome... <separator>  
Invia a <separator>  
Stampa... CTRL + P  
Anteprima di stampa  
Imposta pagina <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Exit ALT + F4 (collegamento di solito non specificato)
</dl> </dd> Edit<dl> Annulla Ctrl + Z  
Ripeti Ctrl + Y <separator>  
Taglia CTRL + X  
Copia Ctrl + C  
Incolla Ctrl + V <separator>  
Seleziona tutto Ctrl + A <separator>  
Delete del (collegamento di solito non specificato) <separator>  
Trova... CTRL + F  
Trova successivo F3 (il comando non è in genere specificato)  
Sostituisci... CTRL + H  
Vai a... CTRL + G
</dl> </dd> View<dl> Barre degli strumenti  
Barra di stato <separator>  
</dl> </dd> Zoom<dl> Zoom avanti CTRL + +  
Zoom indietro Ctrl +- <separator>  
Schermo intero F11  
Aggiorna F5
</dl> </dd> <dd>Strumenti<dl> ... <separator>  
Opzioni
</dl> </dd> Help<dl> <program name> Guida F1 <separator>  
Su <program name>  
</dl> </dd> </dl>

**Pulsanti di menu della barra degli strumenti standard**

I pulsanti di menu della barra degli strumenti standard sono i seguenti. Questo elenco Mostra la categoria di menu e le etichette degli elementi, l'ordine con i separatori, i tasti di scelta rapida e i relativi ellissi.

<dl> Strumenti<dl> ScreenF11 completo (Riassegna la chiave di accesso se viene utilizzata anche la ricerca).  
Barre degli strumenti (si noti che il comando della barra dei menu va qui). <separator>  
Stampa...  
Trova... <separator>  
Zoom  
Dimensioni del testo <separator>  
Opzioni
</dl> </dd> Organize<dl> Nuovo folderCtrl + N <separator>  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V <separator>  
Seleziona allCtrl + A <separator>  
DeleteDel (collegamento generalmente non specificato)  
Rinominare <separator>  
Opzioni
</dl> </dd> Page<dl> Nuovo windowCtrl + N <separator>  
Zoom  
Dimensione del testo
</dl> </dd> </dl>

**Menu di scelta rapida standard**

Il contenuto del menu di scelta rapida standard è il seguente. Questo elenco Mostra le etichette delle voci di menu, l'ordine con i separatori, le relative chiavi di accesso e i relativi ellissi. I menu di scelta rapida non mostrano tasti di scelta rapida.

<dl> Apri  
Esegui  
Esegui  
Modifica  
Stampa... <separator>  
Taglia  
Copia  
Incolla <separator>  
Delete  
Rinominare <separator>  
Blocca (segno di <object name> spunta)  
Proprietà
</dl>

### <a name="using-ellipses"></a>Uso di ellissi

Mentre i comandi di menu vengono utilizzati per le azioni immediate, per eseguire l'azione potrebbero essere necessarie ulteriori informazioni. **Indicare un comando che richiede informazioni aggiuntive (inclusa una conferma) aggiungendo i puntini di sospensione alla fine dell'etichetta.**

![screenshot del comando stampa e della finestra di dialogo Stampa ](images/cmd-menus-image15.png)

In questo esempio, Print... consente di visualizzare una finestra di dialogo Stampa per raccogliere ulteriori informazioni.

**L'uso corretto dei puntini di sospensione è importante per indicare che gli utenti possono effettuare altre scelte prima di eseguire l'azione o persino annullare completamente l'azione.** Il segnale visivo offerto dai puntini di sospensione consente agli utenti di esplorare il software senza timore.

**Questo non significa che è necessario usare i puntini di sospensione ogni volta che un'azione Visualizza un'altra finestra** solo quando sono necessarie altre informazioni per eseguire l'azione. Ad esempio, i comandi su, avanzate, guida, opzioni, proprietà e impostazioni devono visualizzare un'altra finestra quando si fa clic, ma non richiedono informazioni aggiuntive da parte dell'utente. Non sono quindi necessari ellissi.

**In caso di ambiguità (ad esempio, l'etichetta del comando non dispone di un verbo), decidere in base all'azione dell'utente più probabile.** Se la semplice visualizzazione della finestra è un'azione comune, non usare i puntini di sospensione.

**Corretto:**

Altri colori...

Informazioni sulla versione

Nel primo esempio, gli utenti scelgono con maggiore probabilità un colore, quindi l'uso di un ellissi è corretto. Nel secondo esempio, gli utenti visualizzano con maggiore probabilità le informazioni sulla versione, rendendo inutili le ellissi.

> [!Note]  
> Per determinare se un comando di menu necessita di puntini di sospensione, non usare la necessità di [elevare i privilegi](winenv-uac.md) come fattore.

 

L'elevazione non è necessaria per eseguire un comando (piuttosto, è per l'autorizzazione) e la necessità di elevare è indicata con lo scudo di sicurezza.

## <a name="labels"></a>Etichette

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di maiuscole in stile titolo, se necessario, per evitare di combinare stili di maiuscole.

### <a name="menu-category-names"></a>Nomi della categoria di menu

-   **Usare nomi di categorie di menu con verbi o sostantivi a parola singola.** Un'etichetta a più parole potrebbe essere confusa per le etichette di 2 1 parole.
-   **Preferisce i nomi di menu basati su verbi.** Tuttavia, omettere il verbo se è creare, visualizzare, visualizzare o gestire. Le categorie di menu seguenti, ad esempio, non dispongono di verbi:
    -   Tabella
    -   Strumenti
    -   Finestra
-   Per i nomi di categoria non standard, **usare una singola parola specifica che descrive in modo chiaro e preciso il contenuto del menu.** Sebbene i nomi non debbano essere così generali che descrivano tutti gli elementi del menu, dovrebbero essere prevedibili, in modo che gli utenti non siano sorpresi da ciò che trovano nel menu.

### <a name="menu-item-names"></a>Nomi delle voci di menu

-   **Usare nomi di voci di menu che iniziano con un verbo, un sostantivo o una frase nominale.**
-   **Preferisce i nomi di menu basati su verbi.** Tuttavia, omettere il verbo se:
    -   **Il verbo è creare, visualizzare, visualizzare o gestire.** I comandi seguenti, ad esempio, non dispongono di verbi:
        -   Informazioni
        -   Avanzato
        -   Schermo intero
        -   Nuova
        -   Opzioni
        -   Proprietà
    -   **Il verbo corrisponde al nome della categoria di menu per evitare la ripetizione.** Nella categoria menu Inserisci, ad esempio, utilizzare testo, tabella e immagine anziché Inserisci testo, Inserisci tabella e Inserisci immagine.
-   **Usare verbi specifici.** Evitare verbi generici e non helper, ad esempio la modifica e la gestione.
-   **Utilizzare sostantivi singoli per i comandi che si applicano a un singolo oggetto**; in caso contrario, utilizzare Sostantivi plurali.
-   **Usare i modificatori come necessario per distinguere i comandi simili.** Esempi: Inserisci riga sopra, Inserisci riga sotto.
-   **Per le coppie di comandi complementari, scegliere nomi chiaramente complementari.** Esempi: Add, Remove; Mostra, Nascondi; Insert, DELETE.
-   **Scegliere i nomi delle voci di menu in base agli obiettivi e alle attività dell'utente, non alla tecnologia.**

**Corretto:**

![screenshot del menu RIP con la voce di menu Format ](images/cmd-menus-image16.png)

**Non corretto:**

![screenshot del menu RIP con la voce di menu codec ](images/cmd-menus-image17.png)

Nell'esempio errato, la voce di menu è basata sulla relativa tecnologia.

-   Utilizzare i seguenti nomi di voci di menu per lo scopo indicato:
    -   **Opzioni** di Per visualizzare le opzioni del programma.
    -   **Personalizza** Per visualizzare le opzioni di programma specifiche relative alla configurazione dell'interfaccia utente meccanica.
    -   **Personalizza** Per visualizzare un riepilogo delle impostazioni di [personalizzazione](glossary.md) di uso comune.
    -   **Preferenze** Non usare. Usare invece le opzioni.
    -   **Proprietà** di Per visualizzare la finestra delle proprietà di un oggetto.
    -   **Impostazioni** di Non usare come etichetta di menu. Usare invece le opzioni.

### <a name="submenu-names"></a>Nomi di sottomenu

-   **Le voci di menu che visualizzano i sottomenu non hanno mai i puntini di sospensione nell'etichetta.** La freccia del sottomenu indica che è necessaria un'altra selezione.

**Non corretto:**

![screenshot della nuova voce di menu con puntini di sospensione ](images/cmd-menus-image18.png)

In questo esempio, la nuova voce di menu presenta in modo errato i puntini di sospensione.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai menu:

-   In comandi che mostrano o nascondono i menu, fare riferimento alle barre dei menu. Non fare riferimento ad essi come menu classici.
-   Fare riferimento ai menu in base alle etichette. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere la sottolineatura o i puntini di sospensione della chiave di accesso.
-   Per fare riferimento alle categorie di menu, usare "nel <category name> menu". Se il percorso di una voce di menu è deselezionato dal contesto, non è necessario menzionare la categoria di menu.
-   Per descrivere l'interazione dell'utente delle voci di menu, utilizzare clic, senza il menu o il comando Word. Non usare choose, SELECT o pick. Non fare riferimento a una voce di menu come voce di menu tranne che nella documentazione tecnica.
-   Per descrivere la rimozione di un segno di spunta da un'opzione di menu, utilizzare fare clic per rimuovere il segno di spunta. Non usare Clear.
-   Fare riferimento a menu di scelta rapida come menu di scelta rapida, non menu di scelta rapida.
-   Non usare i menu a cascata, a discesa, a discesa o a comparsa per descrivere i menu, tranne che nella documentazione di programmazione.
-   Vedere le voci di menu non disponibili come non disponibili, non come ombreggiate, disabilitate o in grigio. Usare Disabled nella documentazione di programmazione.
-   Quando possibile, formattare le etichette usando il testo in grassetto. In caso contrario, inserire le etichette tra virgolette solo se necessario per evitare confusione.

Esempi:

-   Scegliere **stampa** dal menu **file** per stampare il documento.
-   Scegliere **barre degli strumenti** dal menu **Visualizza** , quindi fare clic su **formattazione**.

 

