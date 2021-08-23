---
title: Menu (nozioni di base sulla progettazione)
description: I menu sono elenchi gerarchici di comandi o opzioni disponibili per gli utenti nel contesto corrente.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9b2c3559163ff77e8e3f08354b017c1b7cb53c95fd51802ae2565efdf71abcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350174"
---
# <a name="menus-design-basics"></a>Menu (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

I menu sono elenchi gerarchici di comandi o opzioni disponibili per gli utenti nel contesto corrente.

I menu a discesa sono menu visualizzati su richiesta al clic del mouse o al passaggio del mouse. In genere sono nascoste e quindi sono un modo efficiente per risparmiare spazio sullo schermo. Un sottomenu o un menu a cascata è un menu secondario visualizzato su richiesta all'interno di un menu. Sono indicate da una freccia alla fine dell'etichetta del sottomenu. Una voce di menu è un singolo comando o opzione all'interno di un menu.

I menu vengono spesso visualizzati da una barra dei menu, ovvero un elenco di categorie di menu con etichetta che si trovano in genere nella parte superiore di una finestra. Al contrario, un menu di scelta rapida viene visualizzato quando gli utenti fa clic con il pulsante destro del mouse su un oggetto o un'area della finestra che supporta un menu di scelta rapida.

![Screenshot della barra dei menu con menu e sottomenu ](images/cmd-menus-image1.png)

Una tipica barra dei menu che visualizza un menu a discesa e un sottomenu.

> [!Note]  
> Le linee guida relative [ai pulsanti di](ctrl-command-buttons.md)comando , alle barre [degli](cmd-toolbars.md)strumenti [e alla](inter-keyboard.md) tastiera sono presentate in articoli separati.

 

## <a name="usage-patterns"></a>Modelli di utilizzo

I menu hanno diversi modelli di utilizzo:



| Uso                                                                                                                                                |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barre dei menu**<br/> una barra dei menu visualizza comandi e opzioni nei menu a discesa. <br/>                                               | le barre dei menu sono molto comuni e facili da trovare, nonché un uso efficiente dello spazio. <br/> ![Screenshot della barra dei menu con menu a discesa ](images/cmd-menus-image2.png)<br/> Una barra dei menu Windows Posta elettronica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Menu della barra degli strumenti**<br/> una barra dei menu implementata come barra degli strumenti. <br/>                                                                   | i menu della barra degli strumenti sono costituiti principalmente da comandi nei pulsanti di [menu](ctrl-command-buttons.md) e nei pulsanti di menu suddivisi, con solo alcuni comandi diretti, se presenti. <br/> ![Screenshot del menu della barra degli strumenti con menu a discesa ](images/cmd-menus-image3.png)<br/> Un menu della barra degli strumenti Windows Raccolta foto.<br/> Per linee guida su questo modello, vedere [Barre degli strumenti.](cmd-toolbars.md)<br/>                                                                                                                                                                                                             |
| **Menu delle schede**<br/> pulsanti all'interno di schede che visualizzano un piccolo set di comandi e opzioni correlati a una scheda in un menu a discesa. <br/> | Le schede con menu sono simili a schede normali, ad eccezione della parte inferiore con un pulsante con freccia a discesa. Facendo clic sul pulsante viene visualizzato un menu a discesa anziché selezionare la scheda. <br/> ![Screenshot del menu della scheda con menu a discesa ](images/cmd-menus-image4.png)<br/> I menu delle schede vengono usati Windows Media Player.<br/>                                                                                                                                                                                                                                                                                           |
| **Pulsanti di menu**<br/> pulsanti di comando che visualizzano un piccolo set di comandi correlati in un menu a discesa. <br/>                       | [I pulsanti di](ctrl-command-buttons.md) menu sono simili ai normali pulsanti di comando, ad eccezione del fatto che al loro interno è visualizzata una freccia a discesa. Facendo clic sul pulsante viene visualizzato un menu a discesa anziché eseguire un comando.<br/> [I pulsanti di](ctrl-command-buttons.md) menu sono simili ai pulsanti di menu, ad eccezione del fatto che sono varianti di un comando e facendo clic sulla parte sinistra del pulsante viene eseguita direttamente l'azione sull'etichetta.<br/> ![Screenshot del pulsante di menu con comandi a discesa ](images/cmd-menus-image5.png)<br/> Pulsante di menu con un piccolo set di comandi correlati.<br/> |
| **Menu di scelta rapida**<br/> menu a discesa che visualizzano un piccolo set di comandi e opzioni correlati al contesto corrente. <br/>       | menu di scelta rapida quando gli utenti fa clic con il pulsante destro del mouse su un oggetto o un'area della finestra che supporta un menu di scelta rapida. <br/> ![Screenshot del menu di scelta rapida che visualizza i comandi ](images/cmd-menus-image6.png)<br/> un menu di scelta rapida da Esplora risorse.<br/> Se i menu di scelta rapida sono la scelta migliore ma è necessaria una soluzione adatta a tutti gli utenti, è possibile usare un pulsante freccia a discesa del menu. <br/> ![Screenshot della foto con il pulsante del menu a discesa ](images/cmd-menus-image7.png)<br/> Menu di scelta rapida reso visibile con un pulsante a discesa di menu.<br/>                                                   |
| **Menu del riquadro attività**<br/> un piccolo set di comandi correlati all'oggetto o alla modalità programma selezionata. <br/>                              | A differenza dei menu di scelta rapida, vengono visualizzati automaticamente all'interno di un riquadro della finestra anziché su richiesta. <br/> ![Screenshot della foto con il menu del riquadro attività a destra ](images/cmd-menus-image8.png)<br/> Menu del riquadro attività dal visualizzatore Windows Raccolta foto attività.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

### <a name="menu-bars"></a>Barre dei menu

Applicare le condizioni seguenti:

-   La finestra è una finestra primaria?
-   Sono disponibili molte voci di menu?
-   Sono disponibili molte categorie di menu?
-   La maggior parte delle voci di menu si applica all'intero programma e alla finestra primaria?
-   Il menu deve funzionare per tutti gli utenti?

In tal caso, è consigliabile usare una barra dei menu.

### <a name="toolbar-menus"></a>Menu della barra degli strumenti

Applicare le condizioni seguenti:

-   La finestra è una finestra primaria?
-   La finestra ha una barra degli strumenti?
-   Sono disponibili solo alcune categorie di menu?
-   Il menu deve funzionare per tutti gli utenti?

In tal caso, è consigliabile usare un menu della barra degli strumenti anziché o in aggiunta a una barra dei menu.

### <a name="tab-menus"></a>Menu delle schede

Applicare le condizioni seguenti:

-   La finestra è una finestra primaria?
-   La finestra dispone di schede, in cui ogni scheda viene usata per un set dedicato di attività (invece di usare le schede per visualizzare visualizzazioni diverse)?
-   Esiste una categoria di menu che si applica a ogni scheda?
-   Sono disponibili molti comandi e opzioni, ma solo un piccolo set per ogni scheda?

In tal caso, è consigliabile usare un menu a schede anziché una barra dei menu.

### <a name="context-menu"></a>Menu di scelta rapida

Applicare le condizioni seguenti:

-   Esiste un piccolo set di comandi e opzioni contestuali che si applicano all'area dell'oggetto o della finestra selezionata?
-   Queste voci di menu sono ridondanti?
-   Gli utenti di destinazione hanno familiarità con i menu di scelta rapida?

In tal caso, è consigliabile fornire menu di scelta rapida per gli oggetti e le aree della finestra che ne hanno bisogno.

Per i programmi basati su browser, i menu del riquadro attività sono una soluzione più comune per i comandi contestuali. Attualmente, gli utenti si aspettano che i menu di scelta rapida nei programmi basati su browser siano generici e inutili.

### <a name="task-pane-menu"></a>Menu del riquadro attività

Applicare le condizioni seguenti:

-   La finestra è una finestra primaria?
-   Esiste un piccolo set di comandi e opzioni contestuali che si applicano all'oggetto selezionato o alla modalità programma?
-   Sono disponibili alcune categorie di menu?
-   Il menu deve funzionare per tutti gli utenti?

In tal caso, è consigliabile usare un menu del riquadro attività anziché un menu di scelta rapida.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Menu efficaci che promuovono un'esperienza utente ottimale:

-   Usare una presentazione dei comandi che corrisponda al tipo di programma, ai tipi di finestra, all'utilizzo dei comandi e agli utenti di destinazione.
-   Sono ben organizzati, usando l'organizzazione standard dei menu quando appropriato.
-   Usare in modo efficace barre dei menu, barre degli strumenti e menu di scelta rapida.
-   Usare le icone in modo efficace.
-   Usare in modo efficace i tasti di scelta rapida e i tasti di scelta rapida.

**Se si fa una sola cosa...**

Scegliere una presentazione di comandi che corrisponda al tipo di programma, ai tipi di finestra, all'utilizzo dei comandi e agli utenti di destinazione.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Tutti i modelli di menu, ad eccezione delle barre dei menu, necessitano di una freccia a discesa per indicare la presenza di un menu a discesa.** La presenza dei menu è un'altra cosa in una barra dei menu, ma non negli altri modelli.
-   **Non modificare i nomi delle voci di menu in modo dinamico.** Questa operazione è confusa e imprevista. Ad esempio, non modificare l'opzione Modalità verticale in modalità orizzontale al momento della selezione. Per le modalità, usare [invece elenchi puntati e segni di](#bullets-and-checkmarks) spunta.
    -   **Eccezione:** È possibile modificare i nomi delle voci di menu basati sui nomi degli oggetti in modo dinamico. Ad esempio, gli elenchi di file usati di recente o i nomi delle finestre possono essere dinamici.

### <a name="menu-bars"></a>Barre dei menu

-   **È consigliabile eliminare le barre dei menu con tre o meno categorie di menu.** Se sono presenti solo pochi comandi, è preferibile usare alternative più leggere, ad esempio i menu della barra degli strumenti, o alternative più dirette, ad esempio pulsanti di comando e collegamenti.
-   **Non sono disponibili più di 10 categorie di menu.** Un numero eccessivo di categorie di menu è eccessivo e rende difficile l'uso della barra dei menu.
-   **È consigliabile nascondere la barra dei menu** se la barra degli strumenti o i comandi diretti forniscono quasi tutti i comandi necessari per la maggior parte degli utenti. Consente agli utenti di visualizzare o nascondere con un'opzione di segno di spunta barra dei menu in un menu della barra degli strumenti.

![Screenshot dell'elenco di opzioni con la barra dei menu selezionata ](images/cmd-menus-image9.png)

In questo esempio, Windows Internet Explorer un'opzione della barra dei menu.

Per altre informazioni, vedere Nascondere [le barre dei menu.](#hiding-menu-bars)

### <a name="hiding-menu-bars"></a>Nascondere le barre dei menu

In genere, le barre degli strumenti funzionano bene insieme alle barre dei menu perché entrambe consentono a ognuna di concentrarsi sui punti di forza senza compromessi.

-   Nascondere la barra dei menu per impostazione predefinita se la progettazione della barra degli strumenti rende ridondante una barra dei menu.
-   Nascondere la barra dei menu invece di rimuoverla completamente, perché le barre dei menu sono più accessibili per gli utenti della tastiera.
-   Per ripristinare la barra dei menu, specificare un'opzione segno di spunta barra dei menu nella categoria di menu Visualizza (per le barre degli strumenti primari) o Strumenti (per le barre degli strumenti secondarie). Per altre informazioni, vedere [Menu Standard e pulsanti di divisione.](cmd-toolbars.md)

### <a name="menu-categories"></a>Categorie di menu

-   **Scegliere nomi di singole parole per le categorie di menu.** L'uso di più parole crea confusione nella separazione tra categorie.
-   **Per i programmi che creano o visualizzano documenti, usare le categorie di menu standard,** ad esempio File, Modifica, Visualizza, Strumenti e Guida. In questo modo, le voci di menu comuni sono prevedibili e più facili da trovare.
-   **Per altri tipi di programmi,** è consigliabile organizzare i comandi e le opzioni in categorie naturali più utili in base allo scopo del programma e al modo in cui gli utenti considerano le attività e gli obiettivi. Non essere obbligati a usare l'organizzazione di menu standard se non è adatta al programma.
-   **Se si sceglie di usare categorie di menu non standard, è necessario scegliere nomi di categoria validi.** Per altre informazioni, vedere la [sezione Etichette.](#labels)
-   **Preferire le categorie di menu orientate alle attività rispetto alle categorie generiche.** Le categorie orientate alle attività semplificano l'individuazione delle voci di menu.

![Screenshot della barra dei menu con rip, masterizzazione e sincronizzazione ](images/cmd-menus-image10.png)

In questo esempio, Windows Media Player le categorie di menu orientate alle attività.

-   **Evitare le categorie di menu con una o due voci di menu.** Se appropriato, consolidare con altre categorie di menu, ad esempio usando un sottomenu.
-   **È consigliabile inserire la stessa voce di menu in più categorie solo se:**
    -   La voce di menu appartiene logicamente a più categorie di menu.
    -   Sono presenti dati che indicano che gli utenti hanno problemi a trovare la voce in una singola categoria di menu.
    -   Sono disponibili solo una o due voci di menu difficili da trovare in più categorie.
-   **Non inserire voci di menu diverse che usano lo stesso nome in più categorie.** Ad esempio, non hanno voci di menu Opzioni diverse in più categorie.
    -   **Eccezione:** Il modello di menu della scheda può avere voci di menu Opzioni e Guida diverse in ogni menu delle schede.

![Screenshot dei menu delle schede con voci di menu ripetute ](images/cmd-menus-image11.png)

In questo esempio, Windows Media Player le voci di menu Opzioni e Guida in ogni menu delle schede.

### <a name="menu-item-organization-and-order"></a>Organizzazione e ordine delle voci di menu

-   **Organizzare le voci di menu in gruppi di sette o meno elementi fortemente correlati.** A questo scopo, i sottomenu vengono conteggiati come una singola voce di menu nel menu padre.
-   **Non inserire più di 25 elementi all'interno** di un singolo livello di un menu (senza contare i sottomenu).
-   **Inserire separatori tra i gruppi all'interno di un menu.** Un separatore è una singola riga che si estende sulla larghezza del menu.
-   **All'interno di un menu inserire i gruppi nell'ordine logico.** Se non è presente alcun ordine logico, posizionare prima i gruppi usati più di frequente.
-   **All'interno di un gruppo inserire gli elementi nell'ordine logico.** Se non è presente alcun ordine logico, posizionare prima gli elementi usati più di frequente. Inserire gli elementi numerici ,ad esempio le percentuali di zoom, in ordine numerico.

### <a name="submenus"></a>Sottomenu

-   **Evitare di usare i sottomenu inutilmente.** I sottomenu richiedono un maggiore impegno fisico da usare e in genere rendono le voci di menu più difficili da individuare.
-   **Non inserire voci di menu usate di frequente in un sottomenu.** In questo modo l'uso di questi comandi non sarebbe efficiente. Tuttavia, è possibile inserire i comandi usati di frequente in un sottomenu se si accede in genere più direttamente, ad esempio con una barra degli strumenti.
-   **È consigliabile usare un sottomenu se:**
    -   Questa operazione semplifica il menu padre perché contiene molte voci (20 o più) o il sottomenu fa parte di un gruppo di più di sette elementi.
    -   Le voci del sottomenu vengono usate meno frequentemente rispetto a quelle del menu padre.
    -   Il sottomenu contiene tre o più elementi.
    -   Esistono tre o più comandi che iniziano con la stessa parola. In questo caso, usare tale parola come etichetta del sottomenu.

![Screenshot del menu "nuovo" con quattro voci di sottomenu ](images/cmd-menus-image12.png)

In questo esempio, il sottomenu Nuovo sostituisce i comandi separati per Nuovo messaggio di posta elettronica, Nuovo messaggio di notizie, Nuova cartella e Nuovo contatto.

-   **Usare al massimo tre livelli di menu.** In altre informazioni, è possibile avere un menu primario e al massimo due livelli di sottomenu. Due livelli di sottomenu devono essere rari.

### <a name="presentation"></a>Presentazione

-   **Disabilitare le voci di menu che non si applicano al contesto corrente,** anziché rimuoverle. In questo modo, il contenuto della barra dei menu risulta stabile e più facile da trovare. **Eccezioni:**
    -   Per le categorie di menu **contestuali, rimuovere anziché disabilitare** le voci del menu di scelta rapida che non si applicano al contesto corrente. Una categoria di menu è contestuale quando viene visualizzata solo per modalità specifiche, ad esempio quando viene selezionato un determinato tipo di oggetto. Per informazioni dettagliate, vedere le [linee guida rimuovi e disabilita](#context-menus) per i menu di scelta rapida.
    -   Se determinare quando deve essere disabilitata una voce di menu causa problemi di prestazioni evidenti, lasciare attiva la voce di menu e, se necessario, fare in modo che la selezione restituirà un messaggio di errore.

### <a name="tab-menus"></a>Menu a schede

-   **Ogni menu della scheda può avere voci di menu Opzioni e Guida specifiche del contesto.** Ciò è in contrasto con tutti gli altri modelli di menu. Ogni scheda viene usata per un set dedicato di attività, quindi qualsiasi ridondanza tra i menu delle schede non crea confusione.

### <a name="context-menus"></a>Menu di scelta rapida

-   **Usare i menu di scelta rapida solo per i comandi e le opzioni contestuali.** Le voci di menu devono essere applicate solo all'area dell'oggetto o della finestra selezionata (o su cui si è fatto clic), non all'intero programma.
-   **Non rendere i comandi disponibili solo tramite i menu di scelta rapida.** Come i tasti di scelta rapida, i menu di scelta rapida sono strumenti alternativi per eseguire comandi e scegliere le opzioni. Ad esempio, un comando Proprietà è disponibile anche tramite la barra dei menu o il tasto di scelta ALT+INVIO.
-   **Fornire menu di scelta rapida per tutti gli oggetti e le aree della finestra** che traggono vantaggio da un piccolo set di comandi e opzioni contestuali. Molti utenti possono fare clic con il pulsante destro del mouse regolarmente e si aspettano di trovare menu di scelta rapida ovunque.
-   **È consigliabile usare un pulsante freccia a discesa per i menu di scelta rapida destinati a tutti gli utenti.** In genere i menu di scelta rapida sono adatti per i comandi e le opzioni destinati agli utenti avanzati. Tuttavia, è possibile usare un pulsante a discesa di menu nei casi in cui i menu di scelta rapida sono la scelta migliore ed è necessario scegliere come destinazione tutti gli utenti.

![Screenshot della foto con il pulsante del menu a discesa ](images/cmd-menus-image7.png)

In questo esempio viene usato un pulsante a discesa di menu per rendere visibile un menu di scelta rapida.

**Organizzazione e ordine delle voci di menu**

-   **Organizzare le voci di menu in gruppi di sette o meno elementi strettamente correlati.**
-   **Evitare di usare i sottomenu** per mantenere i menu di scelta rapida semplici, diretti ed efficienti.
-   **Non inserire più di 15 elementi all'interno di un menu di scelta rapida.**
-   **Inserire separatori tra i gruppi all'interno di un menu.** Un separatore è una singola riga che si estende sulla larghezza del menu.
-   **Presentare le voci di menu usando l'ordine seguente:**

<dl> Comandi primari (usati più di frequente)<dl> Apri  
Esegui  
Esegui  
Stampare <separator>  
</dl> </dd> <dd>Comandi secondari supportati dall'oggetto<dl> <separator>  
</dl> </dd> Comandi di trasferimento<dl> Taglia  
Copia  
Incollare <separator>  
</dl> </dd> <dd>Impostazioni degli oggetti<dl> <separator>  
</dl> </dd> Comandi per gli oggetti<dl> Delete  
Rinominare <separator>  
Proprietà
</dl> </dd> </dl>

**Presentazione**

-   **Visualizzare il comando predefinito in grassetto.** Quando possibile, impostare anche questa opzione come prima voce di menu. Il comando predefinito viene richiamato quando l'utente fa doppio clic o seleziona un oggetto e preme INVIO.
-   **Rimuovere invece di disabilitare le voci del menu di scelta rapida che non si applicano al contesto corrente.** In questo modo i menu di scelta rapida sono contestuali ed efficienti.
    -   **Eccezione:** Disabilitare le voci di menu che non si applicano se è ragionevole aspettarsi che siano disponibili:
        -   Disporre sempre dei comandi del menu di scelta rapida standard pertinenti, ad esempio Taglia, Copia, Incolla, Elimina e Rinomina.
        -   Disporre sempre dei comandi che completano i set correlati. Ad esempio, se è presente un oggetto Back, deve essere presente anche un elemento Forward. Se è presente un'opzione Taglia, è sempre necessario copiare e incollare.

### <a name="bullets-and-checkmarks"></a>Punti elenco e segni di spunta

-   **Le voci di menu che sono opzioni possono utilizzare punti elenco e segni di spunta.** I comandi potrebbero non essere disponibili.
-   **Usare un punto elenco per scegliere un'opzione da un piccolo set di scelte che si escludono a vicenda.** In un gruppo devono essere sempre presenti almeno due punti elenco. Per altre informazioni, vedere [Pulsanti di opzione.](ctrl-radio-buttons.md)
-   **Usare un segno di spunta per attivare o disattivare un'impostazione indipendente.** Se gli stati selezionati e deselezionati non sono opposti chiari e non ambigui, usare invece un set di punti elenco. Per altre informazioni, vedere [Caselle di controllo.](ctrl-check-boxes.md)
-   **Per uno stato con segno di spunta misto, visualizzare una voce di menu senza segno di spunta.** Lo stato misto viene usato per la selezione multipla per indicare che l'opzione è impostata per alcuni oggetti, ma non per tutti, in modo che ogni singolo oggetto abbia lo stato selezionato o deselezionato. Lo stato misto non viene usato come terzo stato per un singolo elemento.
-   **Inserire separatori tra i set correlati di segni di spunta o punti elenco.** Un separatore è una singola riga che si estende sulla larghezza del menu.

### <a name="icons"></a>Icone

-   **Prendi in considerazione l'eventualità di fornire icone per le voci di menu relativamente a:**
    -   Voci di menu usate più di frequente.
    -   Voci di menu la cui icona è standard e nota.
    -   Voci di menu le cui icone illustrino ampiamente la funzione del comando.
-   **Se si usano le icone, non è obbligatorio specificarle per tutte le voci di menu.** Le icone criptiche sono di scarsa utilità, in quanto generano confusione visiva e impediscono agli utenti di concentrarsi sulle voci di menu fondamentali.

![Screenshot delle voci di menu con e senza icone ](images/cmd-menus-image13.png)

In questo esempio il menu Organizza contiene icone solo per le voci di menu usate più di frequente.

-   **Assicurarsi che le icone di menu siano conformi alle linee guida per le icone in stile Aereo.**

Per altre informazioni ed esempi, vedere [Icone.](vis-icons.md)

### <a name="access-keys"></a>Chiavi di accesso

-   **Assegnare le chiavi di accesso a tutte le voci di menu.** Nessuna eccezione.
-   **Quando possibile, assegnare le chiavi di accesso per i comandi di uso comune in base alle assegnazioni standard delle chiavi di accesso.** Anche se le assegnazioni coerenti delle chiavi di accesso non sono sempre possibili, sono sicuramente preferibili, soprattutto per i comandi usati di frequente.
-   **Per le voci di menu dinamico, ad esempio i file usati di recente, assegnare numericamente le chiavi di accesso.**

![Screenshot delle voci di menu con tasti di scelta numerici ](images/cmd-menus-image14.png)

In questo esempio il programma Paint in Windows assegna chiavi di accesso numeriche ai file usati di recente.

-   **Assegnare chiavi di accesso univoche all'interno di un livello di menu.** È possibile riutilizzare le chiavi di accesso in diversi livelli di menu.
-   **Semplificare la ricerca delle chiavi di accesso:**
    -   Per le voci di menu usate più di frequente, scegliere i caratteri all'inizio della prima o della seconda parola dell'etichetta, preferibilmente il primo carattere.
    -   Per le voci di menu usate meno di frequente, scegliere lettere distintive consonanti o vocali nell'etichetta.
-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferisce una consonante distintiva o una vocale,** ad esempio "x" in "Exit".
-   **Evitare di usare caratteri che rendono difficile la sottolineatura,** ad esempio (dalla più problematica alla meno problematica):
    -   Lettere che hanno una larghezza di un solo pixel, ad esempio i e l.
    -   Lettere con discendenti, ad esempio g, j, p, q e y.
    -   Lettere accanto a una lettera con un discendente.

Per altre linee guida ed esempi, vedere [Tastiera.](inter-keyboard.md)

### <a name="shortcut-keys"></a>Combinazioni di tasti

-   **Assegnare i tasti di scelta rapida alle voci di menu usate più di frequente.** Le voci di menu usate raramente non necessitano di tasti di scelta rapida perché gli utenti possono usare i tasti di scelta.
-   **Non creare un tasto di scelta rapida come unico modo per eseguire un'attività.** Gli utenti devono anche essere in grado di usare il mouse o la tastiera con TAB, freccia e tasti di scelta.
-   **Per i tasti di scelta rapida noti, usare le assegnazioni standard.**
-   **Non assegnare significati diversi a tasti di scelta rapida noti.** Poiché sono memorizzati, significati incoerenti per le scelte rapide note sono frustranti e erre. Vedere Windows tasti di scelta rapida per i tasti di scelta rapida ben Windows programmi.
-   **Non provare ad assegnare tasti di scelta rapida del programma a livello di sistema.** I tasti di scelta rapida del programma avranno effetto solo quando il programma ha lo stato attivo per l'input.
-   **Documentare tutti i tasti di scelta rapida.** In questo modo, gli utenti possono apprendere le assegnazioni dei tasti di scelta rapida.
    -   **Eccezione:** Non visualizzare le assegnazioni dei tasti di scelta rapida all'interno dei menu di scelta rapida. I menu di scelta rapida non visualizzano le assegnazioni dei tasti di scelta rapida perché sono ottimizzati per l'efficienza.
-   **Per le assegnazioni di chiave non standard:**
    -   **Scegliere i tasti di scelta rapida che non hanno assegnazioni standard.** Non riassegnare mai i tasti di scelta rapida standard.
    -   **Usare le assegnazioni di chiave non standard in modo coerente in tutto il programma.** Non assegnare significati diversi in finestre diverse.
    -   **Se possibile, scegliere le assegnazioni di tasti mnemoiche,** in particolare per i comandi usati di frequente.
    -   **Usare i tasti funzione per i comandi che hanno un** effetto su scala ridotta, ad esempio i comandi che si applicano all'oggetto selezionato. Ad esempio, F2 rinomina l'elemento selezionato.
    -   **Usare combinazioni di tasti CTRL per i comandi che** hanno un effetto su larga scala, ad esempio i comandi che si applicano a un intero documento. Ad esempio, CTRL+S salva il documento corrente.
    -   **Usare combinazioni di tasti MAIUSC per i comandi che estendono o completano le azioni del tasto di scelta rapida standard.** Ad esempio, il tasto di scelta rapida ALT+TAB scorre le finestre primarie aperte, mentre ALT+MAIUSC+TAB scorre in ordine inverso. Analogamente, F1 visualizza la Guida, mentre MAIUSC+F1 visualizza la Guida sensibile al contesto.
    -   **Non usare i caratteri seguenti per i tasti di scelta rapida:** @ $ {} \[ \] \\  ~  \| ^ ' < >. Questi caratteri richiedono combinazioni di tasti diverse tra lingue o sono specifiche delle impostazioni locali.
    -   **Non usare combinazioni CTRL+ALT,** perché Windows interpreta questa combinazione in alcune versioni del linguaggio come tasto ALTGR, che genera caratteri alfanumerici.
-   **Se il programma assegna molti tasti di scelta rapida, fornire la possibilità di personalizzare le assegnazioni.** In questo modo, gli utenti possono riassegnare i tasti di scelta rapida in conflitto ed eseguire la migrazione da altri prodotti. La maggior parte dei programmi non assegna un numero sufficiente di tasti di scelta rapida per questa funzionalità.

Per altre linee guida e assegnazioni standard dei tasti di scelta rapida, vedere [Tastiera](inter-keyboard.md).

### <a name="standard-menus"></a>Menu standard

-   **Usare l'organizzazione di menu standard per i programmi che creano o visualizzano documenti.** L'organizzazione di menu standard rende le voci di menu comuni prevedibili e più facili da trovare.
-   **Per altri tipi di programmi, usare l'organizzazione di menu standard solo quando è opportuno.** È consigliabile organizzare i comandi e le opzioni in categorie naturali più utili in base allo scopo del programma e al modo in cui gli utenti considerano le attività e gli obiettivi.

**Barre dei menu standard**

La struttura della barra dei menu standard è la seguente. Questo elenco mostra la categoria di menu e le etichette degli elementi, il relativo ordine con separatori, i tasti di scelta rapida e di accesso e i relativi puntini di sospensione.

<dl> File<dl> Nuovo CTRL+N  
Aperto... CTRL+O  
Chiudere <separator>  
Salva CTRL+S  
Salva con nome... <separator>  
Invia a <separator>  
Stampare... CTRL+P  
Anteprima di stampa  
Configurazione della pagina <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Esci da ALT+F4 (collegamento in genere non specificato)
</dl> </dd> Edit<dl> Annulla CTRL+Z  
Ripeti CTRL+Y <separator>  
Taglia CTRL+X  
Copiare CTRL+C  
Incolla CTRL+V <separator>  
Seleziona tutto CTRL+A <separator>  
Elimina Del (collegamento in genere non specificato) <separator>  
Trovare... CTRL+F  
Trova F3 successivo (comando in genere non specificato)  
Sostituire... CTRL+H  
Vai a... CTRL+G
</dl> </dd> View<dl> Barre degli strumenti  
Barra di stato <separator>  
</dl> </dd> Zoom<dl> Zoom avanti CTRL++  
Zoom indietro CTRL+- <separator>  
Schermo intero F11  
Aggiornare F5
</dl> </dd> <dd>Strumenti<dl> ... <separator>  
Opzioni
</dl> </dd> Help<dl> <program name> Guida F1 <separator>  
Circa <program name>  
</dl> </dd> </dl>

**Pulsanti di menu standard della barra degli strumenti**

I pulsanti di menu standard della barra degli strumenti sono i seguenti. Questo elenco mostra la categoria di menu e le etichette degli elementi, il relativo ordine con separatori, i tasti di scelta rapida e i relativi puntini di sospensione.

<dl> Strumenti<dl> Schermo interoF11(Riassegna chiave di accesso se viene usato anche Trova).  
Barre degli strumenti (si noti che il comando Barra dei menu è visualizzato qui). <separator>  
Stampa...  
Trovare... <separator>  
Zoom  
Dimensioni del testo <separator>  
Opzioni
</dl> </dd> Organize<dl> Nuova cartellaCtrl+N <separator>  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V <separator>  
Selezionare allCtrl+A <separator>  
DeleteDel(collegamento in genere non specificato)  
Rinominare <separator>  
Opzioni
</dl> </dd> Page<dl> Nuova finestraCtrl+N <separator>  
Zoom  
Dimensione del testo
</dl> </dd> </dl>

**Menu di scelta rapida standard**

Il contenuto del menu di scelta rapida standard è il seguente. Questo elenco mostra le etichette delle voci di menu, il relativo ordine con separatori, i tasti di scelta e i relativi puntini di sospensione. I menu di scelta rapida non mostrano i tasti di scelta rapida.

<dl> Apri  
Esegui  
Esegui  
Modifica  
Stampare... <separator>  
Taglia  
Copia  
Incollare <separator>  
Delete  
Rinominare <separator>  
Bloccare <object name> (segno di spunta)  
Proprietà
</dl>

### <a name="using-ellipses"></a>Uso dei puntini di sospensione

Mentre i comandi di menu vengono usati per azioni immediate, potrebbero essere necessarie altre informazioni per eseguire l'azione. **Indicare un comando che richiede informazioni aggiuntive (inclusa una conferma) aggiungendo i puntini di sospensione alla fine dell'etichetta.**

![Screenshot del comando di stampa e della finestra di dialogo Stampa ](images/cmd-menus-image15.png)

In questo esempio, print... visualizza una finestra di dialogo Stampa per raccogliere altre informazioni.

**L'uso corretto dei puntini di sospensione è importante per indicare che gli utenti possono effettuare altre scelte prima di eseguire l'azione o persino annullare completamente l'azione.** Il segnale visivo offerto da un puntoni di sospensione consente agli utenti di esplorare il software senza timori.

Questo non significa che è necessario usare i puntini di sospensione ogni volta che un'azione visualizza **un'altra** finestra solo quando sono necessarie informazioni aggiuntive per eseguire l'azione. Ad esempio, i comandi About, Advanced, Help, Options, Properties e Impostazioni devono visualizzare un'altra finestra quando si fa clic, ma non richiedono informazioni aggiuntive da parte dell'utente. Non sono quindi necessari puntini di sospensione.

**In caso di ambiguità (ad esempio, l'etichetta del comando non dispone di un verbo), decidere in base all'azione dell'utente più probabile.** Se la semplice visualizzazione della finestra è un'azione comune, non usare i puntini di sospensione.

**Corretto:**

Altri colori...

Informazioni sulla versione

Nel primo esempio, è molto probabile che gli utenti sceglino un colore, quindi l'uso di un ellisse è corretto. Nel secondo esempio, gli utenti probabilmente visualizzano le informazioni sulla versione, rendendo i puntini di sospensione superflui.

> [!Note]  
> Quando si determina se un comando di menu necessita di puntini di sospensione, non usare la necessità di elevare i privilegi come fattore. [](winenv-uac.md)

 

L'elevazione dei privilegi non è necessaria per eseguire un comando (piuttosto che per l'autorizzazione) e la necessità di elevare è indicata con lo schermo di sicurezza.

## <a name="labels"></a>Etichette

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di maiuscole e minuscole in stile titolo, se necessario, per evitare di combinare gli stili di combinazione di maiuscole e minuscole.

### <a name="menu-category-names"></a>Nomi delle categorie di menu

-   **Usare nomi di categorie di menu che sono verbi o sostantivi a parola singola.** Un'etichetta a più parole potrebbe essere confusa per due etichette di una parola.
-   **Preferisce i nomi dei menu basati su verbi.** Tuttavia, omettere il verbo se è Create, Show, View o Manage. Ad esempio, le categorie di menu seguenti non hanno verbi:
    -   Tabella
    -   Strumenti
    -   Finestra
-   Per i nomi di categoria non standard, usare una singola parola specifica che descriva in modo chiaro e accurato **il contenuto del menu.** Anche se i nomi non devono essere così generali da descrivere tutti gli elementi nel menu, dovrebbero essere sufficientemente prevedibili in modo che gli utenti non siano sorprese da ciò che trovano nel menu.

### <a name="menu-item-names"></a>Nomi delle voci di menu

-   **Usare nomi di voci di menu che iniziano con una frase verbo, sostantivo o sostantivo.**
-   **Preferisce i nomi dei menu basati su verbi.** Tuttavia, omettere il verbo se:
    -   **Il verbo è Create, Show, View o Manage.** Ad esempio, i comandi seguenti non hanno verbi:
        -   Informazioni
        -   Avanzato
        -   Schermo intero
        -   Nuovo
        -   Opzioni
        -   Proprietà
    -   **Il verbo corrisponde al nome della categoria di menu per evitare ripetizioni.** Ad esempio, nella categoria di menu Inserisci usare Testo, Tabella e Immagine invece di Inserisci testo, Inserisci tabella e Inserisci immagine.
-   **Usare verbi specifici.** Evitare verbi generici e inutili, ad esempio Change e Manage.
-   **Usare sostantivi singolari per i comandi che si applicano a un singolo oggetto**, in caso contrario usare sostantivi plurali.
-   **Usare i modificatori in base alle esigenze per distinguere tra comandi simili.** Esempi: Inserisci riga sopra, Inserisci riga sotto.
-   **Per coppie di comandi complementari, scegliere nomi chiaramente complementari.** Esempi: Aggiungi, Rimuovi; Mostra, Nascondi; Inserisci, Elimina.
-   **Scegliere i nomi delle voci di menu in base a obiettivi e attività dell'utente, non alla tecnologia.**

**Corretto:**

![Screenshot del menu a comparsa con la voce di menu Formato ](images/cmd-menus-image16.png)

**Non corretto:**

![Screenshot del menu a comparsa con la voce di menu codec ](images/cmd-menus-image17.png)

Nell'esempio non corretto, la voce di menu è basata sulla relativa tecnologia.

-   Usare i nomi delle voci di menu seguenti per lo scopo indicato:
    -   **Opzioni** Per visualizzare le opzioni del programma.
    -   **Personalizzare** Per visualizzare le opzioni del programma correlate in modo specifico alla configurazione dell'interfaccia utente meccanica.
    -   **Personalizza** Per visualizzare un riepilogo delle impostazioni di personalizzazione [di uso](glossary.md) comune.
    -   **Preferenze** Non usare. In alternativa, usare Opzioni.
    -   **Proprietà** Per visualizzare la finestra delle proprietà di un oggetto.
    -   **Impostazioni** Non usare come etichetta di menu. In alternativa, usare Opzioni.

### <a name="submenu-names"></a>Nomi dei sottomenu

-   **Le voci di menu che visualizzano sottomenu non hanno mai puntini di sospensione sull'etichetta.** La freccia del sottomenu indica che è necessaria un'altra selezione.

**Non corretto:**

![Screenshot della nuova voce di menu con puntini di sospensione ](images/cmd-menus-image18.png)

In questo esempio la voce di menu Nuovo presenta erroneamente i puntini di sospensione.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai menu:

-   Nei comandi che mostrano o nascondono i menu, fare riferimento alle barre dei menu. Non fare riferimento a questi menu come menu classici.
-   Fare riferimento ai menu in base alle relative etichette. Usare il testo esatto dell'etichetta, inclusa la combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura o i puntini di sospensione del tasto di scelta.
-   Per fare riferimento alle categorie di menu, usare "Nel <category name> menu". Se la posizione di una voce di menu è chiara dal contesto, non è necessario menzionare la categoria di menu.
-   Per descrivere l'interazione dell'utente delle voci di menu, usare il clic, senza il menu o il comando word. Non usare scegliere, selezionare o selezionare. Non fare riferimento a una voce di menu come una voce di menu, ad eccezione della documentazione tecnica.
-   Per descrivere la rimozione di un segno di spunta da un'opzione di menu, usare fare clic per rimuovere il segno di spunta. Non usare clear.
-   Fare riferimento ai menu di scelta rapida come menu di scelta rapida, non come menu di scelta rapida.
-   Non usare menu a cascata, a discesa, a discesa o popup per descrivere i menu, ad eccezione della documentazione di programmazione.
-   Fare riferimento alle voci di menu non disponibili come non disponibili, non in grigio, disabilitate o in grigio. Usare disabled nella documentazione di programmazione.
-   Quando possibile, formattare le etichette usando il testo in grassetto. In caso contrario, inserire le etichette tra virgolette solo se necessario per evitare confusione.

Esempi:

-   Scegliere **Stampa** dal menu File **per** stampare il documento.
-   Scegliere Barre **degli** strumenti dal menu Visualizza **e** quindi fare clic su **Formattazione**.

 

