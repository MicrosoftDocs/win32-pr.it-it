---
title: Color
description: Il colore è un elemento visivo importante della maggior parte delle interfacce utente.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 598654c7e96f025bbcc1ff2a97c96df1a328c046
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444642"
---
# <a name="color"></a>Color

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Il colore è un elemento visivo importante della maggior parte delle interfacce utente. Oltre all'aspetto estetico puro, il colore ha associato significati e incita a risposte emotive. Per evitare confusione nel significato, è necessario usare il colore in modo coerente. Per ottenere le risposte emotive desiderate, è necessario usare il colore in modo appropriato.

Il colore viene spesso pensato in termini di spazio colore, dove RGB (rosso, verde, blu), HSL (tonalità, saturazione, luminosità) e HSV (tonalità, saturazione, valore) sono gli spazi colori usati più comunemente.

![Figura di un cubo che mostra le relazioni tra colori ](images/vis-color-image1.png)

Lo spazio colore RGB può essere visualizzato come cubo.

Sebbene la tecnologia di visualizzazione usi valori RGB e di conseguenza gli sviluppatori spesso pensino ai colori in termini di RGB, lo spazio colore RGB non corrisponde al modo in cui gli utenti percepiranno il colore. Ad esempio, se si aggiunge il rosso al ciano scuro, il risultato non viene percepito come più rosso, ma come ciano più chiaro.

![illustrazione di quadrati ciano scuro e chiaro ](images/vis-color-image2.png)

In questo esempio, l'aggiunta del rosso al ciano scuro lo rende più leggero, non più rosso. Lo spazio colore RGB non corrisponde al modo in cui gli utenti percepiranno il colore.

Gli spazi colori HSL/HSV sono costituiti da tre componenti: tonalità, saturazione e luminosità o valore. Questi spazi colori vengono spesso usati al posto di RGB perché corrispondono meglio al modo in cui gli utenti percepiranno il colore.

Lo spazio colori HSL forma un doppio cono bianco nella parte superiore, nero nella parte inferiore e neutro al centro:

-   **Tonalità:** Colore di base nella ruota dei colori, compreso tra 0 e 360 gradi in cui sia 0 che 360 gradi sono rossi.

    ![Figura di un cerchio che mostra le relazioni tra colori ](images/vis-color-image3.png)

    La ruota dei colori, dove rosso è 0 gradi, giallo è 60 gradi, verde è 120 gradi, ciano è 180 gradi, blu è 240 gradi e magenta è 300 gradi.

-   **Saturazione:** Quanto è puro (o noioso) il colore, compreso tra 0 e 100, dove 100 è completamente saturato e 0 è grigio.
-   **Luminosità:** Quanto chiaro è il colore, compreso tra 0 e 100, dove 100 è il più chiaro possibile (bianco, indipendentemente dalla tonalità e dalla saturazione) e 0 è il più scuro possibile (nero).

    ![Figura che illustra lo spazio colore hsl ](images/vis-color-image4.png)

    Lo spazio colori HSL può essere visualizzato come doppio cono.

Lo spazio colori HSV è simile, ad eccezione del fatto che lo spazio forma un singolo cono:

-   **Tonalità:** Colore di base nella ruota dei colori, compreso tra 0 e 360 gradi in cui sia 0 che 360 gradi sono rossi.
-   **Saturazione:** Quanto è puro (o noioso) il colore, compreso tra 0 e 100, dove 100 è completamente saturato e 0 è grigio.
-   **Valore:** Quanto è chiaro il colore, compreso tra 0 e 100, dove 100 è il più chiaro possibile (che è metà luminosità nello spazio HSL) e 0 è il più scuro possibile (nero).

    ![Figura che illustra lo spazio colore hsv ](images/vis-color-image5.png)

    Lo spazio colori HSV può essere visualizzato come singolo cono.

Negli spazi HSL e HSV, se la saturazione è 0, la luminosità specifica una sfumatura di grigio. In Windows, gli spazi HSL e HSV vengono in genere mappati a una scala compresa tra 0 e 240 in modo che i colori possano essere rappresentati con un valore a 32 bit.

**Nota:** Le linee guida relative ai [tipi di](vis-fonts.md) carattere [e all'accessibilità](inter-accessibility.md) sono presentate in articoli separati.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Un uso efficace del colore può rendere più efficace l'interfaccia utente del programma. Il colore può aiutare gli utenti a comprendere a colpo d'occhio determinati significati. Il colore può anche rendere il prodotto più esteticamente piacevole e perfezionato.

Sfortunatamente, è fin troppo facile usare il colore in modo inefficace, soprattutto se non si è formati nella progettazione visiva. L'uso scarso dei risultati dei colori nei progetti che sembrano poco professionale, datati, confusi o semplicemente brutti. Un uso non affatto utilizzato del colore può essere peggiore del non usare il colore.

Questa sezione illustra cosa è necessario sapere per usare il colore in modo efficace.

### <a name="how-color-is-used"></a>Come viene usato il colore

Il colore viene in genere usato nell'interfaccia utente per comunicare:

-   **Significato.** Il significato di un messaggio può essere riepilogato tramite il colore. Ad esempio, il colore viene spesso usato per comunicare lo stato in cui il rosso è un problema o un errore, il giallo è attenzione o avviso e il verde è valido.
-   **Stato.** Lo stato di un oggetto può essere indicato tramite il colore. Ad esempio, Windows usa il colore per indicare gli stati di selezione e passaggio del mouse. I collegamenti all'interno delle pagine Web usano il blu per gli elementi nonvisi e viola per le pagine visitate.
-   **Differenziazione.** Le persone presuppongono che ci sia una relazione tra elementi dello stesso colore, quindi la codifica a colori è un modo efficace per distinguere gli oggetti. Ad esempio, in un elemento del Pannello di controllo, i riquadri attività usano uno sfondo verde per separarli visivamente dal contenuto principale. Microsoft Outlook consente inoltre agli utenti di assegnare flag colorati diversi ai messaggi.
-   **Enfasi.** Il colore può essere usato per attirare l'attenzione degli utenti. Ad esempio, Windows usa le [istruzioni principali blu](text-ui.md) per distinguerle dall'altro testo.

Naturalmente, il colore viene spesso usato nella grafica per motivi puramente estetici. Anche se l'aspetto estetico è importante, è consigliabile scegliere i colori degli elementi dell'interfaccia utente principalmente in base al significato e non all'aspetto.

### <a name="color-interpretation"></a>Interpretazione del colore

**L'interpretazione del colore da parte degli utenti dipende spesso dalle impostazioni cultura.** Ad esempio, nell'Stati Uniti, l'abbigliamento nuziale per la spose è in gran parte associato al colore bianco, mentre il nero è associato ai fiori funebri. Tuttavia, molto tempo fa in Giappone il simbolismo dei colori era esattamente il contrario: il bianco era il colore predominante ai funebri e il nero era considerato un colore che porta buona fortuna per i fedi nuziali.

Detto questo, **l'interpretazione di rosso, giallo e verde** per lo stato è coerente a livello globale. Ciò è dovuto alla Convenzione di Maiolandese [per](https://www.unece.org/trans/conventn/signalse.pdf)i segnali stradali, che definisce la convenzione mondiale per i semafori (dove il rosso indica stop, il verde significa procedere e il giallo indica procedere con cautela). È possibile usare questi colori di stato senza problemi per le interpretazioni dipendenti dalla cultura.

Oltre ai colori di stato, Windows assegna significati ai colori in base alla convenzione, come illustrato nella sezione Linee guida di questo articolo. Assicurarsi che l'utilizzo dei colori del programma sia compatibile con queste convenzioni di colore.

### <a name="color-accessibility"></a>Accessibilità dei colori

L'uso del colore influisce sull'accessibilità del software al pubblico più ampio possibile. Gli utenti con cecità o visione bassa potrebbero non essere in grado di vedere bene i colori, se non del tutto. Circa l'8% dei maschi adulti ha una qualche forma di confusione di colore (spesso definita erroneamente "cecità dei colori"), di cui la confusione di colore rosso-verde è la più comune.

![Figura che mostra i colori primari come di consueto ](images/vis-color-image6.png)

I colori primari, come si vede con la visione dei colori normale.

![figura che mostra gli stessi colori visualizzati con la protanopia ](images/vis-color-image7.png)

I colori primari come si può vedere con Protanopia (1% della popolazione di sesso femminile).

![Figura che mostra gli stessi colori visualizzati con la deuteranopia ](images/vis-color-image8.png)

I colori primari, come si può vedere con Deuteranopia (6% della popolazione di sesso femminile).

![Figura che mostra gli stessi colori visualizzati con tritanopia ](images/vis-color-image9.png)

I colori primari, come si vede con Tritanopia (1% della popolazione di sesso femminile).

Per altre informazioni, vedere [Gli Color-Blind utenti possono visualizzare il sito?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Usare il colore per rinforzare visivamente

La soluzione migliore per l'interpretazione dei colori e i problemi di accessibilità consiste nell'usare il colore per rafforzare visivamente il significato di uno di questi metodi principali di comunicazione:

-   **Testo** Il testo conciso è in genere la comunicazione primaria più efficace direttamente nell'interfaccia utente o tramite una descrizione comando.

![Screenshot di una piccola icona rossa con descrizione comando ](images/vis-color-image10.png)

In questo esempio, il testo della descrizione comando viene usato per comunicare il significato di un'icona.

-   **Design.** Le icone sono facilmente distinguibili dalle progettazioni, in particolare dalla forma del contorno.

![Screenshot delle icone in sfumature di grigio (scala di grigi) ](images/vis-color-image11.png)

In questo esempio, le icone standard sono facilmente distinguibili in base alle progettazioni.

-   **Posizione.** È anche possibile usare la posizione relativa, ma questo approccio è più debole rispetto alle alternative. Per essere efficace, la posizione deve essere standard e ben nota, come per i semafori.

Anche se il colore è l'attributo più ovvio di molte progettazioni, deve essere sempre ridondante.

### <a name="designing-with-color"></a>Progettazione con il colore

Ironia della sorte, il modo migliore per progettare il colore è iniziare progettando senza colore, usando [wireframe](glossary.md) o monocromatici e quindi aggiungere il colore in un secondo momento. In questo modo si garantisce che le informazioni non vengano comunicate usando solo il colore. Garantisce inoltre che le stampe siano molto grandi sulle stampanti monocroma.

### <a name="use-theme-or-system-colors"></a>Usare i colori del tema o del sistema

Anche se esistono molti fattori complessi nell'uso efficace del colore, nell'interfaccia utente [](glossary.md) di Windows la scelta del colore spesso si riduce alla semplice scelta del colore del tema o del colore di sistema appropriato in base ad alcune semplici regole. [](glossary.md) Gli utenti possono quindi selezionare e personalizzare queste combinazioni di colori a scelta.

In questo modo, non solo si adattano le preferenze di colore di tutti gli utenti, ma si elimina l'onere di scegliere l'unica combinazione di colori perfetta che funziona per tutti i gusto, gli stili e le impostazioni cultura (che, naturalmente, è altrimenti impossibile).

**Se si fa una sola cosa...**

Scegliere i colori selezionando il colore del tema o il colore di sistema appropriato. Non usare mai il colore come metodo primario di comunicazione, ma come metodo secondario per rafforzare visivamente il significato. Progettare usando wireframe o monocromi per garantire che il colore sia secondario.

### <a name="use-theme-or-system-colors-correctly"></a>Usare correttamente i colori del tema o del sistema

Si supponga che gli utenti scelgono i colori del tema o del sistema in base alle proprie esigenze personali e che i colori del tema o del sistema siano costruiti in modo appropriato. In base a questo presupposto, se si scelgono sempre i colori del tema o del sistema in base allo scopo desiderato e si associano i primi piani agli sfondi associati, i colori sono garantiti per essere leggibili e rispettare i desideri degli utenti in tutte le modalità video, inclusa la modalità a [contrasto elevato](glossary.md). Ad esempio, il colore di sistema del testo della finestra è garantito per essere leggibile rispetto al colore di sistema di sfondo della finestra.

In particolare, sempre:

-   **Scegliere i colori in base allo scopo.** Non scegliere i colori in base all'aspetto corrente perché tale aspetto può essere modificato dall'utente o dalle versioni future di Windows.
-   **Abbinare i colori di primo piano ai colori di sfondo associati.** È garantito che i colori in primo piano siano leggibili solo rispetto ai colori di sfondo associati. Non combinare e abbinare i colori di primo piano con altri colori di sfondo o, ancora meglio, altri colori di primo piano.
-   **Non combinare tipi di colore.** In altre parole, abbinare sempre i colori del tema ai colori del tema associati, i colori di sistema con i colori di sistema associati e i colori hardwired con altri colori hardwired. Ad esempio, non è garantito che un colore del testo del tema sia leggibile su uno sfondo hardwired.
-   **Se è necessario eseguire il hardwire dei colori, gestire la modalità a contrasto elevato come caso speciale.**

**Se si fa una sola cosa...**

Scegliere sempre i colori del tema o del sistema in base allo scopo desiderato e associare i primi piani agli sfondi associati.

### <a name="using-other-colors"></a>Uso di altri colori

Anche se il tema di Windows definisce un set completo di parti del tema, è possibile che il programma necessita di colori non definiti nel file del tema. Sebbene sia possibile eseguire il hardwire di questi colori, un approccio migliore consiste nel derivare i colori dal tema o dai colori di sistema. L'uso strategico di questo approccio offre tutti i vantaggi dell'uso dei colori del tema e del sistema, ma con una maggiore flessibilità.

Si supponga, ad esempio, che sia necessario uno sfondo della finestra più scuro del colore di sfondo della finestra del tema. Nello spazio colori HSL, avere un colore più scuro significa un colore con una luminosità inferiore. È quindi possibile derivare un colore di sfondo della finestra più scuro seguendo questa procedura:

-   Ottenere il colore RGB del tema di sfondo della finestra.
-   Convertire RGB nel relativo valore HSL.
-   Ridurre il valore di luminosità (ad esempio, del 20%).
-   Eseguire la conversione in valori RGB.

Usando questo approccio, è garantito che il colore derivato venga percepito come una sfumatura più scura del colore originale (a meno che il colore originale non sia molto scuro per iniziare).

![Illustrazione che mostra gli effetti della ridotta luminosità ](images/vis-color-image12.png)

In questo esempio, un colore di sfondo della finestra più scuro deriva dal colore del tema.

### <a name="testing-colors"></a>Test dei colori

Per determinare se l'uso del colore da parte del programma è accessibile e non viene usato come metodo di comunicazione principale, è consigliabile usare le utilità [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) o [Vischeck](https://www.vischeck.com/) per verificare la presenza di:

-   Dipendenza complessiva dal colore usando il filtro Scala grigia.
-   Problemi specifici di confusione dei colori con i filtri Protanopia, Deuteranopia e Tritanopia.

Per determinare se l'uso del colore da parte del programma è programmato correttamente, testare il programma nelle modalità seguenti:

-   Tema abilitato usando il tema predefinito di Windows.
-   Tema abilitato usando un tema non predefinito.
-   Tema disabilitato ("Stile classico di Windows" nelle impostazioni del tema nell'elemento Pannello di controllo personalizzazione).
-   Contrasto elevato nero (testo bianco su sfondo nero).
-   Contrasto elevato bianco (testo nero su sfondo bianco).

Tutti gli elementi dello schermo devono essere leggibili e visualizzati come previsto, anche immediatamente dopo le modifiche della modalità.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non usare mai il colore come metodo primario di comunicazione,** ma come metodo secondario per rafforzare visivamente il significato.

### <a name="using-theme-and-system-colors"></a>Uso del tema e dei colori di sistema

-   Quando possibile, scegliere i colori selezionando il colore del **tema o il colore di sistema appropriato.** In questo modo, è sempre possibile rispettare le preferenze di colore degli utenti.
-   **Scegliere i colori del tema e del sistema in base allo scopo.** Non scegliere i colori in base all'aspetto corrente, perché tale aspetto può essere modificato dall'utente o dalle versioni future di Windows.
-   **Abbinare i colori di primo piano ai colori di sfondo associati.** È garantito che i colori in primo piano siano leggibili solo rispetto ai colori di sfondo associati. Non combinare e abbinare i colori di primo piano con altri colori di sfondo o, ancora meglio, altri colori di primo piano.
-   **Non combinare tipi di colore.** In altre parole, abbinare sempre i colori del tema ai colori del tema associati, i colori di sistema con i colori di sistema associati e i colori hardwired con altri colori hardwired. Ad esempio, non è garantito che un colore del testo del tema sia leggibile su uno sfondo hardwired.
-   **Se è necessario usare un colore diverso da un tema o un colore di sistema:**
    -   **Preferisce derivare il colore da un tema o da un colore di sistema invece di eseguire il hardwiring del relativo valore.** Usare il processo descritto in precedenza in questo articolo, in Uso di altri colori.
    -   **Gestire la modalità a contrasto elevato come caso speciale.**
-   **Gestire le modifiche al tema.** Le modifiche al tema vengono gestite automaticamente dalle finestre con riquadri di finestra standard e controlli comuni. Le finestre con riquadri di finestra personalizzati, controlli personalizzati o di disegno del proprietario e altri usi del colore devono gestire le modifiche del tema in modo esplicito.
    -   **Sviluppatori:** È possibile rispondere agli eventi di modifica del tema gestendo il messaggio WM \_ THEMECHANGED.

### <a name="color-meaning"></a>Significato del colore

-   Anche se è consigliabile usare i colori del tema e del sistema (o i colori derivati) ogni volta che è possibile, assicurarsi che qualsiasi altro uso del colore sia compatibile con l'uso del colore seguente all'interno di Windows.



| Tonalità | Significato | Usare in Windows  |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blu/verde<br/>                | Marchio Windows<br/>                                                      | Background: Personalizzazione di Windows.<br/>                                                                                                                        |
| glass, black, gray, white<br/> | neutrale<br/>                                                            | Sfondo: frame di finestra standard, menu Start, barra delle applicazioni, Barra laterale.<br/> Primo piano: testo normale.<br/>                                                |
| blue<br/>                      | avvio, commit<br/>                                                      | Sfondo: pulsanti di comando predefiniti, ricerca, accesso.<br/> Icone: informazioni, Guida.<br/> Primo piano: istruzioni principali, collegamenti.<br/>           |
| rosso<br/>                       | error, stop, vulnerable, critical, immediate attention, restricted<br/> | Background: stato, stato arrestato (barre di stato).<br/> Icone: errore, arresto, chiusura della finestra, eliminazione, input obbligatorio, mancante, non disponibile.<br/>     |
| yellow<br/>                    | avviso, attenzione, discutibile<br/>                                     | Background: stato, stato sospeso (barre di stato).<br/> Icone: avviso<br/>                                                                       |
| green<br/>                     | go, proceed, progress, safe<br/>                                        | Sfondo: stato, stato normale (barre di stato).<br/> Icone: go, done, refresh.<br/> Primo piano: percorsi e URL (nei risultati della ricerca).<br/> |
| purple<br/>                    | Visitato<br/>                                                            | Primo piano: collegamenti visitati (per i collegamenti all'interno di Internet Explorer e documenti di Windows).<br/>                                                                |



 

-   **Per evitare di comunicare i significati precedenti, scegliere i colori con saturazione da media a bassa e luminosità alta o bassa.** Gli utenti associano i significati precedenti ai colori con saturazione completa o elevata e luminosità di livello intermedio, in modo da evitare queste associazioni scegliendo sfumature diverse.

![figura che illustra l'effetto della luminosità sul colore ](images/vis-color-image13.png)

In questo esempio sono presenti tre diverse sfumature di giallo, ma solo la sfumatura di luminosità altamente satura e di livello intermedio comunica un avviso. L'icona di cartella gialla non sembra un avviso.

### <a name="using-color-with-data"></a>Uso del colore con i dati

-   Quando utile, **assegnare il colore ai dati per consentire agli utenti di distinguerli.** Si noti che gli utenti presuppongono che i dati con colori simili hanno significati simili.
-   **Assegnare per impostazione predefinita colori facili da distinguere.** In genere, i colori sono facili da distinguere se sono distanti l'uno dall'altro negli spazi colori HSL/HSV, mantenendo un contrasto elevato con lo sfondo:
    -   Quando si scelgono i colori, preferire le triade o le sfumature complementari, ma non le tonalità adiacenti.

        ![Figura che illustra come scegliere i colori a contrasto ](images/vis-color-image14.png)

        In questo esempio, se la prima assegnazione di colore è rossa, il colore successivo deve essere blu, verde o ciano, ma non magenta, viola, arancione o giallo.

    -   I colori hanno un contrasto elevato se c'è una grande differenza nella tonalità, nella saturazione o nella luminosità.

        ![figura che mostra un colore su sfondi diversi ](images/vis-color-image15.png)

        In questo esempio, il colore di base blu chiaro è in contrasto con gli sfondi con grandi differenze in tonalità, saturazione o luminosità.

    -   L'uso di uno sfondo bianco o molto chiaro semplifica la distinzione dei colori di primo piano a contrasto.

        ![figura che illustra il contrasto positivo e scarso ](images/vis-color-image16.png)

        In questo esempio, i colori di sfondo bianco e chiaro semplificano la distinzione del colore di primo piano.

-   **Consente agli utenti di personalizzare queste assegnazioni di colori** perché la scelta del colore è soggettiva e una preferenza personale. Se sono presenti molti colori coordinati, consentire agli utenti di modificarli come gruppo usando combinazioni di colori.
-   **Consente agli utenti di etichettare queste assegnazioni di colori.** In questo modo è più facile identificarle e trovarle.
-   **A differenza dei colori dell'interfaccia utente, i dati non devono cambiare quando cambiano i colori di sistema.**

## <a name="documentation"></a>Documentazione

-   **Fare riferimento agli elementi dell'interfaccia utente in base ai relativi nomi, non in base ai colori.** Tali riferimenti non sono accessibili e i colori di sistema possono cambiare. Se il nome di un elemento dell'interfaccia utente non è noto o non è sufficientemente descrittivo, visualizzare uno screenshot per chiarire.

**Corretto:**

![Screenshot del messaggio contenente la barra informazioni ](images/vis-color-image17.png)

**Non corretto:**

![screenshot del messaggio contenente la "barra dorata" ](images/vis-color-image18.png)

Nell'esempio non corretto, il messaggio fa riferimento alla barra Internet Explorer informazioni di Windows in base al colore anziché al nome.

