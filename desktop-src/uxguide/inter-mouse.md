---
title: Mouse e puntatori
description: Il mouse è il dispositivo di input primario usato per interagire con gli oggetti di Windows.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6462c69216ee9acb5149a01a805503cea721bb1c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968833"
---
# <a name="mouse-and-pointers"></a>Mouse e puntatori

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Il mouse è il dispositivo di input primario usato per interagire con gli oggetti di Windows. La funzionalità del mouse può includere anche altri dispositivi di puntamento, ad esempio le trackball, i touchpad e i puntatori incorporati nei computer notebook, le penne usate con la tecnologia Windows Tablet and touch e, nei computer con touchscreen, anche il dito dell'utente.

> [!NOTE]
> Le linee guida relative ad [accessibilità](inter-accessibility.md), [penna](inter-pen.md)e [tocco](inter-touch.md) sono presentate in articoli distinti.

Lo spostamento fisico del mouse sposta il puntatore grafico (noto anche come cursore) sullo schermo. Il puntatore ha diverse forme per indicare il comportamento corrente.

![Screenshot di cinque puntatori del mouse tipici ](images/inter-mouse-image1.png)

*Puntatori del mouse tipici*

I dispositivi mouse hanno spesso un pulsante principale (in genere il pulsante sinistro), un pulsante secondario (in genere il destro) e una rotellina del mouse tra i due. Posizionando il puntatore e facendo clic sui pulsanti primario e secondario sul mouse, gli utenti possono selezionare oggetti ed eseguire azioni su di essi. Per la maggior parte delle interazioni, premendo un pulsante del mouse mentre il cursore si trova su una destinazione viene indicata la destinazione selezionata e il rilascio del pulsante esegue qualsiasi azione associata alla destinazione.

Tutti i puntatori, ad eccezione del puntatore occupato, hanno una posizione sensibile a un solo pixel che definisce la posizione esatta dello schermo del mouse. L'area sensibile determina l'oggetto interessato dalle azioni del mouse. Gli oggetti definiscono una zona sensibile, ovvero l'area in cui l'area sensibile è considerata sull'oggetto. In genere, la zona sensibile coincide con i bordi di un oggetto, ma potrebbe essere più grande per semplificare l'esecuzione dell'intento dell'utente.

Il punto di inserimento è la barra verticale lampeggiante visualizzata quando l'utente digita una casella di testo o un altro editor di testo. Il punto di inserimento è indipendente dal puntatore (per impostazione predefinita, Windows nasconde il puntatore mentre l'utente sta digitando).

![screenshot della casella di testo con cursore ](images/inter-mouse-image2.png)

*Punto di inserimento*

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="the-mouse-is-intuitive"></a>Il mouse è intuitivo

Il mouse è stato un dispositivo di input con successo perché è facile da usare per la mano umana comune. L'interazione basata su puntatore è stata completata perché è intuitiva e offre un'ampia gamma di esperienze.

**Gli oggetti dell'interfaccia utente (interfaccia utente) ben progettati si affermano di avere la convenienza, ovvero proprietà visive e comportamentali di un oggetto che suggerisce come viene usato.** Il puntatore funge da proxy per la mano, consentendo agli utenti di interagire con gli oggetti dello schermo in modo analogo agli oggetti fisici. Gli utenti hanno una conoscenza approfondita del funzionamento della mano umana, quindi, se è possibile che si verifichi un push, si tenta di effettuare il push. Se sembra che possa essere afferrato, cerchiamo di afferrarlo. Di conseguenza, gli utenti possono scoprire come usare gli oggetti con una grande convenienza semplicemente esaminando tali oggetti e provandoli.

![Screenshot di un pulsante e di un dispositivo di scorrimento](images/inter-mouse-image3.png)

*I pulsanti e i dispositivi di scorrimento hanno una grande convenienza*

Al contrario, gli oggetti con una scarsa convenienza sono più difficili da capire. Tali oggetti spesso richiedono un'etichetta o un'istruzione per illustrarli.

![screenshot del testo del collegamento e dell'icona di Internet Earth](images/inter-mouse-image4.png)

*il testo del collegamento e le icone hanno una scarsa convenienza*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Alcuni aspetti dell'uso del mouse non sono intuitivi

**Facendo clic con il pulsante destro del mouse, facendo doppio clic su di esso e scegliendo con i modificatori di tasto MAIUSC o CTRL sono presenti tre interazioni con il mouse non intuitive**, perché non hanno controparti reali. Diversamente dalle scelte rapide da tastiera e dalle chiavi di accesso, queste interazioni del mouse non sono in genere documentate in qualsiasi punto dell'interfaccia Questo suggerisce che è necessario fare clic con il pulsante destro del mouse, fare doppio clic e i modificatori di tastiera non devono essere necessari per eseguire le attività di base, specialmente per gli utenti esperti. Suggerisce anche che queste interazioni avanzate devono avere un comportamento coerente e prevedibile da usare in modo efficace.

### <a name="single-click-or-double-click"></a>Fare clic su un solo clic o su un doppio clic?

Il doppio clic viene utilizzato in modo estensivo sul desktop di Windows che potrebbe non sembrare un'interazione avanzata. Ad esempio, l'apertura di cartelle, programmi o documenti nel riquadro file di Esplora risorse viene eseguita facendo doppio clic. L'apertura di un collegamento sul desktop di Windows usa anche il doppio clic. Al contrario, l'apertura di cartelle o programmi nel menu Start richiede un solo clic.

Gli oggetti selezionabili utilizzano un solo clic per eseguire la selezione, quindi richiedono un doppio clic per l'apertura, mentre gli oggetti non selezionabili richiedono un solo clic per l'apertura. Questa distinzione non è riconosciuta da molti utenti (facendo clic sull'icona di un programma si fa clic sull'icona di un programma, giusto?) e, di conseguenza, alcuni utenti continuano a fare clic sulle icone fino a ottenere quello che desiderano.

### <a name="direct-manipulation"></a>Manipolazione diretta

L'interazione con gli oggetti direttamente viene definita manipolazione diretta. Il puntamento, il clic, la selezione, lo spostamento, il ridimensionamento, la suddivisione, lo scorrimento, la panoramica e lo zoom sono modifiche dirette comuni. Al contrario, l'interazione con un oggetto tramite la finestra proprietà o un'altra finestra di dialogo potrebbe essere descritta come manipolazione indiretta.

**Tuttavia, se è presente una manipolazione diretta, è possibile che si verifichi una manipolazione accidentale e quindi la necessità di un perdono.** Il perdono è la possibilità di invertire o correggere facilmente un'azione indesiderata. Si apportano modifiche dirette con l'annullamento, fornendo un buon feedback visivo e consentendo agli utenti di correggere facilmente gli errori. Associato al perdono impedisce che si verifichino azioni indesiderate, che è possibile eseguire usando controlli vincolati e conferme per azioni rischiose o comandi con conseguenze impreviste.

### <a name="standard-mouse-button-interactions"></a>Interazioni con il pulsante del mouse standard

Le interazioni standard del mouse dipendono da diversi fattori, tra cui il tasto del mouse selezionato, il numero di volte in cui viene fatto clic, la relativa posizione durante i clic e se sono stati premuti i modificatori di tastiera. Di seguito è riportato un riepilogo del modo in cui questi fattori influiscono in genere sull'interazione:

- Per la maggior parte degli oggetti, facendo doppio clic su viene eseguito un solo clic sinistro e viene eseguito il comando predefinito. Il comando predefinito viene identificato nel menu di scelta rapida.
- Per alcuni tipi di oggetti selezionabili, ogni clic espande l'effetto del clic. Ad esempio, se si fa clic con il pulsante destro del mouse in una casella di testo viene impostato il percorso di input, si fa doppio clic su Seleziona una parola e si fa clic su una frase o un paragrafo.
- Facendo clic con il pulsante destro del mouse viene visualizzato il menu di scelta rapida dell'oggetto
- Mantenendo il mouse mentre si puntano i risultati al passaggio del mouse.
- Mantenendo il mouse mentre si preme il pulsante del mouse, viene indicato il clic e la selezione di un singolo oggetto. Lo spostamento del mouse indica lo spostamento, il ridimensionamento, la suddivisione, il trascinamento e la selezione di più oggetti.
- Il tasto MAIUSC estende la selezione in modo contiguo.
- Il tasto CTRL estende la selezione impostando lo stato di selezione dell'elemento selezionato senza influire sulla selezione di altri oggetti.

### <a name="simple-mouse-interactions"></a>Interazioni semplici con il mouse

La tabella seguente descrive gli effetti e le interazioni comuni del mouse.

| Azione semplice | Interazione | Effetto tipico |
|:---|:---|:---|
| Che punta<br/>          | Posizionare il puntatore su un oggetto specifico senza fare clic sui pulsanti del mouse.<br/>                                                                                                                                                                                                                                      | Target Visualizza lo stato del passaggio del mouse e gli eventuali affordances dinamici.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Passando<br/>          | Posizionare il puntatore su un oggetto specifico senza fare clic sui pulsanti del mouse e senza lo spostamento per almeno un secondo.<br/>                                                                                                                                                                                             | Target Visualizza la descrizione comando, infotip o equivalente.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Cliccando<br/>          | Posizionare il puntatore su un oggetto specifico, non selezionabile e premere e rilasciare un pulsante del mouse senza eseguire lo spostamento. Quando si fa clic sul pulsante del mouse viene applicata la versione per consentire agli utenti di annullare il clic spostando il puntatore del mouse sulla destinazione. Quindi, la pressione del mouse indica solo la destinazione selezionata.<br/> | Per i singoli clic con il pulsante primario, attivare l'oggetto. Per i doppio clic con il pulsante primario, attivare l'oggetto ed eseguire il comando predefinito. Per il pulsante secondario, visualizzare il menu di scelta rapida dell'oggetto.<br/>                                                                                                                                                                                         |
| Selezionare:<br/>         | Posizionare il puntatore su un oggetto specifico selezionabile e premere e rilasciare un pulsante del mouse.<br/>                                                                                                                                                                                                                        | Per i singoli clic con il pulsante primario, selezionare l'oggetto. Se gli utenti trascinano il mouse, selezionare un intervallo contiguo di oggetti. Per fare doppio clic con il pulsante primario, selezionare l'oggetto ed eseguire il comando predefinito.<br/> Per il testo, il pulsante primario destro fare clic su Imposta il punto di inserimento, il secondo seleziona la parola nel punto di inserimento e il terzo clic Seleziona la frase o il paragrafo.<br/> |
| Premendo<br/>          | Posizionare il puntatore su un oggetto specifico e premere un pulsante del mouse senza rilasciare.<br/>                                                                                                                                                                                                                              | Per le funzioni di ripetizione automatica (ad esempio la pressione di una freccia di scorrimento per scorrere continuamente), attivare ripetutamente. In caso contrario, indica l'inizio di uno spostamento, un ridimensionamento, una divisione o un trascinamento, a meno che non sia seguito da una versione senza spostamento.<br/>                                                                                                                                                                                               |
| Wheeling<br/>          | Spostare la rotellina del mouse.<br/>                                                                                                                                                                                                                                                                                                  | La finestra scorre verticalmente nella direzione del movimento della rotellina del mouse.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Forme puntatore

La tabella seguente descrive le forme e gli utilizzi comuni del puntatore.

| Con forme | Nome | Quando si usa |
|:---|:---|:---|
| ![screenshot del puntatore con forma freccia ](images/inter-mouse-image5.png)<br/>           | Selezione normale<br/>    | Utilizzato per la maggior parte degli oggetti.<br/>                                             |
| ![screenshot della mano con puntatori di indice ](images/inter-mouse-image6.png)<br/>    | Seleziona collegamento<br/>      | Usato per i collegamenti di testo e grafica a causa della loro convenienza debole.<br/> |
| ![screenshot del puntatore con forma i-Beam ](images/inter-mouse-image7.png)<br/>          | Selezione testo<br/>      | Utilizzato per il testo per indicare una posizione tra i caratteri.<br/>           |
| ![screenshot del puntatore con forma di segno più grande ](images/inter-mouse-image8.png)<br/> | Selezione precisione<br/> | Usato per la rappresentazione grafica e altre interazioni bidimensionali.<br/>            |

### <a name="compound-mouse-interactions"></a>Interazioni del mouse composto

Nella tabella seguente vengono descritte le interazioni comuni del mouse.

| Azione composta | Interazione | Effetto tipico | Puntatori |
|:---|:---|:---|:---|
| Movimento<br/>                | Se lo spostamento è una modalità (immessa con un comando), immettere la modalità, posizionare il puntatore su un oggetto mobile, premere il pulsante e spostare il mouse, rilasciare il pulsante del mouse. in questo caso, il puntatore cambia forma per indicare la modalità.<br/> in caso contrario, posizionare il puntatore sul grabber di un oggetto mobile, premere il pulsante e spostare il mouse, il pulsante di rilascio del mouse. in questo caso, non è necessario che il puntatore modifichi la forma.<br/> | l'oggetto si sposta nella direzione del movimento del puntatore.<br/>            | spostamento<br/> ![screenshot del puntatore con quattro frecce ](images/inter-mouse-image9.png)<br/> utilizzato per spostare una finestra in qualsiasi direzione.<br/> pan<br/> ![screenshot del puntatore con forma mano ](images/inter-mouse-image10.png)<br/> Utilizzato per spostare un oggetto all'interno di una finestra in qualsiasi direzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ridimensionamento<br/>              | Posizionare il puntatore su un bordo ridimensionabile o un handle di ridimensionamento, premere un pulsante del mouse e spostare il mouse, quindi rilasciare il pulsante del mouse.<br/>                                                                                                                                                                                                                                                                                 | ridimensionamento dell'oggetto nella direzione del movimento del puntatore.<br/>          | ridimensionamento verticale e orizzontale<br/> ![Screenshot che mostra i puntatori di scorrimento.](images/inter-mouse-image11.png)![screenshot dei puntatori a destra e a sinistra ](images/inter-mouse-image12.png)<br/> utilizzato per ridimensionare una singola dimensione.<br/> ridimensionamento diagonale<br/> ![bb545459. mouse13 (en-US, MSDN. 10). png](images/inter-mouse-image13.png)![screenshot dei puntatori diagonali con suggerimenti freccia](images/inter-mouse-image14.png)<br/> utilizzato per ridimensionare due dimensioni simultaneamente.<br/> ridimensionamento di righe e colonne<br/> ![bb545459. mouse15 (en-US, MSDN. 10). png](images/inter-mouse-image15.png)![screenshot dei puntatori a freccia con traversa ](images/inter-mouse-image16.png)<br/> Utilizzato per ridimensionare una riga o una colonna in una griglia.<br/> |
| Separazione in corso<br/>             | Posizionare il puntatore su una barra di divisione, premere un pulsante del mouse e spostare il mouse, quindi rilasciare il pulsante del mouse.<br/>                                                                                                                                                                                                                                                                                                          | il bordo del riquadro diviso si sposta nella direzione del movimento del puntatore.<br/> | splitter finestra<br/> ![bb545459. mouse17 (en-US, MSDN. 10). png](images/inter-mouse-image17.png)![screenshot dei puntatori a freccia con doppio traversa ](images/inter-mouse-image18.png)<br/> Utilizzato per ridimensionare un riquadro suddiviso verticalmente o orizzontalmente.<br/> |
| Trascinando e rilasciando le immagini selezionate<br/> | Posizionare il puntatore su un oggetto valido per il trascinamento, premere un pulsante del mouse e spostare il mouse su un obiettivo di rilascio, quindi rilasciare il pulsante del mouse.<br/> | l'oggetto viene spostato o copiato nell'obiettivo di rilascio.<br/>             | selezione normale<br/> ![Screenshot di foto, puntatore standard e infotip ](images/inter-mouse-image19.png)<br/> utilizzato su destinazioni di trascinamento valide. può anche avere un infotip per indicare un effetto specifico.<br/> non disponibile<br/> ![screenshot dell'icona Small blocked/offline ](images/inter-mouse-image20.png)<br/> Utilizzato per indicare che una superficie non è un obiettivo di rilascio valido.<br/> |

### <a name="activity-indicators"></a>Indicatori di attività

La tabella seguente illustra i puntatori visualizzati dagli utenti quando si esegue un'azione che richiede più di un paio di secondi per il completamento.

| Con forme | Nome | Quando si usa |
|:---|:---|:---|
| ![Screenshot che mostra un puntatore ' busy ' a forma di anello.](images/inter-mouse-image21.png)<br/>          | Puntatore occupato<br/>                  | Utilizzato per attendere la reattività di una finestra.<br/>                                  |
| ![screenshot del puntatore a forma di anello e della freccia](images/inter-mouse-image22.png)<br/> | Uso del puntatore in background<br/> | Utilizzato per puntare, fare clic, premere o selezionare mentre un'attività viene completata in background.<br/> |

### <a name="hand-pointers"></a>Puntatori a mano

I collegamenti di testo e grafica utilizzano un puntatore a mano o "collegamento selezionato" (una mano con il dito dell'indice che punta ![screenshot della mano con puntatori di indice ](images/inter-mouse-image6.png)) a causa della loro convenienza debole. Anche se i collegamenti possono avere altri indizi visivi per indicare che si tratta di collegamenti, ad esempio sottolineature e posizionamento speciale, la visualizzazione del puntatore del mouse sul passaggio del mouse è l'indicazione definitiva di un collegamento.

**Per evitare confusione, è imperativo non usare il puntatore a mano per altri scopi.** Ad esempio, i pulsanti di comando hanno già una grande convenienza, quindi non necessitano di un puntatore a mano. Il puntatore a mano deve significare che "questa destinazione è un collegamento" e nient'altro.

### <a name="custom-pointers"></a>Puntatori personalizzati

Windows supporta la creazione di puntatori personalizzati. Per ulteriori informazioni, vedere [impostazione dell'immagine del cursore](../learnwin32/setting-the-cursor-image.md) e [input dell'utente: esempio esteso](../learnwin32/user-input--extended-example.md).

Molte applicazioni forniscono una tavolozza di controlli con puntatori personalizzati per supportare le funzionalità dell'applicazione.

![screenshot della tavolozza con puntatore a spruzzo ](images/inter-mouse-image23.png)

*Microsoft Paint include una tavolozza di diverse funzioni, ognuna con un puntatore univoco*

### <a name="fitts-law"></a>Legge Fitts

La legge di Fitts è un principio molto noto nell'interfaccia utente grafica di progettazione dell'interfaccia utente che essenzialmente dichiara:

- Più lontano è la destinazione, maggiore è il tempo necessario per acquisirla con il mouse.
- Minore è la destinazione, maggiore è il tempo necessario per acquisirla con il mouse.

Pertanto, le destinazioni di grandi dimensioni sono valide. Assicurarsi di fare clic sull'intera area di destinazione.

| Non corretto | Correggi (l'intera destinazione è selezionabile) |
|:---|:---|
| ![screenshot dell'icona con etichetta solo selezionabile ](images/inter-mouse-image24.png) | ![screenshot dell'icona selezionabile e dell'etichetta selezionabile ](images/inter-mouse-image25.png) |

È possibile modificare dinamicamente le dimensioni di una destinazione quando si punta a renderla più semplice da acquisire.

![screenshot della mappa dei caratteri con numero ingrandito ](images/inter-mouse-image26.png)

*Una destinazione diventa più grande quando l'utente punta a renderla più semplice da acquisire*

Anche le destinazioni di chiusura sono ottime. Individuare gli elementi selezionabili vicini alla posizione in cui verranno usati con maggiore probabilità. Nell'immagine seguente la tavolozza dei colori è troppo distante dal selettore degli strumenti.

![screenshot della tavolozza dei colori separati dagli strumenti ](images/inter-mouse-image27.png)

*La tavolozza dei colori è troppo lontano da dove è probabile che venga usata*

Si consideri il fatto che la posizione corrente del puntatore dell'utente è il più vicino possibile a una destinazione, rendendola semplice da acquisire. In questo modo, i menu di scelta rapida sfruttano appieno la legge di Fitts, così come le mini barre degli strumenti utilizzate da Microsoft Office.

![screenshot dei puntatori vicino all'elenco a discesa ](images/inter-mouse-image28.png)

*Il percorso corrente del puntatore è sempre il più semplice da acquisire*

Inoltre, prendere in considerazione i dispositivi di input alternativi per determinare le dimensioni degli oggetti. Ad esempio, la dimensione minima di destinazione consigliata per il tocco è 23x23 pixel (13x13 DLU).

### <a name="environments-without-a-mouse"></a>Ambienti senza mouse

Non tutti gli ambienti Windows hanno un mouse. Ad esempio, i chioschi hanno raramente un mouse e in genere hanno un touchscreen. Questo significa che gli utenti possono eseguire semplici interazioni, ad esempio il clic con il pulsante sinistro e il trascinamento. Tuttavia, non è possibile passare il mouse, fare clic con il pulsante destro del mouse o fare doppio clic. Questa situazione è facile da progettare per perché queste limitazioni sono generalmente note in anticipo.

L'uso di un mouse richiede competenze specifiche del motore e, di conseguenza, non tutti gli utenti possono utilizzare il mouse. Per rendere il software accessibile al pubblico più ampio, assicurarsi che tutte le interazioni per le quali non siano essenziali le competenze motorie possano essere eseguite utilizzando la tastiera.

Per ulteriori informazioni e linee guida, vedere [accessibilità](inter-accessibility.md).

**Se si eseguono solo quattro operazioni...**

1.  Offrire comportamenti di interazione con il mouse coerenti con gli effetti standard, usando i puntatori standard quando appropriato.
2.  Limitare le interazioni avanzate con il mouse, ovvero quelle che richiedono clic con il pulsante destro del mouse, più clic o tasti di modifica, per attività avanzate destinate a utenti avanzati.
3.  Assegnare comportamenti prevedibili e coerenti per le interazioni con il mouse in modo che possano essere utilizzate in modo efficiente.
4.  Verificare che il programma fornisca la possibilità di annullare o correggere le azioni indesiderate, in particolare per i comandi distruttivi. Le azioni accidentali sono più probabili quando si usa la manipolazione diretta.

## <a name="guidelines"></a>Indicazioni

### <a name="click-affordance"></a>Fare clic su offerta

- **Non richiedere mai agli utenti di fare clic su un oggetto per determinare se è selezionabile.** Gli utenti devono essere in grado di determinare la possibilità di fare clic solo tramite controllo visivo.
  - L'interfaccia utente primaria, ad esempio i pulsanti di commit, deve disporre di una convenienza di clic statica. Gli utenti non devono passare il mouse per individuare l'interfaccia utente primaria.
  - L'interfaccia utente secondaria, ad esempio i comandi secondari o i controlli di divulgazione progressiva, può visualizzare la propria offerta di clic al passaggio del mouse.
  - I [collegamenti di testo](ctrl-links.md) devono suggerire staticamente il testo del collegamento, quindi visualizzare la loro offerta di clic (sottolineata o altra modifica della presentazione, con puntatore a [mano](#hand-pointers)) al passaggio del mouse.
  - I [collegamenti grafici](ctrl-links.md) visualizzano solo un puntatore a mano al passaggio del mouse.
- **Usare il puntatore Hand (o "link Select") solo per i collegamenti di testo e grafica.** In caso contrario, gli utenti dovranno fare clic sugli oggetti per determinare se sono collegamenti.

### <a name="standard-mouse-button-interactions"></a>Interazioni con il pulsante del mouse standard

Nella tabella seguente sono riepilogate le interazioni tra i pulsanti del mouse valide nella maggior parte dei casi:



| Interazione                                    | Effetto                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passaggio del mouse<br/>                    | Target Visualizza la descrizione comando, infotip o equivalente.<br/>                                                                                                                                                                                           |
| Singolo clic con il pulsante sinistro<br/>        | Attiva o seleziona l'oggetto. Per il testo, imposta il punto di inserimento.<br/>                                                                                                                                                                           |
| Singolo clic con il pulsante destro del mouse<br/>       | Seleziona l'oggetto e visualizza il menu di scelta rapida.<br/>                                                                                                                                                                                              |
| Doppio clic con il pulsante sinistro<br/>        | Attiva o seleziona l'oggetto ed esegue il comando predefinito. Per testo, seleziona Word in corrispondenza del punto di inserimento (un terzo clic Seleziona la frase o il paragrafo).<br/>                                                                            |
| Doppio clic con il pulsante destro del mouse<br/>       | Uguale a singolo clic con il pulsante destro del mouse.<br/>                                                                                                                                                                                                                    |
| Spostamento di un solo clic con il pulsante sinistro<br/>  | Per gli oggetti selezionabili, estende la selezione in modo contiguo. In caso contrario, equivale a un clic con il pulsante sinistro del mouse con le possibili modifiche. Ad esempio, in Paint, il disegno di un ovale con il modificatore del tasto MAIUSC genera un cerchio.<br/>                  |
| MAIUSC singolo con pulsante destro del mouse<br/> | Uguale a MAIUSC singolo clic a sinistra.<br/>                                                                                                                                                                                                               |
| Maiusc doppio clic con il pulsante sinistro<br/>  | Uguale a MAIUSC singolo clic a sinistra, ed esegue il comando predefinito sull'intera selezione.<br/>                                                                                                                                                     |
| Maiusc doppio clic con il pulsante destro del mouse<br/> | Uguale a MAIUSC singolo clic a sinistra.<br/>                                                                                                                                                                                                               |
| CTRL singolo clic con pulsante sinistro<br/>   | Per gli oggetti selezionabili, estende la selezione impostando lo stato di selezione dell'elemento selezionato senza influire sulla selezione di altri oggetti, consentendo pertanto la selezione non contigua. In caso contrario, fare clic con il pulsante sinistro del mouse.<br/> |
| CTRL singolo clic con il pulsante destro del mouse<br/>  | Uguale al clic con il pulsante sinistro del mouse.<br/>                                                                                                                                                                                                                |
| Ctrl doppio clic con il pulsante destro del mouse<br/>   | Uguale a CTRL singolo clic con il pulsante sinistro del mouse ed esegue il comando predefinito per l'intera selezione.<br/>                                                                                                                                                      |
| Ctrl doppio clic con il pulsante destro del mouse<br/>  | Uguale al clic con il pulsante sinistro del mouse.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Interazione con il mouse

- **Fare clic su destinazioni con almeno 16x16 pixel, in modo che possano essere facilmente selezionate da qualsiasi dispositivo di input.** Per il [tocco](inter-touch.md), le dimensioni minime consigliate per il controllo sono 23x23 pixel (13x13 DLU). Si consiglia di modificare dinamicamente le dimensioni delle destinazioni di piccole dimensioni quando l'utente punta a facilitarne l'acquisizione.

    In questo esempio, i pulsanti di controllo spin sono troppo piccoli per essere usati in modo efficace con il tocco o con una penna.

    ![screenshot del controllo di selezione con piccole frecce ](images/inter-mouse-image29.png) 

- **Rendere i separatori di almeno cinque pixel in larghezza, in modo che possano essere facilmente selezionate da qualsiasi dispositivo di input.** Si consiglia di modificare dinamicamente le dimensioni delle destinazioni di piccole dimensioni quando l'utente punta a facilitarne l'acquisizione.

    In questo esempio, la barra di divisione nel riquadro di spostamento di Esplora risorse è troppo stretta per essere usata in modo efficace con un mouse o una penna.

    ![screenshot della barra di divisione quasi invisibile ](images/inter-mouse-image30.png)

- **Fornire agli utenti un margine di errore a livello spaziale.** Consentire un movimento del mouse (ad esempio, tre pixel) quando gli utenti rilasciano un pulsante del mouse. Gli utenti a volte spostano leggermente il mouse quando rilasciano il pulsante del mouse, quindi la posizione del mouse immediatamente prima della versione del pulsante riflette meglio l'intenzione dell'utente rispetto alla posizione immediatamente successiva.
- **Fornire agli utenti un margine di errore temporaneamente.** Utilizzare la velocità di doppio clic del sistema per distinguere tra clic singoli e doppi.
- **I clic hanno effetto sul pulsante del mouse.** Consente agli utenti di abbandonare le azioni del mouse rimuovendo il mouse da destinazioni valide prima di rilasciare il pulsante del mouse. Per la maggior parte delle interazioni con il mouse, la pressione di un pulsante del mouse indica solo la destinazione selezionata e il rilascio del pulsante attiva l'azione. Le funzioni di ripetizione automatica, ad esempio la pressione di una freccia di scorrimento per scorrere continuamente, rappresentano un'eccezione.
- [Acquisire il mouse per la](/windows/win32/api/winuser/nf-winuser-setcapture) selezione, lo spostamento, il ridimensionamento, la suddivisione e il trascinamento.
- Usare il tasto ESC per consentire agli utenti di abbandonare le interazioni del mouse composto, ad esempio lo spostamento, il ridimensionamento, la suddivisione e il trascinamento.
- **Se un oggetto non supporta i doppio clic ma è probabile che gli utenti lo presuppongano, interpretare un "doppio clic" con un solo clic.** Si supponga che l'utente intenda un'azione singola anziché due.

    Poiché è probabile che gli utenti presuppongano che i pulsanti della barra delle applicazioni supportino i doppi clic, un "doppio clic" deve essere gestito con un solo clic.

    ![screenshot del pulsante della barra delle applicazioni e del puntatore standard ](images/inter-mouse-image31.png)

- **Ignorare i clic del mouse ridondanti mentre il programma è inattivo.** Se, ad esempio, l'utente fa clic su un pulsante 10 volte mentre un programma è inattivo, interpretarlo con un solo clic.
- **Non usare i doppi trascinamenti o gli accordi.** Un doppio segno di trascinamento è un'azione di trascinamento iniziata con un doppio clic e una corda si verifica quando vengono premuti contemporaneamente più pulsanti del mouse. Queste interazioni non sono standard, non sono individuabili, sono difficili da eseguire ed è probabile che vengano eseguite accidentalmente.
- **Non usare Alt come modificatore per le interazioni con il mouse.** Il tasto ALT è riservato per le chiavi di accesso e accesso della barra degli strumenti.
- **Non usare Maiusc + Ctrl come modificatore per le interazioni con il mouse.** Questa operazione potrebbe risultare troppo difficile da utilizzare.
- **Rendere ridondante il passaggio del mouse.** Per rendere il programma toccabile, sfruttare tutti i vantaggi del passaggio del mouse, ma solo in modi che non sono necessari per eseguire un'azione. Ciò significa in genere che un'azione può essere eseguita anche facendo clic su, ma non necessariamente esattamente allo stesso modo. Il passaggio del mouse non è supportato dalla maggior parte delle tecnologie touch, quindi gli utenti con tali touchscreen non possono eseguire attività che richiedono il passaggio del mouse.

### <a name="mouse-wheel"></a>Rotellina del mouse

- **Fare in modo che la rotellina del mouse influisca sul controllo, sul riquadro o sulla finestra su cui è attualmente posizionato il puntatore.** In questo modo si evitano risultati imprevisti.
- **Rendere effettiva la rotellina del mouse senza fare clic o avere lo stato attivo per l'input.** Il passaggio del mouse è sufficiente.
- **Fare in modo che la rotellina del mouse influisca sull'oggetto con l'ambito più specifico.** Se, ad esempio, il puntatore è posizionato su un controllo casella di riepilogo scorrevole in un riquadro scorrevole all'interno di una finestra scorrevole, la rotellina del mouse influiscono sul controllo casella di riepilogo.
- **Non modificare lo stato attivo per l'input quando si usa la rotellina del mouse.**
- Dare alla rotellina del mouse gli effetti seguenti:
  - Per le finestre scorrevoli, i riquadri e i controlli:
    - **La rotazione della rotellina del mouse consente di scorrere l'oggetto verticalmente, in cui la rotazione verso l'alto scorre verso l'alto.** Per consentire il mapping naturale della rotellina, la rotazione della rotellina del mouse non dovrebbe mai scorrere orizzontalmente perché questa operazione è disorientata e imprevista.
      - **Se il tasto CTRL è premuto, la rotazione della rotellina del mouse consente di ingrandire l'oggetto,** dove la rotazione verso l'alto e la rotazione verso il basso ingrandisce.
      - **Inclinando la rotellina del mouse l'oggetto viene spostato orizzontalmente.**
  - Per le finestre e i riquadri zoomati (senza barre di scorrimento):
    - La **rotazione della rotellina del mouse consente di ingrandire l'oggetto,** dove ruotare lo zoom avanti e ruotare verso il basso.
    - L'inclinazione della rotellina del mouse non ha alcun effetto.
  - Per le schede:
    - **Ruotando la rotellina del mouse è possibile modificare la scheda corrente,** indipendentemente dall'orientamento delle schede.
    - L'inclinazione della rotellina del mouse non ha alcun effetto.
  - Se i tasti MAIUSC e ALT sono depressi, la rotellina del mouse non ha alcun effetto.
- **Usare le impostazioni di sistema di Windows per la dimensione di scorrimento verticale (per la rotazione) e le dimensioni di scorrimento orizzontale (per l'inclinazione).** Queste impostazioni possono essere configurate tramite l'elemento del pannello di controllo del mouse.
- **La rotazione più rapida della rotellina del mouse comporta uno scorrimento più rapido.** Questa operazione consente agli utenti di scorrere documenti di grandi dimensioni in modo più efficiente.
- **Per le finestre scorrevoli, provare a fare clic sul pulsante della rotellina del mouse per posizionare la finestra in "modalità lettore".** La modalità lettore consente di piantare un'icona di origine di scorrimento speciale e di scorrere la finestra in una direzione e una velocità rispetto all'origine dello scorrimento.

![screenshot della pagina con icona di scorrimento-origine ](images/inter-mouse-image32.png)

*Internet Explorer supporta la modalità lettore, che include l'icona di scorrimento-origine*

### <a name="hiding-the-pointer"></a>Nascondere il puntatore

- **Non nascondere il puntatore.** Eccezioni:
  - Le applicazioni di presentazione eseguite in modalità presentazione a schermo intero possono nascondere il puntatore. Tuttavia, il puntatore deve essere ripristinato immediatamente quando l'utente sposta il mouse e può essere rinascosto dopo due secondi di inattività.
  - Gli ambienti senza mouse (ad esempio chioschi) possono nascondere il puntatore in modo permanente.
- Per impostazione predefinita, Windows nasconde il puntatore mentre l'utente sta digitando una casella di testo. Questa impostazione di sistema di Windows può essere configurata tramite l'elemento del pannello di controllo del mouse.

### <a name="activity-pointers"></a>Puntatori attività

I puntatori di attività in Windows sono il puntatore occupato (![screenshot del puntatore a forma di anello ](images/inter-mouse-image33.png)) e il puntatore working in background (![screenshot del puntatore a forma di anello e della freccia ](images/inter-mouse-image34.png)).

- Visualizza il puntatore occupato quando gli utenti devono attendere più di un secondo per completare un'azione. Si noti che il puntatore occupato non presenta punti sensibili, quindi gli utenti non possono fare clic su un elemento mentre viene visualizzato.
- Visualizza il puntatore in background quando gli utenti devono attendere più di un secondo per completare un'azione, ma il programma è reattivo e non vi sono altri commenti visivi che l'azione non è completa.
- Non combinare i puntatori di attività con barre di stato o animazioni di avanzamento.

### <a name="caret"></a>Cursore

- **Non visualizzare il cursore finché la finestra input di testo o il controllo non ha lo stato attivo per l'input.** Il punto di inserimento suggerisce lo stato attivo per gli utenti, ma una finestra o un controllo può visualizzare il cursore senza lo stato attivo per l'input. Naturalmente, non rubare lo stato attivo per l'input in modo che una finestra di dialogo non contestuale possa visualizzare il cursore.

    Gestione credenziali di Windows viene visualizzato fuori contesto con il cursore ma senza lo stato attivo per l'input. Di conseguenza, gli utenti digitano la propria password in posizioni impreviste.

    ![Screenshot di gestione credenziali senza stato attivo ](images/inter-mouse-image35.png)

- **Posizionare il punto di inserimento in cui è più probabile che gli utenti digitano prima.** In genere si tratta dell'ultima posizione in cui l'utente stava digitando o alla fine del testo.

### <a name="accessibility"></a>Accessibilità

- Per gli utenti che non possono utilizzare il mouse, rendere il mouse ridondante con la tastiera.
  - Gli utenti dovrebbero essere in grado di eseguire tutte le operazioni con la tastiera con il mouse, eccetto le azioni per le quali sono essenziali le competenze dei motori, come il disegno e la riproduzione del gioco.
  - Gli utenti dovrebbero essere in grado di eseguire tutte le operazioni con il mouse che possono avere con la tastiera, ad eccezione di una voce di testo efficiente.
- Per gli utenti con capacità limitata di utilizzare il mouse:
  - Non fare doppio clic e trascinare l'unico modo per eseguire un'azione.

Per ulteriori informazioni e linee guida, vedere [accessibilità](inter-accessibility.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento al mouse:

- Evitare l'uso dei topi plurali; Se è necessario fare riferimento a più di un mouse, utilizzare i dispositivi mouse.
- Utilizzare il pulsante del mouse per indicare il pulsante sinistro del mouse. Non usare il pulsante del mouse primario. Analogamente, usare il pulsante destro del mouse anziché il pulsante del mouse secondario. Indipendentemente dall'accuratezza, gli utenti comprendono i termini e gli utenti che riprogrammano i pulsanti in modo da rendere il turno mentale.
- Utilizzare la rotellina per la parte girevole della rotellina del mouse e il pulsante della rotellina per fare riferimento alla parte selezionabile.
- Usare i verbi come clic, punto e trascinamento per fare riferimento alle azioni del mouse. Gli utenti ruotano verticalmente la rotella, inclinarla orizzontalmente e fare clic sul pulsante della rotellina.
- Per l'azione di spostare un documento o una cartella, utilizzare il trascinamento e non il trascinamento della selezione. È accettabile usare il trascinamento della selezione come aggettivo, come nello "spostare la cartella è un'operazione di trascinamento della selezione".
- Sillabare sempre doppio clic e fare clic con il pulsante destro del mouse come verbi.
- Usare fai clic, non fare clic su. Fare clic su in (come in "fare clic nella finestra") è accettabile.

Quando si fa riferimento ai puntatori del mouse:

- Fare riferimento al puntatore del mouse come puntatore. Utilizzare il cursore solo nella documentazione tecnica.
- Per i puntatori con indicatori di attività, utilizzare il puntatore occupato per il puntatore costituito solo da un indicatore di attività e utilizzare il puntatore di sfondo per il puntatore di combinazione e l'indicatore di attività.
- Per gli altri tipi di puntatori, non usare etichette descrittive per fare riferimento al puntatore. Se necessario, utilizzare una rappresentazione grafica per descrivere il modo in cui il puntatore del mouse può essere visualizzato sullo schermo.

**Esempi:**

- Puntare al bordo della finestra.
- Usando il mouse, fare clic sul pulsante **Riduci a icona** .
- Tenere premuto MAIUSC e fare clic con il pulsante destro del mouse.
- Quando il puntatore diventa ![screenshot della freccia con due maniglie](images/inter-mouse-image18.png)Trascinare il puntatore per spostare la linea di divisione.

## <a name="see-also"></a>Vedi anche

- [Linee guida sull'interazione di accessibilità](inter-accessibility.md)
- [Linee guida per l'interazione tocco](inter-touch.md)
- [Linee guida sull'interazione della penna](inter-pen.md)
- [Collegamenti di testo](ctrl-links.md)
- [Collegamenti grafici](ctrl-links.md)
- [Acquisire il mouse](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Impostazione dell'immagine del cursore](../learnwin32/setting-the-cursor-image.md)
- [Input utente: esempio esteso](../learnwin32/user-input--extended-example.md)