---
title: Elementi grafici
description: Gli elementi grafici mostrano visivamente relazioni, gerarchie e enfasi. Sono inclusi gli sfondi, i banner, i bicchieri, gli aggregatori, i separatori, le ombreggiature e gli handle.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a452668bc1685143273df80fd144642a18019213
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968823"
---
# <a name="graphic-elements"></a>Elementi grafici

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

*Gli elementi grafici* mostrano visivamente relazioni, gerarchie e enfasi. Sono inclusi gli sfondi, i banner, i bicchieri, gli aggregatori, i separatori, le ombreggiature e gli handle.

![Screenshot di Esplora risorse con ombreggiatura e così via. ](images/vis-graphic-image1.png)

Esempio con diversi tipi di elementi grafici.

Gli elementi grafici in genere non sono interattivi. Tuttavia, i separatori sono interattivi per contenuti ridimensionabili e gli handle sono elementi grafici che mostrano interattività.

**Nota:** Le linee guida correlate a [caselle di gruppo](ctrl-group-boxes.md), [animazioni](vis-animations.md), [Icone](vis-icons.md)e [personalizzazione](exper-branding.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Sebbene gli elementi grafici siano un metodo visivo sicuro per indicare le relazioni, il loro utilizzo aggiunge confusione visiva e riduce lo spazio disponibile su una superficie. Devono essere usati sporadicamente.

Una tendenza di progettazione in Microsoft Windows è un aspetto più semplice e pulito eliminando grafica e linee non necessarie.

Per decidere se un elemento grafico è necessario, prendere in considerazione le domande seguenti:

-   **La presentazione e la comunicazione della progettazione sono altrettanto chiare ed efficaci senza l'elemento?** In tal caso, rimuoverlo.
-   **È possibile comunicare efficacemente le relazioni usando solo il layout?** In caso affermativo, usare invece il [layout](vis-layout.md) . È possibile posizionare i controlli correlati uno accanto all'altro e inserire spazi aggiuntivi tra i controlli non correlati. È anche possibile usare il rientro per visualizzare le relazioni gerarchiche.

![Screenshot di un layout con quattro icone ](images/vis-graphic-image2.png)

In questo esempio, viene usato solo il layout per visualizzare le relazioni di controllo.

-   **La comunicazione è efficace senza testo?** In caso contrario, utilizzare una [casella di gruppo](ctrl-group-boxes.md), un separatore con etichetta o un'altra [etichetta](text-ui.md).

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli elementi grafici includono diversi modelli di utilizzo:



|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Illustrazioni grafiche**<br/> usare per comunicare visivamente un'idea. <br/>                         | Le illustrazioni grafiche sono simili alle icone, ad eccezione del fatto che possono essere di qualsiasi dimensione e in genere non interattive. <br/> ![grafico della Cronologia utilizzo CPU screenshot ](images/vis-graphic-image3.png)<br/> In questo esempio viene usata un'illustrazione grafica per suggerire la natura di una funzionalità.<br/>                                                                                                                                                                                                        |
| **Sfondi**<br/> usare per enfatizzare o deaccentuare tipi diversi di contenuto. <br/>           | Gli sfondi possono essere usati per evidenziare contenuto importante. <br/> ![screenshot del messaggio del virus sullo sfondo rosso ](images/vis-graphic-image4.png)<br/> in questo esempio viene usato uno sfondo per evidenziare un'attività importante.<br/> gli sfondi possono anche essere usati per deaccentuare il contenuto secondario. <br/> ![screenshot degli elementi del pannello di controllo ](images/vis-graphic-image5.png)<br/> In questo esempio, le attività secondarie sono deaccentuate individuando le attività in un riquadro attività.<br/>   |
| **Banner**<br/> utilizzato per indicare lo stato importante. <br/>                                         | A differenza degli sfondi, i banner enfatizzano principalmente una singola stringa di testo. <br/> ![screenshot del banner con le informazioni sulle impostazioni ](images/vis-graphic-image6.png)<br/> In questo esempio viene usato un banner per indicare che le impostazioni della pagina sono controllate da Criteri di gruppo.<br/>                                                                                                                                                                                                       |
| **Vetro**<br/> usare in modo strategico per ridurre il peso visivo di una finestra. <br/>                   | Glass può ridurre il peso di una superficie concentrandosi sul contenuto invece che sulla finestra stessa. <br/> ![Screenshot di Bird nella raccolta foto di Windows ](images/vis-graphic-image7.png)<br/> In questo esempio, Glass concentra l'attenzione dell'utente sul contenuto anziché sui controlli.<br/>                                                                                                                                                                                                 |
| **Aggregatori**<br/> utilizzare per creare una relazione visiva tra i controlli fortemente correlati. <br/> | ![screenshot delle frecce di navigazione indietro e in secondo piano ](images/vis-graphic-image8.png)<br/> in questo esempio viene usato uno sfondo di aggregator per evidenziare la relazione tra i pulsanti indietro e indietro in Esplora.<br/> ![screenshot dei controlli della raccolta foto di Windows ](images/vis-graphic-image7.png)<br/> In questo esempio viene usato un aggregatore di limiti per evidenziare la relazione tra i controlli e fare in modo che sembri un singolo controllo anziché otto.<br/> |
| **Separatori**<br/> usare per separare i controlli correlati o non correlati. <br/>                   | I separatori possono essere interattivi o non interattivi. i separatori interattivi tra contenuti ridimensionabili sono noti come divisori. <br/> ![screenshot del separatore della barra di divisione per il pulsante nome ](images/vis-graphic-image9.png)<br/> in questo esempio viene usato un separatore interattivo per il contenuto ridimensionabile.<br/> ![screenshot del separatore per le informazioni del browser ](images/vis-graphic-image10.png)<br/> In questo esempio il separatore non è interattivo.<br/>                  |
| **Ombreggiature**<br/> usare questa proprietà per far emergere il contenuto in modo visivo rispetto al relativo sfondo. <br/>             | ![Screenshot di quattro foto con ombre ](images/vis-graphic-image11.png)<br/> In questo esempio le ombre fanno emergere l'artwork rispetto allo sfondo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Selettori**<br/> usare per indicare che un oggetto può essere spostato o ridimensionato. <br/>                    | Gli handle sono sempre interattivi e il relativo comportamento viene suggerito dal puntatore del mouse al passaggio del mouse. <br/> ![Screenshot di un angolo della finestra con puntatore di ridimensionamento ](images/vis-graphic-image12.png)<br/> ![screenshot della casella di selezione con puntatore di ridimensionamento ](images/vis-graphic-image13.png)<br/> In questi esempi, gli handle indicano che un oggetto può essere ridimensionato.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non fornire informazioni essenziali solo tramite elementi grafici.** In questo modo si presentano problemi di accessibilità per gli utenti con disabilità visive o difficoltà.

### <a name="graphic-designs"></a>Progettazioni grafiche

-   **I grafici sono più efficaci quando rinforzano una singola idea semplice.** I grafici complessi che richiedono l'interpretazione del pensiero non funzionano correttamente. I geroglifici sono ideali per i disegni delle Cave.

    **Non corretto:**

    ![cattura di schermata dell'avviso utilizzando un elemento grafico complesso ](images/vis-graphic-image14.png)

    In questo esempio, un grafico complesso di Windows XP tenta in modo inefficace di spiegare una decisione di attendibilità complessa.

-   **Non usare frecce, virgolette, frame di pulsanti o altri affordances associati a controlli interattivi.** In questo modo gli utenti possono interagire con la grafica.
-   **Evitare le fasce di colore rosso, giallo e verde puri nei progetti.** Per evitare confusione, riservare questi colori per comunicare lo stato. Se è necessario usare questi colori per un valore diverso da status, usare i toni silenziati anziché i colori puri.
-   **Usare progettazioni indipendenti dalle impostazioni cultura.** Ciò che può avere un determinato significato in un paese, in un'area geografica o in una cultura potrebbe non avere lo stesso significato in un altro.
-   **Evitare di usare persone, visi, sesso o parti del corpo, oltre a simboli religiosi, politici e nazionali.** Tali immagini potrebbero non essere facilmente convertite o potrebbero essere offensive.
-   **Quando è necessario rappresentare persone o utenti, rappresentarli in modo generico;** evitare rappresentazioni realistiche.

### <a name="backgrounds-and-banners"></a>Sfondi e banner

-   **Per enfatizzare il contenuto, usare il testo scuro su uno sfondo chiaro.** Il testo nero su uno sfondo grigio chiaro o giallo funziona correttamente.

    ![screenshot del testo del collegamento blu sullo sfondo giallo ](images/vis-graphic-image15.png)

    In questo esempio il collegamento ottiene l'attenzione dell'utente perché si trova in uno sfondo giallo.

-   **Per deaccentuare il contenuto, usare il testo chiaro sullo sfondo scuro.** Il testo bianco su uno sfondo grigio scuro o blu funziona correttamente.

    ![screenshot del collegamento alla guida bianca sullo sfondo verde ](images/vis-graphic-image16.png)

    In questo esempio, lo sfondo scuro de-enfatizza il contenuto.

-   **Se viene utilizzata una sfumatura, verificare che il colore del testo abbia un contrasto positivo nell'intera sfumatura.**
-   **Usare sempre un'icona di pixel 16x16 per attirare l'attenzione sul banner.** I banner sono troppo semplici da ignorare in altro modo. Per altre linee guida ed esempi, vedere [icone standard](vis-std-icons.md).
-   **Usare gli sfondi e i banner con cautela.** Sebbene lo scopo dello sfondo o del banner possa essere quello di evidenziare il contenuto, molto spesso i risultati sono l'opposto di un fenomeno noto come "cecità del banner".

### <a name="glass"></a>Vetro

-   **Si consiglia di usare il vetro in modo strategico in aree di piccole dimensioni toccando la cornice della finestra senza testo.** Questa operazione può offrire a un programma un aspetto più semplice, più chiaro e più coeso, facendo in modo che l'area appaia come parte del frame.
-   **Non usare il vetro in situazioni in cui uno sfondo normale della finestra sarebbe più interessante o più semplice da usare.**

### <a name="separators"></a>Separatori

-   **Utilizzare linee verticali e orizzontali per i separatori.** Assicurarsi di disporre di spazio sufficiente tra i separatori e il contenuto separato.
-   Per i separatori tra contenuto ridimensionabile (splitter), visualizzare il puntatore di ridimensionamento al passaggio del mouse.

![Screenshot che mostra una barra di divisione con puntatore di ridimensionamento.](images/vis-graphic-image17.png)

![screenshot della barra di divisione con puntatore di ridimensionamento ](images/vis-graphic-image18.png)

In questi esempi, i puntatori di ridimensionamento vengono visualizzati al passaggio del mouse.

### <a name="shadows"></a>Ombreggiature

-   **Usare solo per rendere il contenuto o gli oggetti più significativi del programma trascinati in modo visivo rispetto al relativo sfondo.** Prendere in considerazione le ombreggiature per un disordine visivo in altre circostanze.

### <a name="high-dpi-support"></a>Supporto di valori DPI alti

-   **Supporta le modalità video dpi (punti per pollice) 96 e 120.** Rilevare la modalità dpi all'avvio e gestire gli eventi di modifica dpi. Windows è ottimizzato per 96 e 120 dpi e utilizza 96 dpi per impostazione predefinita.
-   **Preferisci fornire bitmap separate di cui è stato eseguito il rendering in modo specifico per 96 e 120 DPI rispetto alla scala grafica.** Almeno fornire le versioni 96 e 120 dpi per le bitmap più importanti e visibili e centrare o ridimensionare gli altri. Tali applicazioni sono considerate "High-DPI Aware" e offrono un'esperienza visiva complessiva migliore rispetto ai programmi che vengono ridimensionati automaticamente da Windows.
    -   Sviluppatori: è possibile dichiarare un programma con valori DPI elevati (e impedire il ridimensionamento automatico) impostando il flag DPI Aware nel manifesto del programma o chiamando l'API SetProcessDPIAware () durante l'inizializzazione del programma. È possibile utilizzare le macro per semplificare la selezione della grafica corretta. Per le bitmap Win32, è possibile usare SS \_ CENTERIMAGE per centrare o SS \_ REALSIZECONTROL per la scalabilità.
-   Verificare il programma in 96 e 120 dpi per:
    -   Grafica troppo piccola o troppo grande.
    -   I grafici vengono ritagliati, sovrapposti o non vengono adattati in modo corretto.
    -   Grafica non allungata ("scatti").
    -   Testo ritagliato o non adattabile in background grafici.

## <a name="text"></a>Testo

-   **Per l'accessibilità e la localizzazione, non usare testo nella grafica.** Creare eccezioni solo per rappresentare la [personalizzazione](exper-branding.md) e il testo come concetto astratto.

 

