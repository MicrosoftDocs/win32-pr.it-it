---
title: Controlli di divulgazione progressiva
description: Con un controllo di divulgazione progressivo, gli utenti possono visualizzare o nascondere informazioni aggiuntive, tra cui dati, opzioni o comandi.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22c74f60b3184f7fa7f7cdb2b4f2e9d9f64995ea
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351106"
---
# <a name="progressive-disclosure-controls"></a>Controlli di divulgazione progressiva

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un controllo di divulgazione progressivo, gli utenti possono visualizzare o nascondere informazioni aggiuntive, tra cui dati, opzioni o comandi. La divulgazione progressiva promuove la semplicità concentrandosi sull'essenziale, ma rivelando ulteriori dettagli in base alle esigenze.

![screenshot dei controlli di divulgazione progressiva](images/progressive-disclosure-controls-image1.png)

Esempi di controlli di divulgazione progressiva.

> [!Note]  
> Le linee guida relative a [layout](vis-layout.md), [menu](cmd-menus.md)e [barre degli strumenti](cmd-toolbars.md) sono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Gli utenti devono visualizzare le informazioni in alcuni scenari, ma non in tutti gli scenari, ma non in tutti i casi?** In tal caso, la visualizzazione delle informazioni mediante la divulgazione progressiva semplifica l'esperienza di base, ma consente agli utenti di accedere facilmente alle informazioni.

    ![Screenshot che mostra la visualizzazione dello stato del Centro sicurezza.](images/progressive-disclosure-controls-image2.png)

    In questo esempio, il Centro sicurezza Visualizza continuamente lo stato di sicurezza importante, ma usa la divulgazione progressiva per visualizzare i dettagli su richiesta.

-   **Se le informazioni vengono visualizzate per impostazione predefinita, è probabile che gli utenti scelgano di nasconderlo?** Esistono scenari in cui gli utenti dovranno avere più spazio? Gli utenti sono sufficientemente motivati a personalizzare l'interfaccia utente? In caso contrario, visualizzare le informazioni senza utilizzare la divulgazione progressiva.

    **Non corretto:**

    ![screenshot delle opzioni dei dati visualizzate per impostazione predefinita ](images/progressive-disclosure-controls-image3.png)

    In questo esempio gli utenti non saranno motivati a nascondere le informazioni.

-   **Le informazioni aggiuntive sono avanzate, sostanziali, complesse o correlate a una sottoattività indipendente?** In tal caso, è consigliabile visualizzare le informazioni in una finestra separata utilizzando i [pulsanti di comando](ctrl-command-buttons.md) o i [collegamenti](ctrl-command-links.md) anziché utilizzare un controllo di divulgazione progressivo. (Le informazioni aggiuntive sono avanzate se sono destinate agli utenti avanzati. È complesso se rende più difficile la lettura o la disposizione di altre informazioni.

    ![Screenshot di eseguire questo file? ](images/progressive-disclosure-controls-image4.png)

    In questo esempio, le informazioni sul nome e sul server di pubblicazione del software sono significative principalmente per gli utenti avanzati, quindi vengono utilizzati collegamenti a finestre separate.

-   **Le informazioni aggiuntive sono un frammento di frase o di frase che descrive cosa fa un elemento o come può essere usato?** In tal caso, prendere in considerazione l'uso di una [Descrizione comando](ctrl-tooltips-and-infotips.md) o infotip.
-   **Informazioni aggiuntive correlate all'attività corrente, ma indipendenti dalle informazioni attualmente visualizzate?** In tal caso, prendere in considerazione l'uso delle [schede](ctrl-tabs.md) . Tuttavia, gli elenchi comprimibili sono spesso preferibili alle schede perché sono più flessibili e scalabili.
-   **Vengono mostrate o nascoste informazioni aggiuntive essenzialmente un filtro dati?** In tal caso, prendere in considerazione l'uso di un [elenco a discesa](/windows/desktop/uxguide/ctrl-drop) o di [caselle di controllo](ctrl-check-boxes.md) per applicare il filtro all'intero elenco.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gli obiettivi della divulgazione progressiva sono:

-   **Semplifica un'interfaccia utente** concentrandosi sull'essenziale, ma rivelando ulteriori dettagli in base alle esigenze.
-   **Semplifica l'aspetto di un'interfaccia utente** riducendo la percezione del disordine.

Entrambi gli obiettivi possono essere realizzati usando controlli di divulgazione progressivi, in cui gli utenti fanno clic per visualizzare altri dettagli. Tuttavia, è possibile ottenere il secondo obiettivo della semplificazione dell'aspetto senza utilizzare controlli di divulgazione progressivi espliciti per:

-   **Visualizzazione di dettagli contestuali solo nel contesto.** Ad esempio, è possibile visualizzare automaticamente i comandi contestuali o le barre degli strumenti quando pertinente per l'oggetto o la modalità selezionata.
-   **Riduzione del peso di affordances per l'interfaccia utente secondaria.** [Affordances](glossary.md) sono proprietà visive che suggeriscono come vengono usati gli oggetti. La tendenza è quella di avere un'interfaccia utente con cui gli utenti possono interagire sul posto, ma per fare in modo che l'interfaccia utente venga disegnata per urlare "fare clic qui". causa una quantità eccessiva di confusione visiva. Per l'interfaccia utente secondaria, è spesso preferibile usare affordances sottili e ottenere gli effetti completi sul passaggio del mouse.

    ![screenshot delle icone a stella usate per valutare le foto ](images/progressive-disclosure-controls-image5.png)

    In questo esempio, il campo rating è interattivo, ma non viene visualizzato fino al passaggio del mouse.

-   **Visualizzazione dei passaggi di completamento solo dopo aver completato i prerequisiti.** Questo approccio viene usato in modo ottimale con attività comuni, in cui gli utenti possono eseguire con fiducia i primi passaggi.

    ![screenshot delle caselle di testo nome utente e password ](images/progressive-disclosure-controls-image6.png)

    In questo esempio, nella pagina nome utente e password vengono inizialmente visualizzate solo le caselle nome utente e password facoltativa. Le caselle di conferma e di suggerimento vengono visualizzate dopo l'immissione di una password da parte dell'utente.

Sebbene la divulgazione progressiva sia un ottimo modo per semplificare le interfacce utente, presenta questi rischi:

-   **Mancanza di individuabilità.** Gli utenti possono presumere che se non riescono a vedere qualcosa, non esiste. Gli utenti non possono passare il puntatore del mouse oppure fare clic su se non visualizzano ciò che cercano. Esiste sempre la possibilità che gli utenti non possano fare clic su elementi come altre opzioni.
-   **Mancanza di stabilità.** La divulgazione progressiva dovrebbe essere prevista o almeno naturale. Se i controlli vengono visualizzati in modo imprevisto e scompaiono, l'interfaccia utente risultante può essere instabile.

### <a name="progressive-disclosure-controls"></a>Controlli di divulgazione progressiva

I controlli di divulgazione progressivi vengono in genere visualizzati senza etichette dirette che ne descrivono il comportamento, quindi gli utenti devono essere in grado di eseguire le operazioni seguenti in base all'aspetto visivo del controllo:

-   Riconoscere che il controllo fornisce la divulgazione progressiva.
-   Determinare se lo stato corrente è espanso o compresso.
-   Determinare se sono necessarie informazioni, opzioni o comandi aggiuntivi per eseguire l'attività.
-   Determinare come ripristinare lo stato originale, se lo si desidera.

Sebbene gli utenti possano determinare le precedenti in base a una versione di valutazione e a un errore, è consigliabile provare a rendere superflua la sperimentazione.

I controlli di divulgazione progressiva hanno un [affordances](glossary.md)piuttosto debole, ovvero le proprietà visive ne indicano il modo in cui vengono usate, anche se debole. Nella tabella seguente viene confrontato l'aspetto dei controlli di divulgazione progressiva comuni:



|                                                                                                                                                          |                                                                                                                                                                                                             |                                                                                                                                |                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Controllo**<br/>                                                                                                                                   | **Scopo**<br/>                                                                                                                                                                                      | **Aspetto**<br/>                                                                                                      | **Glifo indica**<br/> |
| **Virgolette acute**<br/> ![cattura di schermata di frecce a sinistra/destra e a freccia su/giù ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Mostra tutto:** Mostra o nasconde gli elementi rimanenti nel contenuto completamente o parzialmente nascosto. Gli elementi vengono visualizzati sul posto (usando una singola Chevron) o in un menu a comparsa (usando una doppia freccia di espansione).<br/> | Puntini di espansione nella direzione in cui si verificherà l'azione.<br/>                                                        | Stato futuro<br/>        |
| **Frecce**<br/> ![cattura di schermata di frecce a sinistra/destra e verso l'alto o verso il basso ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Mostra opzioni:** Mostra un menu di comando popup.<br/>                                                                                                                                                    | Frecce che puntano alla direzione in cui si verificherà l'azione.<br/>                                                          | Stato futuro<br/>        |
| **Controlli Plus e minus**<br/> ![Screenshot di due pulsanti più piccoli e meno ](images/progressive-disclosure-controls-image9.png)<br/> | **Espandi contenitori:** Espandi o Comprimi il contenuto del contenitore quando ci si sposta in una gerarchia.<br/>                                                                                        | I simboli Plus e minu non puntano, ma l'azione viene sempre eseguita a destra.<br/>                                    | Stato futuro<br/>        |
| **Rotazione triangoli**<br/> ![Screenshot di due triangoli piccoli ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Mostra dettagli:** Mostra o nasconde informazioni aggiuntive sul posto per un singolo elemento. Vengono usati anche per espandere i contenitori.<br/>                                                                  | La rotazione dei triangoli è leggermente simile alla rotazione delle leve, in modo che puntino nella direzione in cui si è verificata l'azione.<br/> | Stato attuale<br/>       |



 

**Se si esegue una sola operazione...**

Gli utenti devono essere in grado di prevedere il comportamento di un controllo di divulgazione progressivo in modo corretto in base all'ispezione. A tale scopo, selezionare i modelli di utilizzo appropriati e applicarne l'aspetto, la posizione e il comportamento in modo coerente.

## <a name="usage-patterns"></a>Modelli di utilizzo

I controlli di divulgazione progressivi hanno diversi modelli di utilizzo. Alcuni di essi sono incorporati in controlli comuni.

### <a name="chevrons"></a>Virgolette acute

Le frecce mostrano o nascondono gli elementi rimanenti nel contenuto completamente o parzialmente nascosto. In genere, gli elementi vengono visualizzati sul posto, ma possono essere visualizzati anche in un menu a comparsa. Quando è attiva, l'elemento rimane espanso fino a quando non viene compresso dall'utente.

Le frecce vengono utilizzate nei modi seguenti:



|                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interfaccia utente sul posto**<br/> l'oggetto associato riceve lo stato attivo per l'input e la singola freccia di espansione viene attivata con la barra spaziatrice.<br/>                       | ![screenshot della visualizzazione dello stato del Centro sicurezza ](images/progressive-disclosure-controls-image11.png)<br/> In questi esempi, le virgolette singole sul posto vengono posizionate a destra del controllo associato.<br/>                                                                            |
| **Pulsanti di comando con etichette esterne**<br/> il pulsante di comando riceve lo stato attivo per l'input e la singola freccia di espansione viene attivata con la barra spaziatrice.<br/> | ![screenshot della freccia di espansione con l'etichetta ' more options ' ](images/progressive-disclosure-controls-image12.png)<br/> In questo esempio il pulsante con la freccia di espansione singola è contrassegnato e posizionato a sinistra dell'etichetta. Con questo modello, il pulsante sarebbe difficile da comprendere senza l'etichetta.<br/> |
| **Pulsanti di comando con etichette interne**<br/> il pulsante di comando riceve lo stato attivo per l'input e viene attivato con la barra spaziatrice.<br/>                    | ![screenshot dei pulsanti di comando ' more ' è less ' ](images/progressive-disclosure-controls-image13.png)<br/> In questi esempi, i pulsanti di comando normali hanno la virgoletta doppia posizionata per suggerire il significato.<br/>                                                                          |



 

### <a name="arrows"></a>Frecce

Le frecce mostrano un menu di comando popup. L'elemento rimane espanso fino a quando l'utente effettua una selezione o fa clic in un punto qualsiasi.

Se il pulsante freccia è un controllo indipendente, riceve lo stato attivo per l'input e viene attivato con la barra spaziatrice. Se il pulsante freccia è associato a un controllo padre, l'elemento padre riceve lo stato attivo per l'input e la freccia viene attivata con ALT + freccia giù e ALT + freccia su, come nel controllo elenco a discesa.

Le frecce vengono usate nei modi seguenti:



|                                                                                       |                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pulsanti separati**<br/> la freccia si trova in un controllo Button separato.<br/> | ![screenshot delle frecce a destra dei controlli ](images/progressive-disclosure-controls-image14.png)<br/> In questi esempi, i pulsanti freccia separati posizionati a destra indicano un menu di comando.<br/>               |
| **Pulsanti di comando**<br/> la freccia fa parte di un pulsante di comando.<br/>      | ![screenshot dell'etichetta e della freccia sul pulsante di comando ](images/progressive-disclosure-controls-image15.png)<br/> In questi esempi, i pulsanti di menu e i pulsanti di menu combinato hanno le frecce posizionate a destra del testo.<br/> |



 

### <a name="plus-and-minus-controls"></a>Controlli Plus e minus

I controlli più e meno si espandono o comprimono per mostrare il contenuto del contenitore sul posto quando si Esplora una gerarchia. L'elemento rimane espanso fino a quando non viene compresso dall'utente. Sebbene siano simili ai pulsanti, il loro comportamento è sul posto.

L'oggetto associato riceve lo stato attivo per l'input. Il segno più viene attivato con il tasto freccia destra e il segno meno con il tasto freccia sinistra.

I controlli più e meno vengono usati nei modi seguenti:



|                                                                                                |                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alberi comprimibili**<br/> una gerarchia a più livelli per visualizzare il contenuto del contenitore.<br/> | ![Screenshot che mostra un albero delle cartelle di Esplora risorse con "Behavior" selezionato.](images/progressive-disclosure-controls-image16.png)<br/> In questo esempio, i controlli più e meno sono posizionati a sinistra del contenitore associato.<br/>       |
| **Elenchi comprimibili**<br/> una gerarchia a due livelli per visualizzare il contenuto del contenitore.<br/>   | ![screenshot dell'elenco espanso per mostrare due livelli ](images/progressive-disclosure-controls-image17.png)<br/> In questo esempio, i controlli più e meno sono posizionati a sinistra dell'intestazione dell'elenco associato.<br/> |



 

### <a name="rotating-triangles"></a>Rotazione triangoli

I triangoli rotanti mostrano o nascondono informazioni aggiuntive sul posto per un singolo elemento. Vengono usati anche per espandere i contenitori. L'elemento rimane espanso fino a quando non viene compresso dall'utente.

L'oggetto associato riceve lo stato attivo per l'input. Il triangolo compresso (puntamento a destra) viene attivato con il tasto freccia destra e il triangolo espanso (verso il basso) con il tasto freccia sinistra.

I triangoli rotanti vengono usati nei modi seguenti:



|                                                                                                            |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alberi comprimibili**<br/> una gerarchia a più livelli per visualizzare il contenuto del contenitore.<br/>             | ![screenshot dell'albero delle cartelle di Esplora risorse ](images/progressive-disclosure-controls-image18.png)<br/> In questo esempio, i triangoli rotanti vengono posizionati a sinistra del contenitore associato.<br/>       |
| **Elenchi comprimibili**<br/> una gerarchia a due livelli per visualizzare informazioni aggiuntive sul posto.<br/> | ![screenshot dell'elenco che Visualizza dati aggiuntivi ](images/progressive-disclosure-controls-image19.png)<br/> In questo esempio, i triangoli rotanti vengono posizionati a sinistra degli elementi dell'elenco associati.<br/> |



 

### <a name="preview-arrows"></a>Frecce di anteprima

Come le frecce, le informazioni aggiuntive vengono visualizzate o nascoste sul posto. L'elemento rimane espanso fino a quando non viene compresso dall'utente. Diversamente dalle frecce, i glifi hanno una rappresentazione grafica dell'azione, in genere con una freccia che indica che cosa accadrà.

![screenshot dei glifi delle frecce che puntano in diagonale ](images/progressive-disclosure-controls-image20.png)

In questi esempi di Microsoft Windows Media Player, i glifi hanno frecce che suggeriscono l'azione che si verificherà.

Le frecce di anteprima sono particolarmente riservate per le situazioni in cui una freccia di espansione standard non comunica adeguatamente il comportamento del controllo, ad esempio quando la divulgazione è complessa o è presente più di un tipo di divulgazione.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Selezionare il modello di divulgazione progressivo in base al relativo utilizzo.** Per una descrizione di ogni modello di utilizzo, vedere la tabella precedente.
-   **Non usare i collegamenti per i controlli di divulgazione progressivi.** Utilizzare solo i controlli di divulgazione progressivi presentati nella sezione modelli di utilizzo. Tuttavia, usare i collegamenti per passare agli [argomenti della Guida](winenv-help.md).

    **Corretto:**

    ![screenshot della freccia di espansione con etichetta ' Mostra mixer ' ](images/progressive-disclosure-controls-image21.png)

    **Non corretto:**

    ![screenshot del testo del collegamento ' Mostra mixer ' ](images/progressive-disclosure-controls-image22.png)

    Nell'esempio errato, viene usato un collegamento per visualizzare più opzioni. Questo utilizzo è corretto se il collegamento è stato spostato in un'altra pagina o finestra di dialogo oppure è stato visualizzato un argomento della guida.

### <a name="interaction"></a>Interazione

-   **Per le frecce e le frecce non direttamente etichettate, usare le descrizioni comando per descrivere le operazioni eseguite.**

    ![screenshot della descrizione comando ' Espandi il generatore di query ' ](images/progressive-disclosure-controls-image23.png)

    In questo esempio la descrizione comando indica l'effetto di un controllo Chevron senza etichetta.

-   **Se un utente espande o comprime un elemento, rendere permanente lo stato in modo che abbia effetto alla successiva visualizzazione della finestra**, a meno che non sia probabile che gli utenti preferiscono iniziare nello stato predefinito. Rendere lo stato permanente in base al singolo utente.
-   **Assicurarsi che tutto il contenuto espanso possa essere compresso e viceversa e che l'operazione inversa sia evidente.** Questa operazione favorisce l'esplorazione e riduce le frustrazioni. Il modo migliore per rendere ovvia l'operazione inversa consiste nel lasciare il controllo nella stessa posizione fissa. Se è necessario spostare il controllo, conservarlo nella stessa posizione relativa all'interno di un'area visivamente distinta.

    **Non corretto:**

    ![screenshot del pulsante ' Sostituisci ' con la freccia di espansione ](images/progressive-disclosure-controls-image24.png)

    ![screenshot del pulsante ' Sostituisci ' senza virgolette ](images/progressive-disclosure-controls-image25.png)

    In questo esempio, facendo clic sul pulsante Sostituisci con la freccia di espansione viene visualizzata la casella **di testo Sostituisci con** . Al termine di questa operazione, l'espansore Replace diventa il comando Replace, quindi non esiste alcun modo per ripristinare lo stato originale.

-   **Usare solo le chiavi di accesso appropriate per il modello di divulgazione progressiva**, come elencato nella sezione modelli di utilizzo. Non usare invio per attivare la divulgazione progressiva.

### <a name="presentation"></a>Presentazione

-   **Non usare frecce a forma di triangolare per uno scopo diverso dalla divulgazione progressiva.**

    **Non corretto:**

    ![screenshot dell'etichetta con triangolo puntato a destra ](images/progressive-disclosure-controls-image26.png)

    Sebbene questo esempio non sia un modello di divulgazione progressivo, l'uso di una freccia suggerisce che i comandi verranno visualizzati in una finestra popup.

    **Corretto:**

    ![cattura di schermata dell'etichetta con il punto sinistro del testo ](images/progressive-disclosure-controls-image27.png)

    In questo esempio viene usato correttamente un Bullet.

-   **Rimuovere (non disabilitare) i controlli di divulgazione progressivi che non si applicano nel contesto corrente.** I controlli di divulgazione progressivi devono sempre fornire il proprio suggerimento, quindi rimuoverli quando non sono disponibili altre informazioni da assegnare.

    **Non corretto:**

    ![Screenshot di un controllo ' more options ' in grigio ](images/progressive-disclosure-controls-image28.png)

    In questo esempio un controllo di divulgazione progressivo che non si applica è disabilitato in modo errato.

### <a name="chevrons"></a>Virgolette acute

-   **Utilizzare le virgolette singole per mostrare o nascondere sul posto. Usare le virgolette doppie per mostrare o nascondere usando un menu a comparsa.** Tuttavia, è consigliabile usare sempre le virgolette doppie per i pulsanti di comando con etichette interne.

    **Corretto:**

    ![screenshot del controllo delle opzioni con un numero di frecce singolo ](images/progressive-disclosure-controls-image29.png)

    **Non corretto:**

    ![cattura di schermata del controllo opzioni con più frecce ](images/progressive-disclosure-controls-image30.png)

    Nell'esempio errato, viene utilizzata una doppia freccia di espansione per la divulgazione progressiva sul posto.

    **Corretto:**

    ![screenshot del pulsante di comando con un numero di frecce doppio ](images/progressive-disclosure-controls-image31.png)

    In questo esempio viene usata una doppia freccia di espansione per la divulgazione progressiva sul posto perché è un pulsante di comando con un'etichetta interna.

-   **Fornire una relazione visiva tra la freccia di espansione e il controllo associato.** Poiché le frecce sul posto sono posizionate a destra dell'interfaccia utente associata e sono allineate a destra, è possibile che esista una certa distanza tra una freccia di espansione e il controllo associato.

    **Corretto:**

    ![screenshot delle ombreggiature Graduate dietro i controlli ](images/progressive-disclosure-controls-image32.png)

    In questo esempio è presente una chiara relazione tra la freccia di espansione sul posto e l'interfaccia utente associata.

    **Non corretto:**

    ![screenshot dello sfondo solido-bianco per i controlli ](images/progressive-disclosure-controls-image33.png)

    In questo esempio non è presente alcuna relazione visiva chiara tra la freccia di espansione sul posto e l'interfaccia utente associata, quindi sembra che sia mobile nello spazio.

### <a name="arrows"></a>Frecce

-   **Non usare la grafica a freccia che può essere confusa con le funzioni indietro, diretta, go o Play.** Usare frecce semplici a forma di triangolari (frecce senza steli) su sfondi neutri.

    **Corretto:**

    ![Screenshot di due triangoli neri piccoli ](images/progressive-disclosure-controls-image34.png)

    Queste frecce sono controlli di divulgazione chiaramente progressivi.

    **Errato (per la divulgazione progressiva):**

    ![Screenshot di due piccole frecce verdi ](images/progressive-disclosure-controls-image35.png)

    Queste frecce non hanno un aspetto analogo ai controlli di divulgazione progressiva.

    **Errato (per indietro, in poi):**

    ![Screenshot di due pulsanti con triangoli neri ](images/progressive-disclosure-controls-image36.png)

    Queste frecce hanno un aspetto simile ai controlli di divulgazione progressiva, ma non lo sono.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot del ridimensionamento e della spaziatura consigliati ](images/progressive-disclosure-controls-image37.png)

Dimensionamento e spaziatura consigliati per i controlli di divulgazione progressiva.

## <a name="labels"></a>Etichette

-   Per le frecce in un pulsante di comando con un'etichetta esterna:
    -   Assegnare una [chiave di accesso](glossary.md)univoca. Per le linee guida, vedere [tastiera](inter-keyboard.md).
    -   Usare l'uso [di maiuscole in stile frase](glossary.md).
    -   Scrivere l'etichetta come frase e non usare la punteggiatura finale.
    -   Scrivere l'etichetta in modo che descriva l'effetto del clic sul pulsante e modificare l'etichetta quando lo stato cambia.
    -   Se la superficie Visualizza sempre alcune opzioni, comandi o dettagli, usare le coppie di etichette seguenti:
        -   **Opzioni più o meno.** Usare per le opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Comandi più o meno.** Usare solo per i comandi.
        -   **Dettagli più o meno.** Utilizzare solo per informazioni.
        -   **Più o meno <object name> .** Utilizzare per altri tipi di oggetto, ad esempio cartelle.
    -   In caso contrario:
        -   **Mostra/Nascondi opzioni.** Usare per le opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Mostra/Nascondi comandi.** Usare solo per i comandi.
        -   **Mostra/Nascondi dettagli.** Utilizzare solo per informazioni.
        -   **Mostra/Nascondi <object name> .** Utilizzare per altri tipi di oggetto, ad esempio cartelle.
-   Per le frecce in un pulsante di comando con un'etichetta interna, seguire le linee guida per i [pulsanti di comando](ctrl-command-buttons.md) standard.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a controlli di divulgazione progressivi:

-   Se il controllo ha un'etichetta fissa, fare riferimento al controllo in base all'etichetta. non provare a descrivere il controllo. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso.
-   Se il controllo non dispone di un'etichetta o non è corretto, fare riferimento al controllo in base al relativo tipo: Chevron, freccia, triangolo o pulsante più/meno. Se necessario, descrivere anche il percorso del controllo. Se il controllo viene visualizzato in modo dinamico, ad esempio il controllo [dello spazio della pagina](glossary.md) , avviare il riferimento descrivendo come fare in modo che il controllo venga visualizzato.

    **Esempio:** Per visualizzare i file all'interno di una cartella, spostare il puntatore all'inizio del nome della cartella, quindi fare clic sul triangolo accanto alla cartella.

-   Non fare riferimento al controllo come pulsante, a meno che non si contrasti con altri controlli di divulgazione progressivi che non sono pulsanti.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su. Se necessario per maggiore chiarezza, utilizzare fare clic su... per espandere o comprimere.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempi:

-   (Per una freccia di espansione) Per determinare le dimensioni del file, fare clic su **Dettagli**.
-   (Per una freccia) Per visualizzare tutte le opzioni, fare clic sulla freccia accanto alla casella di **ricerca** .
-   (Per più/meno) Per visualizzare l'immagine, fare clic su **Immagini**.

