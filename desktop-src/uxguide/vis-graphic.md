---
title: Elementi grafici
description: Gli elementi grafici mostrano visivamente le relazioni, la gerarchia e l'enfasi. Includono sfondi, banner, vetri, aggregatori, separatori, ombreggiature e punti di controllo.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 03db1f7a90554848f71cd43cdfa769597b71cd2f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444632"
---
# <a name="graphic-elements"></a>Elementi grafici

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

*Gli elementi grafici* mostrano visivamente le relazioni, la gerarchia e l'enfasi. Includono sfondi, banner, vetri, aggregatori, separatori, ombreggiature e punti di controllo.

![screenshot di Esplora risorse con ombreggiatura e così via. ](images/vis-graphic-image1.png)

Esempio con diversi tipi di elementi grafici.

Gli elementi grafici non sono in genere interattivi. Tuttavia, i separatori sono interattivi per il contenuto ridimensionabile e gli handle sono elementi grafici che mostrano interattività.

**Nota:** Le linee guida [relative a caselle di](ctrl-group-boxes.md) [gruppo, animazioni,](vis-animations.md) [icone](vis-icons.md)e [personalizzazione](exper-branding.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Anche se gli elementi grafici sono un mezzo visivo forte per indicare le relazioni, il loro uso in e sovrautilizzo aggiunge confusione visiva e riduce lo spazio disponibile su una superficie. Devono essere usati con moderamento.

Una tendenza di progettazione in Microsoft Windows è un aspetto più semplice e pulito eliminando linee e grafica non necessarie.

Per decidere se è necessario un elemento grafico, considerare queste domande:

-   **La presentazione e la comunicazione del progetto sono così chiare ed efficaci senza l'elemento ?** In tal caso, rimuoverlo.
-   **È possibile comunicare in modo efficace le relazioni usando solo il layout?** In tal caso, usare [invece il layout](vis-layout.md) . È possibile posizionare i controlli correlati uno accanto all'altro e inserire ulteriore spaziatura tra i controlli non correlati. È anche possibile usare il rientro per visualizzare le relazioni gerarchiche.

![Screenshot di un layout a quattro icone ](images/vis-graphic-image2.png)

In questo esempio viene usato solo il layout per mostrare le relazioni tra i controlli.

-   **La comunicazione è efficace senza testo?** In caso contrario, usare una [casella di gruppo,](ctrl-group-boxes.md)un separatore con etichetta o un'altra [etichetta](text-ui.md).

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli elementi grafici hanno diversi modelli di utilizzo:



| Elemento                                                                                                              |   Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Illustrazioni grafiche**<br/> usare per comunicare visivamente un'idea. <br/>                         | Le illustrazioni grafiche sono simili alle icone, ad eccezione del fatto che possono avere qualsiasi dimensione e in genere non sono interattive. <br/> ![screenshot del grafico della cronologia di utilizzo della CPU ](images/vis-graphic-image3.png)<br/> In questo esempio viene usata un'illustrazione grafica per suggerire la natura di una funzionalità.<br/>                                                                                                                                                                                                        |
| **Sfondi**<br/> usare per evidenziare o de-evidenziare diversi tipi di contenuto. <br/>           | Gli sfondi possono essere usati per evidenziare contenuto importante. <br/> ![Screenshot del messaggio di virus sullo sfondo rosso ](images/vis-graphic-image4.png)<br/> In questo esempio viene usato uno sfondo per evidenziare un'attività importante.<br/> Gli sfondi possono essere usati anche per de-evidenziare il contenuto secondario. <br/> ![Screenshot degli elementi del Pannello di controllo ](images/vis-graphic-image5.png)<br/> In questo esempio le attività secondarie vengono de-evidenziate individuandole in un riquadro attività.<br/>   |
| **Banner**<br/> utilizzato per indicare lo stato importante. <br/>                                         | A differenza degli sfondi, i banner evidenziano principalmente una singola stringa di testo. <br/> ![Screenshot del banner con informazioni sulle impostazioni ](images/vis-graphic-image6.png)<br/> In questo esempio viene usato un banner per indicare che le impostazioni della pagina sono controllate da Criteri di gruppo.<br/>                                                                                                                                                                                                       |
| **Vetro**<br/> usare in modo strategico per ridurre il peso visivo di una finestra. <br/>                   | Glass può ridurre il peso di una superficie concentrandosi sul contenuto anziché sulla finestra stessa. <br/> ![screenshot di un volatile nella raccolta foto di Windows ](images/vis-graphic-image7.png)<br/> In questo esempio, glass concentra l'attenzione dell'utente sul contenuto anziché sui controlli .<br/>                                                                                                                                                                                                 |
| **Aggregatori**<br/> Usare per creare una relazione visiva tra controlli fortemente correlati. <br/> | ![Screenshot delle frecce di spostamento avanti e indietro ](images/vis-graphic-image8.png)<br/> In questo esempio viene usato uno sfondo dell'aggregatore per evidenziare la relazione tra i pulsanti Indietro e Avanti in Explorer.<br/> ![Screenshot dei controlli raccolta foto di Windows ](images/vis-graphic-image7.png)<br/> In questo esempio viene usato un aggregatore di limiti per evidenziare la relazione tra i controlli e renderli come un singolo controllo anziché otto.<br/> |
| **Separatori**<br/> Usare per separare i controlli correlati in modo debole o non correlati. <br/>                   | I separatori possono essere interattivi o non interattivi. I separatori interattivi tra contenuto ridimensionabile sono noti come separatori. <br/> ![Screenshot del separatore della barra di divisione per il pulsante Nome ](images/vis-graphic-image9.png)<br/> In questo esempio viene usato un separatore interattivo per il contenuto ridimensionabile.<br/> ![Screenshot del separatore per le informazioni sul browser ](images/vis-graphic-image10.png)<br/> In questo esempio il separatore non è interattivo.<br/>                  |
| **Ombreggiature**<br/> usare per fare in modo che il contenuto si disalva visivamente sullo sfondo. <br/>             | ![screenshot di quattro foto con ombreggiature ](images/vis-graphic-image11.png)<br/> In questo esempio, le ombreggiature fanno in modo che le illustrazioni si distinguono sullo sfondo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Selettori**<br/> Usare per indicare che un oggetto può essere spostato o ridimensionato. <br/>                    | Gli handle sono sempre interattivi e il relativo comportamento è suggerito dal puntatore del mouse al passaggio del mouse. <br/> ![Screenshot dell'angolo di una finestra con il puntatore di ridimensionamento ](images/vis-graphic-image12.png)<br/> ![Screenshot della casella di selezione con il puntatore di ridimensionamento ](images/vis-graphic-image13.png)<br/> In questi esempi, gli handle indicano che un oggetto può essere ridimensionato.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non trasmettere informazioni essenziali solo tramite elementi grafici.** Questa operazione presenta problemi di accessibilità per gli utenti con disabilità visive o problemi.

### <a name="graphic-designs"></a>Progettazioni grafiche

-   **La grafica è la più efficace quando consolida una singola idea semplice.** La grafica complessa che richiede un'interpretazione di tipo "thought" non funziona correttamente. I hieroglifi sono la scelta migliore per i disegni in una grotta.

    **Non corretto:**

    ![Schermata di avviso con immagine complessa ](images/vis-graphic-image14.png)

    In questo esempio, un grafico complesso di Windows XP tenta inefficacemente di spiegare una decisione di attendibilità complessa.

-   **Non usare frecce, frecce di controllo, riquadri dei pulsanti o altri affordance associati ai controlli interattivi.** In questo modo si invitano gli utenti a interagire con la grafica.
-   **Evitare swath di rosso puro, giallo e verde nei progetti.** Per evitare confusione, riservare questi colori per comunicare lo stato. Se è necessario usare questi colori per un valore diverso da status, usare toni disattivati anziché colori puri.
-   **Usare progettazioni indipendenti dalla cultura.** Ciò che può avere un determinato significato in un paese, un'area o una cultura potrebbe non avere lo stesso significato in un altro.
-   **Evitare di usare persone, visi, sesso o parti del corpo, nonché simboli di forza, politiche e nazionali.** Tali immagini potrebbero non essere facilmente tradotte o essere offensive.
-   **Quando è necessario rappresentare persone o utenti, rappresentarle in modo generico;** evitare rappresentazioni realistiche.

### <a name="backgrounds-and-banners"></a>Sfondi e banner

-   **Per evidenziare il contenuto, usare testo scuro su uno sfondo chiaro.** Il testo nero su sfondo grigio chiaro o giallo funziona correttamente.

    ![Screenshot del testo del collegamento blu sullo sfondo giallo ](images/vis-graphic-image15.png)

    In questo esempio, il collegamento riceve l'attenzione dell'utente perché si trova su uno sfondo giallo.

-   **Per de-evidenziare il contenuto, usare testo chiaro su uno sfondo scuro.** Il testo bianco su sfondo grigio scuro o blu funziona correttamente.

    ![Screenshot del collegamento alla Guida bianco su sfondo verde ](images/vis-graphic-image16.png)

    In questo esempio, lo sfondo scuro de-evidenzia il contenuto.

-   **Se si usa una sfumatura, assicurarsi che il colore del testo abbia un buon contrasto nell'intera sfumatura.**
-   **Usare sempre un'icona di 16x16 pixel per attirare l'attenzione sul banner.** I banner sono troppo facili da tralasciare in caso contrario. Per altre linee guida ed esempi, vedere [Icone standard.](vis-std-icons.md)
-   **Usare sfondi e banner con cautela.** Anche se lo scopo dello sfondo o del banner può essere quello di evidenziare il contenuto, spesso i risultati sono l'opposto di un fenomeno noto come "cecità banner".

### <a name="glass"></a>Vetro

-   **È consigliabile usare il cristallo in modo strategico in piccole aree toccando la cornice della finestra senza testo.** In questo modo, un programma può avere un aspetto più semplice, più leggero e più coeso facendo in modo che l'area appaia come parte del frame.
-   **Non usare glass nelle situazioni in cui uno sfondo di finestra normale sarebbe più interessante o più facile da usare.**

### <a name="separators"></a>Separatori

-   **Usare linee verticali e orizzontali per i separatori.** Assicurarsi di disporre di spazio sufficiente tra i separatori e il contenuto da separare.
-   Per i separatori tra contenuto ridimensionabile (separatori), visualizzare il puntatore di ridimensionamento al passaggio del mouse.

![Screenshot che mostra una barra di divisione con puntatore di ridimensionamento.](images/vis-graphic-image17.png)

![Screenshot della barra di divisione con puntatore di ridimensionamento ](images/vis-graphic-image18.png)

In questi esempi i puntatori di ridimensionamento vengono visualizzati al passaggio del mouse.

### <a name="shadows"></a>Ombreggiature

-   **Usare solo per fare in modo che il contenuto o gli oggetti più significativi del programma trascinati si distinguono visivamente sullo sfondo.** Considerare le ombreggiature come confusione visiva in altre circostanze.

### <a name="high-dpi-support"></a>Supporto dpi elevato

-   **Supporto delle modalità video 96 e 120 punti per pollice (dpi).** Rilevare la modalità dpi all'avvio e gestire gli eventi di modifica dpi. Windows è ottimizzato per 96 e 120 dpi e usa 96 dpi per impostazione predefinita.
-   **Preferisce fornire bitmap separate di cui viene eseguito il rendering in modo specifico per 96 e 120 dpi rispetto al ridimensionamento della grafica.** Fornire almeno 96 e 120 dpi per le bitmap più importanti e visibili e per centrare o ridimensionare le altre. Tali applicazioni sono considerate "con valori dpi elevati" e offrono un'esperienza visiva complessiva migliore rispetto ai programmi che vengono ridimensionati automaticamente da Windows.
    -   Sviluppatori: è possibile dichiarare un programma con riconoscimento dpi elevato (e impedire il ridimensionamento automatico) impostando il flag con riconoscimento dpi nel manifesto del programma oppure chiamando l'API SetProcessDPIAware() durante l'inizializzazione del programma. È possibile usare le macro per semplificare la selezione della grafica giusta. Per le bitmap Win32, è possibile usare SS CENTERIMAGE per centrare o \_ SS \_ REALSIZECONTROL per ridimensionare.
-   Controllare il programma in 96 e 120 dpi per:
    -   Grafica troppo piccola o troppo grande.
    -   Grafica ritagliata, sovrapposta o in altro modo non adattata correttamente.
    -   Grafica poco estesa ("pixilated").
    -   Testo ritagliato o non adattato a sfondi grafici.

## <a name="text"></a>Testo

-   **Per l'accessibilità e la localizzazione, non usare testo nella grafica.** Creare eccezioni solo per rappresentare [la personalizzazione e](exper-branding.md) il testo come concetto astratto.

 

