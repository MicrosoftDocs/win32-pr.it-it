---
title: Mouse e puntatori
description: Il mouse è il dispositivo di input primario usato per interagire con gli oggetti in Windows.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e973ad46ec864c20ad7eef5708388f86e8489909df1fdae609106d1ca65d4614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119030322"
---
# <a name="mouse-and-pointers"></a>Mouse e puntatori

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Il mouse è il dispositivo di input primario usato per interagire con gli oggetti in Windows. La funzionalità del mouse può includere anche altri dispositivi di puntamento, ad esempio trackball, touchpad e bastoni di puntamento incorporati nei computer notebook, penne usate con Tecnologia Windows per Tablet PC e, nei computer con touchscreen, anche il dito di un utente.

> [!NOTE]
> Le linee guida relative [all'accessibilità,](inter-accessibility.md) [alla](inter-pen.md)penna e [al tocco](inter-touch.md) sono presentate in articoli separati.

Spostando fisicamente il mouse, il puntatore grafico (detto anche cursore) viene spostato sullo schermo. Il puntatore ha un'ampia gamma di forme per indicarne il comportamento corrente.

![Screenshot di cinque tipici puntatori del mouse ](images/inter-mouse-image1.png)

*Puntatori del mouse tipici*

I dispositivi mouse hanno spesso un pulsante primario (in genere il pulsante sinistro), un pulsante secondario (in genere a destra) e una rotellina del mouse tra i due. Posizionando il puntatore e facendo clic sui pulsanti primario e secondario sul mouse, gli utenti possono selezionare gli oggetti ed eseguire azioni su di essi. Per la maggior parte delle interazioni, la pressione di un pulsante del mouse mentre il cursore si trova su una destinazione indica la destinazione selezionata e il rilascio del pulsante esegue qualsiasi azione associata alla destinazione.

Tutti i puntatori, ad eccezione del puntatore occupato, hanno un'area sensibile a un singolo pixel che definisce la posizione esatta dello schermo del mouse. L'area sensibile determina l'oggetto interessato dalle azioni del mouse. Gli oggetti definiscono una zona sensibile, ovvero l'area in cui l'area sensibile viene considerata sull'oggetto . In genere, la zona calda coincide con i bordi di un oggetto, ma può essere più grande per semplificare l'esecuzione della finalità dell'utente.

Il punto di inserimento è la barra verticale lampeggiante visualizzata quando l'utente digita in una casella di testo o in un altro editor di testo. Il cursore è indipendente dal puntatore (per impostazione Windows nasconde il puntatore mentre l'utente digita).

![Screenshot della casella di testo con cursore ](images/inter-mouse-image2.png)

*Il caret*

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="the-mouse-is-intuitive"></a>Il mouse è intuitivo

Il mouse è stato un dispositivo di input di successo perché è facile da usare per la tipica mano umana. L'interazione basata su puntatore ha avuto esito positivo perché è intuitiva e consente un'ampia gamma di esperienze.

**Si dice che gli oggetti dell'interfaccia utente ben progettati hanno convenienza, ovvero proprietà visive e comportamentali di un oggetto che suggeriscono come viene usato.** Il puntatore funge da proxy per la mano, consentendo agli utenti di interagire con gli oggetti dello schermo come con gli oggetti fisici. Gli esseri umani hanno una conoscenza innata del funzionamento della mano umana, quindi se qualcosa sembra che possa essere spinto, si prova a eseguire il push; se sembra che possa essere afferrato, si prova a afferrarlo. Di conseguenza, gli utenti possono capire come usare gli oggetti con una forte convenienza semplicemente esaminandoli e provandoli.

![Screenshot di un pulsante e di un dispositivo di scorrimento](images/inter-mouse-image3.png)

*I pulsanti e i dispositivi di scorrimento hanno una forte convenienza*

Al contrario, gli oggetti con scarso affordance sono più difficili da capire. Tali oggetti spesso richiedono un'etichetta o un'istruzione per spiegarli.

![Screenshot del testo del collegamento e dell'icona Internet Earth](images/inter-mouse-image4.png)

*il testo del collegamento e le icone hanno un'accessibilità scadente*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Alcuni aspetti dell'uso del mouse non sono intuitivi

**Fare clic con il pulsante destro del mouse,** fare doppio clic e fare clic con i modificatori di tasti MAIUSC o CTRL sono tre interazioni del mouse che non sono intuitive perché non hanno controparti reali. A differenza dei tasti di scelta rapida e dei tasti di scelta, queste interazioni con il mouse in genere non sono documentate in nessun punto dell'interfaccia utente. Ciò suggerisce che non è necessario fare clic con il pulsante destro del mouse, fare doppio clic e i modificatori della tastiera non devono essere necessari per eseguire attività di base, in particolare da utenti principianti. Suggerisce anche che queste interazioni avanzate devono avere un comportamento coerente e prevedibile per poter essere usate in modo efficace.

### <a name="single-click-or-double-click"></a>Fare doppio clic o fare doppio clic?

Il doppio clic viene usato in modo completo sul desktop Windows che potrebbe non sembrare un'interazione avanzata. Ad esempio, l'apertura di cartelle, programmi o documenti nel riquadro dei file di Windows Explorer viene eseguita facendo doppio clic. Anche l'apertura di un collegamento Windows desktop usa il doppio clic. Al contrario, l'apertura di cartelle o programmi nel menu Start richiede un solo clic.

Gli oggetti selezionabili usano un solo clic per eseguire la selezione, quindi richiedono un doppio clic per l'apertura, mentre gli oggetti non selezionabili richiedono un solo clic per l'apertura. Questa distinzione non viene compresa da molti utenti (facendo clic sull'icona di un programma, a destra?) e, di conseguenza, alcuni utenti continuano a fare clic sulle icone finché non ottengono ciò che vogliono.

### <a name="direct-manipulation"></a>Manipolazione diretta

L'interazione diretta con gli oggetti viene definita manipolazione diretta. Il puntamento, il clic, la selezione, lo spostamento, il ridimensionamento, la suddivisione, lo scorrimento, la panoramica e lo zoom sono modifiche dirette comuni. Al contrario, l'interazione con un oggetto tramite la relativa finestra delle proprietà o un'altra finestra di dialogo può essere descritta come manipolazione indiretta.

**Tuttavia, in caso di manipolazione diretta, può essere presente una manipolazione accidentale e quindi la necessità di essere manipolato.** Loro è la possibilità di invertire o correggere facilmente un'azione indesiderata. È possibile apportare modifiche dirette perdonando l'annullamento, fornendo un buon feedback visivo e consentendo agli utenti di correggere facilmente gli errori. L'associazione con 2000 è la prevenzione di azioni indesiderate, che è possibile eseguire usando controlli vincolati e conferme per azioni rischiose o comandi che hanno conseguenze impreviste.

### <a name="standard-mouse-button-interactions"></a>Interazioni standard con il pulsante del mouse

Le interazioni con il mouse standard dipendono da diversi fattori, tra cui il tasto del mouse su cui è stato fatto clic, il numero di clic, la posizione durante i clic e se sono stati premuti modificatori della tastiera. Ecco un riepilogo del modo in cui questi fattori influiscono in genere sull'interazione:

- Per la maggior parte degli oggetti, il doppio clic sinistro esegue un singolo clic a sinistra ed esegue il comando predefinito. Il comando predefinito viene identificato nel menu di scelta rapida.
- Per alcuni tipi di oggetti selezionabili, ogni clic espande l'effetto del clic. Ad esempio, facendo clic singolo in una casella di testo viene impostata la posizione di input, facendo doppio clic viene selezionata una parola e facendo triplo clic viene selezionata una frase o un paragrafo.
- Facendo clic con il pulsante destro del mouse viene visualizzato il menu di scelta rapida di un oggetto.
- Mantenendo il mouse fermo mentre si punta il puntatore, il passaggio del mouse viene attivato.
- Mantenendo il mouse fermo mentre si preme il pulsante del mouse, viene indicato il clic e la selezione di un singolo oggetto. Lo spostamento del mouse indica lo spostamento, il ridimensionamento, la divisione, il trascinamento e la selezione di più oggetti.
- Il tasto MAIUSC estende la selezione in modo contiguo.
- Il tasto CTRL estende la selezione in base allo stato di selezione dell'elemento selezionato senza influire sulla selezione di altri oggetti.

### <a name="simple-mouse-interactions"></a>Interazioni semplici con il mouse

La tabella seguente descrive le interazioni e gli effetti comuni del mouse.

| Azione semplice | Interazione | Effetto tipico |
|:---|:---|:---|
| Puntamento<br/>          | Posizionare il puntatore su un oggetto specifico senza fare clic sui pulsanti del mouse.<br/>                                                                                                                                                                                                                                      | Target visualizza lo stato del passaggio del mouse ed eventuali affordance dinamici.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Bilico<br/>          | Posizionare il puntatore su un oggetto specifico senza fare clic sui pulsanti del mouse e senza spostarsi per almeno un secondo.<br/>                                                                                                                                                                                             | Target visualizza la descrizione comando, la descrizione comando o l'equivalente.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Cliccando<br/>          | Posizionare il puntatore su un oggetto specifico non selezionabile e premere e rilasciare un pulsante del mouse senza spostarsi. Il clic ha effetto sulla versione del pulsante del mouse per consentire agli utenti di annullare il clic spostando il mouse fuori dalla destinazione. Di conseguenza, la pressione del mouse indica solo la destinazione selezionata.<br/> | Per i singoli clic con il pulsante primario, attivare l'oggetto . Per fare doppio clic con il pulsante primario, attivare l'oggetto ed eseguire il comando predefinito. Per il pulsante secondario, visualizzare il menu di scelta rapida dell'oggetto.<br/>                                                                                                                                                                                         |
| Selezionare:<br/>         | Posizionare il puntatore su un oggetto selezionabile specifico e premere e rilasciare un pulsante del mouse.<br/>                                                                                                                                                                                                                        | Per i singoli clic con il pulsante primario, selezionare l'oggetto . Se gli utenti trascinano il mouse, selezionare un intervallo contiguo di oggetti. Per fare doppio clic con il pulsante primario, selezionare l'oggetto ed eseguire il comando predefinito.<br/> Per il testo, il pulsante destro del mouse primario imposta il punto di inserimento, il secondo seleziona la parola nel punto di inserimento e il terzo clic seleziona la frase o il paragrafo.<br/> |
| Premendo<br/>          | Posizionare il puntatore su un oggetto specifico e premere un pulsante del mouse senza rilasciare.<br/>                                                                                                                                                                                                                              | Per le funzioni di ripetizione automatica , ad esempio la pressione di una freccia di scorrimento per scorrere continuamente, attivare ripetutamente. In caso contrario, indica l'inizio di uno spostamento, un ridimensionamento, una divisione o un trascinamento, a meno che non sia seguito da una versione senza spostamento.<br/>                                                                                                                                                                                               |
| Wheeling<br/>          | Spostare la rotellina del mouse.<br/>                                                                                                                                                                                                                                                                                                  | La finestra scorre verticalmente in direzione dello spostamento della rotellina del mouse.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Forme puntatore

La tabella seguente descrive le forme e gli utilizzi comuni del puntatore.

| Forma | Nome | Quando si usa |
|:---|:---|:---|
| ![Screenshot del puntatore con forma a freccia ](images/inter-mouse-image5.png)<br/>           | Selezione normale<br/>    | Usato per la maggior parte degli oggetti.<br/>                                             |
| ![Screenshot della mano con puntamento dell'indice ](images/inter-mouse-image6.png)<br/>    | Selezione collegamento<br/>      | Usato per collegamenti di testo e grafica a causa della loro scarsa convenienza.<br/> |
| ![Screenshot del puntatore con forma i-beam ](images/inter-mouse-image7.png)<br/>          | Selezione del testo<br/>      | Usato per il testo per indicare una posizione tra i caratteri.<br/>           |
| ![Screenshot del puntatore con forma di segno più di grandi dimensioni ](images/inter-mouse-image8.png)<br/> | Selezione precisione<br/> | Usato per l'interazione grafica e altre interazioni bidimensionali.<br/>            |

### <a name="compound-mouse-interactions"></a>Interazioni composte del mouse

Nella tabella seguente vengono descritte le interazioni comuni con il mouse.

| Azione composta | Interazione | Effetto tipico | Pointers |
|:---|:---|:---|:---|
| spostarsi<br/>                | Se lo spostamento è una modalità (immessa inviando un comando), immettere la modalità, posizionare il puntatore su un oggetto mobile, premere il pulsante e spostare il mouse, rilasciare il pulsante del mouse. In questo caso, il puntatore cambia forma per indicare la modalità.<br/> In caso contrario, posizionare il puntatore sul grabber di un oggetto mobile, premere il pulsante e spostare il mouse, rilasciare il pulsante del mouse. In questo caso, il puntatore non deve cambiare forma.<br/> | L'oggetto si sposta nella direzione dello spostamento del puntatore.<br/>            | spostamento<br/> ![Screenshot del puntatore con quattro frecce ](images/inter-mouse-image9.png)<br/> utilizzato per spostare una finestra in qualsiasi direzione.<br/> pan<br/> ![Screenshot del puntatore con la forma della mano ](images/inter-mouse-image10.png)<br/> Usato per spostare un oggetto all'interno di una finestra in qualsiasi direzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ridimensionamento<br/>              | Posizionare il puntatore su un bordo ridimensionabile o un quadratino di ridimensionamento, premere un pulsante del mouse e spostare il mouse e quindi rilasciare il pulsante del mouse.<br/>                                                                                                                                                                                                                                                                                 | L'oggetto viene ridimensionato in direzione dello spostamento del puntatore.<br/>          | ridimensionamento verticale e orizzontale<br/> ![Screenshot che mostra i puntatori verso l'alto verso il basso.](images/inter-mouse-image11.png)![Screenshot dei puntatori verso l'alto e a destra a sinistra ](images/inter-mouse-image12.png)<br/> utilizzato per ridimensionare una singola dimensione.<br/> ridimensionamento diagonale<br/> ![bb545459.mouse13(en-us,msdn.10).png](images/inter-mouse-image13.png)![Screenshot di puntatori diagonali con punte della freccia](images/inter-mouse-image14.png)<br/> utilizzato per ridimensionare contemporaneamente due dimensioni.<br/> ridimensionamento di righe e colonne<br/> ![bb545459.mouse15(en-us,msdn.10).png](images/inter-mouse-image15.png)![Screenshot dei puntatori a freccia con barra incrociata ](images/inter-mouse-image16.png)<br/> Consente di ridimensionare una riga o una colonna in una griglia.<br/> |
| Separazione in corso<br/>             | Posizionare il puntatore su una barra di divisione, premere un pulsante del mouse e spostare il mouse e quindi rilasciare il pulsante del mouse.<br/>                                                                                                                                                                                                                                                                                                          | Il bordo del riquadro di divisione si sposta nella direzione dello spostamento del puntatore.<br/> | separatori delle finestre<br/> ![bb545459.mouse17(en-us,msdn.10).png](images/inter-mouse-image17.png)![Screenshot dei puntatori a forma di freccia con doppia barra incrociata ](images/inter-mouse-image18.png)<br/> Consente di ridimensionare un riquadro di divisione verticalmente o orizzontalmente.<br/> |
| Trascinando e rilasciando le immagini selezionate<br/> | Posizionare il puntatore su un oggetto valido per il trascinamento, premere un pulsante del mouse e spostare il mouse su una destinazione di rilascio e quindi rilasciare il pulsante del mouse.<br/> | l'oggetto viene spostato o copiato nella destinazione di rilascio.<br/>             | normal select<br/> ![Screenshot di foto, puntatore standard e suggerimento ](images/inter-mouse-image19.png)<br/> utilizzato su destinazioni di trascinamento valide. può anche avere un infotip per indicare un effetto specifico.<br/> non disponibile<br/> ![Screenshot dell'icona piccola bloccata/offline ](images/inter-mouse-image20.png)<br/> Usato per indicare che una superficie non è una destinazione di rilascio valida.<br/> |

### <a name="activity-indicators"></a>Indicatori di attività

La tabella seguente mostra i puntatori visualizzati dagli utenti quando eseguono un'azione che richiede più di un paio di secondi per il completamento.

| Forma | Nome | Quando si usa |
|:---|:---|:---|
| ![Screenshot che mostra un puntatore "occupato" a forma di anello.](images/inter-mouse-image21.png)<br/>          | Puntatore occupato<br/>                  | Usato per attendere che una finestra diventi reattiva.<br/>                                  |
| ![Screenshot del puntatore a forma di ciambella e della freccia](images/inter-mouse-image22.png)<br/> | Utilizzo del puntatore in background<br/> | Usato per puntare, fare clic, premere o selezionare mentre un'attività viene completata in background.<br/> |

### <a name="hand-pointers"></a>Puntatori a mano

I collegamenti di testo e grafica usano un puntatore a forma di mano o "selezione collegamento" (una mano con il dito indice che punta ![Screenshot della mano con puntamento dell'indice ](images/inter-mouse-image6.png)) a causa della loro debole convenienza. Anche se i collegamenti possono avere altri indizi visivi per indicare che si tratta di collegamenti (ad esempio sottolineature e posizionamento speciale), la visualizzazione del puntatore a forma di mano al passaggio del mouse è l'indicazione definitiva di un collegamento.

**Per evitare confusione, è fondamentale non usare il puntatore a forma di mano per altri scopi.** Ad esempio, i pulsanti di comando hanno già una forte convenienza, quindi non necessitano di un puntatore a forma di mano. Il puntatore a forma di mano deve significare "questa destinazione è un collegamento" e altro ancora.

### <a name="custom-pointers"></a>Puntatori personalizzati

Windows supporta la creazione di puntatori personalizzati. Per altre informazioni, vedere [Impostazione dell'immagine del cursore e](../learnwin32/setting-the-cursor-image.md) [input dell'utente: esempio esteso](../learnwin32/user-input--extended-example.md).

Molte applicazioni forniscono una tavolozza di controlli con puntatori personalizzati per supportare le funzionalità dell'applicazione.

![Screenshot della tavolozza con puntatore a spray-can ](images/inter-mouse-image23.png)

*Microsoft Paint include una tavolozza di funzioni diverse, ognuna con un puntatore univoco*

### <a name="fitts-law"></a>Legge di Fitts

La legge di Fitts è un principio noto nella progettazione grafica dell'interfaccia utente che essenzialmente indica:

- Più lontano è una destinazione, più tempo è necessario per acquisirla con il mouse.
- Più piccola è la destinazione, maggiore è il tempo necessario per acquisirla con il mouse.

Di conseguenza, le destinazioni di grandi dimensioni sono buone. Assicurarsi di rendere selezionabile l'intera area di destinazione.

| Risposta errata | Corretto (l'intera destinazione è selezionabile) |
|:---|:---|
| ![Screenshot dell'icona con solo etichetta selezionabile ](images/inter-mouse-image24.png) | ![Screenshot dell'icona selezionabile e dell'etichetta selezionabile ](images/inter-mouse-image25.png) |

È possibile modificare dinamicamente le dimensioni di una destinazione quando si punta per semplificare l'acquisizione.

![Screenshot della mappa caratteri con numero ingrandito ](images/inter-mouse-image26.png)

*Una destinazione diventa più grande quando l'utente punta per semplificare l'acquisizione*

E anche le destinazioni di chiusura sono buone. Individuare gli elementi selezionabili nelle vicinanze della posizione in cui è più probabile che verranno usati. Nell'immagine seguente la tavolozza dei colori è troppo distante dal selettore degli strumenti.

![Screenshot della tavolozza dei colori separata dagli strumenti ](images/inter-mouse-image27.png)

*La tavolozza dei colori è troppo distante dalla posizione in cui è probabile che sia usata*

Si consideri il fatto che la posizione corrente del puntatore dell'utente è la più vicina possibile a una destinazione, rendendo semplice l'acquisizione. Di conseguenza, i menu di scelta rapida sfruttano appieno la legge di Fitts, così come le mini barre degli strumenti usate Microsoft Office.

![Screenshot dei puntatori nell'elenco a discesa ](images/inter-mouse-image28.png)

*La posizione corrente del puntatore è sempre la più semplice da acquisire*

Prendere in considerazione anche dispositivi di input alternativi quando si determinano le dimensioni degli oggetti. Ad esempio, le dimensioni minime di destinazione consigliate per il tocco sono 23x23 pixel (13 dLU x 13).

### <a name="environments-without-a-mouse"></a>Ambienti senza mouse

Non tutti gli Windows hanno un mouse. Ad esempio, i chioschi in modalità tutto schermo raramente hanno un mouse e in genere hanno invece un touchscreen. Ciò significa che gli utenti possono eseguire interazioni semplici, ad esempio facendo clic con il pulsante sinistro del mouse e trascinandoli. Tuttavia, non possono passare il mouse, fare clic con il pulsante destro del mouse o fare doppio clic. Questa situazione è facile da progettare perché queste limitazioni sono in genere note in anticipo.

L'uso di un mouse richiede competenze motorie fine e, di conseguenza, non tutti gli utenti possono usare il mouse. Per rendere il software accessibile al pubblico più ampio, assicurarsi che tutte le interazioni per cui non sono essenziali le competenze motorie possano essere eseguite usando la tastiera.

Per altre informazioni e linee guida, vedere [Accessibilità.](inter-accessibility.md)

**Se si eservino solo quattro operazioni...**

1.  Fornire comportamenti coerenti con le interazioni del mouse con i relativi effetti standard, usando i puntatori standard quando appropriato.
2.  Limitare le interazioni avanzate del mouse (quelle che richiedono clic con il pulsante destro del mouse, più clic o tasti di modifica) alle attività avanzate destinate agli utenti avanzati.
3.  Assegnare interazioni avanzate del mouse a comportamenti coerenti e prevedibili in modo che possano essere usati in modo efficace.
4.  Assicurarsi che il programma sia in grado di invertire o correggere eventuali azioni indesiderate, in particolare per i comandi distruttivi. Le azioni accidentali sono più probabili quando si usa la manipolazione diretta.

## <a name="guidelines"></a>Indicazioni

### <a name="click-affordance"></a>Fare clic su affordance

- **Non richiedere mai agli utenti di fare clic su un oggetto per determinare se è selezionabile.** Gli utenti devono essere in grado di determinare la possibilità di fare clic solo tramite l'ispezione visiva.
  - L'interfaccia utente principale, ad esempio i pulsanti di commit, deve avere un affordance di clic statico. Gli utenti non devono passare il puntatore del mouse per individuare l'interfaccia utente primaria.
  - L'interfaccia utente secondaria, ad esempio i comandi secondari o i controlli di divulgazione progressiva, può visualizzare l'affordance del clic al passaggio del mouse.
  - [I collegamenti di](ctrl-links.md) testo dovrebbero suggerire in modo statico il testo del collegamento, quindi visualizzare l'affordance del clic (sottolineatura o altra modifica della presentazione, con il puntatore [della](#hand-pointers)mano) al passaggio del mouse.
  - [I collegamenti grafici visualizzano](ctrl-links.md) solo un puntatore del mouse al passaggio del mouse.
- **Usare il puntatore della mano (o "selezione collegamento") solo per i collegamenti di testo e grafici.** In caso contrario, gli utenti devono fare clic sugli oggetti per determinare se sono collegamenti.

### <a name="standard-mouse-button-interactions"></a>Interazioni standard con i pulsanti del mouse

La tabella seguente riepiloga le interazioni con i pulsanti del mouse che si applicano nella maggior parte dei casi:



| Interazione                                    | Effetto                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passaggio del mouse<br/>                    | La destinazione visualizza la descrizione comando, la descrizione comando o l'equivalente.<br/>                                                                                                                                                                                           |
| Singolo clic con il pulsante sinistro del mouse<br/>        | Attiva o seleziona l'oggetto. Per il testo, imposta il punto di inserimento.<br/>                                                                                                                                                                           |
| Singolo clic con il pulsante destro del mouse<br/>       | Seleziona l'oggetto e visualizza il relativo menu di scelta rapida.<br/>                                                                                                                                                                                              |
| Doppio clic con il pulsante sinistro del mouse<br/>        | Attiva o seleziona l'oggetto ed esegue il comando predefinito. Per il testo, seleziona la parola nel punto di inserimento (un terzo clic seleziona la frase o il paragrafo).<br/>                                                                            |
| Doppio clic con il pulsante destro del mouse<br/>       | Uguale al singolo clic con il pulsante destro del mouse.<br/>                                                                                                                                                                                                                    |
| Maiusc singolo clic con il pulsante sinistro del mouse<br/>  | Per gli oggetti selezionabili, estende in modo contiguo la selezione. In caso contrario, come un singolo clic con il pulsante sinistro del mouse con possibili modifiche. Ad esempio, in Paint, il disegno di un ovale con il modificatore di tasto MAIUSC comporta il disegno di un cerchio.<br/>                  |
| Maiusc singolo clic con il pulsante destro del mouse<br/> | Uguale a MAIUSC singolo clic con il pulsante sinistro del mouse.<br/>                                                                                                                                                                                                               |
| Doppio clic con MAIUSC<br/>  | Come maiusc singolo clic sinistro ed esegue il comando predefinito sull'intera selezione.<br/>                                                                                                                                                     |
| Doppio clic con il pulsante destro del mouse<br/> | Uguale a MAIUSC singolo clic con il pulsante sinistro del mouse.<br/>                                                                                                                                                                                                               |
| CTRL singolo clic con il pulsante sinistro del mouse<br/>   | Per gli oggetti selezionabili, estende la selezione impostando lo stato di selezione dell'elemento selezionato senza influire sulla selezione di altri oggetti (consentendo quindi la selezione non contigua). In caso contrario, uguale al singolo clic con il pulsante sinistro del mouse.<br/> |
| Ctrl singolo clic con il pulsante destro del mouse<br/>  | Uguale a CTRL singolo clic con il pulsante sinistro del mouse.<br/>                                                                                                                                                                                                                |
| CTRL doppio clic con il pulsante sinistro del mouse<br/>   | Come ctrl singolo clic sinistro ed esegue il comando predefinito sull'intera selezione.<br/>                                                                                                                                                      |
| Ctrl doppio clic con il pulsante destro del mouse<br/>  | Uguale a CTRL singolo clic con il pulsante sinistro del mouse.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Interazione con il mouse

- **Impostare come destinazione del clic almeno 16x16 pixel in modo che possano essere facilmente selezionate da qualsiasi dispositivo di input.** Per [il tocco,](inter-touch.md)la dimensione minima consigliata per il controllo è 23x23 pixel (DLU 13x13). Prendere in considerazione la possibilità di modificare dinamicamente le dimensioni delle destinazioni di piccole dimensioni quando l'utente punta per semplificarne l'acquisizione.

    In questo esempio i pulsanti di selezione sono troppo piccoli per essere usati in modo efficace con il tocco o una penna.

    ![Screenshot del controllo di selezione con frecce piccole ](images/inter-mouse-image29.png) 

- **Creare separatori di almeno cinque pixel di larghezza in modo che possano essere facilmente selezionati da qualsiasi dispositivo di input.** Prendere in considerazione la possibilità di modificare dinamicamente le dimensioni delle destinazioni di piccole dimensioni quando l'utente punta per semplificarne l'acquisizione.

    In questo esempio la barra di divisione nel riquadro di spostamento Windows Explorer è troppo stretta per essere usata in modo efficace con un mouse o una penna.

    ![Screenshot della barra di divisione stretta e quasi invisibile ](images/inter-mouse-image30.png)

- **Fornire agli utenti un margine di errore a livello spaziale.** Consentire uno spostamento del mouse (ad esempio, tre pixel) quando gli utenti rilasciano un pulsante del mouse. A volte gli utenti spostano leggermente il mouse mentre rilasciano il pulsante del mouse, quindi la posizione del mouse prima del rilascio del pulsante riflette meglio l'intenzione dell'utente rispetto alla posizione subito dopo.
- **Fornire agli utenti un margine di errore temporale.** Usare la velocità del doppio clic del sistema per distinguere tra clic singoli e doppio clic.
- **Fare in modo che i clic abbia effetto sul pulsante del mouse verso l'alto.** Consente agli utenti di abbandonare le azioni del mouse rimuovendo il mouse dalle destinazioni valide prima di rilasciare il pulsante del mouse. Per la maggior parte delle interazioni con il mouse, la pressione di un pulsante del mouse indica solo la destinazione selezionata e il rilascio del pulsante attiva l'azione. Le funzioni di ripetizione automatica , ad esempio la pressione di una freccia di scorrimento per scorrere continuamente, sono un'eccezione.
- [Acquisire il mouse per](/windows/win32/api/winuser/nf-winuser-setcapture) la selezione, lo spostamento, il ridimensionamento, la suddivisione e il trascinamento.
- Usare il tasto ESC per consentire agli utenti di abbandonare interazioni composte del mouse, ad esempio spostamento, ridimensionamento, suddivisione e trascinamento.
- **Se un oggetto non supporta i doppio clic, ma è probabile che gli utenti presuppongono che lo sia, interpretare un "doppio clic" come un singolo clic.** Si supponga che l'utente intende una singola azione anziché due.

    Poiché è probabile che gli utenti presuppongono che i pulsanti della barra delle applicazioni supportino i doppio clic, un "doppio clic" deve essere gestito come un singolo clic.

    ![Screenshot del pulsante della barra delle applicazioni e del puntatore standard ](images/inter-mouse-image31.png)

- **Ignorare i clic ridondanti del mouse mentre il programma è inattivo.** Ad esempio, se l'utente fa clic su un pulsante 10 volte mentre un programma è inattivo, interpretarlo come un singolo clic.
- **Non usare doppie operazioni di trascinamento o accordi.** Un doppio trascinamento è un'azione di trascinamento avviata con un doppio clic e un accordo è quando più pulsanti del mouse vengono premuti contemporaneamente. Queste interazioni non sono standard, non sono individuabili, sono difficili da eseguire e molto probabilmente vengono eseguite accidentalmente.
- **Non usare ALT come modificatore per le interazioni con il mouse.** Il tasto ALT è riservato per l'accesso alla barra degli strumenti e i tasti di scelta.
- **Non usare MAIUSC+CTRL come modificatore per le interazioni con il mouse.** In questo modo sarebbe troppo difficile da usare.
- **Rendere ridondante il passaggio del mouse.** Per rendere il programma toccabile, sfruttare appieno il passaggio del mouse, ma solo in modi che non sono necessari per eseguire un'azione. Ciò significa in genere che un'azione può essere eseguita anche facendo clic, ma non necessariamente nello stesso modo. Il passaggio del mouse non è supportato dalla maggior parte delle tecnologie di tocco, quindi gli utenti con tali touchscreen non possono eseguire attività che richiedono il passaggio del mouse.

### <a name="mouse-wheel"></a>Rotellina del mouse

- **Fare in modo che la rotellina del mouse influisca sul controllo, sul riquadro o sulla finestra su cui si trova attualmente il puntatore.** In questo modo si evitano risultati imprevisti.
- **Rendere effettiva la rotellina del mouse senza fare clic o avere lo stato attivo per l'input.** Il passaggio del mouse è sufficiente.
- **Fare in modo che la rotellina del mouse influisca sull'oggetto con l'ambito più specifico.** Ad esempio, se il puntatore è posizionato su un controllo casella di riepilogo scorrevole in un riquadro scorrevole all'interno di una finestra scorrevole, la rotellina del mouse influisce sul controllo casella di riepilogo.
- **Non modificare lo stato attivo di input quando si usa la rotellina del mouse.**
- Assegnare alla rotellina del mouse gli effetti seguenti:
  - Per finestre, riquadri e controlli scorrevoli:
    - **La rotazione della rotellina del mouse scorre l'oggetto verticalmente, dove la rotazione verso l'alto scorre verso l'alto.** Affinché la rotellina abbia un mapping naturale, la rotazione della rotellina del mouse non deve mai scorrere orizzontalmente perché questa operazione è disorientante e imprevista.
      - **Se si preme CTRL,** ruotando la rotellina del mouse viene ingrandito l'oggetto, mentre la rotazione verso l'alto consente di eseguire lo zoom avanti e la rotazione verso il basso.
      - **L'inclinazione della rotellina del mouse scorre l'oggetto orizzontalmente.**
  - Per finestre e riquadri ingrandibili (senza barre di scorrimento):
    - **Ruotando la rotellina del mouse viene ingrandito** l'oggetto, in cui la rotazione verso l'alto consente di ingrandire e ruotare verso il basso.
    - L'inclinazione della rotellina del mouse non ha alcun effetto.
  - Per le schede:
    - **Ruotando la rotellina del mouse è** possibile modificare la scheda corrente, indipendentemente dall'orientamento delle schede.
    - L'inclinazione della rotellina del mouse non ha alcun effetto.
  - Se i tasti MAIUSC e ALT sono premuto, la rotellina del mouse non ha alcun effetto.
- **Usare le Windows di sistema per le dimensioni di scorrimento verticale (per la rotazione) e le dimensioni di scorrimento orizzontale (per l'inclinazione).** Queste impostazioni possono essere configurate tramite l'elemento Del pannello di controllo del mouse.
- **La rotazione più rapida della rotellina del mouse comporta uno scorrimento più rapido.** In questo modo, gli utenti possono scorrere documenti di grandi dimensioni in modo più efficiente.
- **Per le finestre scorrevoli, è consigliabile fare clic sul pulsante della rotellina del mouse per posizionare la finestra in "modalità lettore".** La modalità lettore attiva una speciale icona di origine di scorrimento e scorre la finestra in una direzione e una velocità rispetto all'origine di scorrimento.

![Screenshot della pagina con l'icona dell'origine di scorrimento ](images/inter-mouse-image32.png)

*Internet Explorer supporta la modalità lettore, che include l'icona dell'origine di scorrimento*

### <a name="hiding-the-pointer"></a>Nascondere il puntatore

- **Non nascondere il puntatore.** Eccezioni:
  - Le applicazioni di presentazione in esecuzione in modalità presentazione a schermo intero possono nascondere il puntatore. Tuttavia, il puntatore deve essere ripristinato immediatamente quando gli utenti spostano il mouse e possono essere riattivati dopo due secondi di inattività.
  - Gli ambienti senza mouse(ad esempio chioschi) possono nascondere in modo permanente il puntatore.
- Per impostazione predefinita, Windows il puntatore mentre l'utente digita in una casella di testo. Questa Windows di sistema è configurabile tramite l'elemento Del pannello di controllo del mouse.

### <a name="activity-pointers"></a>Puntatori all'attività

I puntatori all'attività Windows sono il puntatore occupato (![Screenshot del puntatore a forma di ciambella ](images/inter-mouse-image33.png)) e il puntatore in background funzionante (![Screenshot del puntatore a forma di ciambella e della freccia ](images/inter-mouse-image34.png)).

- Visualizzare il puntatore occupato quando gli utenti devono attendere più di un secondo per il completamento di un'azione. Si noti che il puntatore occupato non ha un'area sensibile, quindi gli utenti non possono fare clic su alcun elemento mentre viene visualizzato.
- Visualizzare il puntatore in background quando gli utenti devono attendere più di un secondo per il completamento di un'azione, ma il programma è reattivo e non sono presenti altri commenti visivi che l'azione non sia stata completata.
- Non combinare i puntatori di attività con le barre di stato o le animazioni di stato.

### <a name="caret"></a>Cursore

- **Non visualizzare il punto di inserimento finché la finestra o il controllo di input di testo non ha lo stato attivo per l'input.** Il punto di inserimento suggerisce agli utenti lo stato attivo per l'input, ma una finestra o un controllo può visualizzare il punto di inserimento senza lo stato attivo per l'input. Naturalmente, non rubare lo stato attivo per l'input in modo che una finestra di dialogo fuori contesto possa visualizzare il punto di inserimento.

    Il Windows Gestione credenziali viene visualizzato fuori contesto con il punto di inserimento, ma senza lo stato attivo per l'input. Di conseguenza, gli utenti finiscono per digitare la password in posizioni impreviste.

    ![Screenshot di Gestione credenziali senza stato attivo ](images/inter-mouse-image35.png)

- **Posizionare il punto di in cui gli utenti hanno più probabilità di digitare per primi.** In genere si tratta dell'ultima posizione in cui l'utente stava digitando o alla fine del testo.

### <a name="accessibility"></a>Accessibilità

- Per gli utenti che non possono usare il mouse, rendere il mouse ridondante con la tastiera.
  - Gli utenti devono essere in grado di eseguire qualsiasi operazione con la tastiera possibile con il mouse, ad eccezione delle azioni per le quali sono essenziali competenze motorie, ad esempio il disegno e il gioco.
  - Gli utenti devono essere in grado di eseguire tutte le operazioni che possono usare con la tastiera, ad eccezione dell'immissione efficiente del testo.
- Per gli utenti con capacità limitata di usare il mouse:
  - Non fare doppio clic e trascinare l'unico modo per eseguire un'azione.

Per altre informazioni e linee guida, vedere [Accessibilità](inter-accessibility.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento al mouse:

- Evitare di usare i topi plurali; se è necessario fare riferimento a più mouse, usare i dispositivi mouse.
- Usare il pulsante del mouse per indicare il pulsante sinistro del mouse. Non usare il pulsante primario del mouse. Analogamente, usare il pulsante destro del mouse anziché il pulsante secondario del mouse. Indipendentemente dall'accuratezza, gli utenti comprendono questi termini e gli utenti che riprogrammano i pulsanti fanno il cambiamento mentale.
- Usare la rotellina per la parte di rotazione della rotellina del mouse e il pulsante della rotellina per fare riferimento alla parte selezionabile.
- Usare verbi come clic, punto e trascinamento per fare riferimento alle azioni del mouse. Gli utenti ruotano la rotellina verticalmente, la inclinano orizzontalmente e fare clic sul pulsante della rotellina.
- Usare il trascinamento, non il trascinamento della selezione, per l'azione di spostamento di un documento o di una cartella. È accettabile usare il trascinamento della selezione come aggettivo, come in "lo spostamento della cartella è un'operazione di trascinamento della selezione".
- Sillabare sempre il doppio clic e fare clic con il pulsante destro del mouse come verbi.
- Usare click, non fare clic su. Fare clic su (come in "fare clic nella finestra") è accettabile.

Quando si fa riferimento ai puntatori del mouse:

- Fare riferimento al puntatore del mouse come puntatore. Usare il cursore solo nella documentazione tecnica.
- Per i puntatori con indicatori di attività, usare il puntatore occupato per il puntatore costituito solo da un indicatore di attività e lavorare in background per il puntatore di combinazione e l'indicatore di attività.
- Per gli altri tipi di puntatori, non usare etichette descrittive per fare riferimento al puntatore. Se necessario, usare un elemento grafico per descrivere come può essere visualizzato il puntatore del mouse sullo schermo.

**Esempi:**

- Posizionare il punto sul bordo della finestra.
- Con il mouse fare clic sul **pulsante Riduci a** icona.
- Tenere premuto MAIUSC e fare clic con il pulsante destro del mouse.
- Quando il puntatore diventa un ![Screenshot della freccia con due barre incrociate](images/inter-mouse-image18.png), trascinare il puntatore per spostare la linea di divisione.

## <a name="see-also"></a>Vedi anche

- [Linee guida per l'interazione con l'accessibilità](inter-accessibility.md)
- [Linee guida per l'interazione tramite tocco](inter-touch.md)
- [Linee guida per l'interazione con la penna](inter-pen.md)
- [Collegamenti di testo](ctrl-links.md)
- [Collegamenti grafici](ctrl-links.md)
- [Acquisire il mouse](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Impostazione dell'immagine del cursore](../learnwin32/setting-the-cursor-image.md)
- [Input utente: esempio esteso](../learnwin32/user-input--extended-example.md)