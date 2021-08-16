---
title: Barre multifunzione
description: Le barre multifunzione sono il modo moderno per aiutare gli utenti a trovare, comprendere e usare i comandi in modo efficiente e diretto \ 8212; con un numero minimo di clic, con meno necessità di ricorrere alla versione di valutazione e agli errori e senza dover fare riferimento alla Guida.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db5a64d50bd225b714c2ff0578145c47c66bedb557dd067e0cdf89f369178b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042747"
---
# <a name="ribbons"></a>Barre multifunzione

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Le barre multifunzione sono il modo moderno per aiutare gli utenti a trovare, comprendere e usare i comandi in modo efficiente e diretto con un numero minimo di clic, con meno necessità di ricorrere alla versione di valutazione e agli errori e senza dover fare riferimento alla Guida.

Una barra multifunzione è una barra dei comandi che organizza le funzionalità di un programma in una serie di schede nella parte superiore di una finestra. L'uso di una barra multifunzione aumenta l'individuabilità di funzionalità e funzioni, consente un apprendimento più rapido del programma nel suo complesso e rende gli utenti più in controllo della propria esperienza con il programma. Una barra multifunzione può sostituire sia la barra dei menu tradizionale che le barre degli strumenti.

![Screenshot di una barra multifunzione ](images/cmd-ribbons-image1.png)

Una tipica barra multifunzione.

Le schede della barra multifunzione sono costituite da gruppi, ovvero un set etichettato di comandi strettamente correlati. Oltre a schede e gruppi, le barre multifunzione sono costituite da:

- Un pulsante Applicazione, che presenta un menu di comandi che comportano l'esecuzione di un'operazione a o con un documento o un'area di lavoro, ad esempio i comandi correlati ai file.
- Barra di accesso rapido, una piccola barra degli strumenti personalizzabile che visualizza i comandi usati di frequente.
- Le schede principali sono le schede che vengono sempre visualizzate.
- Schede contestuali, che vengono visualizzate solo quando è selezionato un particolare tipo di oggetto. Le schede che vengono sempre visualizzate sono denominate schede principali.
- Un set di schede è una raccolta di schede contestuali per un singolo tipo di oggetto. Poiché gli oggetti possono avere più tipi (ad esempio, un'intestazione in una tabella con un'immagine è di tre tipi), possono essere visualizzati più set di schede contestuali alla volta.
- Schede modali, ovvero schede principali visualizzate con una particolare modalità temporanea, ad esempio l'anteprima di stampa.
- Raccolte, ovvero elenchi di comandi o opzioni presentati graficamente. Una raccolta basata sui risultati illustra l'effetto dei comandi o delle opzioni anziché dei comandi stessi. Una raccolta nella barra multifunzione viene visualizzata all'interno di una barra multifunzione, anziché in una finestra popup.
- Descrizioni comando avanzate, che spiegano concisamente i comandi associati e assegnano i tasti di scelta rapida. Possono anche includere grafica e riferimenti alla Guida. Le descrizioni comando avanzate riducono la necessità di una Guida correlata ai comandi.
- Finestre di avvio delle finestre di dialogo, ovvero pulsanti nella parte inferiore di alcuni gruppi che aprono finestre di dialogo contenenti funzionalità correlate al gruppo.

I nastri sono stati originariamente introdotti con Microsoft Office 2007. Per informazioni sui Office necessario usare le barre multifunzione e i numerosi problemi che si verificano con una barra multifunzione, vedere La storia [della barra multifunzione.](/archive/blogs/jensenh/the-story-of-the-ribbon)

> [!Note]  
> Le linee guida relative [a menu,](cmd-menus.md) [barre degli strumenti,](cmd-toolbars.md) [pulsanti di](ctrl-command-buttons.md)comando e [icone](vis-icons.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere di usare una barra multifunzione, considerare queste domande:

### <a name="program-type"></a>Tipo di programma

- **Quale tipo di programma si sta progettando?** Il tipo di programma è un buon indicatore dell'appropriatezza di una barra multifunzione. Le barre multifunzione funzionano bene per i programmi di creazione e creazione di documenti, nonché per i visualizzatori di documenti e i browser. Le barre multifunzione potrebbero funzionare per altri tipi di programmi, ma altre forme di presentazione dei comandi potrebbero essere più appropriate. In genere, i programmi leggeri devono avere una presentazione di comandi leggera.

### <a name="discoverability-and-learning-issues"></a>Problemi di individuazione e apprendimento

- **Gli utenti hanno problemi a trovare i comandi? Gli utenti richiedono funzionalità già presenti nel programma?** In tal caso, l'uso di una barra multifunzione semplifica l'individuazione dei comandi con etichette autoesplicative e il raggruppamento dei comandi correlati. L'uso di una barra multifunzione offre anche prestazioni migliori rispetto alle barre dei menu e alle barre degli strumenti per una crescita futura.
- **Gli utenti hanno problemi a comprendere i comandi del programma? Spesso si ricorre alla "versione di valutazione ed errore" per selezionare il comando giusto o determinare il funzionamento dei comandi?** In tal caso, l'uso di una barra multifunzione con comandi orientati ai risultati basati su raccolte e anteprime live semplifica la comprensione dei comandi.

### <a name="command-characteristics"></a>Caratteristiche dei comandi

- **I comandi sono presentati in diverse posizioni? Se il programma esiste già, i comandi vengono presentati in barre dei menu, barre degli strumenti, riquadri attività e all'interno dell'area di lavoro stessa?** In tal caso, l'uso di una barra multifunzione unificherà i comandi in un'unica posizione, semplificando l'individuazione.
- **I comandi si applicano all'intera finestra o solo a riquadri specifici?** Le barre multifunzione funzionano meglio per i comandi che si applicano all'intera finestra o a oggetti specifici. I comandi sul posto funzionano meglio per i singoli riquadri della finestra.
- **La maggior parte dei comandi può essere presentata direttamente? In altri, gli utenti possono interagire con loro con un solo clic? Se si accede ai comandi di uso comune da menu e finestre di dialogo, è possibile eseguire il refactoring in modo che siano diretti?** Anche se alcuni comandi possono essere presentati usando menu e finestre di dialogo, la presentazione della maggior parte dei comandi in questo modo compromette l'efficienza di una barra multifunzione, rendendo una barra dei menu una scelta migliore.

### <a name="command-scale"></a>Scalabilità dei comandi

- **È presente un numero ridotto di comandi? I comandi usati più di frequente possono essere presentati facilmente su una singola barra degli strumenti semplice?** L'uso di una barra multifunzione è utile se l'aggiunta di schede di base e contestuali comporta una semplice scheda Home che può essere usata da sola per eseguire le attività più comuni. In caso contrario, il vantaggio dell'uso di una barra multifunzione potrebbe non giustificare il peso aggiuntivo per un numero ridotto di comandi.
- **È presente un numero elevato di comandi? L'uso di una barra multifunzione richiederebbe più di sette schede principali? Gli utenti devono costantemente modificare le schede per eseguire attività comuni?** In tal caso, l'uso delle barre degli strumenti (che non richiedono la modifica delle schede) e delle finestre del riquadro [(che](cmd-toolbars.md) potrebbero richiedere la modifica delle schede, ma possono essere presenti diverse finestre aperte alla volta) potrebbe essere una scelta più efficiente.
- **Gli utenti tendono a usare un numero ridotto di comandi nella maggior parte dei casi?** In tal caso, possono usare una barra multifunzione in modo efficiente inserendo questi comandi nella scheda Home. La modifica costante delle schede renderebbe una barra multifunzione troppo inefficiente.
- **Il programma trae vantaggio dal rendere l'area del contenuto del programma il più grande possibile?** In tal caso, l'uso di una barra dei menu e di una singola barra degli strumenti è più efficiente dello spazio rispetto a una barra multifunzione. Tuttavia, se il programma richiede tre o più righe di barre degli strumenti o usa riquadri attività, l'uso di una barra multifunzione è più efficiente in termini di spazio.
- **Gli utenti tendono a lavorare in un'area specifica all'interno di una finestra di grandi dimensioni nel programma per lunghi periodi di tempo?** In tal caso, potrebbero trarre vantaggio dalla vicinanza di mini-barre degli strumenti, finestre della tavolozza e comandi diretti. Rendere il round trip dall'area di lavoro alla barra multifunzione sarebbe troppo inefficiente.
- **Per efficienza e flessibilità, gli utenti devono apportare modifiche significative al contenuto, alla posizione o alle dimensioni della presentazione del comando?** In tal caso, le barre degli strumenti e le finestre della tavolozza personalizzabili ed estensibili sono una scelta migliore. Si noti che alcuni tipi di barre degli strumenti possono essere disinseriti per diventare finestre della tavolozza e le finestre della tavolozza possono essere spostate, ridimensionate e personalizzate.

Infine, considerare questa domanda finale: il miglioramento dell'individuabilità, della facilità di apprendimento, dell'efficienza e della produttività vale il costo dello spazio aggiuntivo e la necessità di schede per organizzare **i comandi?** In tal caso, l'uso di una barra multifunzione è un'ottima scelta. In caso di insidità, valutare l'usabilità testando una progettazione basata su barra multifunzione e confrontandolo con l'alternativa migliore.

Le barre multifunzione sono una nuova e coinvolgente forma di presentazione dei comandi e un ottimo modo per modernizzare un programma. Ma per quanto siano accattivanti, non sono la scelta giusta per ogni programma.

**Non corretto:**

![Screenshot di una barra multifunzione con una calcolatrice ](images/cmd-ribbons-image2.png)

Non eseguire questa operazione.

## <a name="seven-most-important-things"></a>Sette elementi più importanti

1. Scegliere una soluzione di comando adatta al tipo di programma. L'uso di una barra multifunzione dovrebbe rendere un programma più semplice, più efficiente e più semplice da usare mai al contrario. Se l'uso di una barra multifunzione non è appropriato, è consigliabile usare i comandi rtf.  
2. Non sottovalutare la sfida di creare una barra multifunzione efficace. Non aspettarsi che sia una semplice porta delle barre dei menu e delle barre degli strumenti esistenti. E non dare per scontato che l'uso di una barra multifunzione res migliori automaticamente il programma. La disponibilità a eseguire il commit del tempo e dell'impegno necessari per la riprogettazione dei comandi è un fattore importante per decidere di usare una barra multifunzione.  
3. Rendere individuabili i comandi. Scegliere una struttura di schede con un mapping chiaro, ovvio e univoco tra i comandi e le schede con etichetta descrittiva in cui si trovano. Gli utenti devono essere in grado di determinare in modo rapido e sicuro quale scheda contiene il comando che stanno cercando e raramente scegliere la scheda errata.  
4. Rendere i comandi auto-esplicativi. Gli utenti devono comprendere l'effetto di un comando dall'etichetta, dall'icona, dalla descrizione comando e dall'anteprima. Non devono sperimentare o leggere un argomento della Guida per vedere il funzionamento di un comando.  
5. Rendere efficiente l'uso dei comandi:
    - Gli utenti devono dedicare la maggior parte del tempo alla scheda Home.
    - Gli utenti devono raramente modificare le schede durante le attività comuni.
    - Quando la finestra è ingrandita e gli utenti sono nella scheda corretta, i comandi usati più di frequente hanno maggiore enfasi visiva e gli utenti possono richiamarli con un solo clic. Gli utenti possono eseguire tutti gli altri comandi nella scheda con al massimo quattro clic.
    - Gli utenti non devono aprire finestre di dialogo per assegnare comandi e modificare gli attributi nelle attività comuni.
6. Aiutare gli utenti a scegliere comandi e opzioni in modo sicuro e ridurre al minimo la necessità di tentativi ed errori. Usare comandi orientati ai risultati quando appropriato, spesso sotto forma di raccolte e anteprime live.  
7. Assicurarsi che la barra multifunzione si adatta bene dalle dimensioni delle finestre più grandi alle dimensioni più piccole.  

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adattamento di una barra multifunzione in un programma esistente

Anche se è possibile eseguire semplicemente il refactoring di una barra dei menu tradizionale e della progettazione della barra degli strumenti di un programma esistente in un formato di barra multifunzione, questa operazione non consente di ottenere la maggior parte del valore dell'uso di una barra multifunzione. Le barre multifunzione hanno il massimo valore quando vengono usate per presentare comandi immediati e orientati ai risultati, spesso sotto forma di raccolte e anteprime live. I comandi orientati ai risultati semplificano la comprensione dei comandi e rendono gli utenti molto più efficienti e produttivi. Invece di effettuare il refactoring dei comandi esistenti, è meglio riprogettare completamente il modo in cui i comandi vengono eseguiti nel programma.

Non sottovalutare la sfida di creare una barra multifunzione efficace. E non dare per scontato che l'uso di una barra multifunzione rende automaticamente il programma migliore. La creazione di una barra multifunzione efficace richiede molto tempo e impegno. La disponibilità a impegnarsi nel tempo e nell'impegno necessari per una riprogettazione dei comandi di questo tipo è un fattore importante per decidere di usare una barra multifunzione.

### <a name="the-nature-of-ribbons"></a>Natura dei nastri

Rispetto alle barre dei menu e alle barre degli strumenti tradizionali, le barre multifunzione hanno le caratteristiche seguenti:

- **Una singola interfaccia utente per tutti i comandi.** Le barre dei menu sono complete e facili da imparare e le barre degli strumenti sono efficienti e dirette, ma perché non usare un po' più di spazio sullo schermo per creare una singola interfaccia utente dei comandi che consente di eseguire tutte queste operazioni? Con una sola interfaccia utente, le barre multifunzione non richiedono agli utenti di determinare quale interfaccia utente ha il comando che stanno cercando.
- **Visibile e auto-esplicativo.** I comandi della barra dei menu sono auto-esplicativi tramite le relative etichette, ma sono nascosti nella maggior parte dei casi. Per risparmiare spazio sullo schermo, i pulsanti della barra degli strumenti sono rappresentati principalmente da icone anziché etichette (anche se alcuni pulsanti della barra degli strumenti usano entrambi) e dipendono dalle descrizioni comando quando l'icona non è auto-esplicativa. Tuttavia, gli utenti in genere conoscono le icone solo per i comandi usati più di frequente.
- Presentando la maggior parte dei comandi con icone etichettate, i comandi della barra multifunzione sono sia visibili che auto-esplicativi e usano le descrizioni comando solo per fornire informazioni supplementari. Non è necessario passare altrove , ad esempio la Guida, per comprendere un comando.
- **Raggruppamento con etichetta.** Mentre le categorie di menu sono etichettate, i gruppi all'interno di un menu a discesa non sono e sono indicati solo con un separatore senza etichetta. I gruppi all'interno delle barre degli strumenti sono indicati anche con separatori senza etichetta.
- Organizzando i comandi in gruppi con etichetta, le barre multifunzione semplificano l'individuazione dei comandi e la loro determinazione dello scopo.
- **Modale ma non gerarchico.** Le barre dei menu vengono ridimensionate creando una gerarchia di comandi. I menu con molti elementi possono usare uno o più livelli di sottomenu per fornire più comandi.
- I comandi della barra multifunzione richiedono più spazio rispetto ai comandi della barra degli strumenti, quindi usano le schede per la scalabilità. Questo uso delle schede rende modali le barre multifunzione, che richiedono agli utenti di modificare occasionalmente le modalità per trovare i comandi. Tuttavia, all'interno di una scheda la maggior parte dei comandi è diretta o usa un singolo pulsante di menu o pulsante di menu suddiviso, non una gerarchia.
- **Diretto e immediato.** Un comando è diretto se richiamato con un solo clic (ovvero senza spostarsi tra i menu) e immediato se ha effetto immediato (ovvero senza finestre di dialogo per raccogliere input aggiuntivo). I comandi della barra dei menu sono sempre indiretti e spesso non immediati. Analogamente alle barre degli strumenti, la maggior parte dei comandi della barra multifunzione è progettata per essere diretta e immediata, con i comandi usati più di frequente richiamati con un solo clic e senza richiedere una finestra di dialogo per raccogliere input aggiuntivo.
- **Spaziose.** Le barre dei menu e le barre degli strumenti sono progettate principalmente per essere efficienti a livello di spazio. Per offrire i vantaggi, i nastri possono utilizzare più spazio verticale, essendo approssimativamente equivalente a una barra dei menu più tre righe di barre degli strumenti. Dal momento che pochi programmi hanno tre o più righe di barre degli strumenti, le barre multifunzione in genere utilizzano più spazio rispetto alle tradizionali interfaccia utente per i comandi.
- **Dispone di un pulsante Applicazione e della barra di accesso rapido.** Una barra multifunzione viene sempre visualizzata con un pulsante Applicazione e una barra di accesso rapido. In questo modo gli utenti possono accedere ai comandi correlati ai file e usati di frequente senza modificare le schede e promuovere la coerenza tra i programmi.
- **Personalizzazione minima.** Anche se le barre dei menu hanno una presentazione fissa, molte barre degli strumenti sono piuttosto personalizzabili, consentendo agli utenti di impostare posizioni, dimensioni e contenuto. Una barra multifunzione non è personalizzabile, ma la barra di accesso rapido offre una personalizzazione limitata.
- **Accessibilità della tastiera migliorata.** Le barre dei menu hanno un'eccellente accessibilità da tastiera perché premendo il tasto ALT viene direttamente attivata l'input della barra dei menu. Tuttavia, non esiste un meccanismo di questo tipo per le barre degli strumenti perché condividono lo spostamento tramite tastiera con il contenuto della finestra. Di conseguenza, gli utenti devono passare alla barra degli strumenti usando il tasto TAB (data l'ultima tabulazione) e quindi passare a un comando specifico usando i tasti di direzione.

Al contrario, le barre multifunzione offrono un'accessibilità avanzata della tastiera tramite i [suggerimenti tasto](glossary.md)di scelta, in genere con un processo in tre passaggi:

- Premere ALT per accedere alla modalità del suggerimento tasto di scelta.
- Premere un carattere per scegliere una scheda, il pulsante Applicazione o un comando nella barra di accesso rapido.
- All'interno di una scheda premere una o due lettere per scegliere un comando.

    Questo approccio è altamente visivo. È anche più flessibile, consentendo una migliore scalabilità e più assegnazioni di chiavi di accesso mnemoiche.

    Non confondere i tasti di scelta con i tasti di scelta rapida. Anche se sia i tasti di scelta che i tasti di scelta rapida forniscono l'accesso tramite tastiera all'interfaccia utente, hanno scopi e linee guida diversi. Per altre informazioni, vedere [Tastiera.](inter-keyboard.md)

### <a name="the-nature-of-rich-commands"></a>La natura dei comandi rich

I comandi rich fanno riferimento alla presentazione e all'interazione dei comandi usati dalle barre multifunzione, senza necessariamente usare un contenitore della barra multifunzione. I comandi rich hanno queste caratteristiche:

- **Etichettatura.** A tutti i comandi vengono fornite etichette auto-esplicativi, con eccezioni solo quando le icone sono estremamente note e lo spazio è premium.

    **Corretto:**

    ![Screenshot di una barra multifunzione per la formattazione dei caratteri ](images/cmd-ribbons-image3.png)

    Questi comandi sono estremamente noti e quindi non necessitano di etichette.

    **Non corretto:**

    ![Screenshot di una barra multifunzione con icone usate raramente ](images/cmd-ribbons-image4.png)

    Queste icone incomprensibili richiedono etichette per i comandi rich.

- **Dimensionamento.** Invece di ridimensionamento uniforme, i comandi vengono ridimensionati in base alla frequenza di utilizzo e all'importanza. Oltre a rendere più semplici trovare e fare clic sui comandi usati più di frequente, li rende [anche più toccabili.](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx)

    ![Screenshot di un pulsante grande e tre pulsanti di piccole dimensioni ](images/cmd-ribbons-image5.png)

    In questo esempio, il pulsante usato più di frequente è più grande degli altri.

- **Ridimensionamento dinamico.** I controlli di comando completi si ridimensionano per sfruttare appieno lo spazio disponibile, invece di usare una dimensione fissa e troncare o usare l'overflow quando le dimensioni sono troppo piccole.

    ![Screenshot della barra multifunzione ampia con pulsanti di dimensioni uguali ](images/cmd-ribbons-image6.png)![Screenshot della barra multifunzione di piccole dimensioni con pulsanti misti ](images/cmd-ribbons-image7.png)

    In questo esempio i pulsanti di comando vengono ridimensionati per funzionare correttamente nello spazio disponibile.

- **Pulsanti di divisione.** I pulsanti di divisione sono un buon modo per consolidare un set di varianti di un comando quando necessario, mantenendo al tempo stesso la direttezza per il comando usato più di frequente.

    ![Screenshot del comando Salva con nome e delle relative opzioni ](images/cmd-ribbons-image8.png)

    In questo esempio il comando Salva con nome usa un pulsante di menu suddiviso, in cui il pulsante principale esegue la variazione più comune e la parte di menu visualizza un menu con varianti del comando.

- **Menu a discesa e raccolte.** I menu a discesa, gli elenchi a discesa e le raccolte usano lo spazio necessario per comunicare e differenziare l'effetto delle scelte, spesso usando descrizioni grafiche e di testo. Le categorie vengono usate per organizzare set di opzioni di grandi dimensioni.

    ![Screenshot delle opzioni del menu a discesa con icone ](images/cmd-ribbons-image9.png)

    In questi esempi, facendo clic su un pulsante di menu viene visualizzato un elenco di scelte che ne mostrano l'effetto.

- **Anteprime live.** Ogni volta che l'utente passa il mouse su un'opzione di formattazione, il programma mostra l'aspetto dei risultati con tale formattazione usando il contenuto effettivo.

    ![Screenshot dei risultati delle scelte di formattazione ](images/cmd-ribbons-image10.png)

    Le anteprime live mostrano i risultati dell'applicazione di un'opzione di formattazione al passaggio del mouse.

- **Descrizioni comando avanzate.** Questi elementi illustrano concisamente i comandi associati e forniscono i tasti di scelta rapida. Possono anche includere grafica e riferimenti alla Guida (anche se eliminano in gran parte la necessità di una Guida correlata ai comandi).

    ![Screenshot di una descrizione comando di grandi dimensioni con testo e grafica ](images/cmd-ribbons-image11.png)

    Le descrizioni comando avanzate illustrano in modo conciso i comandi associati.

Anche se le barre multifunzione potrebbero non essere adatte a tutti i programmi, tutti i programmi possono trarre vantaggio dai comandi rich.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Le barre multifunzione hanno sempre un pulsante Applicazione e una barra di accesso rapido

Il pulsante Applicazione e la barra di accesso rapido forniscono comandi utili in qualsiasi contesto, riducendo così la necessità di modificare le schede. Anche se questi tre componenti sono logicamente indipendenti, una barra multifunzione deve sempre avere un pulsante Applicazione e una barra di accesso rapido. Dato che i comandi possono essere visualizzati nella barra multifunzione o nel pulsante Applicazione, ci si potrebbe chiedere dove posizionare i comandi. La scelta non è arbitraria.

Il pulsante Applicazione viene usato per presentare un menu di comandi che comportano l'esecuzione di un'operazione in o con un file, ad esempio i comandi che tradizionalmente vengono usati nel menu File per creare, aprire e salvare file, stampare e inviare e pubblicare documenti.

Al contrario, la barra multifunzione è per i comandi che influiscono sul contenuto della finestra. Ad esempio, i comandi usati per leggere, modificare o usare il contenuto o per modificare la visualizzazione.

Se si usa una barra multifunzione, è necessario usare anche un pulsante Applicazione anche se il programma non include documenti o file. In questi casi, usare il menu Applicazione per presentare i comandi per la stampa, le opzioni del programma e l'uscita dal programma. Anche se probabilmente il pulsante Applicazione non è necessario per tali programmi, l'uso di questo pulsante garantisce coerenza tra i programmi. Gli utenti non devono cercare i comandi di salvataggio e annullamento o le opzioni del programma perché sono sempre nella stessa posizione.

La barra di accesso rapido è obbligatoria anche se la barra multifunzione usa una sola scheda. Anche in questo caso, anche se probabilmente tali programmi non necessitano di una barra di accesso rapido (perché tutti i comandi sono già presenti nella singola scheda), la presenza di una barra di accesso rapido personalizzabile garantisce coerenza tra i programmi. Ad esempio, se gli utenti hanno l'consuetudine di fare clic sul comando Stampa, dovrebbero essere in grado di farlo in qualsiasi programma che usa una barra multifunzione.

### <a name="organization-and-discoverability"></a>Organizzazione e individuabilità

Fornendo schede e gruppi, le barre multifunzione consentono di organizzare i comandi per facilitare l'individuazione. La sfida è che se l'organizzazione viene eseguita in modo non idoneo, può invece danneggiare notevolmente l'individuabilità. Dovrebbe essere presente un mapping chiaro, ovvio e univoco tra i comandi e le schede e i gruppi etichettati in modo descrittivo in cui risiedono.

Gli utenti formeranno un modello psichiale della barra multifunzione dopo averlo utilizzato per un po' di tempo. Se questo modello psichici non ha senso per gli utenti, è inefficiente o non è corretto, può causare confusione e frustrazione. **L'obiettivo più importante nella progettazione di una barra multifunzione è facilitare la ricerca dei comandi in modo rapido e sicuro. In caso contrario, la progettazione della barra multifunzione avrà esito negativo.** Il raggiungimento di questo obiettivo richiede un'attenta progettazione, test utente e iterazione. Non presupporre che sarà facile.

Ecco alcuni problemi comuni da evitare:

- **Evitare nomi generici di schede e gruppi.** Un buon nome di scheda o gruppo deve descrivere accuratamente il contenuto specifico, preferibilmente usando un linguaggio basato su attività e obiettivo. Evitare i nomi generici di schede e gruppi, nonché i nomi basati sulla tecnologia. Ad esempio, quasi tutti i comandi in un programma di creazione e creazione di documenti possono appartenere a schede con etichetta Modifica, Formato, Strumenti, Opzioni, Avanzate e Altro ancora. Basarsi su etichette descrittive specifiche, non sulla memorizzazione.
- **Evitare nomi di schede e gruppi troppo specifici.** Anche se si vuole che i nomi delle schede e dei gruppi siano specifici, non devono essere così specifici che gli utenti sono sorpresi dal contenuto. Gli utenti spesso cercano elementi che usano il processo di eliminazione, quindi impediscono loro di tralasciare le schede o i gruppi perché il nome è fuorviante.
- **Evitare più percorsi per lo stesso comando, soprattutto se il percorso è imprevisto o il comando richiede più clic per richiamare.** Può sembrare una comodità trovare un comando in più percorsi. Tenere tuttavia presente che quando gli utenti trovano ciò che cercano, smettino di guardare. È troppo facile per gli utenti presupporre che il primo percorso trovato sia l'unico percorso che rappresenta un problema grave se tale percorso è inefficiente o imprevisto. Inoltre, la presenza di comandi duplicati rende più difficile per gli utenti trovare altri comandi cercati.

![Screenshot del comando percorso indiretto ai bordi ](images/cmd-ribbons-image12.png)

In questo esempio è possibile modificare i bordi dei paragrafi tramite il comando Bordi pagina, anche se nella scheda Home è presente un tracciato più diretto. Se gli utenti che cercano i bordi dei paragrafi devono attraversare questo percorso imprevisto, potrebbero facilmente presupporre che sia l'unico percorso.

- **Evitare il posizionamento arbitrario dei comandi.** Si supponga di avere una buona progettazione di schede e gruppi, ma di scoprire che diversi comandi non rientrano nella struttura. È probabile che la progettazione di schede e gruppi non sia buona come si pensa e che sia necessario continuare a perfezionarla. Non risolvere questo problema inserendo i comandi a cui non appartengono. In questo caso, gli utenti probabilmente doranno esaminare ogni scheda per trovarle e quindi dimenticare tempestivamente dove si trovano.
- **Evitare il posizionamento basato sul marketing.** Si supponga di avere una nuova versione del programma e che il team di marketing voglia effettivamente promuovere le nuove funzionalità. Potrebbe essere allettante inserire questi dati nella scheda Home, ma questa operazione è un errore dis costoso se danneggia l'individuabilità complessiva. Prendere in considerazione le versioni future del prodotto e il livello di frustrazione che un'organizzazione in continua evoluzione causerà.

### <a name="tabs"></a>Schede

Il primo passaggio migliore consiste nell'esaminare le schede [standard della barra multifunzione](#standard-ribbon-tabs). Se i comandi del programma vengono mappati naturalmente alle schede standard, basare l'organizzazione delle schede su questi standard. D'altra parte, se i comandi del programma non vengono mappati in modo naturale, non provare a forzarlo. Determinare una struttura più naturale e assicurarsi di eseguire molti test utente per assicurarsi che sia stata eseguita nel modo giusto.

Per le schede non standard, considerare questi problemi:

- **Ogni nome di scheda deve descrivere il contenuto.** Scegliere nomi significativi specifici, ma non troppo specifici. Gli utenti non devono mai essere sorpresi dal contenuto.
- **Ogni nome di scheda deve riflettere lo scopo.** Prendere in considerazione l'obiettivo o l'attività associata ai comandi.
- **Ogni nome di scheda deve essere chiaramente diverso da tutti gli altri nomi di scheda.**

La scheda Home è un'eccezione a queste considerazioni. Anche se non è necessario avere una scheda Home, la maggior parte dei programmi lo dovrebbe fare. La scheda Home è la prima scheda e contiene i comandi usati più di frequente. Se sono stati usati di frequente comandi che non rientrano nelle altre schede, la scheda Home è la posizione più adatta.

Se non è possibile determinare un nome di scheda descrittivo significativo, è probabile che la scheda non sia ben progettata. Se l'organizzazione della barra multifunzione non funziona, riconsiderare la progettazione delle schede.

### <a name="groups"></a>Gruppi

Dividendo i comandi in gruppi, i comandi vengono strutturati in set correlati. L'etichetta di gruppo illustra lo scopo comune dei comandi.

Esistono diversi fattori da considerare quando si determinano i gruppi e la relativa presentazione:

- **Raggruppamento standard.** Anche se esistono differenze significative nei comandi tra i programmi, esistono [gruppi standard](#standard-ribbon-groups) comuni in molti programmi. La visualizzazione di questi comandi con gli stessi nomi e posizioni simili migliora notevolmente l'individuabilità.

| Risposta esatta.                                                                                      | Risposta errata                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![Screenshot dello zoom separato dal gruppo di modifica ](images/cmd-ribbons-image13.png)<br/>Il gruppo di comandi di modifica include tutti i comandi di modifica, ma non il comando Zoom.         | ![Screenshot dello zoom incluso nel gruppo di modifica ](images/cmd-ribbons-image14.png)<br/>Il comando Zoom non è un comando di modifica, ma fa parte del gruppo di modifica. |

- **Granularità.** Una struttura è buona, ma una struttura troppo grande rende i comandi più difficili da trovare. Se i nomi dei gruppi sono generici, la granularità potrebbe non essere sufficiente. Se sono presenti gruppi con solo uno o due comandi ciascuno, è probabile che si abbia un numero troppo grande (anche se la presenza di una raccolta nella barra multifunzione senza altri comandi all'interno di un gruppo è accettabile).

| Risposta esatta.                                                                                                 | Risposta errata                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![Screenshot dello zoom separato dal gruppo di modifica ](images/cmd-ribbons-image13.png)<br/> Il gruppo di comandi di modifica include tutti i comandi di modifica| ![Screenshot della modifica del gruppo suddiviso in due gruppi ](images/cmd-ribbons-image15.png)<br/>Il gruppo di comandi di modifica è stato suddiviso in sezioni troppo granulari. Evitare i gruppi con uno o due comandi.|

- **Nomi.** I nomi di gruppo validi spiegano lo scopo dei comandi. Se i nomi dei gruppi non lo sono, riconsiderare il nome o il raggruppamento. Se non è possibile determinare un nome descrittivo significativo, è probabile che il gruppo non sia ben progettato.

| Risposta esatta.                                                                                                 | Risposta errata                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![Screenshot dei comandi suddivisi in quattro gruppi ](images/cmd-ribbons-image17.png) <br/> Usare nomi di gruppo sufficientemente specifici per descrivere i comandi contenuti nel gruppo. | ![Screenshot del gruppo di formato con diversi comandi ](images/cmd-ribbons-image16.png) <br/> Questo nome di gruppo è troppo vago per essere utile. Un approccio migliore consiste nel riorganizzare questi comandi in gruppi più specifici. |

- **Ordine.** Le persone leggono in ordine da sinistra a destra (nelle culture occidentali), quindi si potrebbe pensare che i gruppi all'estrema sinistra siano i più evidenti. Tuttavia, il nome della scheda evidenziato e il contenuto della finestra tendono a fungere da [punti focali,](vis-layout.md)quindi i gruppi al centro della scheda ricevono in genere più attenzione del gruppo più a sinistra. Posizionare i gruppi usati più di frequente nelle posizioni più importanti e assicurarsi che sia presente un flusso logico per i gruppi nella scheda.

![Screenshot del gruppo Appunti all'estrema sinistra ](images/cmd-ribbons-image18.png)

In questo esempio, i gruppi Carattere e Paragrafo sono più evidenti rispetto al gruppo Appunti, perché sono ciò che l'occhio vede per primo quando si sposta verso l'alto dal documento.

![Screenshot del gruppo di rilevamento nella scheda revisione ](images/cmd-ribbons-image19.png)

In questo esempio il gruppo Rilevamento riceve la massima attenzione, in parte perché la scheda Revisione evidenziata funge da punto focale.

- **Uniformità.** Può essere difficile riconoscere i comandi quando la presentazione del comando ha lo stesso aspetto. L'uso di icone con forme e colori diversi, gruppi con formati diversi e comandi di dimensioni diverse semplifica il riconoscimento dei gruppi di comandi da parte degli utenti. I comandi devono avere un ridimensionamento uniforme solo quando la barra multifunzione viene ridotta alle dimensioni inferiori.

| Risposta esatta. | Risposta errata |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Screenshot del gruppo con icone di dimensioni diverse ](images/cmd-ribbons-image20.png)<br/>Usare un'ampia gamma di dimensioni delle icone per migliorare la riconoscibilità| ![Screenshot del gruppo con icone delle stesse dimensioni ](images/cmd-ribbons-image21.png)<br/>Questi comandi sono troppo simili l'uno all'altro perché hanno tutte le stesse dimensioni. |

### <a name="previews"></a>Anteprime

È possibile usare vari tipi di anteprime per visualizzare i risultati di un comando. Usando anteprime utili, è possibile migliorare l'efficienza del programma e ridurre la necessità dell'approccio di apprendimento basato su versioni di valutazione ed errori. Le anteprime live invitano anche alla sperimentazione e incoraggiano la creatività.

Ecco alcuni dei diversi tipi di anteprime che è possibile usare:

- **Icone statiche realistiche e grafica.** Immagini statiche che forniscono un'indicazione realistica dell'effetto di un comando. Possono essere usati nelle raccolte, nei menu a discesa e nelle descrizioni comando avanzate.

![Screenshot dell'elenco a discesa dei tipi di carattere ](images/cmd-ribbons-image22.png)

In questo esempio l'elenco a discesa Tipo di carattere mostra ogni nome del tipo di carattere usando il tipo di carattere stesso.

![Screenshot della raccolta di anteprime delle filigrane ](images/cmd-ribbons-image23.png)

In questo esempio vengono usate anteprime realistiche per visualizzare le diverse filigrane.

- **Icone dinamiche e grafica.** Icone e grafica modificate per riflettere lo stato corrente. Queste icone sono particolarmente utili per le raccolte, nonché per i pulsanti di divisione che modificano l'effetto predefinito in modo che siano uguali all'ultima azione.

![Screenshot della raccolta di stili di paragrafo ](images/cmd-ribbons-image24.png)

In questo esempio, Microsoft Word la raccolta Stili per riflettere gli stili correnti.

![Screenshot dei pulsanti di comando per la formattazione del testo ](images/cmd-ribbons-image25.png)

In questo esempio Word modifica i comandi Colore evidenziazione testo e Colore carattere per indicarne l'effetto corrente.

- **Anteprime live.** Quando gli utenti passano il mouse su un'opzione di formattazione, l'anteprima live mostra l'aspetto dei risultati con tale formattazione. Le anteprime live consentono agli utenti di effettuare selezioni in modo più efficiente e sicuro in base al contesto effettivo dell'utente.

![Screenshot del selettore del colore del comando colore della pagina ](images/cmd-ribbons-image26.png)

In questo esempio, il comando Colore pagina esegue un'anteprima dinamica visualizzando l'effetto delle opzioni di colore al passaggio del mouse.

Le anteprime live sono una funzionalità potente che può davvero migliorare la produttività degli utenti, ma anche le anteprime statiche semplici possono essere di grande aiuto.

### <a name="scaling-the-ribbon"></a>Ridimensionamento della barra multifunzione

Il ridimensionamento di una barra degli strumenti è semplice: se una finestra è troppo stretta per visualizzare una barra degli strumenti, la barra degli strumenti visualizza ciò che si adatta e rende tutto il resto accessibile tramite un pulsante di overflow. L'obiettivo dei comandi completi è sfruttare al meglio lo spazio disponibile, quindi il ridimensionamento di una barra multifunzione richiede più lavoro di progettazione. Non esistono dimensioni predefinite della barra multifunzione, pertanto non è consigliabile progettare una barra multifunzione con una larghezza specifica. È necessario progettare layout con un'ampia gamma di larghezze e rendersi conto che uno di essi potrebbe essere quello che la maggior parte degli utenti vede. Il ridimensionamento è una parte fondamentale della progettazione della barra multifunzione, non l'ultimo passaggio. Quando si progetta una scheda, specificare i diversi layout per ogni gruppo (fino a tre) e le combinazioni che possono essere usate insieme. La barra multifunzione mostrerà la combinazione valida più grande adatta alle dimensioni correnti della finestra.

![Screenshot dei comandi di formattazione nel menu di overflow Le barre degli strumenti vengono ](images/cmd-ribbons-image27.png) ridimensionate usando un pulsante di overflow.

![Screenshot delle barre multifunzione con varie larghezze ](images/cmd-ribbons-image28.png) Non sono presenti dimensioni predefinite della barra multifunzione. La dimensione più piccola è una singola icona del gruppo popup.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

- **Non combinare barre multifunzione con barre dei menu e barre degli strumenti all'interno di una finestra.** Le barre multifunzione devono essere usate al posto delle barre dei menu e delle barre degli strumenti. Tuttavia, una barra multifunzione può essere combinata con le finestre della tavolozza e gli elementi di spostamento, ad esempio i pulsanti Indietro e Avanti e una barra degli indirizzi.
- **Combinare sempre una barra multifunzione con un pulsante Applicazione e una barra di accesso rapido.**
- **Selezionare la scheda più a sinistra (in genere Home) all'avvio di un programma.** Non rendere persistente l'ultima scheda selezionata tra le istanze del programma.
- **Visualizzare la barra multifunzione nello stato normale (non ridotto a icona) quando un programma viene avviato per la prima volta.** Gli utenti spesso lasciano invariate le impostazioni predefinite, quindi ridurre al minimo la barra multifunzione all'avvio del programma causerà probabilmente una minore efficienza di tutti i comandi. Inoltre, la visualizzazione iniziale della barra multifunzione ridotta a icona può disorientare.
- **Rendere persistente lo stato della barra multifunzione tra le istanze del programma.** Ad esempio, se un utente riduce a icona la barra multifunzione, verrà visualizzata ridotta a icona alla successiva esecuzione del programma. Ma anche in questo caso, non rendere persistente l'ultima scheda selezionata in questo modo.

### <a name="using-tabs"></a>Uso delle schede

In genere, è consigliabile avere meno schede, quindi rimuovere le schede che non consentono di raggiungere questi obiettivi.

- **Quando è pratica, usare le schede standard.** L'uso di schede standard migliora notevolmente l'individuabilità, in particolare tra i programmi. Vedere le schede [standard della barra multifunzione](#standard-ribbon-tabs) più avanti in questo articolo.
- **Assegnare un'etichetta alla prima scheda Home, se appropriato.** La scheda Home deve contenere i comandi usati più di frequente. Se sono stati usati spesso comandi che non rientrano nelle altre schede, la scheda Home è la posizione più adatta.
- Aggiungere una nuova scheda se:
  - **I comandi sono fortemente correlati ad attività specifiche e possono essere descritti in modo accurato dall'etichetta della scheda.** L'aggiunta della scheda consente di semplificare l'individuazione dei comandi e non di renderli più difficili.
  - **I comandi non sono per lo più correlati alle attività in altre schede.** L'aggiunta della scheda non dovrebbe richiedere più tab switching durante le attività eseguite comunemente.
  - **La scheda dispone di comandi sufficienti per giustificare la presenza di un'ulteriore posizione in cui cercare.** Non sono disponibili schede con pochi comandi. **Eccezione:** È consigliabile aggiungere una scheda con alcuni comandi se sono strettamente correlati a un'attività specifica e aggiungere la scheda semplifica notevolmente una scheda Home troppo complessa.
- **Per le schede rimanenti, posizionare prima le schede usate più di frequente, mantenendo un ordine logico tra le schede.**
- **Ottimizzare la progettazione della scheda in modo che gli utenti trovino i comandi in modo rapido e sicuro.** Tutte le altre considerazioni sono secondarie.
- **Non specificare una scheda Guida.** Fornire invece assistenza usando la Guida a livello di programma e le descrizioni comando avanzate.
- **Usare un massimo di sette schede principali.** Se sono presenti più di sette, diventa difficile determinare quale scheda include un comando. Sebbene sette schede di base siano accettabili per le applicazioni con molti comandi, la maggior parte dei programmi deve puntare a quattro o meno schede.

### <a name="contextual-tabs"></a>Schede contestuali

- **Usare una scheda contestuale per visualizzare una raccolta di comandi rilevanti solo quando gli utenti selezionano un particolare tipo di oggetto.** Se sono presenti solo pochi comandi usati di frequente, può essere più comodo e stabile usare una scheda normale e disabilitare semplicemente i comandi quando non si applicano.
- ![Screenshot dei comandi taglia e copia in grigio ](images/cmd-ribbons-image29.png)<br>È meglio disabilitare i comandi comuni, ad esempio Taglia e Copia, piuttosto che usare una scheda contestuale.
- **Includere solo i comandi specifici di un determinato tipo di oggetto.** Non inserire i comandi solo in una scheda contestuale se gli utenti potrebbero aver bisogno di questi comandi senza prima selezionare un oggetto.
- **Includere i comandi usati di frequente quando si usa un particolare tipo di oggetto.** Inserire i comandi contestuali generali usati di frequente nei menu di scelta rapida e nelle mini-barre degli strumenti per evitare il cambio di tabulazione durante le attività più comuni. In alternativa, è consigliabile inserire i comandi generali in modo ridondante in una scheda contestuale, se si evita di passare spesso da una scheda all'altra. Tuttavia, non esagerare: non provare a includere tutti i comandi che un utente potrebbe avere bisogno durante l'uso dell'oggetto.
- ![Screenshot del comando dei bordi nella scheda progettazione ](images/cmd-ribbons-image30.png)<br/>In questo esempio il comando Bordi è incluso nella scheda Progettazione per evitare il passaggio frequente da una scheda all'altro durante le attività più comuni.\
- **Scegliere un colore della scheda contestuale diverso dalle schede contestuali attualmente visualizzate.** Lo stesso set di schede può essere visualizzato in un secondo momento usando un colore diverso per ottenere questo risultato, ma provare a usare assegnazioni di colore coerenti tra le chiamate quando possibile.
- **La selezione di una scheda contestuale** favorisce automaticamente l'individuabilità, migliora la percezione della stabilità e riduce la necessità di passare da una scheda all'altra. Selezionare automaticamente una scheda contestuale quando:
  - **L'utente inserisce un oggetto .** In questo caso, selezionare la prima scheda contestuale nel set.
  - **L'utente fa doppio clic su un oggetto.** In questo caso, selezionare la prima scheda contestuale nel set.
  - **L'utente ha selezionato una scheda contestuale, ha fatto clic sull'oggetto e quindi ha fatto immediatamente clic su un oggetto dello stesso tipo.** In questo caso, tornare alla scheda contestuale selezionata in precedenza.
- **Quando si rimuove una scheda contestuale che è la scheda attiva,** impostare la scheda Home o la prima scheda come scheda attiva. In questo modo viene visualizzato il più stabile.

### <a name="modal-tabs"></a>Schede modali

- **Usare una scheda modale per visualizzare una raccolta di comandi che si applicano a una particolare modalità temporanea e nessuna delle schede principali è applicabile.** Se si applicano alcune delle schede principali, usare invece una scheda contestuale e disabilitare i comandi non applicabili. Poiché le schede modali sono molto limitanti, devono essere usate solo quando non esiste un'alternativa migliore.
- ![Screenshot della scheda dell'anteprima di stampa ](images/cmd-ribbons-image31.png)<br/>L'anteprima di stampa è una scheda modale di uso comune.
- **Per chiudere una scheda modale, inserire il comando <mode> Chiudi come ultimo comando nella scheda.** Usare l'icona Chiudi per semplificare la ricerca del comando. Assegnare la modalità nel comando per evitare confusione su ciò che viene chiuso.
- ![Screenshot del pulsante Chiudi anteprima di stampa ](images/cmd-ribbons-image32.png)<br/>In questo esempio, l'etichettatura esplicita del comando Close con la modalità rimuove qualsiasi dubbio su ciò che viene chiuso.
- **Per chiudere una scheda modale, ridefinire anche il pulsante Chiudi sulla barra del titolo della finestra per chiudere la modalità anziché il programma.** I test degli utenti hanno dimostrato che molti utenti si aspettano questo comportamento.

### <a name="standard-ribbon-tabs"></a>Schede della barra multifunzione standard

Quando possibile, eseguire il mapping dei comandi del programma a queste schede standard, in base all'ordine di aspetto standard.

#### <a name="regular-tabs"></a>Schede normali

- **Casa.** Contiene i comandi usati più di frequente. Se usato, è sempre la prima scheda.
- **Inserire.** Contiene comandi per inserire contenuto e oggetti in un documento. Se usato, è sempre la seconda scheda.
- **Layout di pagina.** Contiene comandi che influiscono sul layout di pagina, inclusi temi, impostazione della pagina, sfondi della pagina, rientro, spaziatura e posizionamento. Si noti che i gruppi di rientri e spaziatura possono invece essere nella scheda Home, se c'è spazio sufficiente. Se usato, è sempre la terza scheda.
- **Recensione.** Contiene comandi per aggiungere commenti, tenere traccia delle modifiche e confrontare le versioni.
- **Mostra.** Contiene comandi che influiscono sulla visualizzazione del documento, tra cui la modalità di visualizzazione, le opzioni di visualizzazione/nascondi, lo zoom, la gestione delle finestre e le macro, i comandi tradizionalmente presenti nella categoria Windows menu. Se usata, è l'ultima scheda normale, a meno che non venga visualizzata la scheda Sviluppatore.
- **Sviluppatore.** Contiene i comandi usati solo dagli sviluppatori. Se usato, è nascosto per impostazione predefinita e l'ultima scheda normale quando viene visualizzata.

La maggior parte dei programmi non ha bisogno delle schede Rivedi e Sviluppatore.

#### <a name="standard-contextual-tabs"></a>Schede contestuali standard

- **Formato.** Contiene i comandi correlati alla modifica del formato del tipo di oggetto selezionato. In genere si applica a parte di un oggetto.
- **Design.** Contiene comandi, spesso nelle raccolte, per applicare stili al tipo di oggetto selezionato. In genere si applica all'intero oggetto.
- **Layout.** Contiene comandi per modificare la struttura di un oggetto complesso, ad esempio una tabella o un grafico.

Se si dispone di comandi contestuali correlati al formato, alla progettazione e al layout, ma non sono sufficienti per più schede, è sufficiente specificare una scheda Formato.

### <a name="standard-groups"></a>Gruppi standard

- **Quando possibile, usare gruppi standard.** La presenza di comandi comuni con gli stessi nomi e posizioni simili migliora notevolmente l'individuabilità. Vedere i gruppi [standard della barra multifunzione](#standard-ribbon-groups) più avanti in questo articolo.
- **Aggiungere un nuovo gruppo** se:
  - **I comandi sono fortemente correlati e possono essere descritti in modo accurato dall'etichetta del gruppo.** L'aggiunta del gruppo dovrebbe semplificare l'individuazione dei comandi, non più difficili.
  - **I comandi hanno una relazione più debole con i comandi in altri gruppi.** Anche se tutti i comandi in una scheda devono essere strettamente correlati, alcune relazioni di comando sono più forti di altre.
  - **Il gruppo dispone di comandi sufficienti per giustificare la presenza di un altro punto di controllo.** Puntare a 3-5 comandi per la maggior parte dei gruppi. Evitare di avere gruppi con solo 1-2 comandi, anche se la presenza di una raccolta nella barra multifunzione senza altri comandi all'interno di un gruppo è accettabile. La presenza di molti gruppi con un singolo comando suggerisce una struttura troppo grande o una mancanza di coerenza dei comandi.
- **Non sovra-organizzare aggiungendo** gruppi in cui non sono necessari.
- **È consigliabile suddividere un gruppo** se:
  - ![Screenshot del gruppo di comandi disorganizzato ](images/cmd-ribbons-image35.png)<br/>Il gruppo ha molti comandi di dimensioni diverse e richiede un'organizzazione.
  - ![Screenshot di due nomi di gruppi di paragrafi lunghi ](images/cmd-ribbons-image33.png)<br>Il gruppo include comandi che traggono grande vantaggio dalla disponibilità di etichette aggiuntive.
- **Posizionare i gruppi usati più di frequente nelle posizioni più importanti e assicurarsi che sia presente un ordine logico per i gruppi nella scheda.**
- **Ottimizzare la progettazione dei gruppi in modo che gli utenti trovino i comandi in modo rapido e sicuro.** Tutte le altre considerazioni sono secondarie.
- **Non ridimensionare i gruppi contenenti un singolo pulsante in un'icona di gruppo popup.** Quando si esegue la riduzione, lasciarli come un singolo pulsante.
- **Usare un massimo di sette gruppi.** Se sono presenti più di sette gruppi, diventa più difficile determinare quale gruppo dispone di un comando.

### <a name="standard-ribbon-groups"></a>Gruppi della barra multifunzione standard

Quando possibile, eseguire il mapping dei comandi del programma a questi gruppi standard, che vengono visualizzati all'interno delle schede associate nell'ordine di aspetto standard.

#### <a name="main-tab"></a>Scheda principale

- Appunti
- Carattere
- Paragraph
- In fase di modifica

#### <a name="insert-tab"></a>Scheda Inserisci

- Tabelle
- Illustrazioni

#### <a name="page-layout-tab"></a>Scheda Layout di pagina

- Temi
- Impostazioni di pagina
- Disponi

#### <a name="review-tab"></a>Scheda Rivedi

- Controllo ortografico
- Commenti

#### <a name="view-tab"></a>Scheda Visualizza

- Visualizzazioni documento
- Mostra/Nascondi
- Zoom
- Finestra

### <a name="commands"></a>Comandi

- ![Screenshot del comando dei numeri di riga sulla barra multifunzione ](images/cmd-ribbons-image36.png)<br/>**Sfruttare l'individuabilità e la scalabilità delle barre multifunzione esponendo tutti i comandi di uso comune.** Se appropriato, spostare i comandi usati di frequente dalle finestre di dialogo alla barra multifunzione, in particolare quelli che sono noti per essere difficili da trovare. Idealmente, gli utenti devono essere in grado di eseguire attività comuni senza usare finestre di dialogo.

- **Non usare la scalabilità delle barre multifunzione per giustificare l'aggiunta di complessità non necessaria.** Continuare ad esercitare la moderazione non aggiungere comandi a una barra multifunzione solo perché è possibile. Mantenere semplice l'esperienza complessiva dei comandi. Di seguito sono riportati i modi per semplificare la presentazione:
  - ![Screenshot della barra degli strumenti e del menu di scelta rapida mini ](images/cmd-ribbons-image37.png)</br>**Usare menu di scelta rapida e mini-barre degli strumenti per i comandi contestuali sul posto.**
  - **Spostare (o mantenere) comandi usati raramente nelle finestre di dialogo.** Usare le finestre di avvio delle finestre di dialogo per accedere a questi comandi. È comunque possibile usare le finestre di dialogo con le barre multifunzione. È sufficiente provare a ridurre la necessità di usarli durante le attività comuni.
  - **Eliminare le funzionalità ridondanti e usate raramente.**

#### <a name="presentation"></a>Presentazione

- **Presentare ogni comando in una sola scheda. Evitare più percorsi per lo stesso comando, soprattutto se il comando richiede molti clic per richiamare.** Può sembrare una comodità trovare un comando in più percorsi. Tenere tuttavia presente che quando gli utenti trovano ciò che cercano, smetti di cercare. È troppo facile per gli utenti presupporre che il primo percorso trovato sia l'unico percorso che rappresenta un problema grave se tale percorso è inefficiente. **Eccezione:** Le schede contestuali possono duplicare alcuni comandi dalle schede Home e Inserisci se questa operazione impedisce la modifica delle schede per le attività contestuali comuni.
- **All'interno di un gruppo, inserire i comandi nell'ordine logico, dando la preferenza ai comandi usati più di frequente.** In generale, i comandi devono avere un flusso logico per semplificare l'individuazione, mantenendo i comandi usati più di frequente. In genere, i comandi con icone da 32x32 pixel vengono visualizzati prima dei comandi con icone da 16 x 16 pixel per facilitare la scansione tra gruppi.
- **Evitare di posizionare comandi distruttivi accanto ai comandi usati di frequente.** Un comando è considerato distruttivo se il suo effetto è diffuso e non può essere facilmente annullato o l'effetto non è immediatamente evidente.
- **Usare i separatori per indicare comandi fortemente correlati, ad esempio un set di opzioni che si escludono a vicenda.**
- ![Screenshot dei gruppi di caratteri e paragrafi ](images/cmd-ribbons-image3.png)<br/> **Prendere in considerazione l'uso di gruppi di stile della barra degli strumenti per set di comandi fortemente correlati e noti che non necessitano di etichette.** In questo modo è possibile presentare molti comandi in uno spazio compatto senza influire sull'individuabilità e sulla facilità di apprendimento. Per essere così noti, questi comandi vengono spesso usati, riconosciuti immediatamente e quindi tendono a essere nella scheda Home.

- **Usare icone da 32x32 pixel per i comandi con etichetta più usati e importanti.** Quando si ridimensiona un gruppo verso il basso, impostare questi comandi come ultimi per la conversione in icone di 16x16 pixel.
- **Evitare il posizionamento arbitrario dei comandi.** Valutare attentamente la progettazione di schede e gruppi per assicurarsi che gli utenti non spredranno tempo controllando ogni scheda per trovare il comando desiderato.
- **Evitare il posizionamento basato sul marketing.** Gli obiettivi di marketing per la promozione di nuove funzionalità tendono a cambiare nel tempo. Considerare le versioni future del prodotto e il livello di frustrazione causato da un'organizzazione in continua evoluzione.

#### <a name="interaction"></a>Interazione

- **Disabilitare i comandi che non si applicano al contesto corrente o che restituirebbero direttamente un errore.** Se utile, usare la [descrizione comando avanzata](glossary.md) per spiegare perché il comando è disabilitato. Non nascondere questi comandi perché questa operazione può causare la modifica del layout della barra multifunzione, rendendo la presentazione della barra multifunzione instabile.
- **Non aggiornare le etichette dei comandi in modo dinamico.** Anche in questo caso, il layout della scheda potrebbe cambiare, con un aspetto instabile. Progettare invece i comandi in modo che funzionino con etichette costanti.

    | Risposta esatta.                                                                                       | Risposta errata                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![Screenshot della nota di inserimento e dell'eliminazione di una nota ](images/cmd-ribbons-image38.png)<br/> Disabilitare i comandi quando non sono disponibili | ![Screenshot della nota di inserimento, nessuna nota di eliminazione ](images/cmd-ribbons-image39.png)<br/>Non nascondere i comandi, anche quando non sono disponibili |

- **Preferisce i controlli diretti.** Un comando è diretto se richiamato con un solo clic, ovvero senza spostarsi tra i menu. Tuttavia, ad eccezione delle raccolte nella barra multifunzione, i controlli diretti non supportano l'anteprima live, quindi anche la necessità di un'anteprima live è un fattore importante.
- **Usare l'anteprima** dinamica per indicare l'effetto delle opzioni quando un comando è tra un set correlato di opzioni di formattazione e l'anteprima dinamica è importante e pratica, soprattutto se gli utenti potrebbero scegliere l'opzione errata in caso contrario.
  - Se il comando viene usato di frequente, usare una raccolta nella barra multifunzione per la direttezza.
  - Se il comando viene usato raramente, usare una raccolta a discesa.
- **Esporre i comandi diretti** usando i controlli seguenti nell'ordine di preferenza seguente
  - **Pulsanti di comando, caselle di controllo, pulsanti di opzione e raccolte sul posto.** Questi sono sempre diretti.
  - **Pulsanti di divisione.** Diretto per il comando più comune, ma indiretto per le variazioni di comando.
  - **Pulsanti di menu.** Questi sono indiretti, ma presentano molti comandi facili da trovare.
  - **Caselle di testo (con controlli di selezione).** L'input di testo richiede in genere più impegno rispetto agli altri tipi di controllo.
- ![Screenshot della barra multifunzione con solo pulsanti di menu ](images/cmd-ribbons-image42.png)</br>Se la barra multifunzione è costituita principalmente da pulsanti di menu quando vengono visualizzati a dimensioni complete, è anche possibile usare una barra dei menu.
- **Preferire i comandi immediati.** ![Screenshot del pulsante Dividi stampa e del relativo sottomenu ](images/cmd-ribbons-image43.png)<br/>Un comando è immediato se viene eseguito immediatamente, ovvero senza finestre di dialogo per raccogliere input aggiuntivo. Se un comando può richiedere input, è consigliabile usare un pulsante di divisione, con il comando immediato nella parte del pulsante e i comandi che richiedono l'input nel sottomenu.

### <a name="galleries"></a>Raccolte

**Usare una [raccolta](glossary.md)** se:

- **Esiste un set ben definito e correlato di opzioni tra cui gli utenti scelgono in genere.** È possibile che sia presente un numero illimitato di variazioni, ma è probabile che le selezioni siano ben contenute. Se le scelte non sono strettamente correlate, è consigliabile usare raccolte separate.
- **Le scelte sono meglio espresse visivamente, ad esempio le funzionalità di formattazione.** L'uso delle anteprime semplifica l'esplorazione, la comprensione e la scelta. Anche se le scelte possono essere etichettate, la selezione viene effettuata visivamente e non è necessario che le etichette di testo siano necessarie per comprendere le scelte.
- **Le scelte mostrano il risultato ottenuto immediatamente con un solo clic.** Non deve essere presente alcuna finestra di dialogo di follow-up per chiarire ulteriormente l'intenzione dell'utente o un set di passaggi per ottenere il risultato indicato. Se gli utenti potrebbero voler modificare la scelta, lasciare che lo facciano in un secondo momento.

**Usare una raccolta nella barra multifunzione** se:

- **Le scelte vengono usate di frequente.** Le scelte necessitano dello spazio e valgono lo spazio potenzialmente preso da altri comandi.
- **Per un utilizzo tipico, non è necessario raggruppare o filtrare le scelte presentate.**
- **Le scelte possono essere visualizzate in modo efficace all'interno dell'altezza di una barra multifunzione (ovvero 48 pixel).**

#### <a name="thumbnails-in-galleries"></a>Anteprime nelle raccolte

**Scegliere le dimensioni di anteprima della raccolta standard più piccole** per il processo.

- Per le raccolte nella barra multifunzione, usare anteprime di 16x16, 48x48 o 64x48 pixel.
- Per le raccolte a discesa, usare anteprime di 16x16, 32x32, 48x48, 64x48, 72x96, 96x72, 96x96 o 128x128 pixel.
- Tutti gli elementi della raccolta devono avere le stesse dimensioni di anteprima.

Per le raccolte nella barra multifunzione:

- **Visualizzare un minimo di tre opzioni; altro se c'è spazio.** Se lo spazio disponibile non è sufficiente per visualizzare almeno tre opzioni nelle dimensioni tipiche della finestra, usare invece una raccolta a discesa.
- **Espandere le raccolte nella barra multifunzione per sfruttare lo spazio disponibile.** Usare lo spazio aggiuntivo per visualizzare più elementi e semplificarne la scelta con un solo clic.

Per le raccolte a discesa:

- **Visualizzare la raccolta da una casella combinata, un elenco a discesa, un pulsante di divisione o un pulsante di menu.**
- **Se l'utente fa clic sulla finestra principale per chiudere la raccolta a discesa, è sufficiente chiudere la raccolta senza selezionare o modificare il contenuto della finestra principale.**
- **Se una raccolta ha molte scelte e alcune scelte vengono usate raramente, semplificare la raccolta predefinita concentrandosi sulle scelte di uso comune.** Per i comandi rimanenti, specificare un comando appropriato nella parte inferiore dell'elenco a discesa della raccolta.
  - Se il comando visualizza un elenco di altre varianti, assegnare al comando il nome "Altre `singular feature name` opzioni..."
  - Se il comando presenta una finestra di dialogo che consente agli utenti di creare opzioni personalizzate, assegnare il nome `feature name` "Personalizzato..."
- **Organizzare le scelte in gruppi, se si esegue questa operazione rende più efficiente l'esplorazione.**
- ![Screenshot della raccolta di simboli e dei filtri ](images/cmd-ribbons-image44.png)<br/>**Se una raccolta include molti elementi, è consigliabile aggiungere un filtro per consentire agli utenti di trovare le scelte in modo più efficiente.** Per evitare confusione, visualizzare inizialmente la raccolta senza filtri. Tuttavia, la maggior parte delle raccolte non deve richiedere un filtro perché non devono avere così tante scelte e l'uso dei gruppi dovrebbe essere sufficiente.

### <a name="command-previews"></a>Anteprime dei comandi

- **Usare le anteprime per visualizzare l'effetto di un comando senza che gli utenti lo devono eseguire per primo.** Usando le anteprime utili, è possibile migliorare l'efficienza e la facilità di apprendimento del programma e ridurre la necessità di tentativi ed errori. Per i diversi tipi di anteprime dei comandi, vedere [Anteprime](#previews) nella sezione Concetti di progettazione di questo articolo.
- **Per le anteprime live, assicurarsi che l'anteprima possa essere applicata e che lo stato corrente sia ripristinato entro 500 millisecondi.** Questa operazione richiede la possibilità di applicare le modifiche di formattazione in modo rapido e in un modo che sia interrompibile. Gli utenti devono essere in grado di valutare rapidamente diverse opzioni per consentire alle anteprime live di usufruire del vantaggio completo.
- **Evitare di usare il testo nelle anteprime.** In caso contrario, le immagini di anteprima doranno essere localizzate.

### <a name="icons"></a>Icone

- ![Screenshot dell'elenco a discesa e delle caselle di controllo ](images/cmd-ribbons-image45.png)<br/>**Specificare le icone per tutti i controlli della barra multifunzione, ad eccezione degli elenchi a discesa, delle caselle di controllo e dei pulsanti di opzione.** La maggior parte dei comandi richiede icone di 32x32 e 16x16 pixel (solo le icone 16x16 pixel vengono usate dalla barra di accesso rapido). Le raccolte usano in genere icone 16x16, 48x48 o 64x48 pixel.
- **Specificare icone univoche.** Non usare la stessa icona per comandi diversi.
- **Assicurarsi che le icone della barra multifunzione siano chiaramente visibili sul colore di sfondo della barra multifunzione.** Valutare sempre le icone della barra multifunzione nel contesto e in modalità a contrasto elevato.
- **Scegliere le progettazioni di icone che comunicano chiaramente il loro effetto,** in particolare per i comandi usati più di frequente. Le barre multifunzione ben progettate hanno icone auto-esplicativi che consentono agli utenti di trovare e comprendere i comandi in modo efficiente.
- **Scegliere icone riconoscibili e distinguibili,** in particolare per i comandi usati più di frequente. Assicurarsi che le icone presentino forme e colori distintivi. Questa operazione consente agli utenti di trovare rapidamente i comandi, anche se non ricordano il simbolo dell'icona.

    | Risposta esatta.                                                                                                 | Risposta errata                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![Screenshot del contagocce blu e della matita gialla ](images/cmd-ribbons-image46.png)<br/>Usare la forma e il colore per creare icone facili da distinguere. | ![Screenshot del contagocce blu e della matita blu ](images/cmd-ribbons-image47.png)<br/> Le icone dello stesso colore sono difficili da distinguere|

- ![Screenshot del comando comments nel contenitore popup ](images/cmd-ribbons-image48.png)<br/>**Provare a creare icone di gruppo popup posizionando l'icona 16x16 pixel del comando più importante nel gruppo all'interno di un contenitore visivo da 32x32 pixel.** Non è necessario creare icone diverse per i gruppi popup.
- ![Screenshot dei pulsanti di comando per la formattazione del testo ](images/cmd-ribbons-image25.png)<br/>**Se utile, modificare l'icona in modo che rifletta lo stato corrente.** Questa operazione è particolarmente utile per i pulsanti di divisione il cui effetto predefinito può cambiare.
- **Assicurarsi che le icone della barra multifunzione siano conformi alle linee guida per le icone in stile Aero.** Tuttavia, le icone della barra multifunzione vengono visualizzate direttamente anziché in prospettiva.

| Risposta esatta.                                                                                                 | Risposta errata                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![Screenshot delle icone dei comandi bidimensionali ](images/cmd-ribbons-image49.png)<br/> Usare icone bidimensionali.|![Screenshot delle icone dei comandi tridimensionali ](images/cmd-ribbons-image50.png)<br/> Non usare icone tridimensionali. |
 
### <a name="enhanced-tooltips"></a>Descrizioni comando avanzate

- **Tutti i comandi della barra multifunzione devono avere descrizioni comando avanzate** per assegnare il nome del comando, il tasto di scelta rapida, la descrizione e informazioni supplementari facoltative. Evitare descrizioni comando che restate semplicemente l'etichetta.

    **Non corretto:**

    ![Screenshot della descrizione comando che ripete il nome del comando ](images/cmd-ribbons-image51.png)

    In questo esempio, la descrizione comando ripristina semplicemente l'etichetta del comando.

- **Quando pratico, descrivere completamente il comando usando una descrizione concisa.** Collegarsi alla Guida solo se sono effettivamente necessarie ulteriori spiegazioni.

    **Non corretto:**

    ![Screenshot della descrizione comando per il comando barrato ](images/cmd-ribbons-image52.png)

    In questo esempio il comando non richiede la Guida.

- **Se utile, illustrare l'effetto del comando usando un'anteprima.**

    ![Screenshot della descrizione comando e del grafico per l'inserimento di un grafico ](images/cmd-ribbons-image53.png)

    In questo esempio l'immagine della descrizione comando illustra l'effetto del comando.

Per le linee guida per l'etichettatura, vedere [Etichette di descrizione comando avanzate.](#enhanced-tooltips)

### <a name="access-keys-and-keytips"></a>Tasti di scelta e suggerimenti per i tasti di scelta

I suggerimenti tasti sono il meccanismo usato per visualizzare i tasti di scelta per i comandi visualizzati direttamente su una barra multifunzione.

I tasti di scelta per i comandi del menu a discesa sono indicati con un carattere sottolineato. Differiscono dai tasti di scelta dei menu nei modi seguenti:

- È possibile usare due tasti di scelta dei caratteri. È ad esempio possibile usare FP per accedere al comando Copia formato.
- Le assegnazioni dei tasti di scelta vengono visualizzate usando suggerimenti anziché sottolineature, quindi la larghezza dei caratteri e i discendenti non sono un fattore importante per le assegnazioni.

- **Assegnare i tasti di scelta a tutte le schede e i comandi della barra multifunzione.** L'unica eccezione possibile è per i comandi provenienti da componenti aggiuntivi legacy.
- **Per il pulsante Applicazione e la barra di accesso rapido:**
  - Assegnare F al pulsante Applicazione. Questa assegnazione viene usata a causa della somiglianza del pulsante Applicazione con il menu File tradizionale.
  - ![Screenshot dei suggerimenti per i tasti di scelta rapida su una barra multifunzione ](images/cmd-ribbons-image54.png)<br/>Per la barra di accesso rapido e gli elenchi di file usati di recente, assegnare numericamente i tasti di scelta.
- ![Screenshot che mostra i suggerimenti tasto di scelta per le schede ](images/cmd-ribbons-image55.png)<br/>**Per le schede:**
  - Assegnare H a Home.
  - A partire dalle schede usate più di frequente, assegnare la prima lettera dell'etichetta.
  - Per le schede che non possono essere assegnate alla prima lettera, scegliere una consonante distintiva o una vocale nell'etichetta.
  - Per i programmi che supportano le barre dei menu, cercare di mantenere la compatibilità delle chiavi di accesso nella migliore delle modi pratiche. Evitare di assegnare significati diversi per accedere alle chiavi dalle categorie di menu legacy. Ad esempio, se la versione legacy della barra dei menu di un programma ha un menu Modifica, cercare di usare un tasto di scelta E per la scheda equivalente. Se non è presente alcuna scheda equivalente, non assegnare un tasto di scelta E ad alcuna scheda per evitare confusione.
- ![Screenshot che mostra i suggerimenti tasto di scelta per una barra multifunzione ](images/cmd-ribbons-image56.png)<br/>**Per i comandi, i menu e i sottomenu della barra multifunzione:**
  - Assegnare combinazioni di tasti di scelta univoche all'interno di una scheda. È possibile riutilizzare le combinazioni di tasti di scelta all'interno di schede diverse.
  - Quando possibile, assegnare le chiavi di accesso standard per i comandi di uso comune. Vedere la [tabella della chiave di accesso standard](inter-keyboard.md).
  - Per altri comandi:
    - Per i comandi usati più di frequente, scegliere le lettere all'inizio della prima o della seconda parola dell'etichetta, preferibilmente la prima lettera.
    - Per i comandi usati meno di frequente, scegliere lettere consonanti distintive o vocali nell'etichetta, ad esempio "x" in "Exit".
    - Per i comandi usati meno di frequente e le finestre di avvio delle finestre di dialogo, usare due lettere in base alle esigenze.
    - Per i menu e i sottomenu, usare una singola lettera per ridurre il numero di sequenze di tasti necessarie per il comando completo.
    - Non usare i tasti di scelta che iniziano con J, Y o Z perché vengono usati per schede contestuali, suggerimenti tasto di scelta rapida non assegnati e gruppi popup.
- ![Screenshot dei suggerimenti per i tasti di scelta rapida per i gruppi popup ](images/cmd-ribbons-image58.png)<br/>**Per i gruppi popup:**
  - Usare una chiave di accesso di due lettere che inizia con Z.
  - A partire dai gruppi usati più di frequente, assegnare la seconda lettera della chiave di accesso alla prima lettera dell'etichetta.
  - Per tutti i gruppi rimanenti, scegliere una consonante distintiva o una vocale nell'etichetta.

Per le linee guida per i tasti di [scelta rapida, vedere Tastiera](inter-keyboard.md).

### <a name="application-buttons"></a>Pulsanti dell'applicazione

- **Usare un pulsante Applicazione per presentare un menu di comandi che comportano l'esecuzione di un'operazione a o con un file.** Ad esempio, i comandi che tradizionalmente vengono usati nel menu File per creare, aprire e salvare file, stampare e inviare e pubblicare documenti.
- **Specificare sempre un pulsante Applicazione quando si usa una barra multifunzione.** Se il programma non usa file, usare il pulsante Applicazione per accedere alle opzioni del programma e al comando Esci. I pulsanti dell'applicazione visualizzano sempre un menu di comando che non sono mai solo decorativi.
- **Usare i comandi di menu dell'applicazione standard seguenti quando appropriato:**
  - Nuovo  
  - Apri  
  - Salva  
  - Salva con nome...
  - Stampa...
  - Stampa rapida  
  - Anteprima di stampa  
  - Chiudi  
  - Opzioni  
  - Esci  
  
- **Riservare i comandi che appartengono al menu Applicazione solo per tale menu.** Non posizionarli in modo ridondante in nessuna delle schede.
- Per ogni voce di menu specificare:
  - **Etichetta con il nome del comando.**
  - **Icona di 32x32 pixel.**
  - **Breve descrizione.** Assicurarsi che la descrizione possa essere visualizzata usando al massimo due righe di testo.
- ![Screenshot della descrizione comando che documenta il tasto di scelta rapida ](images/cmd-ribbons-image59.png)<br/>**Usare le descrizioni comando per documentare i tasti di scelta rapida.** A differenza dei normali menu, i menu dell'applicazione non documentano i tasti di scelta rapida usando le etichette.

### <a name="quick-access-toolbars"></a>Barre degli strumenti di accesso rapido

- **Usare la barra di accesso rapido per fornire l'accesso ai comandi usati di frequente.** I comandi possono essere dal pulsante Applicazione o dalla barra multifunzione.
- **Fornire sempre una barra di accesso rapido quando si usa una barra multifunzione.** Eseguire questa operazione anche se la barra multifunzione ha una singola scheda. ciò garantisce coerenza tra i programmi.
- **Prepopolare la barra di accesso rapido con i comandi usati di frequente nel menu Applicazione.** Specificare Salva e Annulla se il programma li supporta e Apri e stampa se supportato e usato di frequente.
- **Per il menu Personalizza barra di accesso rapido, specificare fino a 12 dei comandi immediati usati più di frequente.** I comandi immediati non richiedono un input aggiuntivo prima che siano effettive e sono quindi particolarmente adatti per la barra di accesso rapido. Anche se possono essere comandi immediati, è preferibile usare i comandi che non sono nella scheda Home, perché è più probabile che gli utenti lo scenzino.
- **Per il menu Personalizza barra di accesso rapido, se è presente una coppia di comandi correlati, specificare entrambi, indipendentemente dalla frequenza.** Le coppie comuni sono Open/Close, Back/Forward e Undo/Redo.
- **Per la finestra di dialogo Personalizza barra di accesso rapido, fornire un modo per aggiungere qualsiasi comando.** Specificare un filtro Comandi comuni che visualizza i comandi usati più di frequente e selezionare questo filtro per impostazione predefinita.

### <a name="dialog-box-launchers"></a>Finestre di avvio della finestra di dialogo

- ![Screenshot della finestra di dialogo carattere e del gruppo di tipi di carattere ](images/cmd-ribbons-image60.png)<br/>**Specificare un gruppo con un'icona di avvio della finestra di dialogo se è presente una finestra di dialogo correlata con comandi e impostazioni usati raramente.** La finestra di dialogo deve contenere tutti i comandi nel gruppo, oltre ad altri non un set completamente diverso di comandi o gli stessi comandi del gruppo.
- **Non usare un'utilità di avvio della finestra di dialogo per eseguire direttamente i comandi.** L'icona di avvio di una finestra di dialogo deve visualizzare una finestra di dialogo.
- **Non usare un'utilità di avvio della finestra di dialogo per accedere ai comandi e alle impostazioni usati di frequente.** Rispetto ai comandi direttamente sulla barra multifunzione, i comandi e le impostazioni della finestra di dialogo sono relativamente sconosciuti.
- **Trovare la corrispondenza tra il nome della finestra di dialogo e il nome del gruppo.** Non deve essere una corrispondenza esatta, ma i nomi devono essere sufficientemente simili in modo che gli utenti non siano sorprese dai risultati.

    **Non corretto:**

    ![Screenshot della finestra di dialogo del suono del promemoria ](images/cmd-ribbons-image61.png)

    Mentre un suono di promemoria è un'opzione di promemoria, l'uso dell'icona di avvio della finestra di dialogo per impostare il suono del promemoria è imprevisto.

- **Visualizzare solo i comandi e le impostazioni correlati al gruppo.** Se la finestra di dialogo visualizza altri elementi, gli utenti possono concludere che questo percorso per questi altri comandi e impostazioni è l'unico percorso.

    **Non corretto:**

    ![Screenshot della finestra di dialogo tipo di carattere ](images/cmd-ribbons-image62.png)

    In questo esempio, nella finestra di dialogo Carattere vengono visualizzate le impostazioni di Spaziatura caratteri, che non sono correlate alla scheda associata.

## <a name="labels&quot;></a>Etichette

### <a name=&quot;tab-labels&quot;></a>Etichette di tabulazione

- **Etichettare tutte le schede.**
- In caso di praticità, **usare le schede standard della barra multifunzione**.
- **Preferisce etichette concise con una sola parola.** Sebbene le etichette a più parole siano accettabili, prendono più spazio e sono più difficili da localizzare.
- **Scegliere nomi di schede significativi che descrivano in modo chiaro e accurato il contenuto.** I nomi devono essere specifici, ma non e troppo specifici. I nomi delle schede devono essere sufficientemente prevedibili in modo che gli utenti non siano sorprese dal contenuto. Si noti che la scheda Home è denominata in modo generico perché viene usata per i comandi usati più di frequente.
- **Non usare** nomi di gruppo, ad esempio &quot;Basic&quot; e &quot;Advanced&quot;. Richiedono agli utenti di determinare se il comando che stanno cercando è di base o avanzato.
- **Scegliere i nomi delle schede che riflettono lo scopo.** Prendere in considerazione gli obiettivi o le attività associati alla scheda.
- **Scegliere i nomi delle schede chiaramente distinti da tutti gli altri nomi di scheda.**
- **Usare sostantivi o verbi per le tabulazioni.** I nomi delle schede non richiedono formulazioni parallele, quindi scegliere l'etichetta migliore indipendentemente dal fatto che si tratta di un sostantivo o di un verbo.
- **Non usare gerund (nomi** che terminano con &quot;-ing"). Usare invece il verbo da cui deriva il gerund. Ad esempio, usare "Draw" anziché "Drawing".
- **Evitare i nomi delle schede con le stesse lettere iniziali, in particolare le schede adiacenti.** Quando la barra multifunzione viene ridotta, questi nomi di scheda avranno lo stesso testo troncato.
- **Preferisce i nomi singolari.** Tuttavia, è possibile usare un nome purale se il nome singolare è difficile.
- **Usare l'uso di maiuscole e minuscole in stile titolo.**
- **Non usare punteggiatura finale.**

### <a name="contextual-tab-and-tab-set-labels"></a>Etichette di schede e set di schede contestuali

- **Terminare le etichette dei set di schede contestuali con "Strumenti".** In questo modo è possibile identificare lo scopo delle schede contestuali.
- Usare l'uso di maiuscole e minuscole in stile titolo.
- Non usare punteggiatura finale.

### <a name="group-labels"></a>Raggruppare le etichette

- **Assegnare un'etichetta** a tutti i gruppi, a meno che il gruppo non abbia un singolo comando e le etichette di gruppo e comando non siano uguali.

- **Usare i gruppi della barra multifunzione standardquando possibile.**
- **Preferisce etichette concise a parola singola.** Anche se le etichette con più parole sono accettabili, hanno più spazio e sono più difficili da localizzare.
- **Scegliere nomi di gruppo significativi che descrivano in modo chiaro e accurato il contenuto.** I nomi devono essere specifici, non generici.
- **Scegliere nomi di gruppo che riflettano lo scopo.** Prendere in considerazione gli obiettivi o le attività associati ai comandi nel gruppo.
- **Evitare di usare gerund** (nomi che terminano con "-ing"). È possibile usare i gerund, tuttavia, se si usa il verbo da cui deriva il gerund si crea confusione. Ad esempio, usare "Modifica" e "Prova" anziché "Modifica" e "Prova".
- **Non usare nomi di gruppo uguali ai nomi delle schede.** L'uso del nome della scheda in cui si trova il gruppo non fornisce informazioni e l'uso del nome di una scheda diversa crea confusione.
- **Preferisce nomi singolari.** Tuttavia, è possibile usare un nome purale se il nome singolare è difficile. 
- **Usare le maiuscole/minuscole come nelle frasi comuni.**
- **Non usare punteggiatura finale.**

### <a name="command-labels"></a>Etichette dei comandi

- **Assegnare un'etichetta a tutti i comandi.** La presenza di etichette di testo esplicite consente agli utenti di trovare e comprendere i comandi. **Eccezione:** Un comando può essere senza etichetta se la relativa icona è estremamente nota e lo spazio è premium. È molto probabile che i comandi senza etichetta siano disponibili nella scheda Home. In questo caso, assegnare la proprietà Name a un'etichetta di testo appropriata. In questo modo assistive technology prodotti quali le utilità per la lettura dello schermo per fornire agli utenti informazioni alternative sull'immagine.
- **Per i pulsanti di comando, usare un'etichetta concisa e auto-esplicativa.** Se possibile, usare una singola parola. al massimo quattro parole.
- **Per gli elenchi a discesa, se l'elenco ha sempre un valore, usare il valore corrente come etichetta.**
- ![Screenshot del prompt delle rubriche di ricerca ](images/cmd-ribbons-image67.png)<br/>Se un [elenco a discesa modificabile](/windows/desktop/uxguide/ctrl-drop) non ha un valore, usare un [prompt](glossary.md).
- **Gli elenchi a discesa che non sono auto-esplicativi o non vengono usati raramente necessitano di un'etichetta esplicita.** Inserire i due punti alla fine dell'etichetta.
- ![Screenshot di automaticamente dopo: secondi<br.>Per le caselle \[ di \] ](images/cmd-ribbons-image69.png) **testo, usare un'etichetta esplicita.** Inserire i due punti alla fine dell'etichetta.
- **Usare le maiuscole/minuscole come nelle frasi comuni.** Questa operazione è più appropriata per il tono [Windows.](text-style-tone.md)
- **Avviare l'etichetta con un verbo imperativo.** a meno che non sia uguale al nome della scheda o del gruppo o a un verbo comune come Show, Create, Insert o Format.
- **Non usare punteggiatura finale.**
- **Per risparmiare spazio, non inserire puntini di sospensione nelle etichette dei comandi della barra multifunzione.** I puntini di sospensione vengono tuttavia usati dai comandi nei menu a discesa e nel pulsante Applicazione.

### <a name="enhanced-tooltip-labels"></a>Etichette della descrizione comando migliorate

- **Usare il titolo per assegnare il nome del comando e il relativo tasto di scelta rapida, se applicabile.**
- **Per il titolo, non usare la punteggiatura finale.**
- **Iniziare la descrizione con un verbo.** Usare la descrizione per consentire agli utenti di determinare se una funzionalità specifica è quella cercata. La descrizione deve essere formulata per completare la frase "This is the right feature to use if you want to...".
- **Mantenere breve la descrizione.** Andare direttamente al punto. Il testo lungo sconsiglia la lettura.
-   ![Screenshot del pulsante di menu di menu incollato e di due descrizioni comando ](images/cmd-ribbons-image70.png)<br/>**Per i pulsanti di divisione, usare una descrizione comando diversa per spiegare il menu del pulsante di menu suddiviso.**
- **Usare una descrizione supplementare facoltativa per spiegare come usare il controllo .** Questo testo può includere informazioni sullo stato del controllo (incluso il motivo per cui è disabilitato) se il controllo stesso non indica lo stato. Tenere breve questo testo e usare un argomento della Guida per spiegazioni più dettagliate.
- ![Screenshot della descrizione comando con grafica e testo Per la descrizione e la descrizione supplementare, usare frasi complete ](images/cmd-ribbons-image71.png)**con punteggiatura finale.**
- Usare le maiuscole/minuscole come nelle frasi comuni.

### <a name="application-button-labels"></a>Etichette dei pulsanti dell'applicazione

- [Screenshot dell'opzione di stampa rapida selezionata ](images/cmd-ribbons-image72.png)<br/>**Usare "Quick" per indicare una versione immediata di un comando.**

- **Usare i puntini di sospensione per indicare che un comando richiede altre informazioni.**
- **Usare le maiuscole/minuscole come nelle frasi comuni.**

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle barre multifunzione:

- Fare riferimento alla barra multifunzione e ai relativi componenti come barra multifunzione, schede, gruppi e controlli. Questi termini non sono in maiuscolo.
- Fare riferimento al pulsante rotondo come pulsante Applicazione e al menu che contiene come menu Applicazione.
- Fare riferimento alla barra degli strumenti come barra di accesso rapido.
- Fare riferimento alle schede in base alle etichette e alla scheda delle parole. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola.
- Fare riferimento ai comandi in base alle etichette. Fare riferimento ai comandi senza etichetta in base ai relativi nomi di descrizione comando. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere i puntini di sospensione. Non includere la parola button o command.
- Per descrivere l'interazione dell'utente, usare il clic per schede e controlli. Usare INVIO per gli elenchi a discesa modificabili. Non usare scegliere, selezionare o selezionare.
- Fare riferimento agli elementi non disponibili come non disponibili, non come disattivati, disabilitati o in grigio. Nella documentazione di programmazione usare disabled.
- Quando possibile, formattare le etichette usando il testo in grassetto. In caso contrario, inserire le etichette tra virgolette solo se necessario per evitare confusione.

Esempi:

- Nella scheda **Home** fare clic su **Incolla speciale.**
- Nella casella Carattere della  scheda **Home** immettere "Segoe UI".
- Nella scheda **Revisione** fare clic su **Mostra markup** e quindi su **Revisori**.
- Nella scheda **Formato ,** in Strumenti **immagine**, fare clic su **Comprimi immagini**.