---
title: Controlli di divulgazione progressiva
description: Con un controllo di divulgazione progressiva, gli utenti possono visualizzare o nascondere informazioni aggiuntive, inclusi dati, opzioni o comandi.
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1d561ea6e4f937c6e162f9eaa1f452e73d7de20c9f94c41785641062c21cd1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676166"
---
# <a name="progressive-disclosure-controls"></a>Controlli di divulgazione progressiva

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un controllo di divulgazione progressiva, gli utenti possono visualizzare o nascondere informazioni aggiuntive, inclusi dati, opzioni o comandi. La diffusione progressiva promuove la semplicità concentrandosi sull'essenziale, ma rivelando dettagli aggiuntivi in base alle esigenze.

![Screenshot dei controlli di divulgazione progressiva](images/progressive-disclosure-controls-image1.png)

Esempi di controlli di divulgazione progressiva.

> [!Note]  
> Le linee guida relative [al layout,](vis-layout.md) [ai menu](cmd-menus.md)e alle barre [degli strumenti](cmd-toolbars.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Gli utenti devono visualizzare le informazioni in alcuni scenari, ma non in tutti, o in alcuni, ma non sempre?** In tal caso, la visualizzazione delle informazioni tramite diffusione progressiva semplifica l'esperienza di base, ma consente agli utenti di accedere facilmente alle informazioni.

    ![Screenshot che mostra lo stato del Centro sicurezza.](images/progressive-disclosure-controls-image2.png)

    In questo esempio il Centro sicurezza visualizza sempre lo stato di sicurezza importante, ma usa la diffusione progressiva per visualizzare i dettagli su richiesta.

-   **Se le informazioni vengono visualizzate per impostazione predefinita, è probabile che gli utenti scesino di nasconderli?** Esistono scenari in cui gli utenti avranno bisogno di più spazio? Gli utenti sono sufficientemente motivati a personalizzare l'interfaccia utente? In caso contrario, visualizzare le informazioni senza usare la diffusione progressiva.

    **Non corretto:**

    ![Screenshot delle scelte di dati visualizzate per impostazione predefinita ](images/progressive-disclosure-controls-image3.png)

    In questo esempio gli utenti non saranno motivati a nascondere le informazioni.

-   **Le informazioni aggiuntive sono avanzate, sostanziali, complesse o correlate a una sottoattività indipendente?** In tal caso, è consigliabile visualizzare [](ctrl-command-buttons.md) le informazioni in una finestra separata usando pulsanti di comando o collegamenti [invece](ctrl-command-links.md) di usare un controllo di divulgazione progressiva. Altre informazioni sono avanzate se sono destinate a utenti esperti. È complesso se rende difficile la lettura o il lay out di altre informazioni.

    ![Screenshot di si vuole eseguire questo file? ](images/progressive-disclosure-controls-image4.png)

    In questo esempio, le informazioni sul nome e sull'autore del software sono significative principalmente per gli utenti avanzati, quindi vengono usati collegamenti a finestre separate.

-   **Le informazioni aggiuntive sono un frammento di frase o frase che descrive cosa fa un elemento o come può essere usato?** In tal caso, è consigliabile usare una [descrizione comando](ctrl-tooltips-and-infotips.md) o una descrizione comando.
-   **Le informazioni aggiuntive sono correlate all'attività corrente, ma indipendenti dalle informazioni attualmente visualizzate?** In tal caso, è consigliabile [usare le tabulazioni.](ctrl-tabs.md) Tuttavia, gli elenchi comprimibile sono spesso preferibili alle schede perché sono più flessibili e scalabili.
-   **Le informazioni aggiuntive vengono visualizzate o nascoste essenzialmente come filtro dati?** In tal caso, è consigliabile usare [un](/windows/desktop/uxguide/ctrl-drop) elenco a discesa o caselle [di](ctrl-check-boxes.md) controllo per applicare il filtro all'intero elenco.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gli obiettivi della divulgazione progressiva sono:

-   **Semplificare un'interfaccia** utente concentrandosi sull'essenziale, ma rivelando dettagli aggiuntivi in base alle esigenze.
-   **Semplificare l'aspetto di un'interfaccia** utente riducendo la percezione di confusione.

Entrambi gli obiettivi possono essere raggiunti usando controlli di divulgazione progressiva, in cui gli utenti possono fare clic per visualizzare più dettagli. Tuttavia, è possibile raggiungere il secondo obiettivo di semplificare l'aspetto senza usare controlli espliciti di divulgazione progressiva tramite:

-   **Visualizzazione dei dettagli contestuali solo nel contesto.** Ad esempio, è possibile visualizzare automaticamente i comandi contestuali o le barre degli strumenti quando sono rilevanti per l'oggetto o la modalità selezionata.
-   **Riduzione del peso degli affordance per l'interfaccia utente secondaria.** [Gli affordance sono](glossary.md) proprietà visive che suggeriscono come vengono usati gli oggetti. La tendenza è quella di avere un'interfaccia utente con cui gli utenti possono interagire sul posto, ma di avere tutta questa interfaccia utente disegnata per gridare "click me!" causa troppi disordini visivi. Per l'interfaccia utente secondaria, è spesso meglio usare i affordances sottili e fornire gli effetti completi sul passaggio del mouse.

    ![Screenshot delle icone a stella usate per valutare le foto ](images/progressive-disclosure-controls-image5.png)

    In questo esempio il campo Valutazione è interattivo, ma non viene visualizzato fino al passaggio del mouse.

-   **Visualizzazione dei passaggi di follow-up solo dopo aver eseguito i prerequisiti.** Questo approccio è più adatto alle attività familiari in cui gli utenti possono eseguire con sicurezza i primi passaggi.

    ![Screenshot delle caselle di testo nome utente e password ](images/progressive-disclosure-controls-image6.png)

    In questo esempio la pagina nome utente e password mostra inizialmente solo le caselle nome utente e password facoltative. Le caselle di conferma e suggerimento vengono visualizzate dopo che l'utente ha immesso una password.

Sebbene la diffusione progressiva sia un ottimo modo per semplificare le informazioni utente, presenta questi rischi:

-   **Mancanza di individuabilità.** Gli utenti possono presupporre che se non possono vedere qualcosa, non esiste. Gli utenti non possono passare il puntatore del mouse o fare clic se non vedono ciò che stanno cercando. È sempre possibile che gli utenti non clicno su elementi come Altre opzioni.
-   **Mancanza di stabilità.** La divulgazione progressiva deve essere prevista o almeno sembra naturale. Se i controlli vengono visualizzati e scompaiono in modo imprevisto, l'interfaccia utente risultante può risultare instabile.

### <a name="progressive-disclosure-controls"></a>Controlli di divulgazione progressiva

I controlli di diffusione progressiva vengono in genere visualizzati senza etichette dirette che ne descrivono il comportamento, quindi gli utenti devono poter eseguire le operazioni seguenti in base all'aspetto visivo del controllo:

-   Riconoscere che il controllo fornisce una diffusione progressiva.
-   Determinare se lo stato corrente è espanso o compresso.
-   Determinare se sono necessarie informazioni, opzioni o comandi aggiuntivi per eseguire l'attività.
-   Determinare come ripristinare lo stato originale, se necessario.

Anche se gli utenti possono determinare quanto sopra per versione di valutazione ed errore, è consigliabile provare a rendere questa sperimentazione superflua.

I controlli di diffusione progressiva hanno una convenienza piuttosto [debole,](glossary.md)il che significa che le proprietà visive suggeriscono come vengono usati, anche se in modo debole. Nella tabella seguente viene confrontato l'aspetto dei controlli di divulgazione progressiva comuni:



| Control | Scopo  | Aspetto | Il glifo indica |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Chevrons**<br/> ![Screenshot delle scacchiere sinistra/destra e su/giù ](images/progressive-disclosure-controls-image7.png)<br/>                 | **Mostra tutto:** Mostra o nasconde gli elementi rimanenti nel contenuto completamente o parzialmente nascosto. Gli elementi vengono visualizzati sul posto (usando una singola freccia) o in un menu a comparsa (usando una doppia freccia).<br/> | Le scacchiere puntano nella direzione in cui si verificherà l'azione.<br/>                                                        | Stato futuro<br/>        |
| **Frecce**<br/> ![Screenshot delle frecce sinistra/destra e su/giù ](images/progressive-disclosure-controls-image8.png)<br/>                     | **Mostra opzioni:** Visualizzare un menu di comando popup.<br/>                                                                                                                                                    | Le frecce puntano nella direzione in cui si verificherà l'azione.<br/>                                                          | Stato futuro<br/>        |
| **Controlli più e meno**<br/> ![Screenshot di due piccoli pulsanti più e meno ](images/progressive-disclosure-controls-image9.png)<br/> | **Espandere i contenitori:** Espandere o comprimere il contenuto del contenitore sul posto quando si esplora una gerarchia.<br/>                                                                                        | I simboli più e meno non puntano, ma l'azione si verifica sempre a destra.<br/>                                    | Stato futuro<br/>        |
| **Rotazione dei triangoli**<br/> ![Screenshot di due piccoli triangoli ](images/progressive-disclosure-controls-image10.png)<br/>                  | **Mostra dettagli:** Mostra o nasconde informazioni aggiuntive sul posto per un singolo elemento. Vengono usati anche per espandere i contenitori.<br/>                                                                  | I triangoli rotanti sono simili a leve rotanti, quindi puntano nella direzione in cui si è verificata l'azione.<br/> | Stato attuale<br/>       |



 

**Se si fa una sola cosa...**

Gli utenti devono essere in grado di stimare correttamente il comportamento di un controllo di divulgazione progressiva solo tramite ispezione. A tale scopo, selezionare i modelli di utilizzo appropriati e applicarne l'aspetto, la posizione e il comportamento in modo coerente.

## <a name="usage-patterns"></a>Modelli di utilizzo

I controlli di divulgazione progressiva hanno diversi modelli di utilizzo. Alcuni di essi sono incorporati in controlli comuni.

### <a name="chevrons"></a>Chevrons

Le barre di controllo mostrano o nascondono gli elementi rimanenti in contenuto completamente o parzialmente nascosto. In genere gli elementi vengono visualizzati sul posto, ma possono anche essere visualizzati in un menu a comparsa. Quando è sul posto, l'elemento rimane espanso fino a quando l'utente non lo comprime.

Le virgolette di controllo vengono usate nei modi seguenti:



|      Utilizzo                                                                                                                                                          |    Esempio                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Interfaccia utente sul posto**<br/> L'oggetto associato riceve lo stato attivo per l'input e la singola virgoletta di controllo viene attivata con la barra spaziatrice.<br/>                       | ![Screenshot della visualizzazione dello stato del Centro sicurezza ](images/progressive-disclosure-controls-image11.png)<br/> In questi esempi le virgolette singole sul posto vengono posizionate a destra del controllo associato.<br/>                                                                            |
| **Pulsanti di comando con etichette esterne**<br/> Il pulsante di comando riceve lo stato attivo per l'input e la singola virgoletta di controllo viene attivata con la barra spaziatrice.<br/> | ![Screenshot della casella di controllo con l'etichetta "altre opzioni" ](images/progressive-disclosure-controls-image12.png)<br/> In questo esempio il singolo pulsante di freccia di controllo viene etichettato e posizionato a sinistra dell'etichetta. Con questo modello, il pulsante sarebbe difficile da comprendere senza la relativa etichetta.<br/> |
| **Pulsanti di comando con etichette interne**<br/> il pulsante di comando riceve lo stato attivo per l'input e viene attivato con la barra spaziatrice.<br/>                    | ![Screenshot dei pulsanti di comando "more" e "less" ](images/progressive-disclosure-controls-image13.png)<br/> In questi esempi, i normali pulsanti di comando hanno la doppia freccia di controllo posizionata per suggerire il loro significato.<br/>                                                                          |



 

### <a name="arrows"></a>Frecce

Le frecce mostrano un menu di comando popup. L'elemento rimane espanso fino a quando l'utente non effettua una selezione o non fa clic in un punto qualsiasi.

Se il pulsante freccia è un controllo indipendente, riceve lo stato attivo per l'input e viene attivato con la barra spaziatrice. Se il pulsante freccia ha un controllo padre, l'elemento padre riceve lo stato attivo per l'input e la freccia viene attivata con ALT+freccia GIÙ e ALT+freccia SU, come nel controllo elenco a discesa.

Le frecce vengono usate nei modi seguenti:



|    Utilizzo                                                                                   |    Esempio                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pulsanti separati**<br/> la freccia si trova in un controllo pulsante separato.<br/> | ![Screenshot delle frecce a destra dei controlli ](images/progressive-disclosure-controls-image14.png)<br/> In questi esempi, pulsanti freccia separati posizionati a destra indicano un menu di comando.<br/>               |
| **Pulsanti di comando**<br/> la freccia fa parte di un pulsante di comando.<br/>      | ![Screenshot dell'etichetta e della freccia sul pulsante di comando ](images/progressive-disclosure-controls-image15.png)<br/> In questi esempi, i pulsanti di menu e i pulsanti di menu suddivisi hanno le frecce posizionate a destra del testo.<br/> |



 

### <a name="plus-and-minus-controls"></a>Controlli più e meno

I controlli più e meno si espandono o si comprimino per visualizzare il contenuto del contenitore sul posto durante lo spostamento all'interno di una gerarchia. L'elemento rimane espanso fino a quando l'utente non lo comprime. Anche se sembrano pulsanti, il loro comportamento è sul posto.

L'oggetto associato riceve lo stato attivo per l'input. Il segno più viene attivato con il tasto freccia DESTRA e il segno meno con il tasto freccia sinistra.

I controlli più e meno vengono usati nei modi seguenti:



|       Utilizzo                                                                                         |       Esempio                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alberi comprimibili**<br/> una gerarchia multi-livello per visualizzare il contenuto del contenitore.<br/> | ![Screenshot che mostra un albero Windows di cartelle di Esplora risorse con l'opzione "Comportamento" selezionata.](images/progressive-disclosure-controls-image16.png)<br/> In questo esempio i controlli più e meno vengono posizionati a sinistra del contenitore associato.<br/>       |
| **Elenchi comprimibili**<br/> una gerarchia a due livelli per visualizzare il contenuto del contenitore.<br/>   | ![Screenshot dell'elenco espanso per mostrare due livelli ](images/progressive-disclosure-controls-image17.png)<br/> In questo esempio i controlli più e meno vengono posizionati a sinistra dell'intestazione dell'elenco associato.<br/> |



 

### <a name="rotating-triangles"></a>Rotazione di triangoli

I triangoli rotanti mostrano o nascondono informazioni aggiuntive per un singolo elemento. Vengono usati anche per espandere i contenitori. L'elemento rimane espanso fino a quando l'utente non lo comprime.

L'oggetto associato riceve lo stato attivo per l'input. Il triangolo compresso (puntato a destra) viene attivato con il tasto freccia destra e il triangolo espanso (verso il basso) con il tasto freccia SINISTRA.

La rotazione dei triangoli viene usata nei modi seguenti:



|     Utilizzo                                                                                                       |    Esempio                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Alberi comprimibili**<br/> una gerarchia multi-livello per visualizzare il contenuto del contenitore.<br/>             | ![Screenshot dell'albero delle cartelle di Esplora risorse ](images/progressive-disclosure-controls-image18.png)<br/> In questo esempio i triangoli rotanti vengono posizionati a sinistra del contenitore associato.<br/>       |
| **Elenchi comprimibili**<br/> una gerarchia a due livelli per visualizzare informazioni aggiuntive sul posto.<br/> | ![Screenshot dell'elenco che mostra dati aggiuntivi ](images/progressive-disclosure-controls-image19.png)<br/> In questo esempio i triangoli rotanti vengono posizionati a sinistra degli elementi dell'elenco associati.<br/> |



 

### <a name="preview-arrows"></a>Frecce di anteprima

Come le scacchiere, le informazioni aggiuntive vengono visualizzate o nascoste sul posto. L'elemento rimane espanso fino a quando l'utente non lo comprime. A differenza delle frecce di controllo, i glifi hanno una rappresentazione grafica dell'azione, in genere con una freccia che indica cosa accadrà.

![Screenshot dei glifi a freccia che puntano in diagonale ](images/progressive-disclosure-controls-image20.png)

In questi esempi di Microsoft Windows Media Player, i glifi hanno frecce che suggeriscono l'azione che verrà eseguita.

Le frecce di anteprima sono meglio riservate nelle situazioni in cui una freccia di controllo standard non comunica in modo adeguato il comportamento del controllo, ad esempio quando la divulgazione è complessa o è presente più di un tipo di diffusione.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Selezionare il modello di divulgazione progressiva in base al relativo utilizzo.** Per una descrizione di ogni modello di utilizzo, vedere la tabella precedente.
-   **Non usare collegamenti per i controlli di divulgazione progressiva.** Usare solo i controlli di divulgazione progressiva presentati nella sezione Modelli di utilizzo. Usare tuttavia i collegamenti per passare agli argomenti [della Guida.](winenv-help.md)

    **Corretto:**

    ![Screenshot della casella di controllo con etichetta "show mixer" ](images/progressive-disclosure-controls-image21.png)

    **Non corretto:**

    ![Screenshot del testo del collegamento "Mostra mixer" ](images/progressive-disclosure-controls-image22.png)

    Nell'esempio non corretto viene usato un collegamento per visualizzare altre opzioni sul posto. Questo utilizzo sarebbe corretto se il collegamento passasse a un'altra pagina o finestra di dialogo o visualizzasse un argomento della Guida.

### <a name="interaction"></a>Interazione

-   **Per le frecce e le frecce che non sono etichettate direttamente, usare le descrizioni comando per descrivere le loro funzionalità.**

    ![Screenshot della descrizione comando "Espandi generatore query" ](images/progressive-disclosure-controls-image23.png)

    In questo esempio la descrizione comando indica l'effetto di un controllo chevron senza etichetta.

-   Se un utente espande o comprime un **elemento,** rendere persistente lo stato in modo che venga reso attivo alla successiva visualizzazione della finestra, a meno che gli utenti non preferiscano iniziare con lo stato predefinito. Rendere persistente lo stato per ogni finestra, per utente.
-   **Assicurarsi che tutto il contenuto espanso possa essere compresso e viceversa e che l'operazione inversa sia ovvia.** In questo modo si favorisce l'esplorazione e si riduce la frustrazione. Il modo migliore per rendere ovvia l'operazione inversa è mantenere il controllo nella stessa posizione fissa. Se è necessario spostare il controllo, mantenerlo nella stessa posizione relativa all'interno di un'area visivamente distinta.

    **Non corretto:**

    ![Screenshot del pulsante "sostituisci" con la barra di controllo ](images/progressive-disclosure-controls-image24.png)

    ![Screenshot del pulsante "sostituisci" senza chevron ](images/progressive-disclosure-controls-image25.png)

    In questo esempio, facendo clic sul pulsante Sostituisci con la freccia di sospensione viene visualizzata la **casella di** testo Sostituisci con . Al termine, l'espansione Sostituisci diventa il comando Sostituisci, quindi non è possibile ripristinare lo stato originale.

-   **Usare solo le chiavi di accesso appropriate per il modello di divulgazione progressiva,** come elencato nella sezione Modelli di utilizzo. Non usare INVIO per attivare la diffusione progressiva.

### <a name="presentation"></a>Presentazione

-   **Non usare frecce a forma triangolare per scopi diversi dalla diffusione progressiva.**

    **Non corretto:**

    ![Screenshot dell'etichetta con triangolo puntato a destra ](images/progressive-disclosure-controls-image26.png)

    Anche se questo esempio non è un modello di divulgazione progressiva, l'uso di una freccia in questo caso suggerisce che i comandi verranno visualizzati in una finestra popup.

    **Corretto:**

    ![Screenshot dell'etichetta con punto elenco a sinistra del testo ](images/progressive-disclosure-controls-image27.png)

    In questo esempio viene invece usato correttamente un punto elenco.

-   **Rimuovere (non disabilitare) i controlli di divulgazione progressiva che non si applicano nel contesto corrente.** I controlli di divulgazione progressiva devono sempre garantire la promessa, quindi rimuoverli quando non sono disponibili altre informazioni da fornire.

    **Non corretto:**

    ![Screenshot di un controllo "altre opzioni" in grigio ](images/progressive-disclosure-controls-image28.png)

    In questo esempio, un controllo di divulgazione progressiva che non si applica viene disabilitato in modo errato.

### <a name="chevrons"></a>Chevrons

-   **Usare le virgolette singole per mostrare o nascondere sul posto. Usare le doppie virgolette per visualizzare o nascondere usando un menu a comparsa.** È tuttavia consigliabile usare sempre doppie virgolette per i pulsanti di comando con etichette interne.

    **Corretto:**

    ![Screenshot del controllo di altre opzioni a virgolette singole ](images/progressive-disclosure-controls-image29.png)

    **Non corretto:**

    ![Screenshot del controllo di altre opzioni a doppia freccia di controllo ](images/progressive-disclosure-controls-image30.png)

    Nell'esempio non corretto viene usata una doppia freccia a scacchi per la diffusione progressiva sul posto.

    **Corretto:**

    ![Screenshot del pulsante di comando con doppia freccia di sospensione ](images/progressive-disclosure-controls-image31.png)

    In questo esempio viene usata una doppia freccia di sospensione per la diffusione progressiva sul posto perché è un pulsante di comando con un'etichetta interna.

-   **Fornire una relazione visiva tra la chevron e il controllo associato.** Poiché le scacchiere sul posto sono posizionate a destra dell'interfaccia utente associata e allineate a destra, può esserci una certa distanza tra una freccia di controllo e il controllo associato.

    **Corretto:**

    ![Screenshot dell'ombreggiatura graduale dietro i controlli ](images/progressive-disclosure-controls-image32.png)

    In questo esempio esiste una relazione chiara tra la barra di controllo sul posto e l'interfaccia utente associata.

    **Non corretto:**

    ![Screenshot di sfondo bianco e tinta unita per i controlli ](images/progressive-disclosure-controls-image33.png)

    In questo esempio non esiste una relazione visiva chiara tra la barra di controllo sul posto e l'interfaccia utente associata, quindi sembra essere mobile nello spazio.

### <a name="arrows"></a>Frecce

-   **Non usare elementi grafici a freccia che potrebbero essere confusi con Back, Forward, Go o Play.** Usare semplici frecce a forma triangolare (frecce senza gambi) su sfondi neutri.

    **Corretto:**

    ![Screenshot di due piccoli triangoli neri ](images/progressive-disclosure-controls-image34.png)

    Queste frecce sono controlli di divulgazione chiaramente progressivi.

    **Non corretto (per diffusione progressiva):**

    ![Screenshot di due piccole frecce verdi ](images/progressive-disclosure-controls-image35.png)

    Queste frecce non sono simili ai controlli di divulgazione progressiva.

    **Non corretto (per Back, Forward):**

    ![Screenshot di due pulsanti con triangoli neri ](images/progressive-disclosure-controls-image36.png)

    Queste frecce sembrano controlli di divulgazione progressiva, ma non lo sono.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot del ridimensionamento e della spaziatura consigliati ](images/progressive-disclosure-controls-image37.png)

Dimensioni e spaziatura consigliate per i controlli di diffusione progressiva.

## <a name="labels"></a>Etichette

-   Per le scacchiere su un pulsante di comando con un'etichetta esterna:
    -   Assegnare una chiave [di accesso univoca.](glossary.md) Per le linee guida, vedere [Tastiera](inter-keyboard.md).
    -   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
    -   Scrivere l'etichetta come frase e non usare la punteggiatura finale.
    -   Scrivere l'etichetta in modo che descriva l'effetto del clic sul pulsante e modificare l'etichetta quando cambia lo stato.
    -   Se la superficie visualizza sempre alcune opzioni, comandi o dettagli, usare le coppie di etichette seguenti:
        -   **Più/Meno opzioni.** Usare per opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Più/Meno comandi.** Usare solo per i comandi.
        -   **Più/Meno dettagli.** Usare solo per le informazioni.
        -   **Più o meno <object name> .** Usare per altri tipi di oggetto, ad esempio le cartelle.
    -   In caso contrario:
        -   **Mostra/Nascondi opzioni.** Usare per opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Comandi Mostra/Nascondi.** Usare solo per i comandi.
        -   **Mostra/Nascondi dettagli.** Usare solo per le informazioni.
        -   **Mostra/Nascondi <object name> .** Usare per altri tipi di oggetto, ad esempio le cartelle.
-   Per le virgolette su un pulsante di comando con un'etichetta interna, seguire le linee guida standard [per il pulsante di](ctrl-command-buttons.md) comando.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai controlli di divulgazione progressiva:

-   Se il controllo ha un'etichetta fissa, fare riferimento al controllo solo in base all'etichetta; non provare a descrivere il controllo. Usare il testo esatto dell'etichetta, inclusa la relativa combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura della chiave di accesso.
-   Se il controllo non ha etichetta o non è fisso, fare riferimento al controllo in base al tipo: freccia, triangolo o pulsante più/meno. Se necessario, descrivere anche la posizione del controllo. Se il controllo viene visualizzato in modo dinamico, ad esempio [lo](glossary.md) spazio della pagina, avviare il riferimento descrivendo come visualizzare il controllo.

    **Esempio:** Per visualizzare i file all'interno di una cartella, spostare il puntatore all'inizio del nome della cartella e quindi fare clic sul triangolo accanto alla cartella.

-   Non fare riferimento al controllo come pulsante, a meno che non si contrasti con altri controlli di divulgazione progressiva che non sono pulsanti.
-   Per descrivere l'interazione dell'utente, usare click. Se necessario per maggiore chiarezza, usare click... per espandere o comprimere.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempi:

-   (Per una chevron) Per determinare le dimensioni del file, fare clic su **Dettagli**.
-   (Per una freccia) Per visualizzare tutte le opzioni, fare clic sulla freccia accanto alla **casella Di** ricerca.
-   (per più/meno) Per visualizzare l'immagine, fare clic su **Immagini**.

